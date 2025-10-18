# Custom Variants

_Create conditional styles with the @custom-variant directive in Tailwind CSS v4+_

---

## 🎯 Overview

The `@custom-variant` directive in Tailwind CSS v4+ allows you to create custom conditional styles that work with any utility class. This powerful feature enables you to build sophisticated responsive designs, theme systems, and interactive states.

```mermaid
flowchart TD
    A[Custom Variants] --> B[@custom-variant Directive]
    A --> C[Theme Variants]
    A --> D[Media Query Variants]
    A --> E[State Variants]
    A --> F[Best Practices]

    B --> B1[Basic Syntax]
    B --> B2[Selector Patterns]
    B --> B3[Slot System]

    C --> C1[Dark Mode]
    C --> C2[Custom Themes]
    C --> C3[Theme Switching]

    D --> D1[Responsive Design]
    D --> D2[Print Styles]
    D --> D3[Accessibility]

    E --> E1[Hover Detection]
    E --> E2[Focus States]
    E --> E3[Custom States]

    F --> F1[Naming Conventions]
    F --> F2[Performance]
    F --> F3[Organization]

    style A fill:#e3f2fd
    style B fill:#f3e5f5
    style C fill:#e8f5e8
    style D fill:#fff3e0
    style E fill:#fce4ec
    style F fill:#f1f8e9
```

---

## 🚀 Basic Syntax

### Simple Variant

```css
@import "tailwindcss";

@custom-variant dark (&:where([data-theme="dark"] *));
```

### Media Query Variant

```css
@import "tailwindcss";

@custom-variant any-hover {
  @media (any-hover: hover) {
    &:hover {
      @slot;
    }
  }
}
```

### Complex Selector Variant

```css
@import "tailwindcss";

@custom-variant theme-midnight (&:where([data-theme="midnight"] *));
```

---

## 🎨 Theme Variants

### Dark Mode Variant

```css
@import "tailwindcss";

@custom-variant dark (&:where([data-theme="dark"] *));
```

### Using Dark Mode Variant

```html
<!-- Use your custom dark mode variant -->
<button class="bg-white dark:bg-black text-black dark:text-white">
  Theme-aware button
</button>

<div class="bg-gray-100 dark:bg-gray-800 text-gray-900 dark:text-gray-100">
  Theme-aware content
</div>
```

### Multiple Theme Variants

```css
@import "tailwindcss";

@custom-variant dark (&:where([data-theme="dark"] *));
@custom-variant light (&:where([data-theme="light"] *));
@custom-variant high-contrast (&:where([data-theme="high-contrast"] *));
@custom-variant theme-midnight (&:where([data-theme="midnight"] *));
@custom-variant theme-sunset (&:where([data-theme="sunset"] *));
```

### Using Multiple Theme Variants

```html
<!-- Use multiple theme variants -->
<button
  class="
  bg-white dark:bg-black
  high-contrast:bg-yellow-400
  theme-midnight:bg-purple-900
  theme-sunset:bg-orange-500
  text-black dark:text-white
  high-contrast:text-black
  theme-midnight:text-white
  theme-sunset:text-white
"
>
  Multi-theme button
</button>
```

### Theme Switching Implementation

```javascript
// Theme switching functionality
function setTheme(theme) {
  document.documentElement.setAttribute("data-theme", theme);
  localStorage.setItem("theme", theme);
}

// Load saved theme
const savedTheme = localStorage.getItem("theme") || "light";
setTheme(savedTheme);

// Theme toggle button
document.getElementById("theme-toggle").addEventListener("click", () => {
  const currentTheme = document.documentElement.getAttribute("data-theme");
  const newTheme = currentTheme === "dark" ? "light" : "dark";
  setTheme(newTheme);
});
```

---

## 📱 Media Query Variants

### Responsive Variants

```css
@import "tailwindcss";

@custom-variant mobile-only {
  @media (max-width: 639px) {
    @slot;
  }
}

@custom-variant tablet-only {
  @media (min-width: 640px) and (max-width: 1023px) {
    @slot;
  }
}

@custom-variant desktop-only {
  @media (min-width: 1024px) {
    @slot;
  }
}
```

### Using Responsive Variants

