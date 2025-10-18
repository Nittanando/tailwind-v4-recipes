# Plugins

_Extend Tailwind CSS v4+ functionality with the @plugin directive and third-party plugins_

---

## 🎯 Overview

The `@plugin` directive in Tailwind CSS v4+ allows you to load plugins directly in your CSS, extending the framework's functionality with additional utilities, components, and features. This system provides a clean, CSS-first approach to plugin management.

```mermaid
flowchart TD
    A[Plugins] --> B[@plugin Directive]
    A --> C[Official Plugins]
    A --> D[Third-party Plugins]
    A --> E[Custom Plugins]
    A --> F[Best Practices]

    B --> B1[Basic Syntax]
    B --> B2[Plugin Loading]
    B --> B3[Configuration]

    C --> C1[Typography]
    C --> C2[Forms]
    C --> C3[Container Queries]
    C --> C4[Aspect Ratio]

    D --> D1[Community Plugins]
    D --> D2[UI Libraries]
    D --> D3[Specialized Tools]

    E --> E1[Plugin Development]
    E --> E2[Custom Utilities]
    E --> E3[Plugin Distribution]

    F --> F1[Plugin Selection]
    F --> F2[Performance]
    F --> F3[Maintenance]

    style A fill:#e3f2fd
    style B fill:#f3e5f5
    style C fill:#e8f5e8
    style D fill:#fff3e0
    style E fill:#fce4ec
    style F fill:#f1f8e9
```

---

## 🚀 Basic Syntax

### Loading Plugins

```css
@import "tailwindcss";

@plugin "@tailwindcss/typography";
@plugin "@tailwindcss/forms";
@plugin "@tailwindcss/container-queries";
```

### Plugin Configuration

```css
@import "tailwindcss";

@plugin "@tailwindcss/typography" {
  /* Plugin configuration goes here */
}
```

---

## 🎨 Official Plugins

### Typography Plugin

The Typography plugin provides beautiful typography styles for rich text content.

```css
@import "tailwindcss";

@plugin "@tailwindcss/typography";
```

#### Using Typography Plugin

```html
<!-- Use typography styles -->
<article class="prose">
  <h1>Typography Plugin Example</h1>
  <p>
    This is a paragraph with beautiful typography styles applied automatically.
  </p>
  <h2>Subheading</h2>
  <p>Another paragraph with consistent spacing and typography.</p>
  <ul>
    <li>List item 1</li>
    <li>List item 2</li>
    <li>List item 3</li>
  </ul>
</article>

<!-- Customize typography styles -->
<article class="prose prose-lg prose-blue">
  <h1>Large Blue Typography</h1>
  <p>This article uses large, blue typography styles.</p>
</article>
```

#### Typography Variants

```html
<!-- Size variants -->
<article class="prose prose-sm">Small typography</article>
<article class="prose prose-base">Base typography</article>
<article class="prose prose-lg">Large typography</article>
<article class="prose prose-xl">Extra large typography</article>

<!-- Color variants -->
<article class="prose prose-gray">Gray typography</article>
<article class="prose prose-blue">Blue typography</article>
<article class="prose prose-green">Green typography</article>
<article class="prose prose-red">Red typography</article>

<!-- Dark mode support -->
<article class="prose dark:prose-invert">Dark mode typography</article>
```

### Forms Plugin

The Forms plugin provides better default styles for form elements.

```css
@import "tailwindcss";

@plugin "@tailwindcss/forms";
```

#### Using Forms Plugin

```html
<!-- Form elements with better styling -->
<form class="space-y-4">
  <div>
    <label class="block text-sm font-medium text-gray-700 mb-1">
      Email Address
    </label>
    <input
      type="email"
      class="
      w-full border border-gray-300 rounded-lg px-3 py-2
      focus:border-blue-500 focus:ring-2 focus:ring-blue-200
      focus:outline-none
    "
      placeholder="Enter your email"
    />
  </div>

  <div>
    <label class="block text-sm font-medium text-gray-700 mb-1">
      Password
    </label>
    <input
      type="password"
      class="
      w-full border border-gray-300 rounded-lg px-3 py-2
      focus:border-blue-500 focus:ring-2 focus:ring-blue-200
      focus:outline-none
    "
      placeholder="Enter your password"
    />
  </div>

  <div class="flex items-center">
    <input
      type="checkbox"
      class="
      h-4 w-4 text-blue-600 border-gray-300 rounded
      focus:ring-blue-500
    "
    />
    <label class="ml-2 text-sm text-gray-700"> Remember me </label>
  </div>

  <div>
    <label class="block text-sm font-medium text-gray-700 mb-1">
      Message
    </label>
    <textarea
      class="
      w-full border border-gray-300 rounded-lg px-3 py-2
      focus:border-blue-500 focus:ring-2 focus:ring-blue-200
      focus:outline-none
    "
      rows="4"
      placeholder="Enter your message"
    ></textarea>
  </div>

  <button
    type="submit"
    class="
    w-full bg-blue-600 text-white py-2 px-4 rounded-lg
    hover:bg-blue-700 focus:ring-2 focus:ring-blue-500
    transition-colors duration-200
  "
  >
    Submit
  </button>
</form>
```

