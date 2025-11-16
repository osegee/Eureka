# Eureka

A small static demo site built with Vite. This repository serves a simple landing page with a hero image, navigation, and product cards.

## Images
All static images live in `public/assets/images/` and are served from the site root by Vite. Reference them from HTML using absolute paths that begin at the web root:

- Example (HTML):
  - `<img src="/assets/images/logo.svg" alt="Logo" />`
  - `<img src="/assets/images/hero.png" alt="Hero image" />`

Notes:
- Files in `public/` are copied to the built site as-is and are available at `/<filename-or-folder>`.
- Use `src/assets/` only when you want Vite to process an image via imports in JS/CSS (hashed filenames, optimizations). For simple HTML references keep images in `public/`.

## Run locally (Windows PowerShell)
1. Install dependencies:

```powershell
npm install
```

2. Start the dev server:

```powershell
npm run dev
```

Open the URL printed by Vite (usually http://localhost:5173).

## Common tips & small issues to check
- Make sure you reference images starting with `/assets/images/` when using them directly in `index.html`. The project already uses these paths.
- Accessibility: add meaningful `alt` text to any non-decorative images. Use `alt=""` for purely decorative images.
- Avoid nesting interactive elements: do not put an `<a>` inside a `<button>`; use one or the other (e.g., `<a class="cta" href="/shop">Shop</a>`).
- DOM/CSS layout notes:
  - To overlay content on the hero image, keep the image container positioned (`.hero_image { position: relative }`) and place overlay content absolutely inside it (`.hero { position: absolute; inset:0; display:flex; align-items:center; justify-content:center }`).
  - If you want the nav centered inside the hero, ensure the `<nav>` is a child of the hero container.

## What I checked
- I scanned the repository for image references and verified the HTML uses `/assets/images/...` paths.
- No other files in `src/` reference images with incorrect paths.

If you want, I can:
- Fix the small HTML issues I noticed (for example `class=".header_container"` includes a leading dot and there are `<a>` elements nested inside `<button>` elements). I can update those and any remaining image references automatically. Tell me if you'd like me to apply those fixes now.
