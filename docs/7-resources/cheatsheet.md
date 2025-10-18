# 📋 Tailwind CSS v4+ Cheatsheet

Quick reference guide for Tailwind CSS v4+ classes, utilities, and configuration.

## 🎯 Overview

This cheatsheet provides quick reference for the most commonly used Tailwind CSS v4+ classes and utilities.

## 📐 Layout

### Flexbox

```html
<!-- Flex container -->
<div class="flex">
  <!-- display: flex -->
  <div class="inline-flex">
    <!-- display: inline-flex -->
    <div class="flex-row">
      <!-- flex-direction: row -->
      <div class="flex-col">
        <!-- flex-direction: column -->
        <div class="flex-wrap">
          <!-- flex-wrap: wrap -->
          <div class="flex-nowrap">
            <!-- flex-wrap: nowrap -->

            <!-- Flex alignment -->
            <div class="justify-start">
              <!-- justify-content: flex-start -->
              <div class="justify-center">
                <!-- justify-content: center -->
                <div class="justify-end">
                  <!-- justify-content: flex-end -->
                  <div class="justify-between">
                    <!-- justify-content: space-between -->
                    <div class="justify-around">
                      <!-- justify-content: space-around -->

                      <div class="items-start">
                        <!-- align-items: flex-start -->
                        <div class="items-center">
                          <!-- align-items: center -->
                          <div class="items-end">
                            <!-- align-items: flex-end -->
                            <div class="items-stretch">
                              <!-- align-items: stretch -->

                              <!-- Flex items -->
                              <div class="flex-1">
                                <!-- flex: 1 1 0% -->
                                <div class="flex-auto">
                                  <!-- flex: 1 1 auto -->
                                  <div class="flex-initial">
                                    <!-- flex: 0 1 auto -->
                                    <div class="flex-none">
                                      <!-- flex: none -->
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div></div
  >
</div>
```

### Grid

```html
<!-- Grid container -->
<div class="grid">
  <!-- display: grid -->
  <div class="inline-grid">
    <!-- display: inline-grid -->

    <!-- Grid columns -->
    <div class="grid-cols-1">
      <!-- grid-template-columns: repeat(1, minmax(0, 1fr)) -->
      <div class="grid-cols-2">
        <!-- grid-template-columns: repeat(2, minmax(0, 1fr)) -->
        <div class="grid-cols-3">
          <!-- grid-template-columns: repeat(3, minmax(0, 1fr)) -->
          <div class="grid-cols-4">
            <!-- grid-template-columns: repeat(4, minmax(0, 1fr)) -->
            <div class="grid-cols-6">
              <!-- grid-template-columns: repeat(6, minmax(0, 1fr)) -->
              <div class="grid-cols-12">
                <!-- grid-template-columns: repeat(12, minmax(0, 1fr)) -->

                <!-- Grid rows -->
                <div class="grid-rows-1">
                  <!-- grid-template-rows: repeat(1, minmax(0, 1fr)) -->
                  <div class="grid-rows-2">
                    <!-- grid-template-rows: repeat(2, minmax(0, 1fr)) -->
                    <div class="grid-rows-3">
                      <!-- grid-template-rows: repeat(3, minmax(0, 1fr)) -->

                      <!-- Grid gap -->
                      <div class="gap-0">
                        <!-- gap: 0px -->
                        <div class="gap-1">
                          <!-- gap: 0.25rem -->
                          <div class="gap-2">
                            <!-- gap: 0.5rem -->
                            <div class="gap-4">
                              <!-- gap: 1rem -->
                              <div class="gap-8">
                                <!-- gap: 2rem -->

                                <!-- Grid gap (specific) -->
                                <div class="gap-x-4">
                                  <!-- column-gap: 1rem -->
                                  <div class="gap-y-4">
                                    <!-- row-gap: 1rem -->
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div></div
  >
</div>
```

## 📏 Spacing

### Padding