### Container Queries Plugin

The Container Queries plugin provides utilities for container-based responsive design.

```css
@import "tailwindcss";

@plugin "@tailwindcss/container-queries";
```

#### Using Container Queries Plugin

```html
<!-- Container query utilities -->
<div class="@container">
  <div
    class="
    grid grid-cols-1
    @sm:grid-cols-2
    @md:grid-cols-3
    @lg:grid-cols-4
    gap-4
  "
  >
    <div class="bg-white p-4 rounded-lg shadow">Item 1</div>
    <div class="bg-white p-4 rounded-lg shadow">Item 2</div>
    <div class="bg-white p-4 rounded-lg shadow">Item 3</div>
    <div class="bg-white p-4 rounded-lg shadow">Item 4</div>
  </div>
</div>

<!-- Container query typography -->
<div class="@container">
  <h2
    class="
    text-lg
    @sm:text-xl
    @md:text-2xl
    @lg:text-3xl
    font-bold
  "
  >
    Container-responsive heading
  </h2>
</div>
```

### Aspect Ratio Plugin

The Aspect Ratio plugin provides utilities for maintaining aspect ratios.

```css
@import "tailwindcss";

@plugin "@tailwindcss/aspect-ratio";
```

#### Using Aspect Ratio Plugin

```html
<!-- Aspect ratio utilities -->
<div class="aspect-square bg-gray-200 rounded-lg">
  <!-- Square aspect ratio -->
</div>

<div class="aspect-video bg-gray-200 rounded-lg">
  <!-- 16:9 aspect ratio -->
</div>

<div class="aspect-4/3 bg-gray-200 rounded-lg">
  <!-- 4:3 aspect ratio -->
</div>

<div class="aspect-3/2 bg-gray-200 rounded-lg">
  <!-- 3:2 aspect ratio -->
</div>

<!-- Responsive aspect ratios -->
<div
  class="
  aspect-square
  sm:aspect-video
  md:aspect-4/3
  lg:aspect-3/2
  bg-gray-200 rounded-lg
"
>
  Responsive aspect ratio
</div>
```

---

## 🔌 Third-party Plugins

### Popular Community Plugins

#### Headless UI

```css
@import "tailwindcss";

@plugin "@headlessui/tailwindcss";
```

#### Heroicons

```css
@import "tailwindcss";

@plugin "@heroicons/tailwindcss";
```

#### Tailwind UI

```css
@import "tailwindcss";

@plugin "@tailwindui/tailwindcss";
```

### Using Third-party Plugins

```html
<!-- Headless UI components -->
<div class="relative">
  <button
    class="
    bg-blue-600 text-white px-4 py-2 rounded-lg
    hover:bg-blue-700 focus:ring-2 focus:ring-blue-500
  "
  >
    Toggle Menu
  </button>

  <div
    class="
    absolute top-full left-0 mt-2 w-48
    bg-white rounded-lg shadow-lg border border-gray-200
    hidden
  "
  >
    <a
      href="#"
      class="
      block px-4 py-2 text-gray-700 hover:bg-gray-100
      first:rounded-t-lg last:rounded-b-lg
    "
    >
      Menu Item 1
    </a>
    <a
      href="#"
      class="
      block px-4 py-2 text-gray-700 hover:bg-gray-100
      first:rounded-t-lg last:rounded-b-lg
    "
    >
      Menu Item 2
    </a>
  </div>
</div>
```

---

## 🛠️ Custom Plugins

### Creating Custom Plugins

While Tailwind CSS v4+ focuses on CSS-first configuration, you can still create custom plugins for complex functionality:

```javascript
// custom-plugin.js
module.exports = function ({ addUtilities, addComponents, addBase, theme }) {
  // Add custom utilities
  addUtilities({
    ".text-shadow": {
      textShadow: "0 2px 4px rgba(0, 0, 0, 0.1)",
    },
    ".text-shadow-lg": {
      textShadow: "0 4px 8px rgba(0, 0, 0, 0.15)",
    },
  });

  // Add custom components
  addComponents({
    ".btn": {
      padding: theme("spacing.2") + " " + theme("spacing.4"),
      borderRadius: theme("borderRadius.lg"),
      fontWeight: theme("fontWeight.medium"),
      transition: "colors 0.2s",
    },
    ".btn-primary": {
      backgroundColor: theme("colors.blue.600"),
      color: theme("colors.white"),
      "&:hover": {
        backgroundColor: theme("colors.blue.700"),
      },
    },
  });

  // Add base styles
  addBase({
    html: {
      fontFamily: theme("fontFamily.sans"),
    },
  });
};
```

### Loading Custom Plugins

```css
@import "tailwindcss";

@plugin "./custom-plugin.js";
```

---

## 🎯 Plugin Configuration

### Typography Plugin Configuration

```css
@import "tailwindcss";

@plugin "@tailwindcss/typography" {
  /* Customize typography styles */
  --typography-color: theme("colors.gray.900");
  --typography-heading-color: theme("colors.gray.900");
  --typography-link-color: theme("colors.blue.600");
  --typography-link-hover-color: theme("colors.blue.700");
}
```

