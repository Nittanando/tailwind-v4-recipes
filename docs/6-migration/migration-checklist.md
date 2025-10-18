# ✅ Migration Checklist

Comprehensive step-by-step checklist for migrating from Tailwind CSS v3 to v4+.

## 🎯 Overview

This checklist ensures a systematic and complete migration from Tailwind CSS v3 to v4+. Follow each step carefully and check off items as you complete them.

## 📋 Pre-Migration Checklist

### ✅ Project Assessment

- [ ] **Document current Tailwind version**
  ```bash
  npm list tailwindcss
  ```
- [ ] **List all custom configuration**
  ```bash
  cat tailwind.config.js
  ```
- [ ] **Identify custom plugins**
  ```bash
  grep -r "plugins" tailwind.config.js
  ```
- [ ] **List custom utilities**
  ```bash
  grep -r "@layer" src/
  ```
- [ ] **Check for custom components**
  ```bash
  grep -r "@apply" src/
  ```

### ✅ Backup Preparation

- [ ] **Create backup branch**
  ```bash
  git checkout -b backup-before-migration
  ```
- [ ] **Commit current state**
  ```bash
  git add .
  git commit -m "Backup before Tailwind v4 migration"
  ```
- [ ] **Create migration branch**
  ```bash
  git checkout -b tailwind-v4-migration
  ```
- [ ] **Document current setup**
  - [ ] Screenshot current design
  - [ ] List all components
  - [ ] Document custom utilities
  - [ ] Note plugin usage

## 📦 Package Updates

### ✅ Remove Old Packages

- [ ] **Remove Tailwind CSS v3**
  ```bash
  npm uninstall tailwindcss
  ```
- [ ] **Remove old plugins**
  ```bash
  npm uninstall @tailwindcss/forms @tailwindcss/typography @tailwindcss/aspect-ratio
  ```
- [ ] **Check for other Tailwind packages**
  ```bash
  npm list | grep tailwindcss
  ```

### ✅ Install New Packages

- [ ] **Install Tailwind CSS v4 packages**
  ```bash
  npm install @tailwindcss/postcss @tailwindcss/cli @tailwindcss/vite
  ```
- [ ] **Install new plugin packages**
  ```bash
  npm install @tailwindcss/forms @tailwindcss/typography @tailwindcss/container-queries
  ```
- [ ] **Verify installation**
  ```bash
  npm list | grep tailwindcss
  ```

## ⚙️ Configuration Updates

### ✅ Remove Old Configuration

- [ ] **Remove tailwind.config.js**
  ```bash
  rm tailwind.config.js
  ```
- [ ] **Remove tailwind.config.ts** (if exists)
  ```bash
  rm tailwind.config.ts
  ```
- [ ] **Check for other config files**
  ```bash
  find . -name "*tailwind*" -type f
  ```

### ✅ Update CSS Files

- [ ] **Update main CSS file**

  ```css
  /* Before */
  @tailwind base;
  @tailwind components;
  @tailwind utilities;

  /* After */
  @import "tailwindcss";
  ```

- [ ] **Update component CSS files**
  ```bash
  find src/ -name "*.css" -exec grep -l "@tailwind" {} \;
  ```
- [ ] **Update global CSS files**
  ```bash
  find . -name "*.css" -exec grep -l "@tailwind" {} \;
  ```

### ✅ Convert Configuration

- [ ] **Convert theme configuration**
  ```css
  @theme {
    --color-primary: #3b82f6;
    --color-secondary: #10b981;
    --spacing-18: 4.5rem;
    --font-sans: "Inter", "sans-serif";
  }
  ```
- [ ] **Convert plugin configuration**
  ```css
  @plugin "@tailwindcss/forms";
  @plugin "@tailwindcss/typography";
  ```
- [ ] **Convert custom utilities**
  ```css
  @utility btn-primary {
    background-color: theme("colors.blue.500");
    color: theme("colors.white");
    padding: theme("spacing.2") theme("spacing.4");
    border-radius: theme("borderRadius.md");
  }
  ```

## 🔧 Build Tool Updates

### ✅ Vite Configuration