```html
<!-- Use your custom responsive variants -->
<div
  class="
  text-sm
  mobile-only:text-xs
  tablet-only:text-base
  desktop-only:text-lg
"
>
  Responsive text
</div>

<div
  class="
  grid grid-cols-1
  mobile-only:grid-cols-1
  tablet-only:grid-cols-2
  desktop-only:grid-cols-3
"
>
  Responsive grid
</div>
```

### Print Variants

```css
@import "tailwindcss";

@custom-variant print {
  @media print {
    @slot;
  }
}

@custom-variant screen-only {
  @media screen {
    @slot;
  }
}
```

### Using Print Variants

```html
<!-- Use your custom print variants -->
<div
  class="
  bg-white text-black
  print:bg-transparent print:text-black
  print:shadow-none
"
>
  Print-friendly content
</div>

<button
  class="
  bg-blue-600 text-white px-4 py-2
  print:hidden
"
>
  Screen-only button
</button>
```

### Accessibility Variants

```css
@import "tailwindcss";

@custom-variant reduced-motion {
  @media (prefers-reduced-motion: reduce) {
    @slot;
  }
}

@custom-variant high-contrast {
  @media (prefers-contrast: high) {
    @slot;
  }
}

@custom-variant dark-mode {
  @media (prefers-color-scheme: dark) {
    @slot;
  }
}
```

### Using Accessibility Variants

```html
<!-- Use your custom accessibility variants -->
<div
  class="
  transition-all duration-300
  reduced-motion:transition-none
"
>
  Motion-aware content
</div>

<button
  class="
  bg-blue-600 text-white
  high-contrast:bg-blue-800 high-contrast:text-white
  dark-mode:bg-blue-500 dark-mode:text-white
"
>
  Accessible button
</button>
```

---

## 🎯 State Variants

### Hover Detection Variants

```css
@import "tailwindcss";

@custom-variant any-hover {
  @media (any-hover: hover) {
    &:hover {
      @slot;
    }
  }
}

@custom-variant no-hover {
  @media (any-hover: none) {
    @slot;
  }
}
```

### Using Hover Detection Variants

```html
<!-- Use your custom hover detection variants -->
<button
  class="
  bg-blue-600 text-white px-4 py-2
  any-hover:hover:bg-blue-700
  no-hover:active:bg-blue-700
"
>
  Hover-aware button
</button>
```

### Focus Variants

```css
@import "tailwindcss";

@custom-variant focus-visible {
  &:focus-visible {
    @slot;
  }
}

@custom-variant focus-within {
  &:focus-within {
    @slot;
  }
}
```

### Using Focus Variants

```html
<!-- Use your custom focus variants -->
<input
  class="
  border border-gray-300 rounded-lg px-3 py-2
  focus-visible:ring-2 focus-visible:ring-blue-500
  focus-within:border-blue-500
"
  placeholder="Focus me"
/>
```

### Custom State Variants

```css
@import "tailwindcss";

@custom-variant loading {
  &:where([data-state="loading"]) {
    @slot;
  }
}

@custom-variant error {
  &:where([data-state="error"]) {
    @slot;
  }
}

@custom-variant success {
  &:where([data-state="success"]) {
    @slot;
  }
}
```

### Using Custom State Variants

```html
<!-- Use your custom state variants -->
<button
  class="
  bg-blue-600 text-white px-4 py-2
  loading:opacity-50 loading:cursor-wait
  error:bg-red-600 error:text-white
  success:bg-green-600 success:text-white
"
  data-state="loading"
>
  State-aware button
</button>
```

---

## 🎨 Advanced Patterns

### Component Variants

```css
@import "tailwindcss";

@custom-variant card-hover {
  &:hover {
    @slot;
  }
}

@custom-variant card-focus {
  &:focus {
    @slot;
  }
}

@custom-variant card-active {
  &:active {
    @slot;
  }
}
```

### Using Component Variants

```html
<!-- Use your custom component variants -->
<div
  class="
  bg-white rounded-lg shadow-md p-6
  card-hover:shadow-lg card-hover:scale-105
  card-focus:ring-2 card-focus:ring-blue-500
  card-active:scale-95
  transition-all duration-200
"
>
  Interactive card
</div>
```

### Form Variants

```css
@import "tailwindcss";

@custom-variant form-valid {
  &:valid {
    @slot;
  }
}

@custom-variant form-invalid {
  &:invalid {
    @slot;
  }
}

@custom-variant form-required {
  &:required {
    @slot;
  }
}
```

