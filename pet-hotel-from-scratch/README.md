# Paws & Rest Pet Hotel - From Scratch Website

## Project Overview

A responsive pet hotel website built from scratch using pure HTML5 and CSS3 without any frameworks. This project demonstrates modern web development techniques including semantic HTML, responsive design, and CSS animations.

## 🎯 Features

### Core Requirements Met
- ✅ Pure HTML5/CSS3 (no frameworks)
- ✅ Main container with proper semantic structure
- ✅ Header, navigation, content, and footer containers
- ✅ Multiple navigation types (horizontal text, horizontal graphic, vertical text)
- ✅ Responsive multi-column layout (3+ columns at 1200px+)
- ✅ AI-generated video gallery page
- ✅ W3C HTML5 and CSS3 compliant

### Website Structure

#### HTML5 Semantic Elements
- `<header>` - Site header with logo and contact info
- `<nav>` - Multiple navigation sections
- `<article>` - Content sections (home, services, rooms, gallery, contact)
- `<aside>` - Left and right sidebars
- `<section>` - Sub-sections within articles
- `<footer>` - Site footer with links and copyright

#### Navigation Types
1. **Horizontal Text Navigation** - Sticky top menu with hover effects
2. **Horizontal Graphic Navigation** - Icon-based navigation with emoji icons
3. **Vertical Text Navigation** - Sidebar menu with hierarchical links

### Responsive Design

#### Breakpoints (Bootstrap v5.0+ standard)
- **< 576px** - Extra small devices (portrait phones)
- **576px - 768px** - Small devices (landscape phones)
- **768px - 992px** - Medium devices (tablets)
- **992px - 1200px** - Large devices (desktops)
- **1200px - 1400px** - Extra large devices (large desktops)
- **1400px+** - Extra extra large devices (larger desktops)

#### Layout Approaches
- Fluid layout with percentage-based widths
- Flexible grid using CSS Grid
- Flexbox for component alignment
- Responsive images and typography
- Mobile-first approach

### CSS Properties Used

#### Positioning & Layout
- `display` (flex, grid, block, inline-block)
- `position` (relative, absolute, sticky, fixed)
- `flex` (flex-direction, justify-content, align-items, gap)
- `grid` (grid-template-columns, gap)
- `float` & `clear`
- `z-index`
- `overflow`
- `visibility`
- `opacity`

#### Styling
- **Background**: gradients, colors, images
- **Box Model**: padding, margin, border, border-radius
- **Colors**: CSS variables, rgba
- **Fonts**: font-family, font-size, font-weight, text-transform, letter-spacing
- **Text**: text-align, text-decoration, text-shadow, line-height
- **Links**: hover states, transitions
- **Lists**: list-style, custom list markers
- **Transforms**: translateY, scale
- **Transitions**: all, specific properties
- **Animations**: fadeIn, fadeInDown, fadeInUp

### AI-Generated Content

The website includes an AI-generated video gallery showcasing:

#### Video Content (8 videos, 15+ minutes total)
1. **Welcome to Paws & Rest** (3:45) - Synthesia
2. **Virtual Facility Tour** (2:30) - Fliki.ai
3. **A Day in the Life** (2:15) - Kapwing
4. **Grooming & Spa Services** (1:50) - VEED
5. **Happy Pet Parents** (1:35) - Synthesia
6. **Pet Care Tips & Tricks** (2:00) - Canva

#### AI Generation Techniques
- **Text-to-Speech (TTS)** - Natural voiceovers from scripts
- **Speech-to-Text (STT)** - Automatic transcription
- **Script-to-Video** - Video generation from text
- **Auto-Subtitling** - Synchronized captions

#### Tools Used
- fliki.ai
- synthesia
- kapwing
- veed
- canva
- leonardo.ai

## 📁 File Structure

```
pet-hotel-from-scratch/
├── index.html           # Main homepage
├── gallery.html         # Dedicated AI video gallery page
├── css/
│   ├── style.css       # Main stylesheet
│   └── gallery.css     # Gallery-specific styles
├── images/             # Image assets
└── README.md           # This file
```

## 🎨 Design Features

### Color Scheme
- Primary: `#4a7c59` (Forest Green)
- Secondary: `#8fbc8f` (Light Green)
- Accent: `#f4a460` (Sandy Brown)
- Dark: `#2c3e50` (Dark Blue-Gray)
- Light: `#f8f9fa` (Off-White)

### Typography
- Font Family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif
- Base Font Size: 16px
- Responsive scaling via rem units

### Animations
- Fade-in effects on hero section
- Hover transitions on cards and buttons
- Transform effects (translateY, scale)
- Smooth scrolling behavior

## 🔧 Technical Implementation

### CSS Architecture
- CSS Variables for consistent theming
- Mobile-first responsive design
- Utility classes for reusable styles
- Semantic class naming
- Media queries for all breakpoints

### Accessibility Features
- Semantic HTML5 elements
- ARIA labels where appropriate
- Keyboard navigation support
- Visually-hidden utility class
- Focus states for interactive elements

### Performance Optimizations
- Minimal CSS reset
- Efficient selectors
- CSS animations (GPU-accelerated)
- No external dependencies
- Optimized media queries

## 📱 Pages

### 1. Homepage (index.html)
- Hero section with call-to-action
- Features grid (4 feature cards)
- Services overview (6 services)
- Rooms showcase (3 room types)
- Contact information
- Booking widget (sidebar)
- Testimonials (sidebar)
- Opening hours (sidebar)

### 2. Gallery Page (gallery.html)
- Dedicated AI video gallery
- AI tools information banner
- Video showcase (multiple videos)
- AI techniques explanation
- Gallery statistics
- Video metadata (duration, tool used)
- Technique tags

## 🌐 Browser Support

Tested and compatible with:
- Chrome 90+
- Firefox 88+
- Safari 14+
- Edge 90+
- Opera 76+

## ✅ Validation

### W3C HTML5 Validation
URL: http://www.w3.org/QA/Tools/

### W3C CSS3 Validation
URL: http://jigsaw.w3.org/css-validator/

## 🚀 How to Use

1. Open `index.html` in a web browser
2. Navigate through sections using any of the three navigation types
3. View the AI video gallery by clicking on the Gallery link
4. Resize browser window to see responsive behavior

## 📝 Development Notes

### Best Practices Followed
- Semantic HTML structure
- CSS custom properties
- Mobile-first design
- Progressive enhancement
- Accessibility considerations
- Performance optimization
- Clean, maintainable code

### Key Learning Points
- Pure CSS responsive layouts
- Grid vs Flexbox use cases
- CSS animations and transitions
- Responsive navigation patterns
- Multi-column layouts
- CSS theming with variables

## 📄 License

University course project - Educational use only

## 👨‍💻 Author

University Web Programming Course Project
2024
