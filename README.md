# VoiceAI Landing Page Maintenance Guide

This guide will help you maintain and customize the VoiceAI landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common updates.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text**: Find this line and change "VoiceAI" to your brand name:
```html
<a href="/" class="text-xl font-semibold">VoiceAI</a>
```

2. **Navigation Menu Items**: Located in the header's `<div class="hidden md:flex space-x-8">`. Each item follows this pattern:
```html
<a href="#section-name" class="text-gray-600 hover:text-gray-900 transition-colors duration-200">Menu Item</a>
```

### Hero Section
Find the main headline in the first `<section>` tag:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold tracking-tight text-gray-900 mb-6">
    Your Direct Portal for Engaging Prospective Clients Effortlessly
</h1>
```

To modify:
- Change text between the `<h1>` tags
- Adjust text size using Tailwind classes:
  - `text-4xl`: Base size
  - `md:text-5xl`: Medium screens
  - `lg:text-6xl`: Large screens

### Understanding Tailwind Classes
Common classes used throughout:
- `mx-auto`: Centers content horizontally
- `px-4`: Adds horizontal padding
- `py-24`: Adds vertical padding
- `bg-white`: White background
- `text-gray-600`: Gray text color
- `hover:`: Prefix for hover effects

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Change the `href` value to match your section ID
2. Ensure the corresponding section has the matching ID attribute
3. For external links, use the full URL:
```html
<a href="https://your-external-link.com">Link Text</a>
```

### Call-to-Action Buttons
The main CTA button currently points to:
```html
<a href="https://canadiansred.aibizbots4u.com/" class="inline-flex items-center px-8 py-4...">
```

To update:
1. Replace the URL with your destination
2. Maintain the existing classes for consistent styling
3. Update the button text between the `<a>` tags

## Adding Privacy and Terms Pages

### Footer Link Updates
Locate the Legal section in the footer:
```html
<div>
    <h3 class="text-white text-lg font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <li><a href="#" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
    </ul>
</div>
```

To link to policy pages:
1. Create your privacy.html and terms.html files
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition-colors duration-200">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition-colors duration-200">Terms of Service</a></li>
```

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
   - Ensure section IDs match exactly with href values
   - IDs are case-sensitive
   - Check for extra spaces in IDs

2. **Responsive Design Issues**
   - Keep the responsive classes (`md:`, `lg:`) when updating
   - Test on different screen sizes after changes
   - Don't remove the `max-w-7xl` class from container elements

3. **Styling Problems**
   - Always maintain the existing class structure
   - Add new classes at the end of the class list
   - Use Tailwind's utility classes instead of custom CSS

### Need Help?
If you encounter issues:
1. Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
2. Verify all HTML tags are properly closed
3. Use browser developer tools to inspect elements
4. Ensure the Tailwind CDN link remains in the header

Remember to always test your changes across different devices and browsers before deploying to production.