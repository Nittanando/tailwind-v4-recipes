# 🛠️ Development Tools

Essential tools and utilities for working with Tailwind CSS v4+ effectively.

## 🎯 Overview

This guide covers development tools, IDE extensions, online utilities, and command-line tools that enhance your Tailwind CSS v4+ development experience.

## 💻 IDE Extensions

### 1. VS Code Extensions

```json
{
  "recommendations": [
    "bradlc.vscode-tailwindcss",
    "formulahendry.auto-rename-tag",
    "ms-vscode.vscode-typescript-next",
    "esbenp.prettier-vscode",
    "ms-vscode.vscode-json"
  ]
}
```

**Tailwind CSS IntelliSense**

- Autocomplete for class names
- Hover previews for styles
- Linting and error detection
- Color previews
- Documentation on hover

**Installation**:

```bash
# Install via VS Code
code --install-extension bradlc.vscode-tailwindcss

# Or search in VS Code Extensions
# Search: "Tailwind CSS IntelliSense"
```

### 2. WebStorm Support

```javascript
// WebStorm Tailwind CSS support
// Enable in Settings > Languages & Frameworks > CSS > Tailwind CSS
{
  "tailwind": {
    "enabled": true,
    "config": "tailwind.config.js",
    "css": "src/styles/globals.css"
  }
}
```

**Features**:

- Autocomplete for class names
- Hover previews
- Refactoring support
- Code completion
- Error highlighting

### 3. Sublime Text Package

```json
// Package Control: Install Package
// Search: "Tailwind CSS"
{
  "packages": [
    "Tailwind CSS",
    "Package Control",
    "SublimeLinter",
    "SublimeLinter-csslint"
  ]
}
```

**Features**:

- Syntax highlighting
- Autocomplete
- Snippets
- Linting support

### 4. Vim Plugin

```vim
" Install using vim-plug
Plug 'tailwindcss/tailwindcss', { 'for': ['html', 'css', 'javascript', 'typescript'] }

" Or using Vundle
Plugin 'tailwindcss/tailwindcss'

" Configuration
let g:tailwindcss_autocomplete = 1
let g:tailwindcss_hover_preview = 1
```

## 🌐 Online Tools

### 1. Tailwind Play

```html
<!-- Online playground for Tailwind CSS -->
<!-- URL: https://play.tailwindcss.com -->
<!DOCTYPE html>
<html>
  <head>
    <script src="https://cdn.tailwindcss.com"></script>
  </head>
  <body>
    <div class="bg-blue-500 text-white p-4 rounded-lg">Hello Tailwind!</div>
  </body>
</html>
```

**Features**:

- Live preview
- Code sharing
- Responsive testing
- Export options
- Collaboration

### 2. Tailwind UI

```html
<!-- Component library -->
<!-- URL: https://tailwindui.com -->
<div class="bg-white overflow-hidden shadow rounded-lg">
  <div class="px-4 py-5 sm:p-6">
    <h3 class="text-lg leading-6 font-medium text-gray-900">Component Title</h3>
    <div class="mt-2 max-w-xl text-sm text-gray-500">
      <p>Component description goes here.</p>
    </div>
  </div>
</div>
```

**Features**:

- Pre-built components
- Responsive designs
- Accessibility features
- Code examples
- Design system

### 3. Headless UI

```jsx
// Unstyled, accessible UI components
import { Dialog, Transition } from "@headlessui/react";

function MyDialog() {
  return (
    <Dialog>
      <Dialog.Overlay className="fixed inset-0 bg-black opacity-30" />
      <Dialog.Title className="text-lg font-medium">Dialog Title</Dialog.Title>
      <Dialog.Description className="text-sm text-gray-500">
        Dialog description goes here.
      </Dialog.Description>
    </Dialog>
  );
}
```

**Features**:

- Accessible components
- Unstyled by default
- Framework agnostic
- TypeScript support
- Documentation

### 4. Heroicons

```html
<!-- Icon library -->
<!-- URL: https://heroicons.com -->
<svg class="w-6 h-6" fill="none" stroke="currentColor" viewBox="0 0 24 24">
  <path
    stroke-linecap="round"
    stroke-linejoin="round"
    stroke-width="2"
    d="M12 4.354a4 4 0 110 5.292M15 21H3v-1a6 6 0 0112 0v1zm0 0h6v-1a6 6 0 00-9-5.197m13.5-9a2.5 2.5 0 11-5 0 2.5 2.5 0 015 0z"
  />
</svg>
```

**Features**:

- SVG icons
- Multiple styles
- Optimized for web
- Easy to customize
- Free to use

## 🔧 Command Line Tools

### 1. Tailwind CLI

```bash
# Install Tailwind CLI
npm install -g @tailwindcss/cli

# Basic usage
npx tailwindcss -i ./src/input.css -o ./dist/output.css

# Watch mode
npx tailwindcss -i ./src/input.css -o ./dist/output.css --watch

# Minify output
npx tailwindcss -i ./src/input.css -o ./dist/output.css --minify

# Content detection
npx tailwindcss -i ./src/input.css -o ./dist/output.css --content "./src/**/*.{js,jsx,ts,tsx}"
```

**Features**:

- Build CSS from source
- Watch mode for development
- Content detection
- Minification
- Source maps

### 2. PostCSS CLI

```bash
# Install PostCSS CLI
npm install -g postcss-cli

# Basic usage
postcss src/input.css -o dist/output.css

# With plugins
postcss src/input.css -o dist/output.css --use @tailwindcss/postcss

# Watch mode
postcss src/input.css -o dist/output.css --watch
```

**Features**:

- CSS processing
- Plugin support
- Watch mode
- Source maps
- Minification

### 3. Vite CLI

```bash
# Install Vite
npm install -g vite

# Development server
vite

# Build for production
vite build

# Preview build
vite preview
```

