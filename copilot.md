# Copilot.md - Web Programming Course Project

## Project Overview

This repository contains **two separate responsive single-page websites** created for Web Programming 1 course at Plovdiv University Paisii Hilendarski. The project demonstrates comprehensive understanding of HTML5, CSS3, responsive design principles, and Bootstrap framework through practical implementation.

### Project Structure
```
WebProgrammingWebsites/
├── pet-hotel-from-scratch/     # Pure HTML5/CSS3 single-page website
│   ├── index.html              # (259 lines)
│   ├── css/style.css          # (391 lines)
│   ├── images/
│   ├── README.md
│   └── CSS-DOCUMENTATION.md
├── pet-shop-with-bootstrap/    # Bootstrap 5.3.2 single-page website
│   ├── index.html              # (783 lines)
│   ├── css/custom.css         # (47 lines)
│   ├── images/
│   └── README.md
├── CLAUDE.md                   # AI assistant guidance
├── instructions.txt            # Course requirements (Bulgarian)
├── copilot.md                  # This file
├── index.js                    # Entry point
└── package.json                # Node.js project config
```

---

## Two Website Approach

### 1. Paws & Rest Pet Hotel (From Scratch)
**Path:** `/pet-hotel-from-scratch/`
**Tech Stack:** Pure HTML5 + CSS3 (no frameworks)

#### Key Features:
- ✅ **Semantic HTML5 structure** using `<header>`, `<nav>`, `<article>`, `<aside>`, `<section>`, `<footer>`
- ✅ **Three navigation types:**
  - Horizontal text navigation (sticky)
  - Horizontal secondary navigation (text-based, different styling)
  - Vertical text navigation (in sidebar)
- ✅ **Multi-column responsive layout:**
  - 3+ columns at width > 1200px
  - Left sidebar with vertical navigation
  - Main content area
  - Right sidebar with booking widget
- ✅ **Custom CSS from scratch** (391 lines - essential only)
- ✅ **Responsive breakpoints:** 576px, 768px, 992px, 1200px, 1400px (Bootstrap v5.0+ standard)
- ✅ **Single-page application** with smooth scroll navigation
- ✅ **Gallery section** with Unsplash placeholder images
#### CSS Techniques Demonstrated:
**Positioning & Layout:**
- `display` (flex, grid, block, inline-block)
- `position` (relative, absolute, sticky, fixed)
- `flexbox` (flex-direction, justify-content, align-items, gap)
- `CSS Grid` (grid-template-columns, gap)
- `float` & `clear`
- `z-index`, `overflow`, `visibility`, `opacity`

**Styling:**
- CSS Custom Properties (CSS Variables)
- Background gradients and images
- Box model (margin, padding, border, border-radius)
- Typography (font-family, font-size, font-weight, text-transform, letter-spacing)
- Text effects (text-shadow, line-height)
- Transforms (translateY, scale)
- Transitions and animations (fadeIn, fadeInDown, fadeInUp)
- Hover states and interactive elements

#### File Structure:
```
pet-hotel-from-scratch/
├── index.html              # Main single-page application
├── gallery.html            # Dedicated video gallery page
├── css/
│   ├── style.css          # Main stylesheet (1356 lines)
│   └── gallery.css        # Gallery-specific styles
├── images/                # Image assets
├── README.md              # Project documentation (229 lines)
└── CSS-DOCUMENTATION.md   # Detailed CSS guide (669 lines)
```

---

### 2. Happy Paws Pet Shop (Bootstrap)
**Path:** `/pet-shop-with-bootstrap/`
**Tech Stack:** Bootstrap 5.3.2 + Custom CSS

#### Key Features:
- ✅ **Bootstrap 5.3.2 Framework** via CDN
- ✅ **Bootstrap Icons** library integration (navbar and header only)
- ✅ **Bootstrap Grid System showcase:**
  - 12-column responsive grid layouts
  - Nested grids and complex layouts
  - Grid breakpoint demonstrations
  - Column sizing and responsive behavior
- ✅ **Responsive Bootstrap components:**
  - Navbar (responsive, no icons in links)
  - Card components (products, services, gallery images)
  - Buttons, badges, and forms
  - Utility classes for spacing/colors
- ✅ **Minimal custom CSS** (47 lines - hero gradient and hover effects only)
- ✅ **Mobile-first responsive design**
- ✅ **Single-page application** with scrollspy
- ✅ **Gallery section** with Unsplash placeholder images

