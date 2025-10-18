# 🚀 Next.js Examples

Sample Next.js projects demonstrating Tailwind CSS v4+ usage in Next.js 13+ applications with the App Router.

## 🎯 Overview

This directory contains complete Next.js examples that showcase Tailwind CSS v4+ features and best practices in modern Next.js applications.

## 📁 Project Structure

```
nextjs-examples/
├── README.md
├── basic-setup/
│   ├── package.json
│   ├── next.config.js
│   ├── postcss.config.mjs
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── globals.css
│   │   └── about/
│   │       └── page.tsx
│   └── .next/
├── blog/
│   ├── package.json
│   ├── next.config.js
│   ├── postcss.config.mjs
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── globals.css
│   │   ├── blog/
│   │   │   ├── page.tsx
│   │   │   └── [slug]/
│   │   │       └── page.tsx
│   │   └── components/
│   │       ├── Header.tsx
│   │       ├── Footer.tsx
│   │       └── BlogCard.tsx
│   └── .next/
├── dashboard/
│   ├── package.json
│   ├── next.config.js
│   ├── postcss.config.mjs
│   ├── app/
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   ├── globals.css
│   │   ├── dashboard/
│   │   │   ├── page.tsx
│   │   │   ├── analytics/
│   │   │   │   └── page.tsx
│   │   │   └── settings/
│   │   │       └── page.tsx
│   │   └── components/
│   │       ├── Sidebar.tsx
│   │       ├── Navbar.tsx
│   │       └── Chart.tsx
│   └── .next/
└── e-commerce/
    ├── package.json
    ├── next.config.js
    ├── postcss.config.mjs
    ├── app/
    │   ├── layout.tsx
    │   ├── page.tsx
    │   ├── globals.css
    │   ├── products/
    │   │   ├── page.tsx
    │   │   └── [id]/
    │   │       └── page.tsx
    │   ├── cart/
    │   │   └── page.tsx
    │   └── components/
    │       ├── ProductCard.tsx
    │       ├── CartItem.tsx
    │       └── CheckoutForm.tsx
    └── .next/
```

## 🚀 Getting Started

### 1. Basic Setup

```bash
# Navigate to basic setup example
cd examples/nextjs-examples/basic-setup

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

### 2. Blog

```bash
# Navigate to blog example
cd examples/nextjs-examples/blog

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

### 3. Dashboard

```bash
# Navigate to dashboard example
cd examples/nextjs-examples/dashboard

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

### 4. E-commerce

```bash
# Navigate to e-commerce example
cd examples/nextjs-examples/e-commerce

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## 📋 Features

### 1. Basic Setup

- **Next.js 13+ App Router**
- **Tailwind CSS v4+ configuration**
- **TypeScript support**
- **Server-side rendering**
- **Static site generation**

### 2. Blog

- **Dynamic routing**
- **Markdown support**
- **SEO optimization**
- **Responsive design**
- **Content management**

### 3. Dashboard

- **Protected routes**
- **Data visualization**
- **Real-time updates**
- **User authentication**
- **Admin interface**

### 4. E-commerce

- **Product catalog**
- **Shopping cart**
- **Checkout process**
- **Payment integration**
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

## ⚛️ Next.js Components

### 1. Layout Component

```tsx
// app/layout.tsx
import type { Metadata } from "next";
import { Inter } from "next/font/google";
import "./globals.css";

const inter = Inter({ subsets: ["latin"] });

export const metadata: Metadata = {
  title: "Next.js + Tailwind CSS v4+",
  description:
    "A modern web application built with Next.js and Tailwind CSS v4+",
};

export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body className={inter.className}>
        <div className="min-h-screen bg-gray-100">{children}</div>
      </body>
    </html>
  );
}
```

### 2. Page Component

