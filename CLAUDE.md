# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Project Overview

University course project requiring **two separate websites**:
1. **"From scratch" website** - Built with pure HTML5/CSS3 without frameworks
2. **"Bootstrap" website** - Built using Bootstrap framework (or Bootstrap Studio)

Both sites must include AI-generated content (videos, graphics) in a video gallery page.

## Commands

```bash
# Run the main entry point
node index.js
```

## Architecture Requirements

### From Scratch Website Structure
- Main container wrapping all content
- `header-container` - Header section
- Horizontal text navigation
- Horizontal graphic navigation
- `content-container` - Main content with multiple columns
  - At width > 1200px: minimum 3 columns, one containing vertical text navigation
- `footer-container` - Footer section

### Required HTML5 Semantic Tags
Use `<header>`, `<nav>`, `<article>`, `<aside>`, `<section>`, `<footer>`

### Responsive Design
- Breakpoints: 576px, 768px, 992px, 1200px, 1400px (Bootstrap v5.0+ standard)
- Layout approaches: relative, liquid, elastic, fluid, or flexible

### Required CSS Properties
Positioning/layout: `display`, `visibility`, `position`, `float`, `clear`, `z-index`, `flex`, `grid`, `opacity`, `overflow`

Styling: background, box model, color, fonts, text, links, lists, graphics, transforms, transitions, animations

### AI-Generated Content Requirements
- 3+ video clips (each > 1 minute, with 5+ different style frames)
- At least 3 AI generation processes (text-to-speech, speech-to-text, script-to-video, subtitling, etc.)
- Tools: fliki.ai, kapwing, veed, leonardo.ai, canva, clipchamps, synthesia, etc.
- Content displayed in a dedicated video gallery page

### Validation
HTML5 and CSS3 must validate against W3C standards: http://www.w3.org/QA/Tools/