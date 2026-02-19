# CV Website Project Status

**Last Updated:** 2026-02-19

**Phase:** MVP → Content Refinement

**What's Working**
- Homepage: hero section, feature cards, CTA buttons (Sazinies ar mani, Download CV).
- About page: goals, strengths overview.
- Education page: timeline layout (education, work experience, skills).
- Contact page: form html structure + hybrid fallback script (tries tunnel, falls back to Formspree).
- Mobile responsive: 768px and 720px breakpoints defined in CSS.
- Static assets: images in `assets/`, Roboto font via Google Fonts.
- Favicon: SVG in `assets/favicon.svg` (orange accent + dark background).
- 404 page: custom error fallback for Cloudflare Pages.
- Deployment: Cloudflare Pages auto-synced from GitHub main branch.
- Local preview: http://localhost:5500 (frontend), http://localhost:3000 (backend).
- **Form backend (new):** Node.js/Express server at `../cv-website-backend/`.
  - Saves submissions to SQLite DB (local `submissions.db`).
  - Sends email notifications via Nodemailer.
  - Rate-limited (5 submissions per 15 min per IP).
  - Ready to expose via CloudFlare Tunnel.

**What's Not Working / Blocked**
- Contact form submission: endpoint placeholder **`https://api.yourdomain.com/api/submit-form`** (needs tunnel configured).
  - Blocker: requires Cloudflare Tunnel setup on local machine + .env configuration with email credentials.
- Backend: not yet running (requires `npm install` in cv-website-backend + .env setup).
- Content accuracy: Education, experience, and skills text may not match real CV yet.
- Mobile visual polish: nav spacing, contact form layout at smaller widths not finalized.

**Known Quirks / Edge Cases**
- Form shows "insecure" warning if not HTTPS — fixed by switching from `mailto:` to HTTPS endpoint.
- No database or persistence layer yet (awaiting form backend decision).
- Favicon links in all pages; SVG format supported by all modern browsers.
- 404.html courtesy fallback (Cloudflare Pages will use it automatically for 404s).

**Test Coverage**
- Manual: all 4 pages (index, about, education, contact) load on localhost 5500.
- Mobile: breakpoints defined (@media 768px, 720px) but visual QA pending.

**Implementation Notes**
- CSS: Squarespace-inspired full-width sections, centered 1200px max-width containers.
- HTML: semantic markup, proper meta tags (viewport, description, open graph later).
- Responsive: `flex` + `grid` layout, clamp() for fluid font sizing.
- No build step: direct HTML/CSS/JS in repo root (static site).
- Git workflow: main branch → Cloudflare Pages auto-deploy.

**Dependency Map**
- Depends on: GitHub (for Cloudflare Pages sync), Cloudflare (hosting).
- Forms depend on: (decision pending) Formspree OR (CloudFlare Tunnel + local backend on homelab).
- Job hunting use case ties to: homelab ecosystem potentially (can showcase projects via CV site).
