# Happy Paws Pet Shop - Bootstrap Website

## Project Overview

A modern, responsive single-page pet shop website built using Bootstrap 5.3.2 framework. This project demonstrates professional web development with Bootstrap grid system, components, and minimal custom CSS styling.

## Key Features

- Bootstrap 5.3.2 Framework via CDN
- Bootstrap Icons library integration
- **Bootstrap Grid System showcase** (12-column responsive grid)
- Responsive Bootstrap components (Navbar, Cards, Buttons, Forms)
- Minimal custom CSS (~47 lines)
- Mobile-first responsive design
- **Single-page application** with smooth scroll navigation
- Gallery with placeholder images from Unsplash
- W3C HTML5 compliant

## File Structure

```
pet-shop-with-bootstrap/
├── index.html          # Main single-page application (783 lines)
├── css/
│   └── custom.css     # Minimal custom styles (47 lines)
├── images/            # Image assets folder
└── README.md          # This file
```

## 🎨 Design Features

### Color Scheme (Bootstrap Theme)
- Primary: `#0d6efd` (Bootstrap Blue)
- Secondary: `#6c757d` (Gray)
- Success: `#198754` (Green)
- Warning: `#ffc107` (Yellow)
- Danger: `#dc3545` (Red)
- Info: `#0dcaf0` (Cyan)

### Bootstrap Utilities Used
- **Spacing**: m-*, p-*, g-* (margin, padding, gap)
- **Colors**: bg-*, text-*
- **Display**: d-flex, d-grid, d-none, d-block
- **Position**: position-relative, position-absolute, sticky-top
- **Sizing**: w-*, h-*, mw-*, mh-*
- **Shadows**: shadow-sm, shadow, shadow-lg
- **Borders**: border, rounded-*
- **Typography**: fw-bold, text-center, lead, display-*

### Custom Enhancements
- CSS variables for consistency
- Custom animations (fadeIn, float, pulse)
- Enhanced hover effects
- Gradient backgrounds
- Smooth transitions
- Custom scrollbar styling

## 🛍️ E-Commerce Features

### Product Catalog
- Product categories (Dogs, Cats, Birds, Fish)
- Featured products grid
- Product cards with:
  - Images (placeholders)
  - Ratings (star icons)
  - Pricing (original + discount)
  - Add to cart button
  - Wishlist button
  - Sale badges

### Shopping Features
- Cart icon with notification badge
- Price display with discounts
- Category filtering
- Product search (UI ready)
- Account access button

## 💼 Services Section

### Service Offerings
1. **Grooming** ($35+)
   - Bath & Blow Dry
   - Haircuts & Styling
   - Nail Trimming
   - Ear Cleaning

2. **Vet Clinic** ($50+)
   - Health Check-ups
   - Vaccinations
   - Minor Treatments
   - Pet Consultations

3. **Training Classes** ($75+)
   - Puppy Training
   - Obedience Classes
   - Private Sessions
   - Behavior Correction

### Customer Testimonials
- Star ratings
- Customer photos (avatar placeholders)
- Review text
- Customer names and roles

## 📺 Gallery Page Features

### Layout
- Dedicated gallery page with breadcrumb navigation
- Two-column layout (8 col main + 4 col sidebar on lg+)
- Fully responsive grid system
- Category filtering ready

### Video Presentation
- **Featured Video** - Large hero placement
- **Product Showcase** - 2-column grid
- **Pet Care Tips** - 2-column grid
- **Customer Stories** - 3-column grid

### Video Card Components
- Gradient placeholder backgrounds
- Play icon overlay
- Video metadata (duration, tool used)
- AI technique badges
- Hover effects

### Sidebar Components
1. **AI Tools Used** - List with video counts
2. **AI Techniques** - Detailed explanations
3. **Newsletter CTA** - Subscription widget

### Gallery Statistics
- Total videos count
- Total content duration
- Number of AI tools used

## 🎭 Interactive Features

### Animations
- Fade-in hero section
- Hover lift effects on cards
- Button hover transforms
- Dropdown fade animations
- Float animation on gallery header
- Pulse animation on badges

### User Experience
- Smooth scrolling
- Scroll spy navigation
- Collapsible mobile menu
- Dropdown product categories
- Sticky navigation bar
- Social media links
- Newsletter subscription

