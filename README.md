# Essendon Accounting Landing Page - Maintenance Guide

This guide will help you maintain and customize the Essendon Accounting landing page. Whether you're new to web development or need a quick reference, follow these detailed instructions for common maintenance tasks.

## Table of Contents
1. [Updating Text and Styling](#updating-text-and-styling)
2. [Managing Links](#managing-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Styling

### Header Section
The header contains the company name and navigation menu. To update:

1. Company Name:
```html
<a href="/" class="text-2xl font-bold text-white hover:text-blue-400 transition duration-300">
    Essendon<span class="text-blue-400">.</span>
</a>
```
- Change "Essendon" to your company name
- The blue dot can be removed by deleting the `<span>` element

2. Navigation Menu Items:
```html
<div class="hidden md:flex space-x-8">
    <a href="#services" class="text-gray-300 hover:text-white transition duration-300">Services</a>
    <a href="#benefits" class="text-gray-300 hover:text-white transition duration-300">Benefits</a>
    <a href="#contact" class="text-gray-300 hover:text-white transition duration-300">Contact</a>
</div>
```
- Update text between `<a>` tags
- Maintain the class attributes for consistent styling

### Hero Section
Located at the top of the page:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8">
    Essendon accounting services
</h1>
<p class="text-xl md:text-2xl text-gray-300 mb-12 max-w-3xl mx-auto">
    Trusted advisors for your financial future
</p>
```
- Update heading and subheading text
- Keep responsive text classes (`text-4xl md:text-5xl lg:text-6xl`) for proper scaling

### Tailwind CSS Class Guide
Common classes used throughout:
- Text sizes: `text-xl`, `text-2xl`, `text-3xl`, etc.
- Colors: `text-gray-300`, `text-blue-400`, `bg-gray-900`
- Spacing: `mb-8` (margin bottom), `px-6` (padding left/right)
- Hover effects: `hover:text-white`, `hover:bg-blue-700`

## Managing Links

### Navigation Links
Current internal links:
```html
<a href="#services">Services</a>
<a href="#benefits">Benefits</a>
<a href="#contact">Contact</a>
```
To update:
1. For internal sections, keep the `#` prefix
2. Ensure the href matches the section's ID attribute
3. Example: `<a href="#new-section">New Section</a>`

### External Links
The "Get Started" button links:
```html
<a href="https://theaccountants.com" class="px-6 py-2 bg-blue-600">
    Get Started
</a>
```
To update:
1. Replace `https://theaccountants.com` with your desired URL
2. Test the link after updating
3. Consider adding `target="_blank"` for external links

### Email Links
Located in the contact section:
```html
<a href="mailto:support@example.com">
    support@example.com
</a>
```
- Replace both the href and text content with your actual email address
- Example: `<a href="mailto:contact@yourdomain.com">contact@yourdomain.com</a>`

## Adding Privacy and Terms Pages

### Footer Link Updates
Current placeholder links:
```html
<div>
    <h4 class="text-lg font-semibold mb-4">Legal</h4>
    <ul class="space-y-2 text-gray-400">
        <li><a href="#" class="hover:text-white transition duration-300">Privacy Policy</a></li>
        <li><a href="#" class="hover:text-white transition duration-300">Terms of Service</a></li>
    </ul>
</div>
```

To add proper links:
1. Create privacy.html and terms.html files in your root directory
2. Update the href attributes:
```html
<li><a href="privacy.html" class="hover:text-white transition duration-300">Privacy Policy</a></li>
<li><a href="terms.html" class="hover:text-white transition duration-300">Terms of Service</a></li>
```

### Maintaining Consistent Styling
When creating privacy.html and terms.html:
1. Copy the header and footer from index.html
2. Use the same Tailwind CSS classes for consistency
3. Example structure:
```html
<!DOCTYPE html>
<html lang="en" class="scroll-smooth">
<head>
    <!-- Copy head section from index.html -->
</head>
<body class="bg-gray-900 text-gray-100 font-inter antialiased">
    <!-- Copy header section -->
    
    <!-- Add your privacy/terms content here -->
    <main class="container mx-auto px-6 py-24">
        <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
        <!-- Add your content -->
    </main>
    
    <!-- Copy footer section -->
</body>
</html>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Layout**
   - Check for missing closing tags
   - Verify Tailwind CSS classes are spelled correctly
   - Ensure container divs maintain their structure

2. **Non-Working Links**
   - Verify file names match exactly (case-sensitive)
   - Check for proper path references
   - Test all links after updates

3. **Responsive Issues**
   - Keep responsive classes (`md:`, `lg:` prefixes)
   - Test on multiple screen sizes
   - Maintain the existing grid structure

Remember to:
- Back up files before making changes
- Test all updates in multiple browsers
- Maintain consistent spacing and indentation
- Keep the original class structure for proper styling

Need help? Refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or contact your web development team.