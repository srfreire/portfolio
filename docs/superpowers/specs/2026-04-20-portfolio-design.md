# Portfolio — Juan Freire Alvarez

## Overview

Single-page portfolio website with narrative scroll (Apple/Inditex-inspired). Clean, spacious, elegant typography, smooth scroll-triggered animations. Hosted on GitHub Pages.

## Sections (scroll order)

### 1. Hero

Full-viewport intro. Name displayed large, tagline "Backend Developer" below. Subtle fade-in animation on load. Minimal — no image, no nav bar. Just text and whitespace.

### 2. About

2-3 short paragraphs telling Juan's story: passion for building backend systems, studying CS at USC, working at OSIX Tech. Key facts woven into narrative (not a bullet list). Appears with fade-up on scroll.

### 3. Projects

Four projects, each as a large block occupying most of the viewport. Revealed sequentially on scroll with staggered fade-up.

Each project card contains:
- Project name (large)
- One-liner description
- 2-3 sentence explanation of what it does and Juan's role
- Tech stack as subtle tags
- Link to repo (if public)

**Projects in order:**

1. **DecisionLab** — Virtual laboratory for simulating human decision-making paradigms with AI agents. Multi-agent system (Architect, Tracker, Analyst, Reporter) built with Python, FastAPI, Claude API, React. TFG at USC.

2. **Ohara** — Online note repository with integrated AI assistant. Users store and query their documents via RAG. Built with NestJS, Node.js, Zod.

3. **Nessie** — AI assistant for querying Google Drive documents. Real-time sync via webhooks, Supabase storage, Node.js + Express backend.

4. **RecDS** — Experimental tourist recommendation engine using vector similarity. API returns restaurant recommendations given a tourist profile and model config. Designed for RAG pipeline integration.

### 4. Contact

Email, LinkedIn, and GitHub displayed as styled links. Centered, minimal. No form.

- Email: juaan.freirea@gmail.com
- LinkedIn: linkedin.com/in/juan-freire-alvarez
- GitHub: github.com/srfreire

## Visual Design

### Aesthetic

Inspired by Inditex and Apple product pages:
- Generous whitespace between sections
- Large typography for headings
- Neutral palette with subtle accent
- Content reveals on scroll
- Parallax-like depth on hero

### Colors

- Background: white (`#FFFFFF`) with warm off-white sections (`#F5F2EF`)
- Text: near-black (`#1A1A1A`)
- Secondary text: medium gray (`#6B7280`)
- Accent: to be defined by chisel design system

### Typography

- Sans-serif (Inter or similar)
- Headings: large, bold, generous letter-spacing
- Body: regular weight, comfortable line-height (1.6-1.7)

### Animations

- Hero: fade-in on load (0.8s ease)
- Sections: fade-up when entering viewport (Framer Motion `whileInView`)
- Project cards: staggered entrance (100ms delay between each)
- No parallax scroll on mobile (performance)

### Responsive

- Desktop-first, adapts to mobile
- Single column on mobile, same scroll narrative
- Reduced animation on `prefers-reduced-motion`

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Framework | React 19 + Vite |
| Styling | Tailwind CSS 4 |
| Animations | Framer Motion |
| Deploy | GitHub Pages (gh-pages) |
| Design System | Chisel (custom tokens) |

## Out of Scope

- Dark mode
- Blog / CMS
- Contact form
- Analytics
- i18n (single language: Spanish or English TBD — likely English for portfolio)
