# Denzel Lawrence Otieno — Portfolio Website

A modern, responsive portfolio showcasing full-stack development expertise, backend engineering, and featured projects including **Vistara**, a tourist safety and tracking management system.

**Live Site:** [https://denzelotieno.github.io](https://denzel60.github.io)  
**GitHub:** [Denzel60 (D.LaWrenc3)](https://github.com/Denzel60)

---

## 📋 Overview

This is a single-page portfolio website built with **vanilla HTML, CSS, and JavaScript**. It features:

- **Responsive Design** — Optimized for mobile, tablet, and desktop
- **Dark Theme** — Modern dark UI with teal and blue accents
- **Smooth Animations** — Scroll-triggered reveals and micro-interactions
- **Featured Project** — Vistara highlighted as the flagship project
- **Skill Grid** — 9 key technical competencies with descriptions
- **Project Showcase** — 5 completed projects with tech tags
- **Experience Timeline** — Work history at Teach2Give Foundation and The Jitu Foundation
- **Contact Links** — Direct email, phone, GitHub, and location

---

## 🎨 Design & Features

### Visual Highlights
- **Custom Fonts**: Syne (display) + DM Sans (body) + DM Mono (code)
- **Colour Scheme**: Dark background (#0a0f1a) with teal accents (#00c2a8)
- **Grid Background**: Subtle animated grid overlay
- **Floating Badge**: Rotating "3+ Years Experience" badge on hero
- **Hover Effects**: Cards lift on hover with dynamic border colours
- **Scroll Animations**: Elements fade and slide up as you scroll

### Key Sections
1. **Navigation** — Fixed header with smooth scroll links
2. **Hero** — Large introduction with CTA buttons
3. **Skills Grid** — 9-cell grid of technical competencies
4. **Projects** — Featured Vistara project + 4 supporting projects
5. **Experience** — Work experience timeline
6. **Contact** — Email, phone, GitHub, and location

---

## 🚀 Getting Started

### View the Site
Simply open `index.html` in your web browser, or visit the live site:
```
https://denzelotieno.github.io
```

### Local Development
1. Clone or download this repository
2. Open `index.html` in your browser
3. Edit and refresh to see changes in real-time

No build tools, dependencies, or servers required — pure HTML/CSS/JS.

---

## 🛠️ Tech Stack

| Layer | Technology |
|-------|-----------|
| **Frontend** | HTML5, CSS3, Vanilla JavaScript |
| **Fonts** | Google Fonts (Syne, DM Sans, DM Mono) |
| **Animations** | CSS Keyframes + JavaScript Intersection Observer |
| **Hosting** | GitHub Pages |
| **Version Control** | Git / GitHub |

---

## 📝 Customization

### Edit Your Details

**Hero Section** (around line 620):
```html
<h1 class="hero-name">Denzel<br/><span class="accent">Lawrence.</span></h1>
<p class="hero-title">Full-Stack Developer & Backend Engineering</p>
<p class="hero-desc">Your description here...</p>
```

**Featured Project** (around line 750):
```html
<h3>Vistara – Tourist Safety & Tracking</h3>
<p>Project description...</p>
<div class="tags">
  <span class="tag">Technology</span>
  <!-- Add more tags -->
</div>
```

**Skills** (around line 680):
```html
<div class="skill-cell">
  <div class="skill-cell-icon">☕</div>
  <h3>Your Skill</h3>
  <p>Description of your skill...</p>
</div>
```

**Contact Links** (around line 900):
```html
<a href="mailto:your-email@example.com" class="contact-link">
  <div class="contact-link-icon">✉️</div>
  <div class="contact-link-text">
    <span>Email</span>
    <strong>your-email@example.com</strong>
  </div>
</a>
```

### Customize Colours

Edit the CSS variables at the top of the `<style>` section:
```css
:root {
  --bg: #0a0f1a;           /* Main background */
  --accent: #00c2a8;       /* Primary accent (teal) */
  --accent2: #0077ff;      /* Secondary accent (blue) */
  --accent3: #ff6b35;      /* Tertiary accent (orange) */
  --text: #e8edf5;         /* Main text colour */
  --muted: #7a8aaa;        /* Muted text colour */
}
```

### Add or Remove Projects

**Add a new project card:**
```html
<div class="project-card reveal">
  <p class="project-num">Project — 06</p>
  <h3>Your Project Title</h3>
  <p>Brief project description...</p>
  <div class="tags">
    <span class="tag">Tech 1</span>
    <span class="tag">Tech 2</span>
  </div>
</div>
```

---

## 📱 Responsive Design

The site is fully responsive across:
- **Desktop** (1200px+) — Full layout with 2-column project grid
- **Tablet** (768px–1199px) — Adjusted spacing and single-column projects
- **Mobile** (< 768px) — Stacked layout, hidden navigation, no floating badge

Breakpoint:
```css
@media (max-width: 768px) {
  /* Mobile-optimized styles */
}
```

---

## 🎬 Animations

### CSS Animations
- **fadeUp** — Elements fade in and slide up on page load
- **fadeIn** — Simple opacity fade
- **spin** — Rotating badge animation
- **barGrow** — Bar chart animation on scroll

### JavaScript Interactions
- **Scroll Reveal** — Elements animate into view using Intersection Observer
- **Bar Animation Trigger** — Chart bars animate when section comes into view
- **Smooth Scrolling** — Navigation links scroll smoothly to sections

---

## 🌐 Hosting on GitHub Pages

1. **Create a repository** named `[username].github.io`
2. **Upload `index.html`** to the root
3. **Wait 2–3 minutes** for the site to go live
4. **Access it at:** `https://[username].github.io`

To update:
- Edit the file locally
- Commit and push to GitHub
- Changes appear live within seconds

---

## 📊 File Structure

```
.
├── index.html          # Main portfolio file (HTML + CSS + JS)
├── README.md          # This file
└── assets/            # (Optional) For future images/icons
```

The entire portfolio is a **single HTML file** for simplicity and easy deployment.

---

## ✨ Features Breakdown

### Scroll Animations
Elements fade in as you scroll past them using the Intersection Observer API:
```javascript
const reveals = document.querySelectorAll('.reveal');
const observer = new IntersectionObserver((entries) => {
  entries.forEach((entry, i) => {
    if (entry.isIntersecting) {
      setTimeout(() => entry.target.classList.add('visible'), i * 80);
    }
  });
}, { threshold: 0.1 });
```

### Floating Badge
The "3+ Years Experience" badge rotates on the hero section:
```css
animation: spin 20s linear infinite 1.5s;
```

### Hover Effects
Project cards lift and change border colour on hover:
```css
.project-card:hover {
  transform: translateY(-4px);
  border-color: rgba(0,194,168,0.3);
  box-shadow: 0 16px 48px rgba(0,0,0,0.4);
}
```

---

## 🔧 Browser Support

- **Chrome/Chromium** ✅ Fully supported
- **Firefox** ✅ Fully supported
- **Safari** ✅ Fully supported
- **Edge** ✅ Fully supported
- **IE 11** ❌ Not supported (modern CSS & JS features)

---

## 📧 Contact

- **Email**: [lawrencedenzel60@gmail.com](mailto:lawrencedenzel60@gmail.com)
- **Phone**: +254 112 552 334
- **GitHub**: [Denzel60 (D.LaWrenc3)](https://github.com/Denzel60)
- **Location**: Nairobi, Kenya

---

## 📄 License

This portfolio is open source and available for personal use and modification. Feel free to adapt it for your own needs.

---

## 🙏 Credits

- **Fonts**: [Google Fonts](https://fonts.google.com)
- **Design Inspiration**: Modern dark UI patterns
- **Icons**: Unicode emojis
- **Hosting**: [GitHub Pages](https://pages.github.com)

---

## 🚀 Next Steps

- Deploy to GitHub Pages
- Share the link on LinkedIn, Twitter, and professional profiles
- Update project links to point to GitHub repositories
- Add more projects as you complete them
- Consider adding a blog section for technical articles

---

**Last Updated**: June 2026  
**Portfolio Version**: 1.0  
**Author**: Denzel Lawrence Otieno