## 📱 Pages

### 1. Homepage (index.html)
Single-page application with sections:
- Top bar (contact info, hours)
- Navigation (sticky)
- Hero section
- Features strip
- Shop by Pet categories
- Featured products
- Services
- Testimonials
- AI Video Gallery preview
- Contact section
- Newsletter
- Footer

### 2. Gallery Page (gallery.html)
Dedicated video gallery:
- Header with breadcrumb
- Gallery statistics
- Featured video
- Categorized videos
- Sidebar with AI info
- Full footer

## 🔧 Technical Implementation

### Bootstrap Integration
- CDN-hosted Bootstrap CSS (5.3.2)
- CDN-hosted Bootstrap Icons (1.11.1)
- Bootstrap JavaScript bundle
- Data attributes for interactions
- Bootstrap utility classes

### Custom CSS Architecture
- Extends Bootstrap defaults
- CSS variables for theming
- Component-specific styles
- Responsive overrides
- Animation keyframes
- Print styles

### Accessibility
- ARIA labels on navigation
- Semantic HTML structure
- Keyboard navigation
- Focus states
- Alt text ready for images
- Screen reader support

### Performance
- CDN delivery
- Minimal custom CSS
- Efficient selectors
- No blocking scripts
- Print stylesheet optimization

## 🌐 Browser Support

Modern browsers with Bootstrap 5 support:
- Chrome 60+
- Firefox 60+
- Safari 12+
- Edge 79+
- Opera 47+

## 📋 Bootstrap Classes Reference

### Layout
```
container, row, col-*, col-sm-*, col-md-*, col-lg-*, col-xl-*, col-xxl-*
g-*, gx-*, gy-* (gutters)
```

### Components
```
navbar, navbar-expand-*, nav-link, dropdown
card, card-body, card-header, card-title
btn, btn-primary, btn-outline-*, btn-lg, btn-sm
badge, rounded-pill
form-control, form-label, form-select
```

### Utilities
```
d-flex, d-grid, flex-wrap, justify-content-*, align-items-*
m-*, mt-*, mb-*, mx-*, my-* (margins)
p-*, pt-*, pb-*, px-*, py-* (padding)
text-center, text-white, text-muted
bg-primary, bg-light, bg-dark
shadow-sm, shadow, shadow-lg
position-relative, position-absolute, sticky-top
```

## ✅ Validation

### W3C HTML5 Validation
URL: http://www.w3.org/QA/Tools/

Bootstrap 5.3.2 is W3C compliant

## 🚀 How to Use

1. Open `index.html` for the main e-commerce site
2. Navigate to `gallery.html` for the dedicated video gallery
3. Responsive - resize browser to see breakpoint changes
4. All Bootstrap components are fully functional

## 💡 Development Approach

### Bootstrap Best Practices
- Utilize built-in components
- Extend, don't override
- Mobile-first methodology
- Semantic class naming
- Component reusability
- Utility-first styling

### Custom Enhancements
- CSS variables for brand colors
- Animation enhancements
- Gradient backgrounds
- Custom hover states
- Enhanced visual hierarchy
- Print optimizations

## 📚 Technologies Used

- **HTML5** - Semantic markup
- **CSS3** - Custom styling
- **Bootstrap 5.3.2** - Framework
- **Bootstrap Icons 1.11.1** - Icon library
- **JavaScript** (Bootstrap Bundle) - Interactions

## 🎓 Learning Outcomes

- Bootstrap grid system mastery
- Component customization
- Responsive design patterns
- Utility class efficiency
- Framework integration
- Modern CSS techniques
- E-commerce UI/UX
- AI content integration

## 📝 Notes

### Differences from "From Scratch" Version
- Uses Bootstrap framework
- Faster development time
- Consistent component library
- Built-in responsiveness
- Pre-styled components
- E-commerce focus vs hotel booking

### Future Enhancements
- Add actual video embeds
- Implement shopping cart functionality
- Add product detail pages
- Integrate payment gateway
- Add user authentication
- Implement search functionality

## 📄 License

University course project - Educational use only

## 👨‍💻 Author

University Web Programming Course Project
2024
