# Bussar

A responsive, single-page landing site for the fictional digital services agency **Bussar**, built with Angular, TypeScript, HTML and CSS.

The page features a warm orange-themed design: a minimal white header with navigation, a two-column hero section with a 3D character illustration, and a "Why Choose Us" section with three feature cards layered above a wide orange gradient band. Everything is static and frontend-only.

## Tech stack

- Angular 21 (standalone components, no Router)
- TypeScript
- Plain CSS (component styles + global reset)
- Google Fonts (Inter)
- No backend, database, forms, authentication or third-party UI libraries

## Getting started

Requirements: Node.js 20.19+, 22.12+ or 24+ and npm.

```bash
npm install
npm start
```

`npm start` is an alias for `ng serve`. Open `http://localhost:4200/` in a browser.

You can also run the Angular CLI directly:

```bash
npx ng serve
```

### Production build

```bash
npm run build
```

The optimized output is written to `dist/agency-age/browser/`.

### Unit tests

```bash
npm test -- --watch=false
```

## Project structure

```text
public/
  favicon.svg
  fonts/plus-jakarta-sans.woff2
  images/hero-character.jpg
src/
  app/
    app.ts          # Landing-page standalone component
    app.html        # Semantic page template
    app.css         # Page-specific styles and responsive rules
    app.spec.ts
  index.html
  main.ts
  styles.css        # Global reset, typeface and base defaults
```

Angular 21 serves files from `public/` at the application root, so the hero image is referenced as `images/hero-character.jpg`.

## Design notes

- **Color palette:** Primary orange (#FF9F43), secondary yellow (#FFC45E), near-black text, medium gray body text, white backgrounds, and subtle blue/purple/coral icon accents.
- **Header:** Sticky white header with the Bussar logo, navigation links (Home, Course, Pricing, About Us), and an outlined orange "Sign Up" button. The active Home link has an orange dot indicator.
- **Hero section:** Two-column layout with a bold headline ("Digital Services With Excellent Quality"), an orange highlight accent on "Excellent", two CTA buttons (Get Started, Try Free), and service labels with circular orange icons.
- **Hero illustration:** A 3D character sitting on cloud shapes, placed inside a soft off-white background shape.
- **Why Choose Us:** Two-column intro (heading + description) followed by three feature cards (Transparent Process, Fast & Efficient Delivery, Innovative Thinking) with colored icon badges.
- **Orange band:** A wide yellow-orange gradient band sits behind the bottom portion of the feature cards.
- **Responsive breakpoints:**
  - Desktop: two-column hero, three feature cards in one row.
  - Tablet (≤ 900px): stacked, centered hero and single-column cards.
  - Mobile (≤ 640px): compact header, stacked hero, single-column cards.
- Visible keyboard focus, meaningful image alt text and reduced-motion support are included.
- Colors are defined in `src/styles.css`; page layout and breakpoints live in `src/app/app.css`.

There is no application state, data fetching or navigation beyond in-page section anchors.