#### Bootstrap Components Used:
- **Navigation:** Navbar with collapse, dropdown menus
- **Layout:** Container, row, col system (responsive grid)
- **Content:** Cards, badges, buttons
- **Forms:** Contact forms with Bootstrap styling
- **Utilities:** Spacing (m-*, p-*), colors (bg-*, text-*), display, flexbox utilities
- **JavaScript:** Collapse, dropdown, scrollspy

#### File Structure:
```
pet-shop-with-bootstrap/
├── index.html              # Main single-page application (860 lines)
├── gallery.html            # Dedicated AI video gallery (524 lines)
├── css/
│   ├── custom.css         # Custom Bootstrap enhancements
│   └── gallery.css        # Gallery-specific styles
├── images/                # Image assets
└── README.md              # Project documentation (391 lines)
```

---

## Media Content & Placeholders

Both websites include media galleries with placeholder content from internet sources:

### Content Sources:
- ✅ **Placeholder Images** - From Unsplash, Pexels, or similar free stock photo sites
- ✅ **Placeholder Videos** - Embedded YouTube videos or video placeholders
- ✅ **Icon Sets** - Bootstrap Icons, Font Awesome, or emoji
- ✅ **Lorem Ipsum Text** - For demonstration purposes

### Gallery Implementation:

**Pet Hotel (From Scratch):**
- Gallery page showcasing custom CSS grid layouts
- Responsive image galleries
- CSS-based lightbox effects (optional)
- Hover effects and transitions
- Demonstrates CSS Grid and Flexbox mastery

**Pet Shop (Bootstrap):**
- Bootstrap card-based gallery
- Responsive grid using Bootstrap columns
- Modal components for image viewing (optional)
- Bootstrap carousel for featured content
- Demonstrates Bootstrap grid system proficiency

### Placeholder Resources:

| Resource Type | Recommended Sources |
|---------------|-------------------|
| **Images** | Unsplash.com, Pexels.com, Pixabay.com |
| **Videos** | YouTube embeds, Vimeo embeds |
| **Icons** | Bootstrap Icons, Font Awesome, Heroicons |
| **Text** | Lorem Ipsum, Cupcake Ipsum, Bacon Ipsum |
| **Avatars** | UI Avatars, Pravatar.cc, Avatar Placeholder |

---

## Responsive Design Implementation

### Breakpoints (Bootstrap v5.0+ Standard)

Both websites use consistent responsive breakpoints:

```css
/* Extra small devices (portrait phones) */
@media (max-width: 575.98px) { }

/* Small devices (landscape phones) */
@media (min-width: 576px) and (max-width: 767.98px) { }

/* Medium devices (tablets) */
@media (min-width: 768px) and (max-width: 991.98px) { }

/* Large devices (desktops) */
@media (min-width: 992px) and (max-width: 1199.98px) { }

/* Extra large devices (large desktops) */
@media (min-width: 1200px) and (max-width: 1399.98px) { }

/* Extra extra large devices (larger desktops) */
@media (min-width: 1400px) { }
```

### Layout Approaches Used:

1. **Fluid Layout** - Percentage-based widths that scale
2. **Flexible Grid** - CSS Grid and Flexbox for responsive columns
3. **Mobile-First Approach** - Base styles for mobile, enhanced for larger screens
4. **Responsive Images** - Images scale appropriately to container
5. **Adaptive Typography** - Font sizes adjust based on viewport

### From Scratch Site - Column Layout:

At width > 1200px, the content-container displays **3 columns:**
```
┌─────────────────────────────────────────┐
│           Header Container              │
├─────────────────────────────────────────┤
│     Horizontal Text Navigation          │
├─────────────────────────────────────────┤
│    Horizontal Graphic Navigation        │
├───────────┬───────────────┬─────────────┤
│  Sidebar  │     Main      │   Sidebar   │
│   Left    │   Content     │    Right    │
│ (Vertical │   (Articles)  │  (Booking   │
│   Nav)    │               │   Widget)   │
│           │               │             │
├───────────┴───────────────┴─────────────┤
│          Footer Container               │
└─────────────────────────────────────────┘
```

---

## Course Requirements Compliance