### Using Form Variants

```html
<!-- Use your custom form variants -->
<input
  type="email"
  class="
  border border-gray-300 rounded-lg px-3 py-2
  form-valid:border-green-500 form-valid:bg-green-50
  form-invalid:border-red-500 form-invalid:bg-red-50
  form-required:border-blue-500
"
  required
/>
```

### Navigation Variants

```css
@import "tailwindcss";

@custom-variant nav-current {
  &:where([aria-current="page"]) {
    @slot;
  }
}

@custom-variant nav-active {
  &:where([data-active="true"]) {
    @slot;
  }
}
```

### Using Navigation Variants

```html
<!-- Use your custom navigation variants -->
<nav class="flex space-x-4">
  <a
    href="#"
    class="
    text-gray-500 hover:text-gray-900
    nav-current:bg-gray-100 nav-current:text-gray-900
    nav-active:bg-blue-100 nav-active:text-blue-900
  "
  >
    Home
  </a>
  <a
    href="#"
    class="
    text-gray-500 hover:text-gray-900
    nav-current:bg-gray-100 nav-current:text-gray-900
    nav-active:bg-blue-100 nav-active:text-blue-900
  "
    aria-current="page"
  >
    About
  </a>
</nav>
```

---

## 🎯 Best Practices

### 1. **Naming Conventions**

```css
/* Good: Clear, descriptive names */
@custom-variant dark (&:where([data-theme="dark"] *));
@custom-variant mobile-only {
  @media (max-width: 639px) {
    @slot;
  }
}
@custom-variant reduced-motion {
  @media (prefers-reduced-motion: reduce) {
    @slot;
  }
}

/* Avoid: Unclear, generic names */
@custom-variant theme (&:where([data-theme="dark"] *));
@custom-variant small {
  @media (max-width: 639px) {
    @slot;
  }
}
@custom-variant motion {
  @media (prefers-reduced-motion: reduce) {
    @slot;
  }
}
```

### 2. **Organization**

```css
/* Good: Group related variants */
/* Theme variants */
@custom-variant dark (&:where([data-theme="dark"] *));
@custom-variant light (&:where([data-theme="light"] *));
@custom-variant high-contrast (&:where([data-theme="high-contrast"] *));

/* Responsive variants */
@custom-variant mobile-only {
  @media (max-width: 639px) {
    @slot;
  }
}
@custom-variant tablet-only {
  @media (min-width: 640px) and (max-width: 1023px) {
    @slot;
  }
}
@custom-variant desktop-only {
  @media (min-width: 1024px) {
    @slot;
  }
}

/* Avoid: Random organization */
@custom-variant dark (&:where([data-theme="dark"] *));
@custom-variant mobile-only {
  @media (max-width: 639px) {
    @slot;
  }
}
@custom-variant light (&:where([data-theme="light"] *));
```

### 3. **Performance**

```css
/* Good: Efficient selectors */
@custom-variant dark (&:where([data-theme="dark"] *));
@custom-variant mobile-only {
  @media (max-width: 639px) {
    @slot;
  }
}

/* Avoid: Inefficient selectors */
@custom-variant dark (*:where([data-theme="dark"] *));
@custom-variant mobile-only {
  @media (max-width: 639px) {
    * {
      @slot;
    }
  }
}
```

### 4. **Consistency**

```css
/* Good: Consistent patterns */
@custom-variant dark (&:where([data-theme="dark"] *));
@custom-variant light (&:where([data-theme="light"] *));
@custom-variant high-contrast (&:where([data-theme="high-contrast"] *));

/* Avoid: Inconsistent patterns */
@custom-variant dark (&:where([data-theme="dark"] *));
@custom-variant light {
  @media (prefers-color-scheme: light) {
    @slot;
  }
}
@custom-variant high-contrast {
  @media (prefers-contrast: high) {
    @slot;
  }
}
```

---

## 🚀 Next Steps

Now that you understand custom variants:

1. **[Plugins](./plugins.md)** - Extend functionality with plugins
2. **[Performance](./performance.md)** - Optimize your builds
3. **[UI Examples](../4-ui-examples/README.md)** - See real-world implementations
4. **[Best Practices](../5-best-practices/README.md)** - Learn production patterns

---

**Ready to explore plugins?** 👉 **[Plugins Guide](./plugins.md)**

