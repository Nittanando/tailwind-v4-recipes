# 🖼️ Images

This directory contains images and visual assets for the Tailwind CSS v4+ documentation.

## 🎯 Overview

The images directory is organized to support the documentation with logos, screenshots, and icons.

## 📁 Directory Structure

```
images/
├── README.md
├── logos/
│   ├── tailwind-logo.svg
│   ├── tailwind-logo-dark.svg
│   └── tailwind-logo-light.svg
├── screenshots/
│   ├── setup/
│   │   ├── html-setup.png
│   │   ├── react-setup.png
│   │   └── nextjs-setup.png
│   ├── components/
│   │   ├── button-examples.png
│   │   ├── card-examples.png
│   │   └── form-examples.png
│   └── examples/
│       ├── landing-page.png
│       ├── dashboard.png
│       └── e-commerce.png
└── icons/
    ├── feature-icons/
    │   ├── responsive.svg
    │   ├── customizable.svg
    │   ├── fast.svg
    │   └── accessible.svg
    └── social-icons/
        ├── github.svg
        ├── twitter.svg
        ├── discord.svg
        └── linkedin.svg
```

## 🎨 Logos

### 1. Tailwind Logo

- **File**: `tailwind-logo.svg`
- **Usage**: Default logo for light backgrounds
- **Format**: SVG
- **Colors**: Tailwind brand colors

### 2. Dark Logo

- **File**: `tailwind-logo-dark.svg`
- **Usage**: Logo optimized for dark backgrounds
- **Format**: SVG
- **Colors**: Light colors for dark backgrounds

### 3. Light Logo

- **File**: `tailwind-logo-light.svg`
- **Usage**: Logo optimized for light backgrounds
- **Format**: SVG
- **Colors**: Dark colors for light backgrounds

## 📸 Screenshots

### 1. Setup Screenshots

- **HTML Setup**: Visual guide for HTML setup process
- **React Setup**: Visual guide for React setup process
- **Next.js Setup**: Visual guide for Next.js setup process

### 2. Component Screenshots

- **Button Examples**: Various button styles and states
- **Card Examples**: Different card layouts and designs
- **Form Examples**: Form components and validation states

### 3. Example Screenshots

- **Landing Page**: Complete landing page example
- **Dashboard**: Dashboard interface example
- **E-commerce**: E-commerce application example

## 🎯 Icons

### 1. Feature Icons

- **Responsive**: Icon representing responsive design
- **Customizable**: Icon representing customization
- **Fast**: Icon representing performance
- **Accessible**: Icon representing accessibility

### 2. Social Icons

- **GitHub**: GitHub logo and link
- **Twitter**: Twitter logo and link
- **Discord**: Discord logo and link
- **LinkedIn**: LinkedIn logo and link

## 🔧 Usage

### 1. In Documentation

```markdown
<!-- Logo in markdown -->

![Tailwind CSS Logo](./assets/images/logos/tailwind-logo.svg)

<!-- Screenshot in markdown -->

![Setup Screenshot](./assets/images/screenshots/setup/html-setup.png)

<!-- Icon in markdown -->

![Responsive Icon](./assets/images/icons/feature-icons/responsive.svg)
```

### 2. In HTML

```html
<!-- Logo in HTML -->
<img src="./assets/images/logos/tailwind-logo.svg" alt="Tailwind CSS Logo" />

<!-- Screenshot in HTML -->
<img
  src="./assets/images/screenshots/setup/html-setup.png"
  alt="HTML Setup Screenshot"
/>

<!-- Icon in HTML -->
<img
  src="./assets/images/icons/feature-icons/responsive.svg"
  alt="Responsive Design Icon"
/>
```

### 3. In React

```tsx
// Logo in React
import TailwindLogo from "./assets/images/logos/tailwind-logo.svg";

const Header = () => {
  return (
    <header>
      <img src={TailwindLogo} alt="Tailwind CSS Logo" />
    </header>
  );
};
```

## 📋 Image Checklist

### ✅ Logos

- [ ] All logos are high quality and properly sized
- [ ] Logos are available in different color schemes
- [ ] Logos are optimized for web delivery
- [ ] Logos have proper alt text
- [ ] Logos are consistent with brand guidelines

### ✅ Screenshots

- [ ] Screenshots are clear and up-to-date
- [ ] Screenshots show relevant information
- [ ] Screenshots are properly sized for documentation
- [ ] Screenshots have proper alt text
- [ ] Screenshots are optimized for web delivery

### ✅ Icons

- [ ] Icons are consistent with design system
- [ ] Icons are properly sized and aligned
- [ ] Icons have proper alt text
- [ ] Icons are optimized for web delivery
- [ ] Icons are accessible and readable

## 🚀 Next Steps

1. **Create the image files** based on the documentation needs
2. **Optimize images** for web delivery
3. **Add alt text** for accessibility
4. **Update documentation** to reference images
5. **Test image loading** in different environments

## 💡 Pro Tips

- **Use SVG for logos and icons**: Better scalability and smaller file sizes
- **Optimize images**: Compress images for faster loading
- **Provide alt text**: Make content accessible to all users
- **Keep images organized**: Use logical folder structure
- **Version control**: Track changes to images over time

---

Ready to explore diagrams? Check out the [Diagrams](../diagrams/README.md) directory next!
