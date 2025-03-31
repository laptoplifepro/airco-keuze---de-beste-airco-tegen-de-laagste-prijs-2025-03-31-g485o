# Airco Keuze Landing Page - Maintenance Guide

This guide will help you maintain and customize the Airco Keuze landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the main navigation and logo. To update:

1. **Logo Text:**
```html
<a href="/" class="text-2xl font-bold text-blue-600">Airco Keuze</a>
```
- Replace "Airco Keuze" with your desired text
- The `text-2xl` class controls size
- `text-blue-600` controls the blue color

2. **Navigation Links:**
```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-blue-600 transition-colors">Voordelen</a>
    <!-- Additional nav items -->
</div>
```
- Replace "Voordelen" and other text with your desired navigation labels
- Keep the `href` attributes matching your section IDs

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold text-gray-900 leading-tight mb-6">
    Snel De Juiste Airco Voor De Laagste Prijs
</h1>
```
- Update the heading text while maintaining the existing classes
- The responsive text sizes are:
  - Mobile: `text-4xl`
  - Tablet: `text-5xl`
  - Desktop: `text-6xl`

### Features Section
Each feature card follows this structure:
```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition-shadow duration-300">
    <div class="w-16 h-16 bg-blue-100 rounded-full flex items-center justify-center mb-6">
        <!-- SVG icon here -->
    </div>
    <h3 class="text-xl font-semibold mb-4">Ruime Keuze</h3>
    <p class="text-gray-600">Ontdek ons uitgebreide assortiment airco's voor elke ruimte en budget.</p>
</div>
```
- Update the `h3` text for feature titles
- Modify the paragraph text while keeping the `text-gray-600` class for consistent styling

## Managing Links

### Navigation Menu Links
Current internal links in the navigation:
```html
<a href="#features">Voordelen</a>
<a href="#benefits">Benefits</a>
<a href="#faq">FAQ</a>
<a href="#contact">Contact</a>
```
To update:
1. Ensure the `href` matches the `id` of the target section
2. Example: `<section id="features">` corresponds to `href="#features"`

### Call-to-Action Links
Currently using Amazon affiliate links:
```html
<a href="https://amzn.to/4iRgNla" class="bg-blue-600 text-white px-6 py-2 rounded-full">
    Bekijk Aanbod
</a>
```
To update:
1. Replace `https://amzn.to/4iRgNla` with your desired URL
2. Keep the existing classes for consistent styling

### Social Media Links
Located in the footer:
```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors">
        <!-- Facebook icon -->
    </a>
</div>
```
- Replace the `#` with your social media profile URLs
- Example: `href="https://facebook.com/yourpage"`

## Adding Privacy and Terms Pages

### Footer Link Updates
Current placeholder links:
```html
<ul class="space-y-2">
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
    <li><a href="#" class="text-gray-400 hover:text-white transition-colors">Algemene Voorwaarden</a></li>
</ul>
```

To link to new pages:
1. Create `privacy.html` and `terms.html` in your root directory
2. Update the links:
```html
<li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors">Privacy Policy</a></li>
<li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors">Algemene Voorwaarden</a></li>
```

## Troubleshooting

### Common Issues

1. **Broken Internal Links**
- Check that section IDs match their corresponding href attributes
- Example: If `href="#features"` doesn't work, verify there's a `<section id="features">`

2. **Responsive Design Issues**
- Classes starting with `md:` apply to screens ≥768px wide
- Classes starting with `lg:` apply to screens ≥1024px wide
- Example: `text-4xl md:text-5xl lg:text-6xl` creates responsive text sizing

3. **Styling Inconsistencies**
- Always maintain the full chain of Tailwind classes when updating elements
- Example: Keep `class="text-gray-400 hover:text-white transition-colors"` together for links

### Need Help?
- Review the [Tailwind CSS documentation](https://tailwindcss.com/docs) for class references
- Test all links after updating
- View the page at different screen sizes to ensure responsive design
- Keep backups of working versions before making changes

Remember to test all changes in multiple browsers and screen sizes before deploying to production.