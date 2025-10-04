# Minimal Layout Framework - Documentation

Complete documentation for all layout utilities.

## Table of Contents

- [Container](#container)
- [Flexbox](#flexbox)
- [Grid](#grid)
- [Spacing](#spacing)
- [Sizing](#sizing)
- [Display](#display)
- [Position](#position)
- [Text Alignment](#text-alignment)
- [Responsive Design](#responsive-design)

---

## Container

Container classes for constraining content width.

### Classes

- `.container` - Centered container with max-width of 1200px and horizontal padding
- `.container-fluid` - Full-width container with horizontal padding

### Example

```html
<div class="container">
  <p>Centered content with max-width</p>
</div>

<div class="container-fluid">
  <p>Full-width content</p>
</div>
```

---

## Flexbox

Powerful utilities for creating flexible layouts.

### Display

- `.flex` - Display as flex container
- `.inline-flex` - Display as inline flex container

### Direction

- `.flex-row` - Horizontal direction (default)
- `.flex-col` - Vertical direction
- `.flex-row-reverse` - Horizontal reversed
- `.flex-col-reverse` - Vertical reversed

### Wrap

- `.flex-wrap` - Allow items to wrap
- `.flex-nowrap` - Prevent wrapping (default)

### Justify Content

Controls horizontal alignment (or vertical in column layouts).

- `.justify-start` - Align to start
- `.justify-end` - Align to end
- `.justify-center` - Center items
- `.justify-between` - Space between items
- `.justify-around` - Space around items
- `.justify-evenly` - Even spacing

### Align Items

Controls vertical alignment (or horizontal in column layouts).

- `.items-start` - Align to start
- `.items-end` - Align to end
- `.items-center` - Center items
- `.items-baseline` - Align to baseline
- `.items-stretch` - Stretch to fill (default)

### Align Self

Override alignment for individual items.

- `.self-start` - Align self to start
- `.self-end` - Align self to end
- `.self-center` - Center self
- `.self-stretch` - Stretch self

### Flex Grow/Shrink

- `.flex-1` - Grow and shrink equally
- `.flex-auto` - Grow and shrink based on content
- `.flex-none` - Don't grow or shrink
- `.grow` - Allow item to grow
- `.shrink` - Allow item to shrink
- `.shrink-0` - Prevent shrinking

### Examples

```html
<!-- Centered header -->
<header class="flex justify-center items-center">
  <h1>Centered Title</h1>
</header>

<!-- Navigation bar -->
<nav class="flex justify-between items-center">
  <div>Logo</div>
  <div class="flex gap-4">
    <a href="#">Home</a>
    <a href="#">About</a>
    <a href="#">Contact</a>
  </div>
</nav>

<!-- Card layout -->
<div class="flex flex-col gap-4">
  <div class="flex-1">Header</div>
  <div class="flex-auto">Content expands</div>
  <div class="flex-none">Footer</div>
</div>

<!-- Responsive column to row -->
<div class="flex flex-col md:flex-row gap-4">
  <div class="flex-1">Column 1</div>
  <div class="flex-1">Column 2</div>
</div>
```

---

## Grid

CSS Grid utilities for powerful layouts.

### Display

- `.grid` - Display as grid container

### Grid Columns

- `.grid-cols-1` - 1 column
- `.grid-cols-2` - 2 columns
- `.grid-cols-3` - 3 columns
- `.grid-cols-4` - 4 columns
- `.grid-cols-6` - 6 columns
- `.grid-cols-12` - 12 columns

### Gap

Space between grid items (also works with flexbox).

- `.gap-0` - No gap
- `.gap-1` - 0.25rem (4px)
- `.gap-2` - 0.5rem (8px)
- `.gap-3` - 0.75rem (12px)
- `.gap-4` - 1rem (16px)
- `.gap-6` - 1.5rem (24px)
- `.gap-8` - 2rem (32px)

### Examples

```html
<!-- Simple grid -->
<div class="grid grid-cols-3 gap-4">
  <div>Item 1</div>
  <div>Item 2</div>
  <div>Item 3</div>
</div>

<!-- Responsive grid -->
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
  <div>Card 1</div>
  <div>Card 2</div>
  <div>Card 3</div>
  <div>Card 4</div>
</div>

<!-- Dashboard layout -->
<div class="grid grid-cols-12 gap-4">
  <div class="grid-cols-3">Sidebar</div>
  <div class="grid-cols-9">Main content</div>
</div>
```

---

## Spacing

Margin and padding utilities using a consistent spacing scale.

### Scale

- `0` = 0
- `1` = 0.25rem (4px)
- `2` = 0.5rem (8px)
- `3` = 0.75rem (12px)
- `4` = 1rem (16px)
- `6` = 1.5rem (24px)
- `8` = 2rem (32px)

### Margin

- `.m-{size}` - Margin on all sides
- `.m-auto` - Auto margin
- `.mx-auto` - Horizontal auto margin (centering)
- `.my-4` - Vertical margin

### Padding

- `.p-{size}` - Padding on all sides

### Examples

```html
<!-- Centered block -->
<div class="mx-auto" style="width: 300px;">
  Centered element
</div>

<!-- Card with padding -->
<div class="p-6">
  <h2 class="m-0">Card Title</h2>
  <p class="my-4">Card content with vertical spacing</p>
</div>

<!-- Remove default spacing -->
<h1 class="m-0">No margin</h1>
```

---

## Sizing

Width and height utilities.

### Width

- `.w-full` - 100% width
- `.w-auto` - Auto width
- `.w-1/2` - 50% width
- `.w-1/3` - 33.33% width
- `.w-2/3` - 66.67% width
- `.w-1/4` - 25% width
- `.w-3/4` - 75% width

### Height

- `.h-full` - 100% height
- `.h-screen` - 100vh height
- `.h-auto` - Auto height

### Examples

```html
<!-- Two column layout -->
<div class="flex">
  <div class="w-1/3">Sidebar</div>
  <div class="w-2/3">Main content</div>
</div>

<!-- Full height section -->
<section class="h-screen flex items-center justify-center">
  <h1>Full screen hero</h1>
</section>

<!-- Responsive widths -->
<div class="w-full lg:w-1/2 mx-auto">
  Responsive centered content
</div>
```

---

## Display

Control element display type.

### Classes

- `.block` - Display as block
- `.inline-block` - Display as inline-block
- `.inline` - Display as inline
- `.hidden` - Hide element

### Examples

```html
<!-- Mobile menu toggle -->
<div class="hidden md:flex">
  Desktop navigation
</div>

<div class="flex md:hidden">
  Mobile menu button
</div>

<!-- Inline elements -->
<span class="inline-block p-2">Badge</span>
```

---

## Position

Positioning utilities.

### Classes

- `.relative` - Relative positioning
- `.absolute` - Absolute positioning
- `.fixed` - Fixed positioning
- `.sticky` - Sticky positioning

### Examples

```html
<!-- Relative parent with absolute child -->
<div class="relative">
  <img src="image.jpg" alt="Image">
  <div class="absolute" style="top: 10px; right: 10px;">
    Badge
  </div>
</div>

<!-- Fixed header -->
<header class="fixed w-full" style="top: 0;">
  Navigation
</header>

<!-- Sticky sidebar -->
<aside class="sticky" style="top: 20px;">
  Table of contents
</aside>
```

---

## Text Alignment

Simple text alignment utilities.

### Classes

- `.text-left` - Left align text
- `.text-center` - Center align text
- `.text-right` - Right align text

### Examples

```html
<h1 class="text-center">Centered Heading</h1>
<p class="text-right">Right aligned paragraph</p>
```

---

## Responsive Design

Mobile-first responsive utilities using breakpoints.

### Breakpoints

- `sm:` - 640px and up
- `md:` - 768px and up
- `lg:` - 1024px and up

### Usage

Prefix any utility with a breakpoint to apply it only at that screen size and above.

### Examples

```html
<!-- Responsive flexbox -->
<div class="flex flex-col md:flex-row">
  <div>Stacks on mobile, row on tablet+</div>
</div>

<!-- Responsive grid -->
<div class="grid grid-cols-1 sm:grid-cols-2 lg:grid-cols-4 gap-4">
  <div>1 col mobile, 2 cols tablet, 4 cols desktop</div>
</div>

<!-- Responsive visibility -->
<div class="block lg:hidden">
  Visible on mobile and tablet only
</div>

<div class="hidden lg:flex">
  Visible on desktop only
</div>

<!-- Responsive widths -->
<div class="w-full md:w-2/3 lg:w-1/2 mx-auto">
  Full width on mobile, narrower on larger screens
</div>
```

---

## Common Patterns

### Card Layout

```html
<div class="container">
  <div class="grid grid-cols-1 md:grid-cols-3 gap-6">
    <div class="p-6">
      <h3 class="m-0">Card 1</h3>
      <p>Content</p>
    </div>
    <div class="p-6">
      <h3 class="m-0">Card 2</h3>
      <p>Content</p>
    </div>
    <div class="p-6">
      <h3 class="m-0">Card 3</h3>
      <p>Content</p>
    </div>
  </div>
</div>
```

### Sidebar Layout

```html
<div class="flex flex-col md:flex-row">
  <aside class="w-full md:w-1/4 p-4">
    Sidebar
  </aside>
  <main class="flex-1 p-4">
    Main content
  </main>
</div>
```

### Centered Content

```html
<div class="flex items-center justify-center h-screen">
  <div class="w-full" style="max-width: 400px;">
    <h1 class="text-center">Welcome</h1>
  </div>
</div>
```

### Header with Navigation

```html
<header class="container">
  <nav class="flex justify-between items-center py-4">
    <div class="text-left">Logo</div>
    <div class="flex gap-6">
      <a href="#">Home</a>
      <a href="#">About</a>
      <a href="#">Contact</a>
    </div>
  </nav>
</header>
```

---

## Tips & Best Practices

1. **Mobile-first**: Start with mobile styles, add responsive classes for larger screens
2. **Use Flexbox for one-dimensional layouts**: Navigation bars, button groups
3. **Use Grid for two-dimensional layouts**: Card grids, dashboard layouts
4. **Combine utilities**: Mix and match classes for complex layouts
5. **Keep it semantic**: Use appropriate HTML elements even when using utility classes
6. **Don't fight the framework**: If you need custom spacing, add a custom class

---

## Need More?

This framework is intentionally minimal. If you need more utilities:

- Add your own custom classes
- Extend the framework
- Use it alongside other CSS

The goal is to handle 80% of layout needs with 20% of the complexity!