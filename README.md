# AI Directory Landing Page - Maintenance Guide

This guide will help you maintain and customize the AI Directory landing page. It's written for beginners with no prior coding experience.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To modify:

1. Change the logo text:
```html
<!-- Find this line in the header section -->
<a href="#" class="text-2xl font-bold text-blue-500">AI Directory</a>
```
Simply replace "AI Directory" with your desired text.

2. Update navigation menu items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-300 hover:text-white transition-colors duration-300">Features</a>
    <!-- Add or modify menu items here -->
</div>
```

### Hero Section
The hero section is your main landing area. To update:

1. Change the main heading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-extrabold mb-8 bg-clip-text text-transparent bg-gradient-to-r from-blue-400 to-blue-600">
    The BEST AI Tool Directory
</h1>
```
Replace "The BEST AI Tool Directory" with your heading.

2. Modify the subheading:
```html
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Best AI Tool For Writing Content - Powered by Claude (Anthropic)
</p>
```

### Understanding Tailwind Classes
Common classes used in this template:

- Text sizes: `text-xl`, `text-2xl`, etc.
- Colors: `text-gray-300`, `bg-blue-600`
- Spacing: `px-4` (padding left/right), `py-4` (padding top/bottom)
- Responsive design: `md:text-2xl` (applies at medium screens)

## Managing Links

### Current Link Inventory
1. Navigation Menu Links:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

2. Call-to-Action Links:
```html
<a href="https://www.bestaitoolsforwritingcontent.com">Get Started</a>
```

### Updating Links
To update any link:

1. Locate the `<a>` tag
2. Modify the `href` attribute
3. Update the text between the tags

Example:
```html
<!-- From -->
<a href="https://www.bestaitoolsforwritingcontent.com">Get Started</a>

<!-- To -->
<a href="https://your-new-url.com">Start Now</a>
```

## Adding Privacy and Terms Pages

### Footer Link Setup
Locate the footer section with legal links:

```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To link to your policy pages:

1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Links**
- Check that all href values start with either "#" (for page sections) or "https://" (for external links)
- Verify file names match exactly for internal pages (privacy.html, terms.html)

2. **Styling Problems**
- Make sure Tailwind CSS is properly loaded:
```html
<script src="https://cdn.tailwindcss.com"></script>
```
- Check for typos in class names
- Verify responsive classes (md:, lg:) are properly formatted

3. **Layout Issues**
- Check container classes: `container mx-auto`
- Verify padding classes: `px-4 sm:px-6 lg:px-8`
- Ensure proper grid column setup: `grid-cols-1 md:grid-cols-3`

### Need Help?
If you encounter issues:
1. Check the browser's developer tools (F12) for errors
2. Verify all HTML tags are properly closed
3. Ensure all required classes are present
4. Compare your changes against the original code

Remember to always backup your code before making changes!