### ✅ HTML5 Semantic Structure
- `<header>` - Site header with logo and contact info
- `<nav>` - Multiple navigation sections
- `<article>` - Main content sections
- `<aside>` - Sidebars with supplementary content
- `<section>` - Subsections within articles
- `<footer>` - Site footer with links and copyright

### ✅ Navigation Types (From Scratch Site)
1. **Horizontal Text Navigation** - Traditional menu bar with text links
2. **Horizontal Graphic Navigation** - Icon-based navigation with emoji/graphics
3. **Vertical Text Navigation** - Sidebar menu with hierarchical structure

### ✅ Multi-Column Layout
- **Width > 1200px:** 3+ columns in content-container
- One column contains vertical text navigation
- Responsive collapse to single column on mobile

### ✅ Responsive Design
- Breakpoints: 576px, 768px, 992px, 1200px, 1400px
- Mobile-first approach (Bootstrap site)
- Fluid/flexible layout techniques
- Media queries for all breakpoints

### ✅ CSS Properties Demonstrated
**Positioning:** display, visibility, position, float, clear, z-index, flex, grid, opacity, overflow
**Styling:** background, box model, color, fonts, text, links, lists, graphics, transforms, transitions, animations

### ✅ Bootstrap Grid System (Bootstrap Site)
- 12-column grid layout system
- Responsive breakpoints (xs, sm, md, lg, xl, xxl)
- Column sizing and ordering
- Nested grids
- Row and column utilities
- Gap/gutter customization

### ✅ W3C Validation
- HTML5 validation: http://validator.w3.org/
- CSS3 validation: http://jigsaw.w3.org/css-validator/
- Target: Minimal errors and warnings

---

## Development Guidelines for AI Assistants

### When Working with This Project:

#### 1. File Organization
- **Two separate projects** - Don't mix pet-hotel and pet-shop files
- Keep CSS in respective `css/` folders
- Maintain semantic HTML5 structure
- Follow existing naming conventions

#### 2. Pet Hotel (From Scratch) Constraints
- **NO frameworks or libraries** - Pure HTML5/CSS3 only
- **NO Bootstrap classes** - Write all CSS from scratch
- **NO JavaScript libraries** - Vanilla JS only if needed
- Use semantic HTML5 elements
- Follow CSS custom properties pattern (`:root` variables)
- Maintain existing responsive breakpoints

#### 3. Pet Shop (Bootstrap) Guidelines
- **Use Bootstrap 5.3.2** - Via CDN link
- **Use Bootstrap Icons** - For consistent icon style
- **Extend with custom CSS** - Don't override Bootstrap unnecessarily
- Use Bootstrap grid system (container, row, col-*)
- Use Bootstrap utility classes where appropriate
- Follow Bootstrap component patterns

#### 4. Responsive Design Rules
- **Always test at all breakpoints:** 576px, 768px, 992px, 1200px, 1400px
- **Mobile-first approach** for Bootstrap site
- **Desktop-first approach** for from-scratch site (acceptable)
- Ensure 3-column layout appears at 1200px+ (from-scratch site)
- Test navigation collapse on mobile

#### 5. Media Content Integration
- Gallery sections use placeholder images from free sources
- Image optimization for web (appropriate sizes)
- Responsive images with srcset (optional enhancement)
- Maintain consistent card/gallery styling
- Credit image sources where appropriate (Unsplash, Pexels, etc.)

#### 6. Code Quality Standards
- **Semantic HTML5** - Use appropriate tags
- **Valid HTML5/CSS3** - Target W3C validation
- **Consistent indentation** - 4 spaces preferred
- **Meaningful class names** - Follow BEM or semantic naming
- **Comments for complex sections** - Especially in CSS
- **Accessible markup** - ARIA labels where needed

#### 7. CSS Best Practices
**From Scratch Site:**
- Use CSS custom properties (variables) in `:root`
- Group related styles together
- Comment major sections
- Use flexbox and grid for layouts
- Implement smooth transitions
- Add hover states for interactive elements

**Bootstrap Site:**
- Custom styles in `custom.css`
- Don't override Bootstrap core unnecessarily
- Use Bootstrap utilities first, custom CSS second
- Follow Bootstrap naming conventions
- Extend Bootstrap themes properly

#### 8. Common Tasks

**Adding a New Section (From Scratch):**
```html
<article id="new-section" class="page-section">
    <section class="section-header">
        <h2>Section Title</h2>
        <p class="section-subtitle">Description</p>
    </section>
    <section class="section-content">
        <!-- Content here -->
    </section>
</article>
```