```html
<div class="p-0">
  <!-- padding: 0px -->
  <div class="p-1">
    <!-- padding: 0.25rem -->
    <div class="p-2">
      <!-- padding: 0.5rem -->
      <div class="p-4">
        <!-- padding: 1rem -->
        <div class="p-8">
          <!-- padding: 2rem -->

          <!-- Padding (specific) -->
          <div class="pt-4">
            <!-- padding-top: 1rem -->
            <div class="pr-4">
              <!-- padding-right: 1rem -->
              <div class="pb-4">
                <!-- padding-bottom: 1rem -->
                <div class="pl-4">
                  <!-- padding-left: 1rem -->
                  <div class="px-4">
                    <!-- padding-left: 1rem; padding-right: 1rem -->
                    <div class="py-4">
                      <!-- padding-top: 1rem; padding-bottom: 1rem -->
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

### Margin

```html
<div class="m-0">
  <!-- margin: 0px -->
  <div class="m-1">
    <!-- margin: 0.25rem -->
    <div class="m-2">
      <!-- margin: 0.5rem -->
      <div class="m-4">
        <!-- margin: 1rem -->
        <div class="m-8">
          <!-- margin: 2rem -->

          <!-- Margin (specific) -->
          <div class="mt-4">
            <!-- margin-top: 1rem -->
            <div class="mr-4">
              <!-- margin-right: 1rem -->
              <div class="mb-4">
                <!-- margin-bottom: 1rem -->
                <div class="ml-4">
                  <!-- margin-left: 1rem -->
                  <div class="mx-4">
                    <!-- margin-left: 1rem; margin-right: 1rem -->
                    <div class="my-4">
                      <!-- margin-top: 1rem; margin-bottom: 1rem -->

                      <!-- Auto margin -->
                      <div class="mx-auto">
                        <!-- margin-left: auto; margin-right: auto -->
                        <div class="ml-auto">
                          <!-- margin-left: auto -->
                          <div class="mr-auto"><!-- margin-right: auto --></div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

## 🎨 Colors

### Background Colors

```html
<div class="bg-white">
  <!-- background-color: #ffffff -->
  <div class="bg-black">
    <!-- background-color: #000000 -->
    <div class="bg-gray-100">
      <!-- background-color: #f3f4f6 -->
      <div class="bg-gray-200">
        <!-- background-color: #e5e7eb -->
        <div class="bg-gray-300">
          <!-- background-color: #d1d5db -->
          <div class="bg-gray-400">
            <!-- background-color: #9ca3af -->
            <div class="bg-gray-500">
              <!-- background-color: #6b7280 -->
              <div class="bg-gray-600">
                <!-- background-color: #4b5563 -->
                <div class="bg-gray-700">
                  <!-- background-color: #374151 -->
                  <div class="bg-gray-800">
                    <!-- background-color: #1f2937 -->
                    <div class="bg-gray-900">
                      <!-- background-color: #111827 -->

                      <!-- Blue colors -->
                      <div class="bg-blue-100">
                        <!-- background-color: #dbeafe -->
                        <div class="bg-blue-500">
                          <!-- background-color: #3b82f6 -->
                          <div class="bg-blue-600">
                            <!-- background-color: #2563eb -->
                            <div class="bg-blue-700">
                              <!-- background-color: #1d4ed8 -->

                              <!-- Green colors -->
                              <div class="bg-green-100">
                                <!-- background-color: #dcfce7 -->
                                <div class="bg-green-500">
                                  <!-- background-color: #22c55e -->
                                  <div class="bg-green-600">
                                    <!-- background-color: #16a34a -->
                                    <div class="bg-green-700">
                                      <!-- background-color: #15803d -->

                                      <!-- Red colors -->
                                      <div class="bg-red-100">
                                        <!-- background-color: #fee2e2 -->
                                        <div class="bg-red-500">
                                          <!-- background-color: #ef4444 -->
                                          <div class="bg-red-600">
                                            <!-- background-color: #dc2626 -->
                                            <div class="bg-red-700">
                                              <!-- background-color: #b91c1c -->
                                            </div>
                                          </div>
                                        </div>
                                      </div>
                                    </div>
                                  </div>
                                </div>
                              </div>
                            </div>
                          </div>
                        </div>
                      </div>
                    </div>
                  </div>
                </div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

### Text Colors

```html
<p class="text-white"><!-- color: #ffffff --></p>
<p class="text-black"><!-- color: #000000 --></p>
<p class="text-gray-100"><!-- color: #f3f4f6 --></p>
<p class="text-gray-200"><!-- color: #e5e7eb --></p>
<p class="text-gray-300"><!-- color: #d1d5db --></p>
<p class="text-gray-400"><!-- color: #9ca3af --></p>
<p class="text-gray-500"><!-- color: #6b7280 --></p>
<p class="text-gray-600"><!-- color: #4b5563 --></p>
<p class="text-gray-700"><!-- color: #374151 --></p>
<p class="text-gray-800"><!-- color: #1f2937 --></p>
<p class="text-gray-900">
  <!-- color: #111827 -->

  <!-- Blue text -->
</p>

<p class="text-blue-500"><!-- color: #3b82f6 --></p>
<p class="text-blue-600"><!-- color: #2563eb --></p>
<p class="text-blue-700">
  <!-- color: #1d4ed8 -->

  <!-- Green text -->
</p>

