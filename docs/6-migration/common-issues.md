# ⚠️ Common Issues

Solutions for typical migration problems when upgrading from Tailwind CSS v3 to v4+.

## 🎯 Overview

This guide covers the most common issues encountered during migration and provides step-by-step solutions.

## 🔧 Build Issues

### 1. Module Not Found Errors

```bash
# Error: Cannot find module 'tailwindcss'
# Solution: Update import statements
```

**Problem**: Old import statements causing module not found errors.

**Solution**:

```css
/* Before: v3 imports */
@tailwind base;
@tailwind components;
@tailwind utilities;

/* After: v4 imports */
@import "tailwindcss";
```

### 2. PostCSS Plugin Errors

```bash
# Error: PostCSS plugin not found
# Solution: Update PostCSS configuration
```

**Problem**: PostCSS configuration not updated for v4.

**Solution**:

```javascript
// Before: postcss.config.js
module.exports = {
  plugins: {
    tailwindcss: {},
    autoprefixer: {},
  },
};

// After: postcss.config.mjs
const config = {
  plugins: {
    "@tailwindcss/postcss": {},
  },
};

export default config;
```

### 3. Vite Plugin Errors

```bash
# Error: Vite plugin not found
# Solution: Update Vite configuration
```

**Problem**: Vite configuration not updated for v4.

**Solution**:

```typescript
// Before: vite.config.ts
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";
import tailwindcss from "tailwindcss";
import autoprefixer from "autoprefixer";

export default defineConfig({
  plugins: [react()],
  css: {
    postcss: {
      plugins: [tailwindcss, autoprefixer],
    },
  },
});

// After: vite.config.ts
import { defineConfig } from "vite";
import react from "@vitejs/plugin-react";
import tailwindcss from "@tailwindcss/vite";

export default defineConfig({
  plugins: [react(), tailwindcss()],
});
```

## ⚙️ Configuration Issues

### 1. Configuration File Errors

```bash
# Error: tailwind.config.js not found
# Solution: Remove old config and use CSS-first configuration
```

**Problem**: Old configuration file causing errors.

**Solution**:

```bash
# Remove old config file
rm tailwind.config.js

# Update CSS file
@import "tailwindcss";

@theme {
  --color-primary: #3b82f6;
  --color-secondary: #10b981;
}
```

### 2. Plugin Configuration Errors

```bash
# Error: Plugin not found
# Solution: Update plugin imports
```

**Problem**: Plugin configuration not updated for v4.

**Solution**:

```css
/* Before: v3 plugin configuration */
// tailwind.config.js
plugins: [ require("@tailwindcss/forms"), require("@tailwindcss/typography"), ]
    /* After: v4 plugin configuration */ @plugin "@tailwindcss/forms";
@plugin "@tailwindcss/typography";
```

### 3. Theme Configuration Errors

```bash
# Error: Theme configuration not found
# Solution: Convert to CSS-first configuration
```

**Problem**: Theme configuration not converted to CSS-first.

**Solution**:

```javascript
// Before: tailwind.config.js
module.exports = {
  theme: {
    extend: {
      colors: {
        primary: '#3b82f6',
        secondary: '#10b981',
      },
      spacing: {
        '18': '4.5rem',
      },
    },
  },
};

// After: CSS-first configuration
@theme {
  --color-primary: #3b82f6;
  --color-secondary: #10b981;
  --spacing-18: 4.5rem;
}
```

## 🎨 CSS Issues

### 1. Styles Not Applying

```bash
# Problem: Tailwind styles not applying
# Solution: Check CSS imports and configuration
```

**Problem**: Tailwind styles not being applied.

**Solution**:

```css
/* Check CSS imports */
@import "tailwindcss";

/* Check theme configuration */
@theme {
  --color-primary: #3b82f6;
}

/* Check custom utilities */
@utility btn-primary {
  background-color: theme("colors.blue.500");
  color: theme("colors.white");
  padding: theme("spacing.2") theme("spacing.4");
  border-radius: theme("borderRadius.md");
}
```

