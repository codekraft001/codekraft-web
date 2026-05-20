# CODEKRAFT — Futuristic Digital Innovation

A visually striking, modern agency website for **CODEKRAFT**, a digital innovation firm specializing in high-performance software engineering, web platforms, mobile applications, and cutting-edge digital ecosystems.

---

## Core Purpose

CODEKRAFT is a full-service digital innovation agency headquartered in Accra and Kumasi, Ghana. The website serves as a premium digital storefront — communicating the firm's capabilities, portfolio, and value proposition to prospective clients. It positions CODEKRAFT as a forward-thinking engineering partner that delivers scalable, future-proof digital products across **50+ completed projects** spanning **10+ industry verticals**.

The site's primary goal is to:
- **Showcase technical breadth** across web, mobile, AI, and infrastructure domains.
- **Build trust** through social proof (stats, testimonials, featured projects).
- **Drive conversions** via a prominent contact form and consultation booking CTA.
- **Demonstrate craftsmanship** by embodying the same design and engineering quality CODEKRAFT delivers to its clients.

---

## Visual Style

The design language is a deliberate fusion of **deep space minimalism** and **electric futurism**, built around a carefully curated palette:

| Variable | Value | Role |
|---|---|---|
| Dark Background | `#050816` | Primary canvas / void tone |
| Card Surface | `rgba(255,255,255,0.03)` | Glassmorphism base |
| Primary Blue | `#2F80FF` | Accent, CTA gradients, borders |
| Secondary/Deep Blue | `#0057D9` | Gradient anchor, highlights |
| Gold | `#FFC531` | Statistics, premium emphasis |
| Text Primary | `#FFFFFF` | Headings, labels |
| Text Secondary | `#B5B5C3` | Body copy, muted content |
| Glass Border | `rgba(255,255,255,0.10)` | Card edge definition |

**Key visual characteristics:**

- **Dark, immersive base** — a void-like deep navy (`#050816`) creates depth and lets luminous elements command attention.
- **Glassmorphism** — semi-transparent cards use `backdrop-filter: blur()` with a fine white border to create a layered, translucent depth effect.
- **Electric blue dominance** — a saturated blue (`#2F80FF`) is the singular action colour, used consistently for icons, gradient buttons, glowing borders, scrollbars, and accent text.
- **Gold emphasis** — reserved almost exclusively for the statistics section to signal authority and premium positioning.
- **Gradient primitives** — blue-to-blue gradients power buttons and section transitions; radial gradients darken section boundaries for organic separation.
- **Generous surface separation** — large border-radius values (~24–28px), wide padding, and padding-only spacing remove hard edges throughout.
- **Typography tension** — headings use the geometric, bold *Space Grotesk* (700 weight) while body copy uses *Inter* (300–500), creating a clear hierarchy between display and prose.

---

## Design Principles

### 1. Intentional Minimalism
Every section serves a purpose. There are no decorative elements or "for show" components — the animated 3D backgrounds, stat counters, and scroll-based reveals all reinforce the brand message.

### 2. Depth Through Layering
Rather than flat colour fills, visual depth is created by stacking translucent surfaces (glass cards) over glowing accent borders and subtle background gradients. This evokes a sense of the UI floating in digital space.

### 3. Motion as Information
Animations are geist and purposeful, not gratuitous:
- **AOS (Animate On Scroll)** drives fade, zoom, and flip transitions as sections enter the viewport — signalling the passage of the user's attention.
- **Stat counters** animate from zero to their targets only when scrolled into view, giving numbers credibility and energy.
- **3D hero scene** — a slowly rotating torus knot surrounded by an ambient 1200-particle star field communicates motion, scale, and technical sophistication before the user has read a single word.
- **Cursor glow** — a small radial light follows the pointer with `mix-blend-mode: screen`, making the cursor feel alive and connected to the interactive surface.
- **Hover lifts** — service and project cards rise on hover (`translateY(-10px)`), reinforcing the three-tiered layering model.

### 4. Consistent Micro-Interactions
Every button, card, and icon responds to a hover state with a transform, glow, or colour shift — building muscle memory and perceived responsiveness across the entire experience.

### 5. Accessibility & Readability
- Body text adheres to 1.5rem+ sizes with generous line-height embeds.
- Secondary text uses a muted colour (`#B5B5C3`) at full weight contrast against the dark base.
- Navigation uses a fixed, glass-blurred navbar that always remains accessible.
- Touch targets (buttons, nav links) are sized for both mouse and finger interfaces.

### 6. Performance-First Assets
- AOS is lightweight (~3 KB gzipped) and loaded asynchronously.
- Three.js is dynamically imported — the 3D hero scene runs at `alpha: true` to avoid unnecessary frame buffering.
- Parallelling libraries: Bootstrap 5 grid, Font Awesome free suite, and Three.js are all pulled from CDN, keeping the repository footprint near-zero.

