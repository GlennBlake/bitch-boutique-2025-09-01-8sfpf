# Bitch.Boutique Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Bitch.Boutique landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the site logo and navigation menu:

```html
<header class="fixed w-full bg-white/95 backdrop-blur-sm z-50 border-b border-gray-100">
```

To update the logo text:
1. Locate: `<a href="#" class="text-2xl font-['Playfair_Display'] font-bold text-black tracking-tight">Bitch.Boutique</a>`
2. Replace "Bitch.Boutique" with your desired text
3. Key classes explained:
   - `text-2xl`: Controls text size
   - `font-bold`: Makes text bold
   - `tracking-tight`: Controls letter spacing

### Hero Section
The main banner section contains the primary heading and call-to-action:

```html
<h1 class="text-5xl md:text-7xl font-['Playfair_Display'] font-bold text-black mb-6 leading-tight">We Bark.<br>We Bite.</h1>
```

To modify:
1. Replace text between `<h1>` tags
2. The `<br>` tag creates a line break
3. Important classes:
   - `text-5xl md:text-7xl`: Makes text responsive (smaller on mobile, larger on desktop)
   - `mb-6`: Adds margin bottom spacing
   - `leading-tight`: Controls line height

### Features Grid
Each feature card follows this structure:

```html
<div class="group p-8 rounded-2xl bg-white border border-gray-100 hover:border-gray-200 transition-all duration-300 hover:shadow-xl">
    <h3 class="text-2xl font-semibold mb-4">Clothing</h3>
    <p class="text-gray-600 leading-relaxed">Premium pieces for the fearless fashionista.</p>
</div>
```

To customize:
1. Locate the feature you want to change
2. Update the `<h3>` heading text
3. Modify the description in the `<p>` tag
4. Key styling classes:
   - `p-8`: Adds padding
   - `rounded-2xl`: Rounds corners
   - `hover:shadow-xl`: Adds shadow on hover

## Fixing Broken Links

### Navigation Menu Links
Current placeholder links in the header:

```html
<div class="hidden md:flex space-x-8">
    <a href="#" class="text-gray-800 hover:text-black transition-colors duration-300">Shop</a>
    <a href="#" class="text-gray-800 hover:text-black transition-colors duration-300">Collections</a>
    <a href="#" class="text-gray-800 hover:text-black transition-colors duration-300">About</a>
    <a href="#" class="text-gray-800 hover:text-black transition-colors duration-300">Blog</a>
</div>
```

To update links:
1. Replace `#` with proper URLs:
   ```html
   <a href="shop.html">Shop</a>
   <a href="collections.html">Collections</a>
   <a href="about.html">About</a>
   <a href="blog.html">Blog</a>
   ```
2. For external links, use complete URLs:
   ```html
   <a href="https://example.com/shop">Shop</a>
   ```

### Footer Links
The footer contains multiple link sections:

```html
<div>
    <h5 class="font-semibold mb-4">Shop</h5>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">Clothing</a></li>
        <!-- More links -->
    </ul>
</div>
```

To update:
1. Locate the appropriate section
2. Replace `#` with correct paths
3. Maintain the existing classes for consistent styling

## Adding Privacy and Terms Pages

To add privacy and terms links to the footer:

1. Locate the footer's company links section:
```html
<div>
    <h5 class="font-semibold mb-4">Company</h5>
    <ul class="space-y-2">
        <!-- Existing links -->
```

2. Add new links maintaining consistent styling:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

3. Create corresponding HTML files (privacy.html and terms.html) in your root directory

## Troubleshooting

Common issues and solutions:

1. **Broken Responsive Design**
   - Check for `md:` prefixed classes
   - Ensure you haven't removed important responsive classes
   - Example: `text-5xl md:text-7xl` makes text responsive

2. **Inconsistent Spacing**
   - Look for missing padding (`p-`) or margin (`m-`) classes
   - Reference existing spacing patterns
   - Example: `mb-6` adds margin bottom

3. **Hover Effects Not Working**
   - Verify `hover:` classes are present
   - Check parent `group` class if using group hover
   - Example: `hover:text-white`

Remember:
- Always test changes across different screen sizes
- Maintain consistent spacing and typography
- Back up files before making changes
- Keep the original class structure for consistent styling

Need more help? Contact technical support at the email provided in the footer section.