### 2. Custom Utilities Not Working

```bash
# Problem: Custom utilities not working
# Solution: Update utility syntax
```

**Problem**: Custom utilities not working after migration.

**Solution**:

```css
/* Before: v3 custom utilities */
@layer components {
  .btn-primary {
    @apply bg-blue-500 text-white px-4 py-2 rounded;
  }
}

/* After: v4 custom utilities */
@utility btn-primary {
  background-color: theme("colors.blue.500");
  color: theme("colors.white");
  padding: theme("spacing.2") theme("spacing.4");
  border-radius: theme("borderRadius.md");
}
```

### 3. Responsive Design Issues

```bash
# Problem: Responsive design not working
# Solution: Check breakpoint configuration
```

**Problem**: Responsive design not working after migration.

**Solution**:

```css
/* Check breakpoint configuration */
@theme {
  --breakpoint-sm: 640px;
  --breakpoint-md: 768px;
  --breakpoint-lg: 1024px;
  --breakpoint-xl: 1280px;
  --breakpoint-2xl: 1536px;
}

/* Test responsive utilities */
<div class="
  grid grid-cols-1
  sm:grid-cols-2
  md:grid-cols-3
  lg:grid-cols-4
  gap-4
">
  <!-- Grid items -->
</div>
```

## 🔌 Plugin Issues

### 1. Plugin Not Found

```bash
# Error: Plugin not found
# Solution: Update plugin packages
```

**Problem**: Plugin packages not updated for v4.

**Solution**:

```bash
# Remove old plugin packages
npm uninstall @tailwindcss/forms @tailwindcss/typography

# Install new plugin packages
npm install @tailwindcss/forms @tailwindcss/typography
```

### 2. Plugin Configuration Errors

```bash
# Error: Plugin configuration not working
# Solution: Update plugin syntax
```

**Problem**: Plugin configuration not working after migration.

**Solution**:

```css
/* Before: v3 plugin configuration */
// tailwind.config.js
plugins: [ require("@tailwindcss/forms"), require("@tailwindcss/typography"), ]
    /* After: v4 plugin configuration */ @plugin "@tailwindcss/forms";
@plugin "@tailwindcss/typography";
```

### 3. Custom Plugin Issues

```bash
# Error: Custom plugin not working
# Solution: Convert to custom utilities
```

**Problem**: Custom plugins not working after migration.

**Solution**:

```javascript
// Before: v3 custom plugin
const plugin = require('tailwindcss/plugin');

module.exports = {
  plugins: [
    plugin(function({ addUtilities }) {
      addUtilities({
        '.btn-primary': {
          backgroundColor: '#3b82f6',
          color: '#ffffff',
          padding: '0.5rem 1rem',
          borderRadius: '0.375rem',
        },
      });
    }),
  ],
};

// After: v4 custom utilities
@utility btn-primary {
  background-color: #3b82f6;
  color: #ffffff;
  padding: 0.5rem 1rem;
  border-radius: 0.375rem;
}
```

## 🧪 Testing Issues

### 1. Build Failures

```bash
# Error: Build failing
# Solution: Check configuration and dependencies
```

**Problem**: Build process failing after migration.

**Solution**:

```bash
# Check dependencies
npm list | grep tailwindcss

# Check configuration
cat postcss.config.mjs

# Test build
npm run build

# Check for errors
npm run build 2>&1 | grep -i error
```

### 2. Development Server Issues

```bash
# Error: Development server not starting
# Solution: Check Vite configuration
```

**Problem**: Development server not starting after migration.

**Solution**:

```typescript
// Check Vite configuration
import { defineConfig } from 'vite';
import react from '@vitejs/plugin-react';
import tailwindcss from '@tailwindcss/vite';

export default defineConfig({
  plugins: [react(), tailwindcss()],
});

// Test development server
npm run dev
```

### 3. Hot Module Replacement Issues