<p class="text-green-500"><!-- color: #22c55e --></p>
<p class="text-green-600"><!-- color: #16a34a --></p>
<p class="text-green-700">
  <!-- color: #15803d -->

  <!-- Red text -->
</p>

<p class="text-red-500"><!-- color: #ef4444 --></p>
<p class="text-red-600"><!-- color: #dc2626 --></p>
<p class="text-red-700"><!-- color: #b91c1c --></p>
```

## 📝 Typography

### Font Size

```html
<p class="text-xs"><!-- font-size: 0.75rem; line-height: 1rem --></p>
<p class="text-sm"><!-- font-size: 0.875rem; line-height: 1.25rem --></p>
<p class="text-base"><!-- font-size: 1rem; line-height: 1.5rem --></p>
<p class="text-lg"><!-- font-size: 1.125rem; line-height: 1.75rem --></p>
<p class="text-xl"><!-- font-size: 1.25rem; line-height: 1.75rem --></p>
<p class="text-2xl"><!-- font-size: 1.5rem; line-height: 2rem --></p>
<p class="text-3xl"><!-- font-size: 1.875rem; line-height: 2.25rem --></p>
<p class="text-4xl"><!-- font-size: 2.25rem; line-height: 2.5rem --></p>
<p class="text-5xl"><!-- font-size: 3rem; line-height: 1 --></p>
<p class="text-6xl"><!-- font-size: 3.75rem; line-height: 1 --></p>
```

### Font Weight

```html
<p class="font-thin"><!-- font-weight: 100 --></p>
<p class="font-extralight"><!-- font-weight: 200 --></p>
<p class="font-light"><!-- font-weight: 300 --></p>
<p class="font-normal"><!-- font-weight: 400 --></p>
<p class="font-medium"><!-- font-weight: 500 --></p>
<p class="font-semibold"><!-- font-weight: 600 --></p>
<p class="font-bold"><!-- font-weight: 700 --></p>
<p class="font-extrabold"><!-- font-weight: 800 --></p>
<p class="font-black"><!-- font-weight: 900 --></p>
```

### Text Alignment

```html
<p class="text-left"><!-- text-align: left --></p>
<p class="text-center"><!-- text-align: center --></p>
<p class="text-right"><!-- text-align: right --></p>
<p class="text-justify"><!-- text-align: justify --></p>
```

## 🎭 Borders

### Border Width

```html
<div class="border-0">
  <!-- border-width: 0px -->
  <div class="border">
    <!-- border-width: 1px -->
    <div class="border-2">
      <!-- border-width: 2px -->
      <div class="border-4">
        <!-- border-width: 4px -->
        <div class="border-8">
          <!-- border-width: 8px -->

          <!-- Border (specific) -->
          <div class="border-t">
            <!-- border-top-width: 1px -->
            <div class="border-r">
              <!-- border-right-width: 1px -->
              <div class="border-b">
                <!-- border-bottom-width: 1px -->
                <div class="border-l"><!-- border-left-width: 1px --></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

### Border Color

```html
<div class="border-gray-200">
  <!-- border-color: #e5e7eb -->
  <div class="border-gray-300">
    <!-- border-color: #d1d5db -->
    <div class="border-gray-400">
      <!-- border-color: #9ca3af -->
      <div class="border-blue-500">
        <!-- border-color: #3b82f6 -->
        <div class="border-green-500">
          <!-- border-color: #22c55e -->
          <div class="border-red-500"><!-- border-color: #ef4444 --></div>
        </div>
      </div>
    </div>
  </div>
</div>
```

### Border Radius

```html
<div class="rounded-none">
  <!-- border-radius: 0px -->
  <div class="rounded-sm">
    <!-- border-radius: 0.125rem -->
    <div class="rounded">
      <!-- border-radius: 0.25rem -->
      <div class="rounded-md">
        <!-- border-radius: 0.375rem -->
        <div class="rounded-lg">
          <!-- border-radius: 0.5rem -->
          <div class="rounded-xl">
            <!-- border-radius: 0.75rem -->
            <div class="rounded-2xl">
              <!-- border-radius: 1rem -->
              <div class="rounded-3xl">
                <!-- border-radius: 1.5rem -->
                <div class="rounded-full"><!-- border-radius: 9999px --></div>
              </div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

## 🌫️ Shadows

### Box Shadow

```html
<div class="shadow-sm">
  <!-- box-shadow: 0 1px 2px 0 rgb(0 0 0 / 0.05) -->
  <div class="shadow">
    <!-- box-shadow: 0 1px 3px 0 rgb(0 0 0 / 0.1), 0 1px 2px -1px rgb(0 0 0 / 0.1) -->
    <div class="shadow-md">
      <!-- box-shadow: 0 4px 6px -1px rgb(0 0 0 / 0.1), 0 2px 4px -2px rgb(0 0 0 / 0.1) -->
      <div class="shadow-lg">
        <!-- box-shadow: 0 10px 15px -3px rgb(0 0 0 / 0.1), 0 4px 6px -4px rgb(0 0 0 / 0.1) -->
        <div class="shadow-xl">
          <!-- box-shadow: 0 20px 25px -5px rgb(0 0 0 / 0.1), 0 8px 10px -6px rgb(0 0 0 / 0.1) -->
          <div class="shadow-2xl">
            <!-- box-shadow: 0 25px 50px -12px rgb(0 0 0 / 0.25) -->
            <div class="shadow-inner">
              <!-- box-shadow: inset 0 2px 4px 0 rgb(0 0 0 / 0.05) -->
              <div class="shadow-none"><!-- box-shadow: none --></div>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</div>