**Features**:

- Fast development server
- Hot Module Replacement
- Optimized builds
- Plugin ecosystem
- TypeScript support

## 🎨 Design Tools

### 1. Figma Plugins

```javascript
// Tailwind CSS Figma Plugin
// URL: https://www.figma.com/community/plugin/738806821514947478/Tailwind-CSS
{
  "name": "Tailwind CSS",
  "description": "Generate Tailwind CSS classes from Figma designs",
  "version": "1.0.0",
  "main": "code.js"
}
```

**Features**:

- Design to code
- Class generation
- Responsive design
- Component library
- Export options

### 2. Sketch Plugins

```javascript
// Tailwind CSS Sketch Plugin
// URL: https://github.com/tailwindcss/sketch-plugin
{
  "name": "Tailwind CSS",
  "description": "Sketch plugin for Tailwind CSS",
  "version": "1.0.0",
  "main": "plugin.js"
}
```

**Features**:

- Design system integration
- Component generation
- Style extraction
- Responsive design
- Export options

### 3. Adobe XD Plugins

```javascript
// Tailwind CSS XD Plugin
// URL: https://github.com/tailwindcss/xd-plugin
{
  "name": "Tailwind CSS",
  "description": "Adobe XD plugin for Tailwind CSS",
  "version": "1.0.0",
  "main": "plugin.js"
}
```

**Features**:

- Design system integration
- Component generation
- Style extraction
- Responsive design
- Export options

## 🔍 Development Utilities

### 1. CSS Purging

```bash
# Purge unused CSS
npx tailwindcss -i ./src/input.css -o ./dist/output.css --purge

# Purge with content detection
npx tailwindcss -i ./src/input.css -o ./dist/output.css --content "./src/**/*.{js,jsx,ts,tsx}"
```

**Features**:

- Remove unused styles
- Reduce bundle size
- Content detection
- Performance optimization
- Build optimization

### 2. CSS Analysis

```bash
# Analyze CSS bundle
npx tailwindcss -i ./src/input.css -o ./dist/output.css --analyze

# Generate CSS report
npx tailwindcss -i ./src/input.css -o ./dist/output.css --report
```

**Features**:

- Bundle analysis
- Size optimization
- Performance metrics
- Dependency tracking
- Build insights

### 3. CSS Validation

```bash
# Validate CSS
npx tailwindcss -i ./src/input.css -o ./dist/output.css --validate

# Check for errors
npx tailwindcss -i ./src/input.css -o ./dist/output.css --check
```

**Features**:

- CSS validation
- Error detection
- Syntax checking
- Best practices
- Performance validation

## 🧪 Testing Tools

### 1. Visual Regression Testing

```javascript
// Playwright visual testing
import { test, expect } from "@playwright/test";

test("visual regression test", async ({ page }) => {
  await page.goto("/");
  await expect(page).toHaveScreenshot("homepage.png");
});
```

**Features**:

- Visual comparison
- Regression detection
- Cross-browser testing
- Responsive testing
- Performance testing

### 2. Component Testing

```javascript
// Storybook for component testing
import { Meta, Story } from '@storybook/react';
import { Button } from './Button';

export default {
  title: 'Components/Button',
  component: Button,
} as Meta;

const Template: Story = (args) => <Button {...args} />;

export const Primary = Template.bind({});
Primary.args = {
  variant: 'primary',
  children: 'Click me',
};
```

**Features**:

- Component isolation
- Interactive testing
- Visual testing
- Documentation
- Collaboration

### 3. Accessibility Testing

```javascript
// Jest accessibility testing
import { render, screen } from "@testing-library/react";
import { axe, toHaveNoViolations } from "jest-axe";

expect.extend(toHaveNoViolations);

test("should not have accessibility violations", async () => {
  const { container } = render(<Button>Click me</Button>);
  const results = await axe(container);
  expect(results).toHaveNoViolations();
});
```

**Features**:

- Accessibility validation
- Screen reader testing
- Keyboard navigation
- Color contrast
- ARIA compliance

## 📊 Performance Tools

### 1. Bundle Analysis

```bash
# Analyze bundle size
npm run build -- --analyze

# Generate bundle report
npm run build -- --report
```

**Features**:

- Bundle size analysis
- Dependency tracking
- Performance metrics
- Optimization suggestions
- Build insights

### 2. Performance Monitoring

```javascript
// Performance monitoring
import { getCLS, getFID, getFCP, getLCP, getTTFB } from "web-vitals";

getCLS(console.log);
getFID(console.log);
getFCP(console.log);
getLCP(console.log);
getTTFB(console.log);
```

**Features**:

- Core Web Vitals
- Performance metrics
- Real user monitoring
- Performance insights
- Optimization guidance

### 3. Build Optimization

```typescript
// Vite build optimization
export default defineConfig({
  build: {
    rollupOptions: {
      output: {
        manualChunks: {
          tailwind: ["tailwindcss"],
          vendor: ["react", "react-dom"],
        },
      },
    },
  },
});
```

**Features**:

- Build optimization
- Code splitting
- Tree shaking
- Minification
- Performance tuning

## 🚀 Next Steps

1. **Install the tools** that fit your development workflow
2. **Configure your IDE** for the best Tailwind experience
3. **Set up testing** for quality assurance
4. **Monitor performance** for optimization
5. **Explore the community** for additional tools

## 💡 Pro Tips

- **Use the right tools**: Choose tools that fit your workflow
- **Configure properly**: Set up tools for maximum efficiency
- **Test regularly**: Use testing tools for quality assurance
- **Monitor performance**: Keep track of performance metrics
- **Stay updated**: Keep tools and extensions up to date

---

Ready to connect with the community? Check out the [Community](./community.md) guide next!
