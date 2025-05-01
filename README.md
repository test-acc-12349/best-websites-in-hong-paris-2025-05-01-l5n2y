# Hong Paris Landing Page - Maintenance Guide

This guide will help you maintain and customize the Hong Paris landing page. Whether you're new to web development or need a quick reference, follow these instructions to make common updates safely and effectively.

## Table of Contents
- [Updating Text and Styling](#updating-text-and-styling)
- [Managing Links](#managing-links)
- [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
- [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains your main navigation and brand name. To update:

1. **Company Name:**
```html
<a href="/" class="text-2xl font-bold text-gray-900">Hong Paris</a>
```
Replace "Hong Paris" with your company name. Keep the classes to maintain styling.

2. **Navigation Menu Items:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900">Features</a>
    <!-- Other menu items -->
</div>
```
Modify the text between `<a>` tags to change menu items.

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold">Best Websites In Hong Paris</h1>
<p class="text-xl md:text-2xl text-gray-600">Custom Websites For Your Business</p>
```
- Change the h1 text to your main headline
- Update the paragraph for your subheading
- Keep the responsive classes (`md:`, `lg:`) to maintain mobile friendliness

### Tailwind CSS Tips
- `text-{size}`: Controls font size (xl, 2xl, etc.)
- `md:` prefix: Applies styles on medium screens and up
- `hover:` prefix: Applies styles on mouse hover
- `bg-{color}-{shade}`: Changes background colors

## Managing Links

### Navigation Links
Current internal links are:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```

To update:
1. Identify the section ID you want to link to
2. Add a matching ID to that section: `<section id="your-section-name">`
3. Update the href to match: `<a href="#your-section-name">`

### Call-to-Action Buttons
Current external link:
```html
<a href="https://sigmaseo.io" class="inline-block bg-blue-600 text-white">Get Started</a>
```

To update:
1. Replace `https://sigmaseo.io` with your desired URL
2. Test the link before deploying
3. Consider adding `target="_blank"` for external links

## Adding Privacy and Terms Pages

### Current Footer Links
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="#" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="#" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

### Steps to Add Policy Pages:

1. Create new HTML files:
   - `privacy.html`
   - `terms.html`

2. Update the footer links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
```

3. Ensure consistent styling by copying these classes to new page links:
   - `text-gray-400`: Default text color
   - `hover:text-white`: Hover state
   - `transition-colors duration-300`: Smooth color transition

## Troubleshooting

### Common Issues:

1. **Broken Internal Links**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Remove any spaces in IDs

2. **Responsive Design Problems**
   - Keep all responsive classes (`sm:`, `md:`, `lg:`)
   - Test on multiple screen sizes
   - Don't remove the viewport meta tag

3. **Style Inconsistencies**
   - Maintain Tailwind class structure
   - Copy existing classes for new elements
   - Use the same color schemes (blue-600, gray-900, etc.)

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Validate HTML at [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser dev tools

Remember to always backup your files before making changes and test thoroughly before deploying to production.