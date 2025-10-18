# 🌐 HTML Examples

Sample HTML projects demonstrating Tailwind CSS v4+ usage in standalone HTML applications.

## 🎯 Overview

This directory contains complete HTML examples that showcase Tailwind CSS v4+ features and best practices.

## 📁 Project Structure

```
html-examples/
├── README.md
├── basic-setup/
│   ├── index.html
│   ├── src/
│   │   └── input.css
│   └── dist/
│       └── output.css
├── landing-page/
│   ├── index.html
│   ├── src/
│   │   └── input.css
│   └── dist/
│       └── output.css
├── portfolio/
│   ├── index.html
│   ├── about.html
│   ├── contact.html
│   ├── src/
│   │   └── input.css
│   └── dist/
│       └── output.css
└── e-commerce/
    ├── index.html
    ├── product.html
    ├── cart.html
    ├── src/
    │   └── input.css
    └── dist/
        └── output.css
```

## 🚀 Getting Started

### 1. Basic Setup

```bash
# Navigate to basic setup example
cd examples/html-examples/basic-setup

# Install dependencies
npm install

# Build CSS
npm run build

# Start development server
npm run dev
```

### 2. Landing Page

```bash
# Navigate to landing page example
cd examples/html-examples/landing-page

# Install dependencies
npm install

# Build CSS
npm run build

# Start development server
npm run dev
```

### 3. Portfolio

```bash
# Navigate to portfolio example
cd examples/html-examples/portfolio

# Install dependencies
npm install

# Build CSS
npm run build

# Start development server
npm run dev
```

### 4. E-commerce

```bash
# Navigate to e-commerce example
cd examples/html-examples/e-commerce

# Install dependencies
npm install

# Build CSS
npm run build

# Start development server
npm run dev
```

## 📋 Features

### 1. Basic Setup

- **Simple HTML structure**
- **Tailwind CSS v4+ configuration**
- **Basic styling examples**
- **Responsive design**
- **Custom utilities**

### 2. Landing Page

- **Hero section**
- **Features section**
- **Testimonials**
- **Call-to-action**
- **Footer**

### 3. Portfolio

- **Navigation**
- **Hero section**
- **About section**
- **Projects showcase**
- **Contact form**

### 4. E-commerce

- **Product catalog**
- **Shopping cart**
- **Checkout process**
- **User authentication**
- **Order management**

## 🎨 Design System

### 1. Color Palette

```css
@theme {
  --color-primary: #3b82f6;
  --color-secondary: #10b981;
  --color-accent: #f59e0b;
  --color-neutral: #6b7280;
  --color-success: #22c55e;
  --color-warning: #f59e0b;
  --color-error: #ef4444;
  --color-info: #3b82f6;
}
```

### 2. Typography

```css
@theme {
  --font-sans: "Inter", "system-ui", "sans-serif";
  --font-serif: "Georgia", "serif";
  --font-mono: "Fira Code", "monospace";

  --font-size-xs: 0.75rem;
  --font-size-sm: 0.875rem;
  --font-size-base: 1rem;
  --font-size-lg: 1.125rem;
  --font-size-xl: 1.25rem;
  --font-size-2xl: 1.5rem;
  --font-size-3xl: 1.875rem;
  --font-size-4xl: 2.25rem;
}
```

### 3. Spacing

```css
@theme {
  --spacing-0: 0;
  --spacing-1: 0.25rem;
  --spacing-2: 0.5rem;
  --spacing-3: 0.75rem;
  --spacing-4: 1rem;
  --spacing-5: 1.25rem;
  --spacing-6: 1.5rem;
  --spacing-8: 2rem;
  --spacing-10: 2.5rem;
  --spacing-12: 3rem;
  --spacing-16: 4rem;
  --spacing-20: 5rem;
  --spacing-24: 6rem;
}
```

## 🔧 Custom Utilities

### 1. Button Components

```css
@utility btn-primary {
  background-color: theme("colors.blue.500");
  color: theme("colors.white");
  padding: theme("spacing.2") theme("spacing.4");
  border-radius: theme("borderRadius.md");
  font-weight: theme("fontWeight.medium");
  transition: all 0.2s ease-in-out;

  &:hover {
    background-color: theme("colors.blue.600");
    transform: translateY(-1px);
  }

  &:focus {
    outline: 2px solid theme("colors.blue.300");
    outline-offset: 2px;
  }
}

@utility btn-secondary {
  background-color: theme("colors.gray.200");
  color: theme("colors.gray.800");
  padding: theme("spacing.2") theme("spacing.4");
  border-radius: theme("borderRadius.md");
  font-weight: theme("fontWeight.medium");
  transition: all 0.2s ease-in-out;

  &:hover {
    background-color: theme("colors.gray.300");
  }
}
```

