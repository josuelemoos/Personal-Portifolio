# Portfolio Website - Current Specification

## Goal
Maintain a single-page personal portfolio for **Josué Lemos Mesquita**, a Computer Science student and Python back-end developer. The current visual direction follows a compact resume-style reference: centered card, clean typography, profile image at the top, square contact buttons, concise sections, and clear desktop/mobile behavior.

The site must keep working as a static HTML, CSS, and JavaScript project with no build step.

---

## Stack
- Semantic HTML in `index.html`
- Plain CSS in `styles.css`
- Minimal inline JavaScript for theme switching
- Google Fonts: `Inter` and `Roboto Mono`
- Local profile image: `assets/profile-photo.jpg`

---

## Visual Direction

### Style
- Resume-inspired compact portfolio layout.
- On mobile, content stays in a narrow single-column layout similar to the original reference.
- On desktop, the card expands and sections use two columns: section title on the left, content on the right.
- Profile image is square with rounded corners and aligned to the right on larger screens.
- Contact buttons are square and icon-only.
- Minimal decoration, with focus on readability, hierarchy, and spacing.

### Typography
- Name, headings, and labels: `Inter`.
- Body copy and descriptions: `Roboto Mono`.
- Avoid serif fonts in this version because the current direction is more technical and compact.

### Light Palette
```css
Background: #f4f4f2
Paper:      #ffffff
Text:       #111111
Muted:      #555555
Soft:       #f2f2f2
Border:     #dedede
```

### Dark Palette
```css
Background: #111111
Paper:      #191919
Text:       #f2f2f2
Muted:      #b9b9b9
Soft:       #242424
Border:     #303030
```

---

## Site Structure

### Header
- Name: **Josué Lemos Mesquita**
- Role: `Python Back-End Developer`
- Location: `Crateus, CE, Brazil`
- Links:
  - Email: `mailto:josuemesquita29@gmail.com`
  - GitHub: `https://github.com/josuelemoos`
  - LinkedIn: `https://linkedin.com/in/josué-lemos-mesquita-53a97434b`
- Profile image: `assets/profile-photo.jpg`
- Fixed theme toggle button.

### About
Short text about Computer Science, back-end development, distributed systems, API integrations, and experience with Python, FastAPI, Flask, and gRPC.

### Education
- Federal University of Ceara
- Bachelor's Degree in Computer Science - Crateus Campus
- Period: `2023 - 2028`

### Work Experience
- Rascunhos UFC
- Role: Extension Program Fellow
- Period: `2023 - present`
- Short description covering workshops, visual production, and university event presentations.

### Projects
List all projects as compact items with name, GitHub link, description, and stack:
- FastAPI Books
- REST API Python - Drinks
- Hospital Management System
- AutoriaIA
- Media Tracker
- Hackathon FIT 2025

### Skills
Compact grouped text:
- Programming
- Frameworks
- Tools
- Concepts
- AI & Data

### Languages
- Portuguese: Native
- English: Upper-intermediate for technical reading and written communication

### Footer
- `© 2026 Josué Lemos Mesquita`

---

## Responsiveness
- Mobile up to `430px`: layout fills the screen, with no external card shadow.
- Very small screens up to `360px`: profile image moves above the text and item headings become single-column.
- Desktop from `760px`: card max-width is `980px`, sections become two-column, and projects use a two-column grid.
- The theme toggle shows text on desktop and becomes icon-only on mobile to avoid covering content.

---

## Dark Mode
- Initial theme respects `prefers-color-scheme`.
- Manual choice is saved in `localStorage` under the `theme` key.
- The theme is applied with `document.documentElement.dataset.theme`.
- The toggle uses `aria-pressed`, updates its `aria-label`, and changes visible text between `Dark mode` and `Light mode`.

---

## Maintenance Rules
- Keep the project simple, framework-free, and build-free.
- Avoid external JavaScript dependencies.
- Use CSS variables for colors and states.
- Preserve readability on both mobile and desktop.
- External links must use `target="_blank"` and `rel="noreferrer"`.
- Keep the public profile image stripped of EXIF/GPS metadata before committing.