```bash
# Error: HMR not working
# Solution: Check Vite configuration
```

**Problem**: Hot Module Replacement not working after migration.

**Solution**:

```typescript
// Check Vite configuration
export default defineConfig({
  plugins: [react(), tailwindcss()],
  server: {
    hmr: true,
    watch: {
      usePolling: false,
    },
  },
});
```

## 🔄 Migration Issues

### 1. Partial Migration

```bash
# Problem: Some components not migrated
# Solution: Check for missed components
```

**Problem**: Some components not properly migrated.

**Solution**:

```bash
# Search for old Tailwind classes
grep -r "bg-blue-500" src/

# Check for old configuration
grep -r "tailwind.config" .

# Check for old imports
grep -r "@tailwind" src/
```

### 2. Styling Inconsistencies

```bash
# Problem: Styling inconsistencies
# Solution: Check for missing utilities
```

**Problem**: Styling inconsistencies after migration.

**Solution**:

```css
/* Check for missing utilities */
@utility btn-primary {
  background-color: theme("colors.blue.500");
  color: theme("colors.white");
  padding: theme("spacing.2") theme("spacing.4");
  border-radius: theme("borderRadius.md");

  &:hover {
    background-color: theme("colors.blue.600");
  }

  &:focus {
    outline: 2px solid theme("colors.blue.300");
    outline-offset: 2px;
  }
}
```

### 3. Performance Issues

```bash
# Problem: Performance degradation
# Solution: Check build configuration
```

**Problem**: Performance issues after migration.

**Solution**:

```typescript
// Check Vite configuration
export default defineConfig({
  plugins: [react(), tailwindcss()],
  build: {
    cssCodeSplit: true,
    rollupOptions: {
      output: {
        manualChunks: {
          tailwind: ["tailwindcss"],
        },
      },
    },
  },
});
```

## 🛠️ Troubleshooting Tools

### 1. Debug Configuration

```bash
# Enable debug mode
DEBUG=tailwindcss npm run build

# Check configuration
npx tailwindcss --help

# Test configuration
npx tailwindcss --config postcss.config.mjs
```

### 2. Build Analysis

```bash
# Analyze build output
npm run build -- --analyze

# Check bundle size
npm run build -- --report

# Monitor build performance
time npm run build
```

### 3. Development Tools

```bash
# Check for errors
npm run dev 2>&1 | grep -i error

# Check for warnings
npm run dev 2>&1 | grep -i warning

# Check for deprecations
npm run dev 2>&1 | grep -i deprecated
```

## 📋 Troubleshooting Checklist

### ✅ Build Issues

- [ ] Check package dependencies
- [ ] Verify configuration files
- [ ] Test build process
- [ ] Check for errors
- [ ] Fix configuration issues

### ✅ CSS Issues

- [ ] Check CSS imports
- [ ] Verify theme configuration
- [ ] Test custom utilities
- [ ] Check responsive design
- [ ] Fix styling issues

### ✅ Plugin Issues

- [ ] Update plugin packages
- [ ] Check plugin configuration
- [ ] Test plugin functionality
- [ ] Fix plugin issues
- [ ] Update custom plugins

### ✅ Testing Issues

- [ ] Test build process
- [ ] Test development server
- [ ] Test HMR functionality
- [ ] Check for errors
- [ ] Fix testing issues

## 🚀 Next Steps

1. **Identify the specific issue** you're encountering
2. **Follow the solution steps** for that issue
3. **Test the fix** to ensure it works
4. **Document the solution** for future reference
5. **Continue with migration** if the issue is resolved

## 💡 Pro Tips

- **Read error messages carefully**: They often contain the solution
- **Check the documentation**: Tailwind v4 docs have migration guides
- **Use community resources**: GitHub issues and Discord can help
- **Test incrementally**: Fix one issue at a time
- **Document solutions**: Keep track of what works

---

Ready to follow a systematic migration process? Check out the [Migration Checklist](./migration-checklist.md) guide next!