### Forms Plugin Configuration

```css
@import "tailwindcss";

@plugin "@tailwindcss/forms" {
  /* Customize form styles */
  --form-input-border-color: theme("colors.gray.300");
  --form-input-focus-border-color: theme("colors.blue.500");
  --form-input-focus-ring-color: theme("colors.blue.200");
}
```

### Container Queries Plugin Configuration

```css
@import "tailwindcss";

@plugin "@tailwindcss/container-queries" {
  /* Customize container query breakpoints */
  --container-sm: 640px;
  --container-md: 768px;
  --container-lg: 1024px;
  --container-xl: 1280px;
}
```

---

## 🎨 Plugin Combinations

### Complete Setup

```css
@import "tailwindcss";

/* Official plugins */
@plugin "@tailwindcss/typography";
@plugin "@tailwindcss/forms";
@plugin "@tailwindcss/container-queries";
@plugin "@tailwindcss/aspect-ratio";

/* Third-party plugins */
@plugin "@headlessui/tailwindcss";
@plugin "@heroicons/tailwindcss";

/* Custom plugins */
@plugin "./custom-plugin.js";
```

### Using Multiple Plugins

```html
<!-- Typography plugin -->
<article class="prose prose-lg prose-blue">
  <h1>Article Title</h1>
  <p>Article content with beautiful typography.</p>
</article>

<!-- Forms plugin -->
<form class="space-y-4">
  <input
    type="email"
    class="
    w-full border border-gray-300 rounded-lg px-3 py-2
    focus:border-blue-500 focus:ring-2 focus:ring-blue-200
  "
    placeholder="Email"
  />
</form>

<!-- Container queries plugin -->
<div class="@container">
  <div
    class="
    grid grid-cols-1
    @sm:grid-cols-2
    @md:grid-cols-3
    gap-4
  "
  >
    <!-- Grid items -->
  </div>
</div>

<!-- Aspect ratio plugin -->
<div class="aspect-video bg-gray-200 rounded-lg">
  <!-- Video content -->
</div>
```

---

## 🎯 Best Practices

### 1. **Plugin Selection**

```css
/* Good: Only load plugins you need */
@import "tailwindcss";

@plugin "@tailwindcss/typography";
@plugin "@tailwindcss/forms";

/* Avoid: Loading unnecessary plugins */
@import "tailwindcss";

@plugin "@tailwindcss/typography";
@plugin "@tailwindcss/forms";
@plugin "@tailwindcss/container-queries";
@plugin "@tailwindcss/aspect-ratio";
@plugin "@headlessui/tailwindcss";
@plugin "@heroicons/tailwindcss";
/* ... many more plugins */
```

### 2. **Performance Considerations**

```css
/* Good: Load plugins in order of importance */
@import "tailwindcss";

@plugin "@tailwindcss/typography"; /* Most used */
@plugin "@tailwindcss/forms"; /* Frequently used */
@plugin "@tailwindcss/container-queries"; /* Occasionally used */

/* Avoid: Loading plugins in random order */
@import "tailwindcss";

@plugin "@tailwindcss/container-queries";
@plugin "@tailwindcss/typography";
@plugin "@tailwindcss/forms";
```

### 3. **Configuration**

```css
/* Good: Configure plugins when needed */
@import "tailwindcss";

@plugin "@tailwindcss/typography" {
  --typography-color: theme("colors.gray.900");
  --typography-heading-color: theme("colors.gray.900");
}

/* Avoid: Over-configuring plugins */
@import "tailwindcss";

@plugin "@tailwindcss/typography" {
  --typography-color: theme("colors.gray.900");
  --typography-heading-color: theme("colors.gray.900");
  --typography-link-color: theme("colors.blue.600");
  --typography-link-hover-color: theme("colors.blue.700");
  --typography-code-color: theme("colors.gray.800");
  --typography-code-background: theme("colors.gray.100");
  /* ... many more customizations */
}
```

### 4. **Maintenance**

```css
/* Good: Document plugin usage */
@import "tailwindcss";

/* Typography plugin for rich text content */
@plugin "@tailwindcss/typography";

/* Forms plugin for better form styling */
@plugin "@tailwindcss/forms";

/* Container queries for component-based responsive design */
@plugin "@tailwindcss/container-queries";

/* Avoid: No documentation */
@import "tailwindcss";

@plugin "@tailwindcss/typography";
@plugin "@tailwindcss/forms";
@plugin "@tailwindcss/container-queries";
```

---

## 🚀 Next Steps

Now that you understand plugins:

1. **[Performance](./performance.md)** - Optimize your builds
2. **[UI Examples](../4-ui-examples/README.md)** - See real-world implementations
3. **[Best Practices](../5-best-practices/README.md)** - Learn production patterns
4. **[Migration Guide](../6-migration/README.md)** - Upgrade from v3 to v4

---

**Ready to optimize performance?** 👉 **[Performance Guide](./performance.md)**