```tsx
// app/page.tsx
import Link from "next/link";

export default function HomePage() {
  return (
    <div className="container mx-auto px-4 py-8">
      <div className="text-center">
        <h1 className="text-4xl font-bold text-gray-900 mb-4">
          Welcome to Next.js + Tailwind CSS v4+
        </h1>
        <p className="text-xl text-gray-600 mb-8">
          A modern web application built with the latest technologies.
        </p>
        <div className="space-x-4">
          <Link href="/about" className="btn-primary">
            Learn More
          </Link>
          <Link href="/contact" className="btn-secondary">
            Get Started
          </Link>
        </div>
      </div>
    </div>
  );
}
```

### 3. Dynamic Route Component

```tsx
// app/blog/[slug]/page.tsx
import { notFound } from "next/navigation";

interface BlogPost {
  slug: string;
  title: string;
  content: string;
  publishedAt: string;
}

async function getBlogPost(slug: string): Promise<BlogPost | null> {
  // Fetch blog post from API or database
  const posts = await fetch("/api/posts").then((res) => res.json());
  return posts.find((post: BlogPost) => post.slug === slug) || null;
}

export default async function BlogPostPage({
  params,
}: {
  params: { slug: string };
}) {
  const post = await getBlogPost(params.slug);

  if (!post) {
    notFound();
  }

  return (
    <article className="max-w-4xl mx-auto px-4 py-8">
      <header className="mb-8">
        <h1 className="text-4xl font-bold text-gray-900 mb-4">{post.title}</h1>
        <time className="text-gray-600">
          {new Date(post.publishedAt).toLocaleDateString()}
        </time>
      </header>
      <div className="prose prose-lg max-w-none">
        <div dangerouslySetInnerHTML={{ __html: post.content }} />
      </div>
    </article>
  );
}
```

## 🎯 Best Practices

### 1. App Router Structure

```tsx
// app/layout.tsx
import type { Metadata } from "next";
import { Inter } from "next/font/google";
import "./globals.css";

const inter = Inter({ subsets: ["latin"] });

export const metadata: Metadata = {
  title: "Next.js + Tailwind CSS v4+",
  description:
    "A modern web application built with Next.js and Tailwind CSS v4+",
};

export default function RootLayout({
  children,
}: {
  children: React.ReactNode;
}) {
  return (
    <html lang="en">
      <body className={inter.className}>{children}</body>
    </html>
  );
}
```

### 2. Server Components

```tsx
// app/components/ServerComponent.tsx
import { getData } from "@/lib/data";

export default async function ServerComponent() {
  const data = await getData();

  return (
    <div className="card">
      <h2 className="card-header">Server Component</h2>
      <div className="card-body">
        <p>{data.message}</p>
      </div>
    </div>
  );
}
```

### 3. Client Components

```tsx
// app/components/ClientComponent.tsx
"use client";

import { useState } from "react";

export default function ClientComponent() {
  const [count, setCount] = useState(0);

  return (
    <div className="card">
      <h2 className="card-header">Client Component</h2>
      <div className="card-body">
        <p>Count: {count}</p>
        <button onClick={() => setCount(count + 1)} className="btn-primary">
          Increment
        </button>
      </div>
    </div>
  );
}
```

## 📱 Responsive Design

### 1. Mobile-First Approach

```tsx
// Responsive component
const ResponsiveGrid: React.FC = () => {
  return (
    <div
      className="
      grid grid-cols-1
      sm:grid-cols-2
      md:grid-cols-3
      lg:grid-cols-4
      xl:grid-cols-5
      gap-4
    "
    >
      {/* Grid items */}
    </div>
  );
};
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

```tsx
// Responsive text component
const ResponsiveText: React.FC = () => {
  return (
    <h1
      className="
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
  );
};
```

## 🚀 Next Steps

1. **Explore the examples** to see Tailwind CSS v4+ in Next.js
2. **Customize the components** to match your needs
3. **Add your own pages** using the App Router
4. **Test responsive design** on different devices
5. **Deploy your project** to Vercel or another hosting service

## 💡 Pro Tips

- **Use the App Router** for better performance and developer experience
- **Leverage Server Components** for better SEO and performance
- **Use Client Components** only when necessary
- **Test responsive design** on different screen sizes
- **Optimize for performance** by using Next.js features

---

Ready to explore the complete documentation? Check out the [Main README](../../README.md) for an overview of all sections!
