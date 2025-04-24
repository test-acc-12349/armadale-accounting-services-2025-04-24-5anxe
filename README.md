# Armadale Landing Page Maintenance Guide

This guide will help you maintain and customize the Armadale Accounting Services landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. **Company Name**
```html
<!-- Located in the header section -->
<a href="/" class="text-2xl font-bold bg-gradient-to-r from-purple-500 to-pink-500 bg-clip-text text-transparent">
    Armadale  <!-- Change this text -->
</a>
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Update text here -->
    <a href="#benefits">Benefits</a>  <!-- Update text here -->
    <a href="#contact">Contact</a>    <!-- Update text here -->
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-6xl lg:text-7xl font-bold leading-tight mb-8">
    Building financial clarity in a complex world  <!-- Main headline -->
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12">
    Professional accounting services tailored to your business needs  <!-- Subheading -->
</p>
```

### Tailwind CSS Classes Explained
Common classes used throughout:
- `text-[size]`: Controls text size (e.g., `text-xl`, `text-2xl`)
- `mb-[size]`: Adds margin bottom (e.g., `mb-8`, `mb-12`)
- `py-[size]`: Adds padding top and bottom
- `bg-[color]`: Sets background color
- `hover:[property]`: Applies styles on hover

**Tip**: When modifying classes, maintain the responsive prefixes:
- `md:` for medium screens
- `lg:` for large screens

## Managing Links

### Navigation Menu Links
Update the following sections:

1. **Main Navigation**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services">Services</a>  <!-- Internal link -->
    <a href="#benefits">Benefits</a>  <!-- Internal link -->
    <a href="#contact">Contact</a>    <!-- Internal link -->
</div>
```

2. **Call-to-Action Buttons**
```html
<!-- Replace 'theaccountants.com' with your actual URL -->
<a href="https://theaccountants.com" class="hidden md:block px-6 py-2">
    Get Started
</a>
```

3. **Contact Information**
```html
<!-- Update email address -->
<a href="mailto:support@example.com">
    support@example.com
</a>
```

### Footer Links
Update all footer links in their respective sections:

```html
<div class="grid grid-cols-1 md:grid-cols-4 gap-12">
    <!-- Services Section -->
    <ul class="space-y-2 text-gray-400">
        <li><a href="#">Business Valuation</a></li>
        <li><a href="#">Audit Preparation</a></li>
        <li><a href="#">Compliance Monitoring</a></li>
    </ul>

    <!-- Company Section -->
    <ul class="space-y-2 text-gray-400">
        <li><a href="#">About Us</a></li>
        <li><a href="#">Careers</a></li>
        <li><a href="#">Blog</a></li>
    </ul>
</div>
```

## Adding Privacy and Terms Pages

### Step 1: Create New Pages
Create two new files in your project directory:
- `privacy.html`
- `terms.html`

### Step 2: Update Footer Links
Replace the placeholder links in the Legal section:

```html
<!-- Before -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>

<!-- After -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure all internal links start with `#` for same-page navigation
   - Check that section IDs match exactly (case-sensitive)

2. **Responsive Design Issues**
   - Don't remove `md:` or `lg:` prefixes from classes
   - Test on different screen sizes using browser dev tools

3. **Gradient Text Not Showing**
   - Ensure these classes remain together:
     ```html
     bg-gradient-to-r from-purple-400 to-pink-400 bg-clip-text text-transparent
     ```

4. **Images Not Loading**
   - Verify file paths are correct
   - Check image file extensions (case-sensitive)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax using the [W3C Validator](https://validator.w3.org/)
- Test responsiveness using Chrome DevTools (F12)

Remember to always backup your files before making significant changes, and test all modifications in a development environment first.