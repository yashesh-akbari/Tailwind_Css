# **Tailwind CSS Cheat Sheet & Learning Guide (Using CLI)**

This guide will walk you through the process of setting up **Tailwind CSS** using the CLI (Command Line Interface), explain its utility-first concept, and provide practical examples to get you up and running quickly. Tailwind CSS is an incredibly fast and flexible CSS framework for building modern websites.

## **Why Tailwind CSS?**

- **Fast Development**: With utility-first classes, you can build and style elements without writing custom CSS.
- **Performance**: Tailwind CSS optimizes the CSS file size by purging unused styles, making it ideal for production.
- **Customizable**: Tailwind is highly configurable, allowing you to define your styles as you build.

## **Setting Up Tailwind CSS with CLI**

The **Tailwind CLI tool** is the easiest and fastest way to set up Tailwind from scratch, and it doesn’t require Node.js installation if you choose the standalone executable.

### **Step 1: Install Tailwind CSS**

Open your terminal and run the following command to install **Tailwind CSS** and the **Tailwind CLI tool**:
```bash
npm install tailwindcss @tailwindcss/cli
```

### **Step 2: Import Tailwind into Your CSS**

Create an `input.css` file in your `src` directory and add the following `@import` directives:
```css
/* src/input.css */
@import "tailwindcss";
```

### **Step 3: Start the Tailwind CLI Build Process**

Next, use the **CLI tool** to scan your source files and build your CSS. Run the following command in your terminal:
```bash
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```
The `--watch` flag will keep the CLI running and automatically rebuild the CSS whenever changes are made.

### **Step 4: Use Tailwind CSS in Your HTML**

Now, link the generated `output.css` file in your `index.html`:
```html
<!-- src/index.html -->
<!doctype html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="./output.css" rel="stylesheet">
  <title>Tailwind CSS Example</title>
</head>
<body>
  <h1 class="text-3xl font-bold underline">Hello, Tailwind CSS!</h1>
</body>
</html>
```
---

## **Tailwind CSS Properties**

### **1. Background and Text Colors**
- **Background color**: `bg-colorName`
- **Text color**: `text-colorName`

Example:
```html
<div class="bg-red-500 text-white p-4">
  <p>Example Text</p>
</div>
```

### **2. Margin and Padding**
- **Margin**: `m-size` (for all sides)
- **Margin-top**: `mt-size`, **Margin-left**: `ml-size`, **Padding**: `p-size`

Example:
```html
<div class="m-4 p-2 bg-gray-300">
  <p class="ml-2 mt-4">Example with Margin and Padding</p>
</div>
```

### **3. Width and Height**
- **Width**: `w-size`
- **Height**: `h-size`

Example:
```html
<div class="w-64 h-32 bg-green-500">
  <p>Fixed width and height</p>
</div>
```

### **4. Positioning**
- **Relative, Absolute, Fixed** positioning: `relative`, `absolute`, `fixed`

Example:
```html
<div class="relative bg-yellow-500 w-32 h-32">
  <p class="absolute top-0 left-0">Positioned inside a container</p>
</div>
```

### **5. Animations**
- **Common animations**: `animate-spin`, `animate-ping`, `animate-bounce`

Example:
```html
<div class="animate-spin">
  <p>Spinning Element</p>
</div>
```

### **6. Shadow**
- **Box shadows**: `shadow`, `shadow-lg`, `shadow-2xl`

Example:
```html
<div class="shadow-lg bg-white p-6">
  <p>Box with shadow</p>
</div>
```

### **7. Interactivity**
- **Hover, Focus, Active States**: `hover:property`, `focus:property`, `active:property`

Example:
```html
<button class="bg-blue-500 hover:bg-blue-700 focus:ring-4 active:ring-4">
  Hover, Focus & Active States
</button>
```

### **8. Media Queries & Breakpoints**
- **Responsive** classes: `sm:`, `md:`, `lg:`, `xl:`, `2xl:`

Example:
```html
<div class="sm:text-sm md:text-base lg:text-lg">
  <p>This text changes size based on screen width</p>
</div>
```

### **9. Flexbox**
- **Flex classes**: `flex`, `flex-row`, `flex-col`, `flex-wrap`, `items-center`, `justify-center`

Example:
```html
<div class="flex justify-center items-center bg-gray-200 p-6">
  <div class="bg-blue-500 w-32 h-32">Flexbox Centered Item</div>
</div>
```

### **10. Grid**
- **Grid classes**: `grid`, `grid-cols-3`, `row-span-2`, `col-span-2`

Example:
```html
<div class="grid grid-cols-3 gap-4">
  <div class="col-span-2">Grid Item 1</div>
  <div>Grid Item 2</div>
</div>
```

### **11. Transitions & Transforms**
- **Transition properties**: `transition`, `duration-100`, `opacity-5`
- **Transform properties**: `rotate-45`, `scale-x-50`, `scale-y-150`

Example:
```html
<div class="transition transform duration-300 hover:rotate-45">
  <p>Hover to Rotate</p>
</div>
```

### **12. Dark Mode**
Tailwind CSS now supports dark mode with a `dark:` prefix:
```html
<div class="dark:bg-gray-800 dark:text-white">
  <p>This content is dark mode enabled</p>
</div>
```

### **13. Custom Classes**
You can use the `@apply` directive to create custom utility classes in your CSS:

Example (`style.css`):
```css
/* @layer directive */
@layer components {
  .btn-custom {
    @apply bg-blue-500 text-white p-4 rounded-lg;
  }
}
```

---

## **Conclusion**

This guide covers setting up Tailwind CSS using the **CLI** tool and introduces key concepts and utility classes. Tailwind's utility-first approach enables you to build responsive, performant, and customizable web pages without writing custom CSS.

---

Feel free to adjust any part of this README to match your personal project needs. This structure should give you a solid foundation for using Tailwind CSS in your project, and help you understand its powerful utility-based design approach!