- [ ] **Update vite.config.ts**

  ```typescript
  import { defineConfig } from "vite";
  import react from "@vitejs/plugin-react";
  import tailwindcss from "@tailwindcss/vite";

  export default defineConfig({
    plugins: [react(), tailwindcss()],
  });
  ```

- [ ] **Remove old PostCSS configuration**
  ```typescript
  // Remove this from vite.config.ts
  css: {
    postcss: {
      plugins: [tailwindcss, autoprefixer],
    },
  },
  ```

### ✅ PostCSS Configuration

- [ ] **Update postcss.config.mjs**

  ```javascript
  const config = {
    plugins: {
      "@tailwindcss/postcss": {},
    },
  };

  export default config;
  ```

- [ ] **Remove old PostCSS plugins**
  ```bash
  npm uninstall autoprefixer
  ```

### ✅ Webpack Configuration

- [ ] **Update webpack.config.js** (if using Webpack)
  ```javascript
  module.exports = {
    module: {
      rules: [
        {
          test: /\.css$/,
          use: [
            "style-loader",
            "css-loader",
            {
              loader: "postcss-loader",
              options: {
                postcssOptions: {
                  plugins: ["@tailwindcss/postcss"],
                },
              },
            },
          ],
        },
      ],
    },
  };
  ```

## 🎨 Component Updates

### ✅ React Components

- [ ] **Update component imports**
  ```jsx
  // Check for any Tailwind-specific imports
  grep -r "tailwind" src/components/
  ```
- [ ] **Update component classes**

  ```jsx
  // Before: Utility classes
  <div className="bg-white rounded-lg shadow-md p-6">

  // After: Custom utilities (if applicable)
  <div className="card">
  ```

- [ ] **Test component rendering**
  ```bash
  npm run dev
  ```

### ✅ Vue Components

- [ ] **Update component classes**
  ```vue
  <!-- Check for Tailwind classes -->
  grep -r "class=" src/components/
  ```
- [ ] **Update component styling**

  ```vue
  <!-- Before: Utility classes -->
  <div class="bg-white rounded-lg shadow-md p-6">

  <!-- After: Custom utilities (if applicable) -->
  <div class="card">
  ```

### ✅ Svelte Components

- [ ] **Update component classes**
  ```svelte
  <!-- Check for Tailwind classes -->
  grep -r "class=" src/components/
  ```
- [ ] **Update component styling**

  ```svelte
  <!-- Before: Utility classes -->
  <div class="bg-white rounded-lg shadow-md p-6">

  <!-- After: Custom utilities (if applicable) -->
  <div class="card">
  ```

## 🧪 Testing

### ✅ Build Testing

- [ ] **Test build process**
  ```bash
  npm run build
  ```
- [ ] **Check for build errors**
  ```bash
  npm run build 2>&1 | grep -i error
  ```
- [ ] **Check for build warnings**
  ```bash
  npm run build 2>&1 | grep -i warning
  ```

### ✅ Development Testing

- [ ] **Test development server**
  ```bash
  npm run dev
  ```
- [ ] **Check for runtime errors**
  ```bash
  npm run dev 2>&1 | grep -i error
  ```
- [ ] **Test Hot Module Replacement**
  - [ ] Make a change to a component
  - [ ] Verify HMR works
  - [ ] Check for console errors

### ✅ Visual Testing

- [ ] **Test responsive design**
  - [ ] Check mobile breakpoints
  - [ ] Check tablet breakpoints
  - [ ] Check desktop breakpoints
- [ ] **Test component styling**
  - [ ] Check button styles
  - [ ] Check form styles
  - [ ] Check card styles
  - [ ] Check navigation styles
- [ ] **Test dark mode** (if applicable)
  - [ ] Toggle dark mode
  - [ ] Check component styling
  - [ ] Verify theme switching

### ✅ Performance Testing

- [ ] **Test build performance**
  ```bash
  time npm run build
  ```
- [ ] **Test bundle size**
  ```bash
  npm run build -- --analyze
  ```
- [ ] **Test runtime performance**
  - [ ] Check page load times
  - [ ] Check component render times
  - [ ] Monitor memory usage

## 🔍 Issue Resolution

### ✅ Common Issues

- [ ] **Module not found errors**
  - [ ] Check package installation
  - [ ] Verify import statements
  - [ ] Update configuration files
