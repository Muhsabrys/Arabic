# Al-Manara Website - Quick Reference Guide

## 📋 Navigation Paths

All navigation uses **relative paths** to ensure proper functionality on GitHub Pages.

### From Root (index.html)
- To any module: `./[module-name]/` (e.g., `./vocabulary/`)
- Example: `<a href="./vocabulary/">Vocabulary</a>`

### From Module Index (e.g., vocabulary/index.html)
- Back to root: `../index.html`
- To a lesson: `./Lesson[N].html` (e.g., `./Lesson1.html`)
- Example: `<a href="../index.html">Home</a>`

### From Lesson (e.g., vocabulary/Lesson1.html)
- Back to root: `../index.html`
- Back to module: `./index.html`
- To another lesson: `./Lesson[N].html`
- Example: `<a href="./Lesson2.html">Next Lesson</a>`

## 🎨 Color System

### Primary Colors
- **Emerald 850**: `#064e3b` - Deep emerald for backgrounds
- **Emerald 950**: `#022c22` - Darkest emerald for navbar/footer

### Accent Colors
- **Gold 400**: `#fbbf24` - Light gold for highlights
- **Gold 500**: `#f59e0b` - Primary gold for buttons
- **Gold 600**: `#d97706` - Rich gold for hover states

### Module-Specific Colors
Each module has a unique accent color:
- **Vocabulary**: Emerald (`emerald-100`, `emerald-800`)
- **Grammar**: Gold (`gold-100`, `gold-700`)
- **Phonics**: Blue (`blue-100`, `blue-700`)
- **Culture**: Purple (`purple-100`, `purple-700`)
- **Quizzes**: Red (`red-100`, `red-700`)
- **Reading**: Teal (`teal-100`, `teal-700`)
- **Writing**: Yellow (`yellow-100`, `yellow-700`)
- **Listening**: Indigo (`indigo-100`, `indigo-700`)
- **Speaking**: Pink (`pink-100`, `pink-700`)
- **Games**: Orange (`orange-100`, `orange-700`)

## 🔤 Font Usage

### Arabic Text
```html
<span class="font-arabic">مرحباً</span>
```
- Font: Cairo
- Use for all Arabic script

### English Text
```html
<span class="font-sans">Hello</span>
```
- Font: Lato
- Default font family

## 📦 Common Components

### Navbar (Consistent across all pages)
```html
<nav class="bg-emerald-950 text-white shadow-xl sticky top-0 z-50">
    <!-- Logo and navigation links -->
</nav>
```

### Footer (Consistent across all pages)
```html
<footer class="bg-emerald-950 text-white py-8">
    <!-- Footer content -->
</footer>
```

### Lesson Card (Module index pages)
```html
<a href="./Lesson1.html" class="lesson-card bg-white rounded-xl shadow-lg...">
    <!-- Card content -->
</a>
```

### Module Card (Root index.html)
```html
<a href="./vocabulary/" class="bg-white rounded-xl shadow-md...">
    <!-- Module information -->
</a>
```

## 🎯 Difficulty Levels

Each lesson is tagged with a difficulty level:
- **Beginner** (Green badge)
- **Intermediate** (Blue badge)
- **Advanced** (Purple badge)
- **Mastery** (Gold badge)

## 📱 Responsive Breakpoints

- **Mobile**: Default (< 768px)
- **Tablet**: `md:` (≥ 768px)
- **Desktop**: `lg:` (≥ 1024px)

## 🔧 Common CSS Classes

### Hover Effects
- `.hover-card` - Card lift on hover
- `.hover:text-gold-400` - Text color change
- `.group-hover:text-gold-600` - Group hover effect

### Layout
- `.container mx-auto px-6` - Centered container with padding
- `.grid grid-cols-1 md:grid-cols-2 lg:grid-cols-3` - Responsive grid

### Typography
- `.text-emerald-950` - Dark emerald text
- `.font-bold` - Bold weight
- `.font-arabic` - Arabic font family

## 📊 Lesson Template Structure

Every lesson page follows this structure:
1. Navbar (with breadcrumb navigation)
2. Lesson Header (title, number, level)
3. Lesson Overview section
4. Main Content section
5. Cultural Note/Tip section
6. Navigation buttons (Previous/Next)
7. Footer

## 🌐 CDN Resources

### Tailwind CSS
```html
<script src="https://cdn.tailwindcss.com"></script>
```

### Font Awesome
```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css">
```

### Google Fonts
```html
<link href="https://fonts.googleapis.com/css2?family=Cairo:wght@400;600;700&family=Lato:wght@400;700&display=swap" rel="stylesheet">
```

## 🛠️ Customization Guide

### Adding a New Lesson
1. Copy an existing lesson file (e.g., `Lesson1.html`)
2. Update the lesson number and title
3. Modify the content section
4. Update navigation links (prev/next)
5. Add the lesson to the module index page

### Changing Colors
Update the `tailwind.config` object in each HTML file:
```javascript
tailwind.config = {
    theme: {
        extend: {
            colors: {
                // Add your custom colors here
            }
        }
    }
}
```

### Adding Icons
Browse Font Awesome icons at: https://fontawesome.com/icons
Use format: `<i class="fa-solid fa-[icon-name]"></i>`

## 📝 Content Guidelines

- Keep lessons concise (~15 minutes of content)
- Use clear, simple language for instructions
- Include examples and practice exercises
- Add cultural insights where relevant
- Use consistent formatting across lessons

## 🚀 Deployment Checklist

- [ ] All relative paths are correct
- [ ] All images/assets are properly linked
- [ ] CDN resources are loading
- [ ] Test on multiple browsers
- [ ] Test responsive design on mobile
- [ ] Verify all navigation links work
- [ ] Check for broken links
- [ ] Test on GitHub Pages preview

## 📞 Support

For issues or questions:
1. Check this reference guide
2. Review existing lesson files for examples
3. Consult the main README.md
4. Open an issue on GitHub

---

**Last Updated**: December 2025
**Version**: 1.0.0