**Adding a New Section (Bootstrap):**
```html
<section id="new-section" class="py-5">
    <div class="container">
        <div class="row">
            <div class="col-12 text-center mb-4">
                <h2 class="fw-bold">Section Title</h2>
                <p class="lead text-muted">Description</p>
            </div>
        </div>
        <div class="row">
            <!-- Content here -->
        </div>
    </div>
</section>
```

**Adding AI Video Card (From Scratch):**
```html
<div class="video-card">
    <div class="video-wrapper">
        <iframe src="https://www.youtube.com/embed/VIDEO_ID" 
                frameborder="0" 
                allowfullscreen>
        </iframe>
    </div>
    <div class="video-info">
        <h4>Video Title</h4>
        <p class="video-description">Description text</p>
        <div class="video-meta">
            <span class="duration">⏱ 2:30</span>
            <span class="source-tag">Source: YouTube</span>
        </div>
    </div>
</div>
```

**Adding Image Gallery Card (Bootstrap):**
```html
<div class="col-md-6 col-lg-4 mb-4">
    <div class="card h-100">
        <img src="https://images.unsplash.com/photo-..." 
             class="card-img-top" 
             alt="Image description">
        <div class="card-body">
            <h5 class="card-title">Image Title</h5>
            <p class="card-text">Description of the image content.</p>
            <p class="text-muted small">Photo by Photographer on Unsplash</p>
        </div>
    </div>
</div>
```

---

## Project Documentation

### Existing Documentation Files:

1. **pet-hotel-from-scratch/README.md** (229 lines)
   - Comprehensive project overview
   - Feature list and requirements
   - CSS properties catalog
   - AI content documentation

2. **pet-hotel-from-scratch/CSS-DOCUMENTATION.md** (669 lines)
   - Detailed CSS explanations
   - Section-by-section breakdown
   - Property explanations with examples
   - Responsive design guide

3. **pet-shop-with-bootstrap/README.md** (391 lines)
   - Bootstrap components used
   - Project features
   - Color scheme and design
   - File structure

4. **CLAUDE.md** (50 lines)
   - AI assistant guidance
   - Quick reference for requirements
   - Architecture overview

5. **instructions.txt** (120 lines)
   - Original course requirements (Bulgarian)
   - Grading criteria
   - Submission format
   - Evaluation categories

---

## Running the Project

### Prerequisites
- Modern web browser (Chrome, Firefox, Safari, Edge)
- Local web server (optional but recommended for testing)
- Node.js (for running index.js if needed)

### Option 1: Direct Browser Access
1. Navigate to project directory
2. Open HTML files directly in browser:
   - `pet-hotel-from-scratch/index.html`
   - `pet-shop-with-bootstrap/index.html`
   - Gallery pages: `gallery.html` in each directory

### Option 2: Local Web Server
```bash
# Using Python 3
cd WebProgrammingWebsites
python3 -m http.server 8000

# Visit in browser:
# http://localhost:8000/pet-hotel-from-scratch/
# http://localhost:8000/pet-shop-with-bootstrap/
```

### Option 3: Node.js Entry Point
```bash
npm install
node index.js
```

---

## Validation Checklist

### HTML5 Validation
- [ ] **TODO:** Validate pet-hotel-from-scratch/index.html at http://validator.w3.org/
- [ ] **TODO:** Validate pet-hotel-from-scratch/gallery.html
- [ ] **TODO:** Validate pet-shop-with-bootstrap/index.html
- [ ] **TODO:** Validate pet-shop-with-bootstrap/gallery.html
- [ ] Fix all errors, minimize warnings

### CSS3 Validation
- [ ] **TODO:** Validate pet-hotel-from-scratch/css/style.css at http://jigsaw.w3.org/css-validator/
- [ ] **TODO:** Validate pet-hotel-from-scratch/css/gallery.css
- [ ] **TODO:** Validate pet-shop-with-bootstrap/css/custom.css
- [ ] **TODO:** Validate pet-shop-with-bootstrap/css/gallery.css
- [ ] Fix all errors, minimize warnings

### Responsive Testing
- [ ] Test at 320px (mobile portrait)
- [ ] Test at 576px (mobile landscape)
- [ ] Test at 768px (tablet portrait)
- [ ] Test at 992px (tablet landscape)
- [ ] Test at 1200px (desktop)
- [ ] Test at 1400px+ (large desktop)