```

## 📱 Responsive Design

### Breakpoints

```html
<!-- Mobile first approach -->
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

<!-- Breakpoint prefixes -->
<div
  class="
  text-sm
  sm:text-base
  md:text-lg
  lg:text-xl
  xl:text-2xl
"
>
  <!-- Responsive text -->
</div>
```

### Breakpoint Values

```css
/* Default breakpoints */
sm: 640px    /* Small devices */
md: 768px    /* Medium devices */
lg: 1024px   /* Large devices */
xl: 1280px   /* Extra large devices */
2xl: 1536px  /* 2X large devices */
```

## 🎯 States

### Hover

```html
<button
  class="
  bg-blue-500
  hover:bg-blue-600
  hover:text-white
  hover:shadow-lg
"
>
  Hover me
</button>
```

### Focus

```html
<input
  class="
  border border-gray-300
  focus:border-blue-500
  focus:ring-2
  focus:ring-blue-300
  focus:outline-none
"
/>
```

### Active

```html
<button
  class="
  bg-blue-500
  active:bg-blue-700
  active:scale-95
"
>
  Click me
</button>
```

### Disabled

```html
<button
  class="
  bg-gray-300
  text-gray-500
  cursor-not-allowed
  disabled:opacity-50
"
>
  Disabled
</button>
```

## 🎨 Custom Utilities

### Creating Custom Utilities

```css
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

### Using Custom Utilities

```html
<button class="btn-primary">Primary Button</button>
```

## 🔧 Configuration

### CSS-First Configuration

```css
@import "tailwindcss";

@theme {
  --color-primary: #3b82f6;
  --color-secondary: #10b981;
  --spacing-18: 4.5rem;
  --font-sans: "Inter", "sans-serif";
}

@plugin "@tailwindcss/forms";
@plugin "@tailwindcss/typography";
```

### Custom Variants

```css
@custom-variant dark (&:where([data-theme="dark"] *));

@utility dark-mode {
  &:dark {
    background-color: theme("colors.gray.900");
    color: theme("colors.white");
  }
}
```

## 🚀 Quick Tips

### 1. Common Patterns

```html
<!-- Card component -->
<div class="bg-white rounded-lg shadow-md p-6">
  <h3 class="text-xl font-bold text-gray-900 mb-2">Card Title</h3>
  <p class="text-gray-600">Card content goes here.</p>
</div>

<!-- Button component -->
<button
  class="
  bg-blue-500 text-white px-4 py-2 rounded-md
  hover:bg-blue-600 focus:ring-2 focus:ring-blue-300
  transition-colors duration-200
"
>
  Click me
</button>

<!-- Form input -->
<input
  class="
  border border-gray-300 rounded-md px-3 py-2
  focus:border-blue-500 focus:ring-2 focus:ring-blue-300
  focus:outline-none
"
/>
```

### 2. Responsive Design

```html
<!-- Mobile-first responsive design -->
<div
  class="
  grid grid-cols-1
  sm:grid-cols-2
  md:grid-cols-3
  lg:grid-cols-4
  gap-4
"
>
  <!-- Responsive grid -->
</div>
```

### 3. State Management

```html
<!-- Interactive states -->
<button
  class="
  btn-primary
  hover:bg-blue-600
  focus:ring-2 focus:ring-blue-300
  active:bg-blue-700
  disabled:bg-gray-300 disabled:cursor-not-allowed
"
>
  Interactive Button
</button>
```

## 💡 Pro Tips

- **Use the cheatsheet**: Keep it handy while coding
- **Learn the patterns**: Common patterns are reusable
- **Test responsive**: Always test on different screen sizes
- **Use custom utilities**: Create reusable component styles
- **Follow conventions**: Use consistent naming and structure

---

Ready to explore more tools? Check out the [Tools](./tools.md) guide next!
