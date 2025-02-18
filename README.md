# DSJ Tax Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the DSJ Tax landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Text Content Updates

#### Hero Section
The main headline is located in the hero section:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-8 leading-tight">
    DSJ Tax Multi-Services South Florida Debt Collection & Tax Preparation
</h1>
```
To update:
1. Locate this `<h1>` tag in the hero section
2. Replace the text between the opening and closing tags
3. Maintain the existing classes to preserve styling

#### Features Section
Each feature card contains:
- Icon (using Font Awesome)
- Heading
- Description

Example feature card:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-shield-alt text-4xl"></i>
    </div>
    <h3 class="text-xl font-bold text-gray-900 mb-4">Security</h3>
    <p class="text-gray-600">State-of-the-art security measures...</p>
</div>
```

To update a feature:
1. Find the feature card you want to modify
2. Change the icon by updating the `fas fa-[icon-name]` class
3. Update the heading text in the `<h3>` tag
4. Modify the description in the `<p>` tag

### Tailwind CSS Classes Explained

#### Common Classes Used:
- `container mx-auto`: Centers content with automatic margins
- `px-6`: Adds horizontal padding (6 units)
- `py-4`: Adds vertical padding (4 units)
- `text-[size]`: Controls text size (xl, 2xl, 3xl, etc.)
- `bg-[color]-[shade]`: Sets background color (e.g., bg-blue-600)
- `text-[color]-[shade]`: Sets text color
- `rounded-lg`: Adds border radius
- `shadow-md`: Adds medium shadow effect

#### Responsive Design Classes:
```html
<div class="text-xl md:text-2xl">
```
- `text-xl`: Base size for mobile
- `md:text-2xl`: Larger size for medium screens and up

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are in the header:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-blue-600 transition duration-300">Services</a>
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
    <!-- more links -->
</div>
```

To update:
1. Locate the `<a>` tag you want to modify
2. Update the `href` attribute:
   - For same-page sections, use `#section-id`
   - For other pages, use the full path (e.g., `/services.html`)

### External Links
The page contains two external form links:
```html
<a href="https://form.jotform.com/250476421727054" class="inline-block bg-blue-600...">
```

To update:
1. Replace the JotForm URL with your new form URL
2. Test the link to ensure it opens correctly

## Linking Privacy and Terms Pages

### Footer Legal Links
Current placeholder links in the footer:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Replace the `#` in `href="#"` with the correct path:
```html
<li><a href="/privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="/terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues:

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure the Tailwind CDN link is working

2. **Non-Working Links**
   - Verify file paths are correct
   - Check for typos in URLs
   - Ensure anchor tags have both opening and closing tags

3. **Missing Icons**
   - Confirm Font Awesome CDN is loaded
   - Check icon class names against Font Awesome documentation
   - Verify the correct icon prefix (fas, far, fab)

For additional help, consult the [Tailwind CSS documentation](https://tailwindcss.com/docs) or [Font Awesome documentation](https://fontawesome.com/docs).