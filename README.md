# Texas Web Design Landing Page - Maintenance Guide

This guide will help you maintain and customize the Texas Web Design landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**: Find this line in the header:
```html
<div class="text-2xl font-bold text-blue-600">TWD</div>
```
Simply replace "TWD" with your desired text.

2. **Navigation Links**: Locate the navigation menu:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-blue-600 transition duration-300">Benefits</a>
    <!-- More links -->
</div>
```
Change the text between `<a>` tags to update menu items.

### Hero Section
To modify the main headline and subheading:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6">Texas Web Design</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-8">Best Websites In Texas</p>
```

- Change "Texas Web Design" to your headline
- Update "Best Websites In Texas" to your subheading
- The classes `text-4xl`, `md:text-5xl`, etc. control text size at different screen sizes

### Features & Benefits Sections
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 hover:shadow-xl transition duration-300">
    <i class="fas fa-server text-4xl text-blue-600 mb-6"></i>
    <h3 class="text-xl font-semibold mb-4">Free Hosting</h3>
    <p class="text-gray-600">Premium hosting included with every website package</p>
</div>
```

To modify:
1. Change the icon by updating the `fa-server` class to any [Font Awesome](https://fontawesome.com/icons) icon
2. Update the heading text inside `<h3>`
3. Modify the description inside `<p>`

## Fixing Broken Links

### Current Link Structure
The page contains several types of links:

1. **Navigation Menu Links** (internal):
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
These link to page sections using IDs. Ensure corresponding sections have matching IDs.

2. **Call-to-Action Links** (external):
```html
<a href="https://twd.com" class="inline-block bg-blue-600 text-white px-8 py-4">Get Started</a>
```
Replace `https://twd.com` with your actual website URL.

3. **Footer Links** (internal/external):
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white">About</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white">Services</a></li>
    <!-- More links -->
</ul>
```
Replace `#` with actual page URLs.

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
In the footer section, locate:
```html
<li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
```
Replace with:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition duration-300">Privacy Policy</a></li>
```

### Adding Terms of Service Link
Similarly, update:
```html
<li><a href="#" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```
To:
```html
<li><a href="terms.html" class="text-gray-400 hover:text-white transition duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Ensure section IDs match navigation href attributes
- Check for typos in IDs and hrefs
- IDs are case-sensitive

2. **Responsive Design Issues**
- Don't remove `md:` or `lg:` prefixes from Tailwind classes
- Keep the viewport meta tag in the header:
```html
<meta name="viewport" content="width=device-width, initial-scale=1.0">
```

3. **Missing Icons**
- Verify Font Awesome CDN link is present in header
- Check icon class names against Font Awesome documentation
- Ensure internet connectivity for CDN access

### Need Help?
If you encounter issues:
1. Check the browser console for errors (F12)
2. Verify all files are in the correct directory
3. Ensure all HTML tags are properly closed
4. Validate your HTML at [W3C Validator](https://validator.w3.org/)

Remember to always back up your files before making changes, and test your updates across different browsers and devices.