### 2. Card Components

```css
@utility card {
  background-color: theme("colors.white");
  border-radius: theme("borderRadius.lg");
  box-shadow: theme("boxShadow.md");
  padding: theme("spacing.6");
  transition: all 0.2s ease-in-out;

  &:hover {
    box-shadow: theme("boxShadow.lg");
    transform: translateY(-2px);
  }
}

@utility card-header {
  font-size: theme("fontSize.xl");
  font-weight: theme("fontWeight.bold");
  color: theme("colors.gray.900");
  margin-bottom: theme("spacing.4");
}

@utility card-body {
  color: theme("colors.gray.600");
  line-height: theme("lineHeight.relaxed");
}
```

### 3. Form Components

```css
@utility form-input {
  border: 1px solid theme("colors.gray.300");
  border-radius: theme("borderRadius.md");
  padding: theme("spacing.2") theme("spacing.3");
  font-size: theme("fontSize.sm");
  transition: all 0.2s ease-in-out;

  &:focus {
    border-color: theme("colors.blue.500");
    outline: none;
    box-shadow: 0 0 0 3px theme("colors.blue.100");
  }
}

@utility form-label {
  font-weight: theme("fontWeight.medium");
  color: theme("colors.gray.700");
  margin-bottom: theme("spacing.1");
  display: block;
}
```

## 📱 Responsive Design

### 1. Mobile-First Approach

```html
<!-- Mobile-first responsive design -->
<div
  class="
  grid grid-cols-1
  sm:grid-cols-2
  md:grid-cols-3
  lg:grid-cols-4
  xl:grid-cols-5
  gap-4
"
>
  <!-- Responsive grid -->
</div>
```

### 2. Breakpoint System

```css
/* Default breakpoints */
sm: 640px    /* Small devices */
md: 768px    /* Medium devices */
lg: 1024px   /* Large devices */
xl: 1280px   /* Extra large devices */
2xl: 1536px  /* 2X large devices */
```

### 3. Responsive Utilities

```html
<!-- Responsive text -->
<h1
  class="
  text-2xl
  sm:text-3xl
  md:text-4xl
  lg:text-5xl
  xl:text-6xl
  font-bold
  text-gray-900
"
>
  Responsive Heading
</h1>

<!-- Responsive spacing -->
<div
  class="
  p-4
  sm:p-6
  md:p-8
  lg:p-10
  xl:p-12
"
>
  <!-- Responsive padding -->
</div>
```

## 🎯 Best Practices

### 1. HTML Structure

```html
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <title>Tailwind CSS v4+ Example</title>
    <link href="./dist/output.css" rel="stylesheet" />
  </head>
  <body class="bg-gray-100 min-h-screen">
    <!-- Page content -->
  </body>
</html>
```

### 2. CSS Organization

```css
/* src/input.css */
@import "tailwindcss";

@theme {
  --color-primary: #3b82f6;
  --color-secondary: #10b981;
}

@utility btn-primary {
  background-color: theme("colors.blue.500");
  color: theme("colors.white");
  padding: theme("spacing.2") theme("spacing.4");
  border-radius: theme("borderRadius.md");
}
```

### 3. Performance Optimization

```bash
# Build for production
npm run build

# Minify CSS
npm run build:min

# Watch for changes
npm run watch
```

## 🚀 Next Steps

1. **Explore the examples** to see Tailwind CSS v4+ in action
2. **Customize the design** to match your needs
3. **Add your own components** using the custom utilities
4. **Test responsive design** on different devices
5. **Deploy your project** to a hosting service

## 💡 Pro Tips

- **Start with the basic setup** to understand the fundamentals
- **Use the design system** for consistent styling
- **Test responsive design** on different screen sizes
- **Optimize for performance** by purging unused CSS
- **Document your custom utilities** for team collaboration

---

Ready to explore React examples? Check out the [React Examples](../react-examples/README.md) next!