---

## Key Features

### 🏗️ Page Sections

| Section | Purpose |
|---|---|
| **Hero** | Full-viewport 3D canvas (`<canvas id="hero-canvas">`) with rotating torus knot, particle star field, primary headline, and dual CTA buttons |
| **About** | Brand statement, key achievements badge grid, and live 3D rotating wireframe cube |
| **Services** | Six service cards (Web, Mobile, UI/UX, Backend, AI/ML, DevOps) with AOS staggered entry |
| **Tech Stack** | Floating technology icons (React, Node.js, Python, AWS, MongoDB, Docker) with hover scaling |
| **Projects** | Three featured project cards (Nexus Analytics, MetaSpace XR, SwiftCart) with flip-in animation |
| **Stats / Why Us** | Animated counters (58 projects, 24 technologies, 99% satisfaction, 38 engineers) triggered on scroll |
| **Process** | Linear timeline — Discovery → Planning → Design → Development → Testing → Deployment |
| **Testimonials** | Bootstrap carousel with three client quotes |
| **CTA Banner** | Final conversion push with gradient background ring |
| **Contact** | Split layout — contact details (email, phone, address, socials) + full enquiry form |
| **Footer** | Copyright line + Privacy / Terms links |

### 🎬 Animated 3D Scenes

Two separate Three.js canvases are embedded:

1. **Hero Torus Knot** (`hero-canvas`) — A metallic torus knot (`MeshStandardMaterial`, emissive + directional + point lights) floats against a 1200-point starfield. The knot rotates continuously with three independent angular velocities.
2. **About Section Cube** (`rotatingCubeCanvas`) — A solid translucent cube with an overlaid wireframe `EdgesGeometry`, rendered in 280×200px, rotates independently in the About section.

### 📱 Responsive Design
- Hero typography scales from `display-2` on desktop to `2rem` on mobile via media query.
- Service and project cards flow from a 3-column grid on desktop to 2-column on tablet and 1-column on mobile.
- The fixed navbar collapses into a Bootstrap hamburger toggle on narrow viewports.

### ✉️ Contact Form
Six-field enquiry form: Full Name, Email, Company, Project Type (dropdown), Message, and Submit. Focus styles use `--primary-blue` with a soft box-shadow ring. The submit button uses a gradient fill matching the global palette.

---

## Design Principles Summary

| Principle | Implementation |
|---|---|
| **Intentional Minimalism** | Zero decorative filler; every element serves a conversion or communication purpose |
| **Depth Through Layering** | Glassmorphism cards + gradient backgrounds + glow borders create vertical density hierarchy |
| **Motion as Information** | AOS scroll reveals, stat counters, 3D hero, cursor glow — all reinforce brand qualities |
| **Consistent Micro-Interactions** | Uniform hover transforms, colour shifts, and glow effects on all interactive elements |
| **Accessibility & Readability** | High contrast, large touch targets, persistent fixed nav, body text >1.5rem |
| **Performance-First** | CDN-loaded lightweight libraries; Three.js dynamic import; minimal self-hosted footprint |

---

## Tech Stack

| Layer | Technology |
|---|---|
| **Layout / Grid** | Bootstrap 5.3 |
| **Animations** | AOS (Animate On Scroll) 2.3 |
| **3D Graphics** | Three.js 0.128 |
| **Icons** | Font Awesome 6.0.0-beta3 |
| **Typography** | Google Fonts — Space Grotesk (headings), Inter (body) |
| **Browser Support** | Modern browsers with `backdrop-filter` support |

---

## Project Structure

```
codekraft-web/
├── index.html              # Single self-contained page (HTML + CSS + JS)
├── README.md               # This file
└── assets/
    ├── web_logo.png         # CODEKRAFT brand logo
    ├── favicon-16x16.png    # 16px favicon
    ├── favicon-32x32.png    # 32px favicon
    ├── apple-touch-icon.png # iOS home-screen icon
    └── site.webmanifest    # PWA manifest
```

---

## Getting Started

Because the site is a single static HTML file with all dependencies loaded via CDN, no build step or server is required.

1. Open `index.html` directly in a modern browser — or serve the directory with any static HTTP server:
   ```
   python -m http.server 8000
   # or
   npx serve
   ```
2. Navigate to the local URL to view the site at full fidelity (3D scenes require a secure context for `backdrop-filter` in some browsers; HTTP localhost is sufficient).

---

## Browser Requirements

- Chrome 76+, Firefox 103+, Safari 9+, Edge 79+
- `backdrop-filter` CSS property must be supported (hardware-accelerated GPU) for glassmorphism effects to render correctly — all modern browsers support this.
