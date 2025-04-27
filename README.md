# Garrett Park Glass Landing Page - Maintenance Guide

This guide will help you maintain and customize the Garrett Park Glass landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-blue-400 to-teal-400 bg-clip-text text-transparent">
    Garrett Park Glass <!-- Change this text -->
</a>
```

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a> <!-- Change menu item text here -->
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

### Hero Section
Update the main headline and subtext:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8">
    Garrett Park Shower Glass Company <!-- Change main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Commercial shower glass solutions <!-- Change subheading -->
</p>
```

### Tailwind CSS Classes Explained
- `text-4xl`: Text size (increases with screen size)
- `md:text-6xl`: Text size on medium screens
- `mb-8`: Margin bottom spacing
- `text-gray-300`: Text color
- `hover:scale-105`: Slight enlargement on hover
- `transition-colors`: Smooth color transitions

## Managing Links

### Current Link Locations

1. **Navigation Menu Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

2. **Call-to-Action Links:**
```html
<a href="http://www.customeuroglass.com" class="inline-block px-8 py-4">
    Explore Our Solutions
</a>
```

3. **Contact Email:**
```html
<a href="mailto:lt@customeuroglass.com">lt@customeuroglass.com</a>
```

### Updating Links
To update any link:
1. Locate the `<a>` tag
2. Change the `href` attribute value
3. Update the link text between the opening and closing tags

Example:
```html
<!-- Before -->
<a href="http://www.customeuroglass.com">Website</a>

<!-- After -->
<a href="http://www.newwebsite.com">New Website Name</a>
```

## Adding Privacy and Terms Pages

### Footer Modification
Add privacy and terms links to the footer's Quick Links section:

```html
<div>
    <h3 class="text-xl font-bold mb-4">Quick Links</h3>
    <a href="http://www.customeuroglass.com" class="block text-gray-400 hover:text-white transition-colors duration-300">Website</a>
    <!-- Add these new links -->
    <a href="/privacy.html" class="block text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a>
    <a href="/terms.html" class="block text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a>
</div>
```

### Creating Policy Pages
1. Create new files named `privacy.html` and `terms.html`
2. Use the same header and footer as `index.html`
3. Add policy content between `<main>` tags
4. Maintain consistent styling using Tailwind classes

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links:**
- Ensure hashtag (#) links match section IDs
- Example: `href="#features"` must match `id="features"`

2. **Responsive Design Issues:**
- Check media query classes (md:, lg:)
- Verify proper class ordering
```html
<!-- Correct order -->
<div class="text-sm md:text-base lg:text-lg">

<!-- Incorrect order -->
<div class="lg:text-lg text-sm md:text-base">
```

3. **Gradient Text Not Showing:**
- Ensure all three classes are present:
```html
bg-gradient-to-r from-blue-400 to-teal-400 bg-clip-text text-transparent
```

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools

Remember to always test changes across different devices and browsers before deploying to production.