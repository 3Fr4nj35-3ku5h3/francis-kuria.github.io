# Francis Kuria — Portfolio

Live site: https://theepreacher-ai.github.io/francis-kuria.github.io/

This repository contains the source for Francis Kuria’s portfolio website (GitHub Pages). The site showcases projects, case studies, contact information and a downloadable resume.

---

## What this repo contains
- `index.html` — The single-page portfolio (hero, featured projects, focus areas, contact).
- `assets/` — All images, thumbnails, OG image and the resume PDF (e.g. `assets/francis-avatar.jpg`, `assets/Francis_Kuria_CV.pdf`, `assets/og-image.png`, `assets/projects/*`).
- `README.md` — (this file) describes how the site is structured and how to update it.
- Optional: `projects/` — folder for longer case studies or markdown pages (if you add them).

---

## Goals & tone
This portfolio is intended to:
- Present Francis as a cybersecurity-focused IT professional and technical writer.
- Highlight featured projects with concise outcomes and links to code/demo.
- Provide an accessible, fast, and shareable presence (OG metadata + resume download).
- Be easy for you to update from a single HTML file and image assets.

---

## Quick editing guide

1. Edit hero text
   - Open `index.html`
   - Update the name, tagline, and CTAs in the hero section.

2. Replace headshot or resume
   - Drop files into `assets/`:
     - `assets/francis-avatar.jpg` (recommended square crop)
     - `assets/Francis_Kuria_CV.pdf`
   - The page references those paths. If you use different filenames, update the `src`/`href` in `index.html`.

3. Add / update featured projects
   - Add a thumbnail to `assets/projects/` (e.g. `assets/projects/secure-audit-thumb.jpg`).
   - Add or replace a project card in `index.html` inside the Featured Projects grid.
   - Use the Project Card template below.

---

## Project Card template

Copy this HTML into the `index.html` projects grid and replace placeholders:

```html
<article class="card" aria-labelledby="project-secure-audit">
  <img class="project-thumb" src="/assets/projects/secure-audit-thumb.jpg" alt="Screenshot of Secure Audit Toolkit" loading="lazy" width="1200" height="675">
  <h3 id="project-secure-audit">Secure Audit Toolkit</h3>
  <p style="color:var(--muted)">CLI automation for vulnerability discovery and report generation — reduced manual triage time by automating routine scans.</p>
  <div class="project-meta">
    <span class="badge">Bash</span><span class="badge">Python</span>
    <a class="btn btn-ghost" href="https://github.com/theepreacher-ai/secure-audit" target="_blank" rel="noopener">Code</a>
    <a class="btn btn-primary" href="#" target="_blank" rel="noopener">Live</a>
  </div>
</article>
```

Best practice: 1-line summary (problem → solution → outcome). Keep copy short and measurable where possible.

---

## Images & optimization
- Thumbnail recommended size: 1200 × 675 px (16:9) for good social previews.
- Avatar recommended: square crop (≥ 800×800 source; site displays 160×160).
- Provide `.webp` versions where possible and use the `<picture>` element for fallbacks.
- Tools: Squoosh, ImageMagick, or `sharp` for batch optimization.
- Example ImageMagick commands:
  - Create webp: `convert input.jpg -resize 1200x675 -quality 80 assets/projects/slug-thumb.webp`
  - Create jpg: `convert input.jpg -resize 1200x675 -quality 85 assets/projects/slug-thumb.jpg`

---

## Accessibility, SEO, and performance checklist
- Provide meaningful `alt` text for ALL images.
- Ensure color contrast is readable for body text.
- Add `width` and `height` attributes to images to prevent layout shifts.
- Keep `index.html` minimal and client-side only (no heavy libraries).
- Add or update Open Graph meta in `index.html` for social sharing:
  - `og:title`, `og:description`, `og:image`.
- Add JSON-LD Person schema in the head if desired (already present in current `index.html`).

---

## Local preview
You can preview the site locally with a lightweight server.

- Using Python:
  ```bash
  # from repo root
  python -m http.server 8000
  # open http://localhost:8000
  ```

- Or use any static server you prefer (Live Server extension, http-server, etc).

---

## Deploy
- The repo is configured for GitHub Pages and serves from `main` by default.
- To publish updates:
  ```bash
  git add .
  git commit -m "Update portfolio"
  git push origin main
  ```
- GitHub will rebuild the Pages site automatically (usually within a minute).

---

## Adding case studies (optional)
If you want more depth, create pages under `/projects/` (e.g. `projects/secure-audit.md`) using simple markdown. Then link those pages from the project card `Live` or `Read more` button.

Example short case-study structure:
- Problem statement
- Approach (tools, architecture)
- Implementation (code snippets, commands)
- Results & metrics
- Lessons learned (bulleted)

---

## Contributing
If you accept collaboration:
- Fork the repo, make changes on a feature branch, then open a PR.
- PR checklist:
  - New images optimized
  - `alt` text present
  - Mobile/responsive verified
  - No broken links

---

## License
This portfolio repo's source and any included assets you author are under the MIT License by default. If you want a different license add a `LICENSE` file.

---

## Contact
- Email: kuriaf791@gmail.com  
- GitHub: https://github.com/theepreacher-ai  
- Twitter / X: https://twitter.com/insightsphere7

---

