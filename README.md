# Neuro Fortis PRO Landing Page - Maintenance Guide

This guide provides detailed instructions for maintaining and customizing the Neuro Fortis PRO landing page. Whether you're new to web development or need a quick reference, you'll find step-by-step guidance for common maintenance tasks.

## Table of Contents
1. [Updating Text and Tailwind CSS Classes](#updating-text-and-tailwind-css-classes)
2. [Fixing Broken Links](#fixing-broken-links)
3. [Adding Privacy and Terms Pages](#adding-privacy-and-terms-pages)
4. [Troubleshooting](#troubleshooting)

## Updating Text and Tailwind CSS Classes

### Header Section
The header contains the company name and navigation menu:

```html
<div class="text-2xl font-bold bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Neuro Fortis PRO  <!-- Update company name here -->
</div>
```

To modify:
1. Locate this section at the top of the page
2. Change "Neuro Fortis PRO" to your desired text
3. The gradient effect is created by these Tailwind classes:
   - `bg-gradient-to-r`: Creates a right-flowing gradient
   - `from-purple-600`: Starting color
   - `to-blue-500`: Ending color

### Hero Section
The main headline and subtext are located here:

```html
<h1 class="text-4xl md:text-5xl lg:text-6xl font-bold leading-tight mb-8 bg-gradient-to-r from-purple-600 to-blue-500 bg-clip-text text-transparent">
    Enhance Memory & Boost Mental Clarity  <!-- Update main headline here -->
</h1>
<p class="text-xl md:text-2xl text-gray-600 mb-12">
    Experience enhanced cognitive function...  <!-- Update subtext here -->
</p>
```

Text size classes explained:
- `text-4xl`: Default size on mobile
- `md:text-5xl`: Medium screens (768px+)
- `lg:text-6xl`: Large screens (1024px+)

### Features Section
Each feature card follows this structure:

```html
<div class="bg-white rounded-xl p-8 shadow-lg hover:shadow-xl transition duration-300 border border-gray-100">
    <div class="w-16 h-16 bg-purple-100 rounded-full flex items-center justify-center mb-6">
        <i class="fas fa-brain text-2xl text-purple-600"></i>  <!-- Update icon here -->
    </div>
    <h3 class="text-xl font-bold mb-4">Memory Enhancement</h3>  <!-- Update feature title -->
    <p class="text-gray-600">Boost your memory retention...</p>  <!-- Update feature description -->
</div>
```

To modify feature cards:
1. Locate the features section (id="features")
2. Each card is contained in a div with class="bg-white rounded-xl..."
3. Update the icon using Font Awesome classes (fas fa-*)
4. Modify the title and description text as needed

## Fixing Broken Links

### Navigation Menu Links
Current navigation links are:

```html
<div class="hidden md:flex space-x-8">
    <a href="#features" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Features</a>
    <a href="#benefits" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Benefits</a>
    <a href="#faq" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">FAQ</a>
    <a href="#contact" class="text-gray-600 hover:text-gray-900 transition-colors duration-300">Contact</a>
</div>
```

To update links:
1. The `href="#features"` format links to sections within the page
2. For external links, replace with full URL: `href="https://example.com"`
3. For internal pages, use relative paths: `href="about.html"`

### Call-to-Action Links
Located in hero and CTA sections:

```html
<a href="#" class="inline-block bg-gradient-to-r...">
    Discover Neuro Fortis PRO  <!-- Update button text -->
</a>
```

Replace `href="#"` with your actual link destination.

### Social Media Links
Found in the footer:

```html
<div class="flex space-x-4">
    <a href="#" class="text-gray-400 hover:text-white transition-colors duration-300">
        <i class="fab fa-facebook"></i>
    </a>
    <!-- Similar structure for Twitter and Instagram -->
</div>
```

Update each `href="#"` with your social media profile URLs.

## Adding Privacy and Terms Pages

### Step 1: Add Footer Links
Add these links to the footer's Quick Links section:

```html
<ul class="space-y-2">
    <!-- Existing links -->
    <li><a href="privacy.html" class="text-gray-400 hover:text-white transition-colors duration-300">Privacy Policy</a></li>
    <li><a href="terms.html" class="text-gray-400 hover:text-white transition-colors duration-300">Terms of Service</a></li>
</ul>
```

### Step 2: Create New Pages
1. Create `privacy.html` and `terms.html` in your root directory
2. Copy the header and footer from `index.html` to maintain consistent styling
3. Add your policy content between them

### Step 3: Style Consistency
Use these Tailwind classes for consistent text styling:

```html
<div class="container mx-auto px-6 py-24">
    <h1 class="text-3xl font-bold mb-8">Privacy Policy</h1>
    <div class="prose max-w-none">
        <!-- Your policy content here -->
    </div>
</div>
```

## Troubleshooting

Common issues and solutions:

1. **Broken Gradients**
   - Ensure all gradient classes remain together: `bg-gradient-to-r from-purple-600 to-blue-500`
   - Don't remove `bg-clip-text` when using text gradients

2. **Responsive Issues**
   - Keep responsive classes in order: `text-base md:text-lg lg:text-xl`
   - Don't remove the `container` class from main sections

3. **Missing Icons**
   - Verify Font Awesome CDN link in the header
   - Check icon class names against [Font Awesome documentation](https://fontawesome.com/icons)

For additional help, refer to the [Tailwind CSS documentation](https://tailwindcss.com/docs) or create an issue in the project repository.