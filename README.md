# Couples Therapy Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Couples Therapy landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common updates.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the main navigation and logo. To update:

1. **Company Name/Logo**
```html
<!-- Find this line in the header -->
<a href="/" class="text-xl font-semibold text-gray-800">Relational Life Texas</a>
```
- Replace "Relational Life Texas" with your company name
- Adjust text size using `text-xl` (can be `text-lg`, `text-2xl`, etc.)

2. **Navigation Links**
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-600 hover:text-gray-900">Services</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900">FAQ</a>
</div>
```
- Update link text between `<a>` tags
- Maintain the `text-gray-600 hover:text-gray-900` classes for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 mb-6 leading-tight">
    Couples Therapy San Antonio
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    We help struggling couples save their relationship.
</p>
```
- Update heading and paragraph text as needed
- Keep responsive text classes (`text-4xl md:text-5xl lg:text-6xl`)
- Maintain spacing classes (`mb-6`, `mb-12`)

### Common Tailwind CSS Classes Explained
- `container mx-auto`: Centers content with consistent margins
- `px-6`: Adds horizontal padding (6 units)
- `py-24`: Adds vertical padding (24 units)
- `md:`: Applies styles at medium screen sizes
- `hover:`: Applies styles on mouse hover
- `transition-colors`: Smooths color changes
- `rounded-full`: Creates circular corners

## Fixing Broken Links

### Navigation Menu Links
Current internal links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
```
To update:
1. For internal sections, keep the `#` prefix
2. Ensure the href matches the section's ID exactly
3. Example: `<a href="#new-section">New Section</a>`

### Contact Button Links
```html
<a href="https://relationallifetexas.com/contact-us/"
   class="px-6 py-2 bg-blue-600 text-white rounded-full">
    Contact Us
</a>
```
To update:
1. Replace the entire URL in `href`
2. Maintain the same class structure for consistent styling
3. Test the link after updating

### Footer Links
```html
<div class="col-span-2">
    <a href="mailto:contact@relationallifetexas.com">
        contact@relationallifetexas.com
    </a>
</div>
```
- Update email address in both the `href="mailto:"` and display text
- Keep the `mailto:` prefix for email links

## Linking Privacy and Terms Pages

### Adding Privacy Policy Link
```html
<!-- Locate this section in the footer -->
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2">
        <li><a href="privacy.html" class="text-gray-400 hover:text-white">Privacy Policy</a></li>
        <li><a href="terms.html" class="text-gray-400 hover:text-white">Terms of Service</a></li>
    </ul>
</div>
```

To implement:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the `href` attributes to point to your new pages
3. Options for link paths:
   - Relative path: `href="privacy.html"`
   - Subdirectory: `href="policies/privacy.html"`
   - Full URL: `href="https://yoursite.com/privacy"`

## Troubleshooting

### Common Issues and Solutions

1. **Broken Internal Links**
- Check that section IDs match href attributes exactly
- Example: `href="#services"` must match `id="services"`
- IDs are case-sensitive

2. **Responsive Design Issues**
- Verify Tailwind breakpoint classes are correct
- Common breakpoints:
  - `md:` (768px)
  - `lg:` (1024px)
  - `xl:` (1280px)

3. **Styling Inconsistencies**
- Check for missing Tailwind classes
- Compare with similar elements
- Use browser inspector to verify applied styles

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Inspect similar elements for class reference
- Test all changes in multiple browsers
- Maintain backups before making significant changes

Remember to test all updates thoroughly across different devices and screen sizes before deploying to production.