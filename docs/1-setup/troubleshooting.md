# Troubleshooting Guide

_Common issues and solutions when setting up and using Tailwind CSS v4+_

---

## 🧭 Navigation

- [Setup Issues](#setup-issues)
- [Build Problems](#build-problems)
- [CSS Not Working](#css-not-working)
- [Performance Issues](#performance-issues)
- [Framework-Specific Issues](#framework-specific-issues)
- [Migration Problems](#migration-problems)

---

## 🚨 Setup Issues

### Issue: Classes Not Working

**Symptoms:**

- Tailwind classes don't apply styles
- No visual changes when adding classes
- CSS file appears empty or minimal

**Solutions:**

1. **Check CSS Import**

   ```css
   /* Make sure you have this in your CSS file */
   @import "tailwindcss";
   ```

2. **Verify File Paths**

   ```html
   <!-- HTML projects -->
   <link href="./src/output.css" rel="stylesheet" />

   <!-- React/Vue/Svelte -->
   import './index.css' // or style.css

   <!-- Next.js -->
   import './globals.css'
   ```

3. **Check Build Process**

   ```bash
   # HTML projects - ensure build completed
   npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css

   # React/Vite - check dev server is running
   npm run dev

   # Next.js - check dev server is running
   npm run dev
   ```

### Issue: Package Installation Errors

**Symptoms:**

- npm install fails
- Package not found errors
- Version conflicts

**Solutions:**

1. **Clear Cache and Reinstall**

   ```bash
   # Clear npm cache
   npm cache clean --force

   # Remove node_modules and package-lock.json
   rm -rf node_modules package-lock.json

   # Reinstall
   npm install
   ```

2. **Check Node.js Version**

   ```bash
   # Ensure Node.js 16.0+
   node --version

   # Update if needed
   nvm install 18
   nvm use 18
   ```

3. **Use Correct Package Names**

   ```bash
   # v4 packages (correct)
   npm install tailwindcss @tailwindcss/vite
   npm install tailwindcss @tailwindcss/postcss postcss
   npm install tailwindcss @tailwindcss/cli

   # v3 packages (incorrect for v4)
   npm install tailwindcss postcss autoprefixer
   ```

---

## 🔧 Build Problems

### Issue: Build Fails

**Symptoms:**

- Build process crashes
- Error messages during build
- No output files generated

**Solutions:**

1. **Check Configuration Files**

   ```javascript
   // vite.config.ts (React/Vue/Svelte)
   import tailwindcss from "@tailwindcss/vite";

   export default defineConfig({
     plugins: [react(), tailwindcss()],
   });
   ```

   ```javascript
   // postcss.config.mjs (Next.js)
   const config = {
     plugins: {
       "@tailwindcss/postcss": {},
     },
   };
   export default config;
   ```

2. **Verify File Structure**

   ```
   project/
   ├── src/
   │   ├── input.css (HTML projects)
   │   └── output.css (generated)
   ├── app/
   │   └── globals.css (Next.js)
   └── src/
       └── index.css (React/Vue/Svelte)
   ```

3. **Check for Syntax Errors**

   ```css
   /* Correct syntax */
   @import "tailwindcss";

   @theme {
     --color-primary: #3b82f6;
   }

   /* Incorrect syntax */
   @import tailwindcss; /* Missing quotes */
   @theme {
     --color-primary: #3b82f6;
   } /* Missing semicolon */
   ```

### Issue: Slow Builds

**Symptoms:**

- Builds take a long time
- Development server is slow
- HMR is sluggish

**Solutions:**

1. **Use Correct Plugin for Your Framework**

   ```bash
   # React/Vue/Svelte with Vite
   npm install @tailwindcss/vite

   # Next.js
   npm install @tailwindcss/postcss

   # HTML projects
   npm install @tailwindcss/cli
   ```

2. **Optimize Content Detection**

   ```css
   /* Exclude unnecessary files */
   @source not "./src/components/legacy";
   @source not "./node_modules/old-package";
   ```

3. **Check for Large Dependencies**
   ```bash
   # Analyze bundle size
   npm run build
   # Check output for large files
   ```

---

## 🎨 CSS Not Working

### Issue: Styles Not Applying

**Symptoms:**

- Classes exist but don't work
- Partial styling (some classes work, others don't)
- Styles work in development but not production

**Solutions:**

1. **Check Content Detection**

   ```css
   /* Tailwind v4 automatically detects content */
   @import "tailwindcss";

   /* If needed, specify additional sources */
   @source "./src/components/**/*.{js,jsx,ts,tsx}";
   @source "./src/pages/**/*.{js,jsx,ts,tsx}";
   ```

2. **Verify Class Names**

   ```html
   <!-- Correct class names -->
   <div class="bg-blue-500 text-white p-4 rounded-lg">
     <!-- Common mistakes -->
     <div class="bg-blue-500 text-white p-4 rounded-lg">
       <!-- Missing space -->
       <div class="bg-blue-500 text-white p-4 rounded-lg">
         <!-- Typo in class name -->
       </div>
     </div>
   </div>
   ```

3. **Check CSS Specificity**

   ```css
   /* Custom CSS might override Tailwind */
   .my-custom-class {
     background-color: red !important; /* This overrides Tailwind */
   }

   /* Use Tailwind's important modifier */
   <div class="!bg-blue-500"> <!-- Forces blue background -->
   ```

### Issue: Responsive Classes Not Working

**Symptoms:**

- Mobile styles don't apply
- Breakpoint classes don't work
- Responsive design breaks

**Solutions:**

1. **Check Viewport Meta Tag**

   ```html
   <meta name="viewport" content="width=device-width, initial-scale=1.0" />
   ```

2. **Verify Breakpoint Usage**

   ```html
   <!-- Correct responsive classes -->
   <div class="w-full md:w-1/2 lg:w-1/3">
     <!-- Common mistakes -->
     <div class="w-full md:w-1/2 lg:w-1/3">
       <!-- Missing space -->
       <div class="w-full md:w-1/2 lg:w-1/3">
         <!-- Wrong breakpoint order -->
       </div>
     </div>
   </div>
   ```

3. **Test in Browser DevTools**
   - Open DevTools
   - Toggle device toolbar
   - Test different screen sizes
   - Check if classes are applied

---

## ⚡ Performance Issues

### Issue: Large CSS Bundle

**Symptoms:**

- CSS file is very large
- Slow page loading
- High bandwidth usage

**Solutions:**

1. **Use Production Build**

   ```bash
   # HTML projects
   npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --minify

   # React/Vue/Svelte
   npm run build

   # Next.js
   npm run build
   ```

2. **Check for Unused Classes**

   ```css
   /* Remove unused custom utilities */
   @utility unused-class {
     /* This adds to bundle size if not used */
   }
   ```

3. **Optimize Content Detection**
   ```css
   /* Only include necessary files */
   @source "./src/**/*.{js,jsx,ts,tsx}";
   @source not "./src/legacy/**/*";
   ```

### Issue: Slow Development Server

**Symptoms:**

- Dev server takes long to start
- HMR is slow
- File changes take time to reflect

**Solutions:**

1. **Use Correct Plugin**

   ```bash
   # For Vite projects, use the Vite plugin
   npm install @tailwindcss/vite

   # Not the PostCSS plugin
   npm install @tailwindcss/postcss
   ```

2. **Optimize File Watching**

   ```javascript
   // vite.config.ts
   export default defineConfig({
     plugins: [react(), tailwindcss()],
     server: {
       watch: {
         // Exclude unnecessary files
         ignored: ["**/node_modules/**", "**/dist/**"],
       },
     },
   });
   ```

3. **Check for Large Files**
   ```bash
   # Find large files that might slow down watching
   find . -name "*.js" -o -name "*.ts" -o -name "*.jsx" -o -name "*.tsx" | xargs wc -l | sort -nr | head -10
   ```

---

## 🎯 Framework-Specific Issues

### React/Vue/Svelte Issues

**Issue: HMR Not Working**

```bash
# Check Vite configuration
# vite.config.ts
import tailwindcss from "@tailwindcss/vite";

export default defineConfig({
  plugins: [react(), tailwindcss()], // Make sure tailwindcss is included
});
```

**Issue: TypeScript Errors**

```typescript
// Add type definitions
// src/tailwind.d.ts
import "tailwindcss";

declare module "tailwindcss" {
  interface Config {
    theme: {
      extend: {
        colors: {
          primary: string;
        };
      };
    };
  }
}
```

### Next.js Issues

**Issue: SSR Problems**

```tsx
// Make sure CSS is imported in root layout
// app/layout.tsx
import "./globals.css";

export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body>{children}</body>
    </html>
  );
}
```

**Issue: Build Errors**

```javascript
// Check PostCSS configuration
// postcss.config.mjs
const config = {
  plugins: {
    "@tailwindcss/postcss": {},
  },
};

export default config;
```

### HTML Issues

**Issue: CSS Not Generated**

```bash
# Check input file exists
ls src/input.css

# Check build command
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

**Issue: File Not Found**

```html
<!-- Check CSS file path -->
<link href="./src/output.css" rel="stylesheet" />
<!-- Make sure output.css exists after build -->
```

---

## 🔄 Migration Problems

### Issue: v3 to v4 Migration

**Symptoms:**

- Old configuration not working
- Classes not applying
- Build errors

**Solutions:**

1. **Use Migration Tool**

   ```bash
   # Run official migration tool
   npx @tailwindcss/upgrade
   ```

2. **Manual Migration Steps**

   ```bash
   # 1. Update packages
   npm uninstall tailwindcss postcss autoprefixer
   npm install tailwindcss @tailwindcss/vite # or @tailwindcss/postcss

   # 2. Update CSS imports
   # Old: @tailwind base; @tailwind components; @tailwind utilities;
   # New: @import "tailwindcss";

   # 3. Convert configuration
   # Old: tailwind.config.js
   # New: @theme directive in CSS
   ```

3. **Check for Breaking Changes**
   - Remove `tailwind.config.js`
   - Update CSS imports
   - Convert plugins to `@plugin` directive
   - Update build configuration

### Issue: Deprecated Classes

**Symptoms:**

- Classes don't work
- Console warnings
- Visual differences

**Solutions:**

1. **Check Class Names**

   ```html
   <!-- Common deprecated classes -->
   <!-- Old: flex-shrink-0 -->
   <!-- New: shrink-0 -->

   <!-- Old: flex-grow -->
   <!-- New: grow -->

   <!-- Old: transform -->
   <!-- New: (no prefix needed) -->
   ```

2. **Update Custom CSS**

   ```css
   /* Old approach */
   @layer utilities {
     .my-utility {
       /* styles */
     }
   }

   /* New approach */
   @utility my-utility {
     /* styles */
   }
   ```

---

## 🆘 Getting Help

### Debug Steps

1. **Check Console Errors**

   - Open browser DevTools
   - Look for JavaScript errors
   - Check network tab for failed requests

2. **Verify Configuration**

   - Check all config files
   - Verify package versions
   - Ensure file paths are correct

3. **Test Minimal Setup**
   - Create a simple test file
   - Use basic Tailwind classes
   - Verify they work

### Resources

- **[Official Documentation](https://tailwindcss.com/docs)**
- **[GitHub Issues](https://github.com/tailwindlabs/tailwindcss/issues)**
- **[Discord Community](https://discord.gg/tailwindcss)**
- **[Stack Overflow](https://stackoverflow.com/questions/tagged/tailwind-css)**

### Common Solutions

```bash
# Clear everything and start fresh
rm -rf node_modules package-lock.json
npm cache clean --force
npm install

# Check versions
npm list tailwindcss
npm list @tailwindcss/vite
npm list @tailwindcss/postcss

# Verify installation
npx tailwindcss --version
```

---

## 🎯 Prevention Tips

### Best Practices

1. **Use Correct Packages**

   - Match packages to your framework
   - Keep versions up to date
   - Use official packages only

2. **Follow Setup Guides**

   - Use official documentation
   - Follow framework-specific guides
   - Test setup with simple examples

3. **Monitor Performance**

   - Check bundle sizes
   - Monitor build times
   - Optimize content detection

4. **Keep Configuration Simple**
   - Start with defaults
   - Add customizations gradually
   - Document changes

---

**Still having issues?** Check the [Resources Section](../7-resources/README.md) for community help and additional support.