### Feature Verification
- [ ] All navigation types work (from-scratch site)
- [ ] 3-column layout appears at 1200px+ (from-scratch site)
- [ ] Bootstrap navbar collapses on mobile (bootstrap site)
- [ ] Video galleries display correctly
- [ ] Forms are properly styled
- [ ] All links work (or properly stubbed)
- [ ] Images load correctly
- [ ] Hover states work on interactive elements

---

## Submission Preparation

### File Naming Format
```
ФакултетенНомер-ИмеФамилия-Специалност-Курс-Форма-КП.rar
Example: 1010XXXXXX-ИванИванов-СИ1-РЕДОВНО-КП.rar
```

### Archive Contents
```
КП-Archive/
├── pet-hotel-from-scratch/
│   ├── index.html
│   ├── gallery.html
│   ├── css/
│   │   ├── style.css
│   │   └── gallery.css
│   ├── images/
│   ├── README.md
│   └── CSS-DOCUMENTATION.md
├── pet-shop-with-bootstrap/
│   ├── index.html
│   ├── gallery.html
│   ├── css/
│   │   ├── custom.css
│   │   └── gallery.css
│   ├── images/
│   └── README.md
└── РЕЗЮМЕ.txt (500-600 characters)
```

### Резюме (Summary) Content
Should include:
- Project title/theme
- Brief description of main pages
- Technologies used
- Good practices applied
- Student name, faculty number, course, specialty, discipline
- ~500-600 characters total
- Print for in-person submission

---

## Grading Criteria (40 points total for project)

### Макродизайн (Macro Design)
- Main container structure
- Header, navigation, content, footer containers
- Column layout and responsiveness
- Semantic HTML5 structure

### Микродизайн (Micro Design)
- Content organization within sections
- Information hierarchy
- User experience considerations

### Стилизиране (Styling)
- CSS properties application
- Visual design quality
- Consistency across pages
- Custom styling vs. framework usage

### Навигация (Navigation)
- Three navigation types (from-scratch)
- Functionality and usability
- Responsive behavior

### Bootstrap Grid System (Bootstrap Site)
- 12-column grid implementation
- Responsive breakpoint usage
- Complex layouts with nested grids
- Proper use of Bootstrap utilities

### Добри практики (Best Practices)
- Code organization
- Semantic markup
- Accessibility considerations
- Performance optimization

### Валидация (Validation)
- W3C HTML5 compliance
- W3C CSS3 compliance
- Minimal errors and warnings

### Иновации (Innovations)
- Techniques not covered in class
- Creative design solutions
- Advanced implementations

---

## Exam Presentation Tips

### Be Prepared to Discuss:

1. **Macro Design:**
   - Explain the 3-column layout (from-scratch)
   - Describe responsive behavior at each breakpoint
   - Justify container structure choices

2. **Micro Design:**
   - Explain content organization decisions
   - Discuss user flow and navigation paths
   - Describe information architecture

3. **Styling Techniques:**
   - Show specific CSS properties used
   - Explain flexbox vs. grid decisions
   - Discuss color scheme and typography choices

4. **Navigation:**
   - Demonstrate three navigation types
   - Explain horizontal vs. vertical navigation uses
   - Show responsive navigation behavior

5. **Bootstrap Grid System:**
   - Demonstrate 12-column grid usage
   - Explain responsive breakpoint implementation
   - Show nested grids and complex layouts
   - Discuss column ordering and utilities

6. **Bootstrap Components:**
   - Explain component choices (navbar, cards, buttons)
   - Show custom CSS enhancements
   - Discuss utility class usage
   - Demonstrate responsive behavior

7. **Best Practices:**
   - Semantic HTML5 element choices
   - CSS organization methodology
   - Responsive design approach
   - Performance considerations

8. **Validation:**
   - Show validation results
   - Explain any warnings/errors
   - Describe how issues were resolved

---

## Key Files Reference

### Entry Points:
- **Pet Hotel:** `/pet-hotel-from-scratch/index.html`
- **Pet Shop:** `/pet-shop-with-bootstrap/index.html`

### Main Stylesheets:
- **Pet Hotel:** `/pet-hotel-from-scratch/css/style.css` (1356 lines)
- **Pet Shop:** `/pet-shop-with-bootstrap/css/custom.css`

