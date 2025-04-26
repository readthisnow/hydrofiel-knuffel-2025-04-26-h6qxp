# Landing Page Maintenance Guide

This guide will help you maintain and customize the Hydrofiel Knuffel landing page. Follow these detailed instructions to make common updates while preserving the page's functionality and design.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text**:
```html
<a href="#" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Hydrofiel Knuffel  <!-- Change this text -->
</a>
```

2. **Navigation Links**:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Kenmerken</a>  <!-- Change these text labels -->
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
</div>
```

### Hero Section
The main banner section contains:

1. **Main Heading**:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold mb-8 bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent">
    Koop Hydrofiel Knuffel Met Korting  <!-- Update this heading -->
</h1>
```

2. **Subheading**:
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    🔥 Nog maar enkele stuks beschikbaar! 🔥  <!-- Change this text -->
</p>
```

### Understanding Tailwind Classes
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds bottom margin (e.g., `mb-8`, `mb-12`)
- `py-[size]`: Adds vertical padding (e.g., `py-24`)
- `px-[size]`: Adds horizontal padding (e.g., `px-6`)

## Managing Links

### Current Link Locations

1. **Navigation Menu Links**:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Kenmerken</a>
    <a href="#benefits">Voordelen</a>
    <a href="#faq">FAQ</a>
</div>
```
To update, change the `href` value to match your new section IDs.

2. **Call-to-Action Buttons**:
```html
<a href="https://amzn.to/3S5uNvM" class="inline-block bg-gradient-to-r...">
    Bekijk Speciale Aanbieding
</a>
```
Replace the Amazon affiliate link with your product URL.

3. **Footer Links**:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="#">Privacy Policy</a></li>
    <li><a href="#">Terms of Service</a></li>
</ul>
```

### How to Update Links
1. For internal links (same page sections):
   - Ensure the `href` matches the section's `id` attribute
   - Always include the `#` symbol
   - Example: `href="#features"` links to `<section id="features">`

2. For external links:
   - Use the complete URL including `https://`
   - Test the link after updating

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new HTML files in your project folder:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links with:

```html
<ul class="space-y-2 text-gray-400">
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 3: Match Styling
Ensure your new pages use the same styling by copying these head elements:

```html
<link href="https://unpkg.com/tailwindcss@^2/dist/tailwind.min.css" rel="stylesheet">
<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300;400;500;600;700&display=swap" rel="stylesheet">
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Check that section IDs match exactly with href values
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - These control how elements appear on different screen sizes
   - Example: `hidden md:flex` hides on mobile, shows on medium screens

3. **Gradient Text Not Showing**
   - Ensure these classes stay together:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

4. **Missing Styles**
   - Verify Tailwind CSS link is working
   - Check for typos in class names
   - Keep the `font-inter` class on the body element

Remember to test all changes across different screen sizes using your browser's developer tools (F12 or right-click > Inspect).