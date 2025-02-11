# Landing Page Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the landing page. Whether you're new to web development or need a quick reference, follow these steps to make common updates safely and effectively.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Linking Privacy and Terms Pages](#linking-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains your logo and navigation menu. To update:

1. **Logo Text**
```html
<!-- Find this section -->
<div class="text-2xl font-bold bg-gradient-to-r from-indigo-600 to-purple-600 bg-clip-text text-transparent">
    Logo
</div>

<!-- Replace "Logo" with your company name -->
```

2. **Navigation Menu Items**
```html
<div class="hidden md:flex space-x-8">
    <!-- Update these link texts as needed -->
    <a href="#" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Features</a>
    <a href="#" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Benefits</a>
    <a href="#" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Contact</a>
</div>
```

### Hero Section
Update the main headline and subheading:
```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-indigo-600 to-purple-600 bg-clip-text text-transparent">
    <!-- Replace this text -->
    Lorem ipsum dolor
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12 leading-relaxed">
    <!-- Replace this text -->
    Lorem ipsum dolor
</p>
```

### Understanding Tailwind Classes
Common classes explained:
- `text-4xl`: Large text size
- `md:text-5xl`: Larger text on medium screens
- `bg-white`: White background
- `px-6`: Horizontal padding
- `py-4`: Vertical padding
- `rounded-full`: Fully rounded corners
- `hover:shadow-lg`: Shadow effect on hover

## Fixing Broken Links

### Navigation Menu Links
1. Locate the navigation section:
```html
<div class="hidden md:flex space-x-8">
    <!-- Update href attributes with proper URLs -->
    <a href="#features">Features</a>
    <a href="#benefits">Benefits</a>
    <a href="#contact">Contact</a>
</div>
```

2. Replace `#` with proper URLs:
- For same-page sections: Use `#section-id`
- For other pages: Use relative paths like `./about.html`
- For external links: Use full URLs starting with `https://`

### Call-to-Action Buttons
Update the "Get Started" button links:
```html
<button class="bg-gradient-to-r from-indigo-600 to-purple-600 text-white px-6 py-2 rounded-full">
    <!-- Add proper href -->
    <a href="./signup.html">Get Started</a>
</button>
```

## Linking Privacy and Terms Pages

### Footer Links Setup
1. Locate the Legal section in the footer:
```html
<div>
    <h3 class="font-semibold mb-4">Legal</h3>
    <ul class="space-y-2">
        <!-- Update these href attributes -->
        <li><a href="./privacy.html" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Privacy</a></li>
        <li><a href="./terms.html" class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">Terms</a></li>
    </ul>
</div>
```

2. Create matching HTML files:
- Create `privacy.html` in your root directory
- Create `terms.html` in your root directory
- Use the same styling classes for consistency

### Example Privacy Page Link
```html
<!-- In privacy.html -->
<a href="./privacy.html" 
   class="text-gray-600 hover:text-indigo-600 transition-colors duration-300">
    Privacy Policy
</a>
```

## Troubleshooting

Common Issues and Solutions:

1. **Broken Styles**
   - Verify the Tailwind CSS CDN link is working
   - Check for typos in class names
   - Ensure proper spacing between classes

2. **Non-Working Links**
   - Confirm file paths are correct
   - Check for proper URL formatting
   - Verify files exist in the specified location

3. **Responsive Design Issues**
   - Test on different screen sizes
   - Ensure proper use of responsive prefixes (sm:, md:, lg:)
   - Check for conflicting classes

For additional help:
- Reference the [Tailwind CSS documentation](https://tailwindcss.com/docs)
- Use browser developer tools to inspect elements
- Verify all files are in the correct directory structure

Remember to always test changes in multiple browsers and screen sizes before deploying to production.