### Gallery Pages:
- **Pet Hotel:** `/pet-hotel-from-scratch/gallery.html` (382 lines)
- **Pet Shop:** `/pet-shop-with-bootstrap/gallery.html` (524 lines)

### Documentation:
- **This file:** `/copilot.md`
- **AI Assistant Guide:** `/CLAUDE.md`
- **Course Requirements:** `/instructions.txt` (Bulgarian)
- **Pet Hotel Docs:** `/pet-hotel-from-scratch/README.md` + `CSS-DOCUMENTATION.md`
- **Pet Shop Docs:** `/pet-shop-with-bootstrap/README.md`

---

## Quick Commands

```bash
# Validate HTML5
# Visit: http://validator.w3.org/
# Upload or paste file content

# Validate CSS3
# Visit: http://jigsaw.w3.org/css-validator/
# Upload or paste file content

# Start local server (Python)
cd WebProgrammingWebsites
python3 -m http.server 8000

# Start local server (Node.js - if http-server installed)
npx http-server -p 8000

# Create submission archive
cd /path/to/parent/directory
zip -r ФакултетенНомер-ИмеФамилия-СИ-КП.zip WebProgrammingWebsites/ -x "*.git*" "node_modules/*"
```

---

## Course Context

**Institution:** Plovdiv University "Paisii Hilendarski"
**Course:** Web Programming 1
**Language:** Bulgarian (Course instructions in Bulgarian)
**Format:** Two separate single-page websites required
**Framework Rule:** One "from scratch" (pure HTML/CSS) + One with Bootstrap framework
**Content:** Placeholder content from internet sources (Unsplash, Pexels, YouTube, etc.)
**Focus:** Demonstrating HTML5, CSS3, Bootstrap Grid System, and responsive design principles
**Standard:** Bootstrap v5.0+ breakpoints for consistency

---

## Additional Notes

### Technologies Demonstrated:
- HTML5 (semantic elements, forms, media embeds)
- CSS3 (flexbox, grid, animations, transitions, custom properties)
- Bootstrap 5.3.2 (12-column grid, components, utilities)
- Bootstrap Icons
- Responsive Web Design (mobile-first and desktop-first approaches)
- Single-page application pattern

### Development Approach:
- One-shot AI-prompted code generation
- Focused on showcasing HTML, CSS, and Bootstrap fundamentals
- Placeholder content from free internet sources
- Emphasis on responsive design and grid systems

### Not Included:
- JavaScript interactivity (not required by course)
- Backend functionality
- Database integration
- Form processing
- Real content (using placeholders)

### Future Enhancements (if desired):
- Add smooth scroll behavior with JavaScript
- Implement working forms with validation
- Add shopping cart functionality (pet shop)
- Replace placeholders with custom content
- Add image lightbox/modal for gallery
- Implement lazy loading for images
- Add accessibility improvements (ARIA labels, focus management)

---

## Contact & Submission

**Student:** [YOUR NAME]
**Faculty Number:** [YOUR NUMBER]
**Course:** Web Programming
**Specialty:** [YOUR SPECIALTY]
**Form:** [Regular/Distance]

**Instructor Email:** ...@uni-plovdiv.bg
**Student Email:** ...@uni-plovdiv.bg

**Submission:** 3 days before exam date via university email
**Method:** Shared Google Drive link (recommended) or email attachment

---

## License & Academic Integrity

This project is created for educational purposes as part of a university course assignment. All code is original work except where explicitly noted (Bootstrap framework, Bootstrap Icons). Placeholder media content is sourced from free internet resources (Unsplash, Pexels, YouTube) and is properly attributed.

**Development Note:** This project was generated using AI-assisted one-shot prompting to quickly scaffold the structure and demonstrate HTML5, CSS3, and Bootstrap fundamentals. The student must fully understand and be able to explain all code, design decisions, CSS properties, and Bootstrap components during the exam presentation.

**Important:** Students should review and understand:
- All CSS properties used and their effects
- How the Bootstrap 12-column grid system works
- Responsive breakpoints and media queries
- Semantic HTML5 structure and purpose
- Flexbox vs. Grid layout decisions
- All Bootstrap components and utility classes used

---

*Last Updated: February 8, 2026*
*Project Status: In Development - Validation Pending*
*Development Method: AI-assisted one-shot prompting*

