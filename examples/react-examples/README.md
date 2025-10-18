# ⚛️ React Examples

Sample React projects demonstrating Tailwind CSS v4+ usage in React applications with Vite.

## 🎯 Overview

This directory contains complete React examples that showcase Tailwind CSS v4+ features and best practices in modern React applications.

## 📁 Project Structure

```
react-examples/
├── README.md
├── basic-setup/
│   ├── package.json
│   ├── vite.config.ts
│   ├── src/
│   │   ├── main.tsx
│   │   ├── App.tsx
│   │   └── index.css
│   └── dist/
├── component-library/
│   ├── package.json
│   ├── vite.config.ts
│   ├── src/
│   │   ├── components/
│   │   │   ├── Button/
│   │   │   ├── Card/
│   │   │   ├── Input/
│   │   │   └── Modal/
│   │   ├── App.tsx
│   │   └── index.css
│   └── dist/
├── dashboard/
│   ├── package.json
│   ├── vite.config.ts
│   ├── src/
│   │   ├── components/
│   │   ├── pages/
│   │   ├── hooks/
│   │   ├── App.tsx
│   │   └── index.css
│   └── dist/
└── e-commerce/
    ├── package.json
    ├── vite.config.ts
    ├── src/
    │   ├── components/
    │   ├── pages/
    │   ├── hooks/
    │   ├── context/
    │   ├── App.tsx
    │   └── index.css
    └── dist/
```

## 🚀 Getting Started

### 1. Basic Setup

```bash
# Navigate to basic setup example
cd examples/react-examples/basic-setup

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

### 2. Component Library

```bash
# Navigate to component library example
cd examples/react-examples/component-library

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
cd examples/react-examples/dashboard

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
cd examples/react-examples/e-commerce

# Install dependencies
npm install

# Start development server
npm run dev

# Build for production
npm run build
```

## 📋 Features

### 1. Basic Setup

- **React + Vite configuration**
- **Tailwind CSS v4+ setup**
- **TypeScript support**
- **Hot Module Replacement**
- **Basic component examples**

### 2. Component Library

- **Reusable components**
- **TypeScript interfaces**
- **Storybook integration**
- **Component documentation**
- **Testing setup**

### 3. Dashboard

- **Responsive layout**
- **Navigation system**
- **Data visualization**
- **State management**
- **User authentication**

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

## ⚛️ React Components

### 1. Button Component

```tsx
// src/components/Button/Button.tsx
import React from "react";

interface ButtonProps {
  children: React.ReactNode;
  variant?: "primary" | "secondary" | "outline" | "ghost";
  size?: "sm" | "md" | "lg";
  disabled?: boolean;
  onClick?: () => void;
  className?: string;
}

const Button: React.FC<ButtonProps> = ({
  children,
  variant = "primary",
  size = "md",
  disabled = false,
  onClick,
  className = "",
}) => {
  const baseClasses = "btn";
  const variantClasses = {
    primary: "btn-primary",
    secondary: "btn-secondary",
    outline: "btn-outline",
    ghost: "btn-ghost",
  };
  const sizeClasses = {
    sm: "btn-sm",
    md: "btn-md",
    lg: "btn-lg",
  };

  const classes = `${baseClasses} ${variantClasses[variant]} ${sizeClasses[size]} ${className}`;

  return (
    <button className={classes} disabled={disabled} onClick={onClick}>
      {children}
    </button>
  );
};

export default Button;
```

### 2. Card Component

```tsx
// src/components/Card/Card.tsx
import React from "react";

interface CardProps {
  children: React.ReactNode;
  title?: string;
  className?: string;
}

const Card: React.FC<CardProps> = ({ children, title, className = "" }) => {
  return (
    <div className={`card ${className}`}>
      {title && <div className="card-header">{title}</div>}
      <div className="card-body">{children}</div>
    </div>
  );
};

export default Card;
```

### 3. Input Component

```tsx
// src/components/Input/Input.tsx
import React from "react";

interface InputProps {
  type?: "text" | "email" | "password" | "number";
  placeholder?: string;
  value?: string;
  onChange?: (value: string) => void;
  disabled?: boolean;
  className?: string;
}

const Input: React.FC<InputProps> = ({
  type = "text",
  placeholder,
  value,
  onChange,
  disabled = false,
  className = "",
}) => {
  const handleChange = (e: React.ChangeEvent<HTMLInputElement>) => {
    onChange?.(e.target.value);
  };

  return (
    <input
      type={type}
      placeholder={placeholder}
      value={value}
      onChange={handleChange}
      disabled={disabled}
      className={`form-input ${className}`}
    />
  );
};

export default Input;
```

## 🎯 Best Practices

### 1. Component Structure

```tsx
// src/components/Button/Button.tsx
import React from "react";

interface ButtonProps {
  children: React.ReactNode;
  variant?: "primary" | "secondary";
  onClick?: () => void;
}

const Button: React.FC<ButtonProps> = ({
  children,
  variant = "primary",
  onClick,
}) => {
  return (
    <button className={`btn btn-${variant}`} onClick={onClick}>
      {children}
    </button>
  );
};

export default Button;
```

### 2. TypeScript Interfaces

```tsx
// src/types/index.ts
export interface User {
  id: string;
  name: string;
  email: string;
  avatar?: string;
}

export interface Product {
  id: string;
  name: string;
  price: number;
  description: string;
  image: string;
  category: string;
}

export interface CartItem {
  product: Product;
  quantity: number;
}
```

### 3. Custom Hooks

```tsx
// src/hooks/useLocalStorage.ts
import { useState, useEffect } from "react";

export function useLocalStorage<T>(key: string, initialValue: T) {
  const [storedValue, setStoredValue] = useState<T>(() => {
    try {
      const item = window.localStorage.getItem(key);
      return item ? JSON.parse(item) : initialValue;
    } catch (error) {
      console.error(error);
      return initialValue;
    }
  });

  const setValue = (value: T | ((val: T) => T)) => {
    try {
      const valueToStore =
        value instanceof Function ? value(storedValue) : value;
      setStoredValue(valueToStore);
      window.localStorage.setItem(key, JSON.stringify(valueToStore));
    } catch (error) {
      console.error(error);
    }
  };

  return [storedValue, setValue] as const;
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

1. **Explore the examples** to see Tailwind CSS v4+ in React
2. **Customize the components** to match your needs
3. **Add your own components** using the design system
4. **Test responsive design** on different devices
5. **Deploy your project** to a hosting service

## 💡 Pro Tips

- **Start with the basic setup** to understand the fundamentals
- **Use TypeScript** for better development experience
- **Follow component patterns** for consistency
- **Test responsive design** on different screen sizes
- **Optimize for performance** by using React.memo and useMemo

---

Ready to explore Next.js examples? Check out the [Next.js Examples](../nextjs-examples/README.md) next!