- [ ] **Build errors**
  - [ ] Check PostCSS configuration
  - [ ] Verify plugin installation
  - [ ] Update build tools
- [ ] **Styling issues**
  - [ ] Check CSS imports
  - [ ] Verify theme configuration
  - [ ] Test custom utilities
- [ ] **Plugin issues**
  - [ ] Update plugin packages
  - [ ] Check plugin configuration
  - [ ] Test plugin functionality

### ✅ Debugging

- [ ] **Enable debug mode**
  ```bash
  DEBUG=tailwindcss npm run build
  ```
- [ ] **Check configuration**
  ```bash
  npx tailwindcss --help
  ```
- [ ] **Test configuration**
  ```bash
  npx tailwindcss --config postcss.config.mjs
  ```

## 🚀 Deployment

### ✅ Pre-Deployment

- [ ] **Final build test**
  ```bash
  npm run build
  ```
- [ ] **Production build test**
  ```bash
  NODE_ENV=production npm run build
  ```
- [ ] **Bundle analysis**
  ```bash
  npm run build -- --analyze
  ```

### ✅ Staging Deployment

- [ ] **Deploy to staging**
  ```bash
  npm run deploy:staging
  ```
- [ ] **Test in staging environment**
  - [ ] Check all pages
  - [ ] Test all components
  - [ ] Verify responsive design
  - [ ] Test performance
- [ ] **User acceptance testing**
  - [ ] Test with real users
  - [ ] Check accessibility
  - [ ] Verify functionality

### ✅ Production Deployment

- [ ] **Deploy to production**
  ```bash
  npm run deploy:production
  ```
- [ ] **Monitor production**
  - [ ] Check error logs
  - [ ] Monitor performance
  - [ ] Check user feedback
- [ ] **Rollback plan**
  - [ ] Prepare rollback procedure
  - [ ] Test rollback process
  - [ ] Document rollback steps

## 📚 Documentation

### ✅ Update Documentation

- [ ] **Update README.md**
  - [ ] Update installation instructions
  - [ ] Update configuration examples
  - [ ] Update build instructions
- [ ] **Update component documentation**
  - [ ] Update component examples
  - [ ] Update styling guidelines
  - [ ] Update usage instructions
- [ ] **Update team documentation**
  - [ ] Update development guidelines
  - [ ] Update deployment procedures
  - [ ] Update troubleshooting guides

### ✅ Team Training

- [ ] **Train development team**
  - [ ] Explain v4 changes
  - [ ] Show new configuration
  - [ ] Demonstrate new features
- [ ] **Update development guidelines**
  - [ ] Update coding standards
  - [ ] Update review guidelines
  - [ ] Update testing procedures

## 🎯 Post-Migration

### ✅ Monitoring

- [ ] **Monitor performance**
  - [ ] Check build times
  - [ ] Monitor bundle size
  - [ ] Track performance metrics
- [ ] **Monitor errors**
  - [ ] Check error logs
  - [ ] Monitor user feedback
  - [ ] Track issue reports
- [ ] **Monitor usage**
  - [ ] Track feature usage
  - [ ] Monitor user behavior
  - [ ] Check conversion rates

### ✅ Optimization

- [ ] **Optimize build process**
  - [ ] Fine-tune configuration
  - [ ] Optimize dependencies
  - [ ] Improve build performance
- [ ] **Optimize runtime**
  - [ ] Optimize component rendering
  - [ ] Improve user experience
  - [ ] Enhance performance
- [ ] **Optimize bundle size**
  - [ ] Remove unused code
  - [ ] Optimize imports
  - [ ] Minimize dependencies

## 🚀 Next Steps

1. **Complete all checklist items** systematically
2. **Test thoroughly** at each step
3. **Document any issues** encountered
4. **Share knowledge** with your team
5. **Monitor and optimize** after deployment

## 💡 Pro Tips

- **Take your time**: Don't rush through the migration
- **Test incrementally**: Test each step before moving to the next
- **Document everything**: Keep track of what you've done
- **Get help when needed**: Use community resources
- **Plan for rollback**: Always have a backup plan

---

Migration complete! Your Tailwind CSS v4+ setup is ready to go. Check out the [Resources](../7-resources/README.md) section for additional tools and community support.
