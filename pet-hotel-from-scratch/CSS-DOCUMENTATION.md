# Pet Hotel CSS Documentation (From Scratch)

This document explains how the CSS works for each section of the Pet Hotel website. The stylesheet is built from scratch without any CSS framework.

---

## Table of Contents
1. [CSS Foundation](#css-foundation)
2. [Header Container](#header-container)
3. [Horizontal Text Navigation](#horizontal-text-navigation)
4. [Horizontal Graphic Navigation](#horizontal-graphic-navigation)
5. [3-Column Layout System](#3-column-layout-system)
6. [Sidebar Left - Vertical Navigation](#sidebar-left---vertical-navigation)
7. [Main Content Area](#main-content-area)
8. [Sidebar Right](#sidebar-right)
9. [Services Section](#services-section)
10. [Rooms Section](#rooms-section)
11. [Gallery Section](#gallery-section)
12. [Contact Section](#contact-section)
13. [Footer](#footer)
14. [Responsive Breakpoints](#responsive-breakpoints)
15. [Animations](#animations)

---

## CSS Foundation

### CSS Reset
```css
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}
```
**What it does:**
- `margin: 0` and `padding: 0` - Removes default browser spacing from all elements
- `box-sizing: border-box` - Makes padding and border included in element's total width/height (not added to it)

### CSS Custom Properties (Variables)
```css
:root {
    --primary-color: #4a7c59;
    --secondary-color: #8fbc8f;
    --accent-color: #f4a460;
    --dark-color: #2c3e50;
    --light-color: #f8f9fa;
    --text-color: #333;
    --white: #fff;
    --shadow: 0 2px 10px rgba(0, 0, 0, 0.1);
    --transition: all 0.3s ease;
}
```
**What it does:**
- `:root` - Defines variables at the document root (available everywhere)
- `--variable-name` - CSS custom property syntax
- Used via `var(--variable-name)` throughout the stylesheet
- Makes theme changes easy (change once, updates everywhere)

### Base Styles
```css
html {
    font-size: 16px;
    scroll-behavior: smooth;
}

body {
    font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
    line-height: 1.6;
    color: var(--text-color);
    background-color: var(--light-color);
}
```
**What it does:**
- `font-size: 16px` - Base font size for rem calculations
- `scroll-behavior: smooth` - Enables smooth scrolling for anchor links
- `line-height: 1.6` - Spacing between lines (1.6x font size)
- `font-family` - Font stack with fallbacks

---

## Header Container

```css
.header-container {
    display: flex;
    justify-content: space-between;
    align-items: center;
    flex-wrap: wrap;
    padding: 1.5rem 2rem;
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    color: var(--white);
}
```

**Flexbox Properties:**
| Property | Value | Effect |
|----------|-------|--------|
| `display: flex` | - | Enables flexbox layout |
| `justify-content: space-between` | - | Pushes items to opposite ends |
| `align-items: center` | - | Vertically centers items |
| `flex-wrap: wrap` | - | Allows items to wrap on small screens |

**Visual Properties:**
- `linear-gradient(135deg, ...)` - Diagonal gradient from top-left to bottom-right
- `padding: 1.5rem 2rem` - 1.5rem top/bottom, 2rem left/right

### Logo Styles
```css
.logo h1 {
    font-size: 2.5rem;
    font-weight: 700;
    text-transform: uppercase;
    letter-spacing: 2px;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.2);
}
```
- `letter-spacing: 2px` - Adds space between letters
- `text-shadow: 2px 2px 4px rgba(...)` - Offset X, Offset Y, Blur, Color

---

## Horizontal Text Navigation

```css
.nav-horizontal-text {
    background-color: var(--dark-color);
    padding: 0;
    position: sticky;
    top: 0;
    z-index: 100;
}
```

**Sticky Navigation:**
- `position: sticky` - Sticks to viewport when scrolling past it
- `top: 0` - Sticks to the top edge
- `z-index: 100` - Ensures nav stays above other content

### Navigation Links with Underline Effect
```css
.nav-horizontal-text a::after {
    content: '';
    position: absolute;
    bottom: 0;
    left: 50%;
    width: 0;
    height: 3px;
    background-color: var(--accent-color);
    transition: var(--transition);
    transform: translateX(-50%);
}

.nav-horizontal-text a:hover::after {
    width: 80%;
}
```
**How the underline animation works:**
1. `::after` pseudo-element creates an invisible line (width: 0)
2. `left: 50%` + `transform: translateX(-50%)` centers it
3. On hover, `width: 80%` makes the line appear
4. `transition` animates the width change smoothly

---

## Horizontal Graphic Navigation

```css
.nav-horizontal-graphic {
    display: flex;
    justify-content: center;
    flex-wrap: wrap;
    gap: 1rem;
    padding: 1.5rem;
    background-color: var(--light-color);
    border-bottom: 2px solid var(--secondary-color);
}

.nav-graphic-item {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding: 1rem 1.5rem;
    text-decoration: none;
    border-radius: 10px;
    transition: var(--transition);
    box-shadow: var(--shadow);
}

.nav-graphic-item:hover {
    background-color: var(--primary-color);
    color: var(--white);
    transform: translateY(-5px);
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
}
```

**Key Properties:**
- `gap: 1rem` - Spacing between flex items (better than margins)
- `flex-direction: column` - Stacks icon above text
- `transform: translateY(-5px)` - Lifts item up on hover
- `border-radius: 10px` - Rounded corners

---

## 3-Column Layout System

```css
.content-container {
    display: grid;
    grid-template-columns: 1fr;
    gap: 2rem;
    padding: 2rem;
}
```

**Default (Mobile):** Single column (`1fr`)

**At 992px and above:**
```css
@media (min-width: 992px) and (max-width: 1199.98px) {
    .content-container {
        grid-template-columns: 200px 1fr 280px;
    }
}
```

**Grid Column Values by Breakpoint:**
| Breakpoint | Left Sidebar | Main Content | Right Sidebar |
|------------|--------------|--------------|---------------|
| < 992px | Hidden | 1fr (100%) | Full width |
| 992-1199px | 200px | 1fr (flexible) | 280px |
| 1200-1399px | 220px | 1fr (flexible) | 300px |
| 1400px+ | 250px | 1fr (flexible) | 320px |

**`1fr` explanation:** Takes up remaining space after fixed-width columns

---

## Sidebar Left - Vertical Navigation

```css
.nav-vertical a {
    display: block;
    padding: 0.75rem 1rem;
    color: var(--text-color);
    text-decoration: none;
    border-left: 3px solid transparent;
    transition: var(--transition);
    background-color: var(--white);
    border-radius: 0 5px 5px 0;
}

.nav-vertical a:hover,
.nav-vertical a.active {
    border-left-color: var(--primary-color);
    background-color: var(--secondary-color);
    padding-left: 1.5rem;
}
```

**Hover Effect:**
1. `border-left: 3px solid transparent` - Invisible border (prevents layout shift)
2. On hover, border becomes visible (`border-left-color`)
3. `padding-left` increases, pushing text right
4. All changes animate via `transition`

---

## Main Content Area

### Hero Section
```css
.hero {
    text-align: center;
    padding: 3rem 2rem;
    background: linear-gradient(rgba(74, 124, 89, 0.9), rgba(143, 188, 143, 0.9)),
                url('images/hero-bg.jpg') center/cover no-repeat;
    color: var(--white);
    border-radius: 10px;
    margin-bottom: 2rem;
}
```

**Background layering:**
- First layer: Semi-transparent gradient (for color overlay)
- Second layer: Background image
- `center/cover` - Shorthand for `background-position: center` and `background-size: cover`

### Feature Grid
```css
.feature-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1.5rem;
}
```

**`repeat(auto-fit, minmax(200px, 1fr))`:**
- `auto-fit` - Creates as many columns as will fit
- `minmax(200px, 1fr)` - Each column minimum 200px, maximum 1fr
- Result: Automatically responsive grid!

### Feature Card Hover
```css
.feature-card {
    transition: var(--transition);
    border: 2px solid transparent;
}

.feature-card:hover {
    border-color: var(--primary-color);
    transform: translateY(-10px);
    box-shadow: var(--shadow);
}
```

---

## Sidebar Right

```css
.sidebar-right {
    display: flex;
    flex-direction: column;
    gap: 1.5rem;
}
```

**Vertical stacking with gaps between sections**

### Form Inputs
```css
.form-group input:focus,
.form-group select:focus {
    outline: none;
    border-color: var(--primary-color);
    box-shadow: 0 0 5px rgba(74, 124, 89, 0.3);
}
```
- `outline: none` - Removes default browser focus outline
- Custom focus styling with border color change and glow effect

---

## Services Section

```css
.service-card::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 4px;
    background: linear-gradient(90deg, var(--primary-color), var(--secondary-color));
}
```

**Top border gradient effect:**
- `::before` pseudo-element creates a decorative top bar
- `position: absolute` positions it relative to the card (which has `position: relative`)
- Gradient runs left to right (90deg)

### Service Features List
```css
.service-features li::before {
    content: '✓';
    position: absolute;
    left: 0;
    color: var(--primary-color);
    font-weight: bold;
}
```
- Custom checkmark bullet using `::before` pseudo-element
- `content: '✓'` inserts the checkmark character

---

## Rooms Section

```css
.room-card {
    background: var(--white);
    border-radius: 15px;
    overflow: hidden;
    box-shadow: var(--shadow);
    transition: var(--transition);
    position: relative;
}

.room-card:hover {
    transform: translateY(-10px);
    box-shadow: 0 15px 40px rgba(0, 0, 0, 0.15);
}
```

### Room Badge Positioning
```css
.room-badge {
    position: absolute;
    top: 1rem;
    right: 1rem;
    background: var(--primary-color);
    color: var(--white);
    padding: 0.4rem 1rem;
    border-radius: 20px;
    font-size: 0.8rem;
    z-index: 10;
}
```
- `position: absolute` relative to `.room-card`
- `z-index: 10` ensures badge stays above image

---

## Gallery Section

### Video Placeholder Gradients
```css
.video-placeholder.featured-bg {
    background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
}

.video-placeholder.tour-bg {
    background: linear-gradient(135deg, #f093fb 0%, #f5576c 100%);
}
```
Each video has a unique gradient background for visual variety.

### Featured Video Card (Spans Full Width)
```css
.video-card.featured {
    grid-column: 1 / -1;
    display: grid;
    grid-template-columns: 1fr 1fr;
}
```
- `grid-column: 1 / -1` - Spans from first to last column
- Inner grid splits into two equal columns

### AI Technique Tags
```css
.technique-tag {
    display: inline-block;
    padding: 0.25rem 0.75rem;
    background-color: var(--light-color);
    color: var(--primary-color);
    font-size: 0.75rem;
    border-radius: 15px;
    border: 1px solid var(--secondary-color);
    transition: var(--transition);
}

.technique-tag:hover {
    background-color: var(--primary-color);
    color: var(--white);
}
```

---

## Contact Section

### Contact Info Grid
```css
.contact-info-grid {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1.5rem;
}
```

### Contact Form Row
```css
.form-row {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 1rem;
}

.form-group.full-width {
    grid-column: 1 / -1;
}
```
- Two-column form layout that stacks on mobile
- `.full-width` makes textarea span all columns

### Submit Button Gradient
```css
.btn-submit {
    background: linear-gradient(135deg, var(--primary-color), var(--secondary-color));
    color: var(--white);
    border: none;
    border-radius: 5px;
    cursor: pointer;
    transition: var(--transition);
}

.btn-submit:hover {
    transform: translateY(-2px);
    box-shadow: 0 5px 15px rgba(74, 124, 89, 0.3);
}
```

---

## Footer

```css
.footer-content {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr));
    gap: 2rem;
}
```

### Social Links
```css
.social-links a {
    padding: 0.5rem 1rem;
    background-color: rgba(255, 255, 255, 0.1);
    border-radius: 5px;
    transition: var(--transition);
}

.social-links a:hover {
    background-color: var(--accent-color);
    color: var(--dark-color);
}
```

---

## Responsive Breakpoints

The stylesheet uses Bootstrap's standard breakpoints:

| Breakpoint | Prefix | Range |
|------------|--------|-------|
| Extra small | - | < 576px |
| Small | sm | 576px - 767.98px |
| Medium | md | 768px - 991.98px |
| Large | lg | 992px - 1199.98px |
| Extra large | xl | 1200px - 1399.98px |
| XXL | xxl | >= 1400px |

### Mobile Adjustments (< 576px)
```css
@media (max-width: 575.98px) {
    html { font-size: 14px; }
    .header-container { flex-direction: column; }
    .nav-horizontal-text ul { flex-direction: column; }
    .sidebar-left { display: none; }
}
```

### Tablet Adjustments (768px - 991.98px)
```css
@media (min-width: 768px) and (max-width: 991.98px) {
    .sidebar-right {
        flex-direction: row;
        flex-wrap: wrap;
    }
    .sidebar-right section {
        flex: 1 1 calc(50% - 0.75rem);
    }
}
```
- Sidebar sections display side-by-side
- `flex: 1 1 calc(50% - 0.75rem)` = grow, shrink, basis (50% minus gap)

---

## Animations

### Fade In Down
```css
@keyframes fadeInDown {
    from {
        opacity: 0;
        transform: translateY(-30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
```
Element starts invisible and 30px above, then fades in and moves down.

### Fade In Up
```css
@keyframes fadeInUp {
    from {
        opacity: 0;
        transform: translateY(30px);
    }
    to {
        opacity: 1;
        transform: translateY(0);
    }
}
```
Element starts invisible and 30px below, then fades in and moves up.

### Usage
```css
.hero h2 {
    animation: fadeInDown 1s ease;
}

.hero-text {
    animation: fadeInUp 1s ease 0.3s both;
}
```
- `1s` - Duration
- `ease` - Timing function (slow start/end, fast middle)
- `0.3s` - Delay before starting
- `both` - Applies styles from keyframes before and after animation

---

## Print Styles

```css
@media print {
    .nav-horizontal-text,
    .nav-horizontal-graphic,
    .sidebar-left,
    .sidebar-right,
    .footer-container {
        display: none;
    }
}
```
Hides navigation and sidebars when printing for cleaner output.

---

## Utility Classes

### Visually Hidden (Accessibility)
```css
.visually-hidden {
    position: absolute;
    width: 1px;
    height: 1px;
    padding: 0;
    margin: -1px;
    overflow: hidden;
    clip: rect(0, 0, 0, 0);
    white-space: nowrap;
    border: 0;
    visibility: hidden;
}
```
Hides content visually but keeps it accessible to screen readers.

### Clearfix
```css
.clearfix::after {
    content: '';
    display: table;
    clear: both;
}
```
Clears floated elements (legacy technique, mostly replaced by flexbox/grid).
