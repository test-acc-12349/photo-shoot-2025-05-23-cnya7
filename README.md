# Photo-Shoot Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Photo-Shoot landing page. Whether you're new to web development or need a quick reference, follow these step-by-step instructions.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the logo and navigation menu. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-gray-800">Photo-Shoot</a>
```
- Replace "Photo-Shoot" with your desired brand name
- Adjust text size using `text-2xl` (options: text-sm, text-base, text-lg, text-xl, text-2xl, etc.)

2. **Navigation Menu Items:**
```html
<a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
```
- Update link text between `>` and `</a>`
- Modify colors using Tailwind classes:
  - Current text color: `text-gray-600`
  - Hover color: `hover:text-gray-900`

### Hero Section
Located at the top of the page with a background image:

1. **Main Heading:**
```html
<h1 class="text-4xl md:text-6xl font-bold mb-6">Photo-Shoot</h1>
```
- Replace "Photo-Shoot" with your headline
- `md:text-6xl` means text size changes on medium screens
- `mb-6` adds margin bottom spacing

2. **Subheading:**
```html
<p class="text-xl md:text-2xl mb-8 max-w-2xl mx-auto">Get the ultimate product photography lightbox</p>
```
- Update the text between `<p>` tags
- `max-w-2xl` limits text width
- `mx-auto` centers the text

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl shadow-lg p-8 transform hover:scale-105 transition-all duration-300">
    <div class="text-blue-600 mb-4">
        <i class="fas fa-plug text-4xl"></i>
    </div>
    <h3 class="text-xl font-semibold mb-4">USB Powered</h3>
    <p class="text-gray-600">Connect to any USB port for consistent, reliable power supply</p>
</div>
```
To modify:
- Change icon: Update `fa-plug` to any [Font Awesome](https://fontawesome.com/icons) icon
- Update heading: Replace text in `<h3>` tags
- Update description: Modify text in `<p>` tags

## Fixing Broken Links

### Navigation Menu Links
Current links in the navigation:
```html
<a href="#features">Features</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="https://buy.stripe.com/14k5mM58ObjBbRK000">Buy Now</a>
```

To update:
1. Internal links (starting with #):
   - Ensure the href matches the section ID
   - Example: `href="#features"` links to `<section id="features">`

2. External links:
   - Replace the Stripe URL with your payment link
   - Format: `href="your-new-url-here"`

### Footer Links
Social media links need updating:
```html
<a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
    <i class="fab fa-facebook"></i>
</a>
```
Replace `href="#"` with your social media profiles.

## Linking Privacy and Terms Pages

### Adding Policy Links
In the footer section, locate:
```html
<ul class="space-y-2 text-gray-400">
    <li>Shipping Policy</li>
    <li>Return Policy</li>
    <li>Privacy Policy</li>
    <li>Terms of Service</li>
</ul>
```

Update to include links:
```html
<ul class="space-y-2 text-gray-400">
    <li><a href="shipping.html" class="hover:text-white transition-colors duration-300">Shipping Policy</a></li>
    <li><a href="returns.html" class="hover:text-white transition-colors duration-300">Return Policy</a></li>
    <li><a href="privacy.html" class="hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links:**
   - Check that section IDs match href attributes exactly
   - IDs are case-sensitive
   - Example: `href="#FAQ"` won't link to `id="faq"`

2. **Responsive Design Issues:**
   - Look for classes starting with `md:` or `lg:`
   - These control appearance on different screen sizes
   - Example: `text-xl md:text-2xl` means normal size on mobile, larger on desktop

3. **Icon Not Showing:**
   - Verify Font Awesome is properly loaded in `<head>`
   - Check icon class names against Font Awesome documentation
   - Example: `fas fa-plug` should show a plug icon

### Need Help?
- Check the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Verify HTML syntax using [W3C Validator](https://validator.w3.org/)
- Test responsiveness using browser developer tools (F12)

Remember to always test changes across different devices and browsers before publishing updates.