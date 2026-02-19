# CV Website Project Status

**Last Updated:** 2026-02-19

**Phase:** MVP COMPLETE → CONTENT ACCURACY (CRITICAL FOR EMPLOYMENT)

**Session Status:** Docker backend deployed & tested on home server. Form submissions live. **BLOCKER: CV content is placeholder — must fix before job applications.**

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
- **✅ Form backend LIVE:** Docker container on home server (persistent).
  - Port mapping: 3001 (host) → 3000 (container).
  - Saves submissions to SQLite DB (`submissions.db`).
  - Email notifications to tavarskristaps@gmail.com working ✅.
  - Rate-limited (5 submissions per 15 min per IP).
  - Cloudflare Tunnel routing: cv.kristapshomelab.com/api/* → localhost:3001 (verified working).
CRITICAL BLOCKERS FOR JOB HUNT**
- **CONTENT ACCURACY:** Education, experience, skills are placeholder/inaccurate.\n  - Cannot use current CV for job applications (would be lying to employer).\n  - Fix: Replace all placeholder text with REAL details.\n  - Scope: Edit index.html, about.html, education.html with accurate info.\n- Mobile polish: Secondary priority (nav/form spacing at 768px breakpoint)
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
- Forms: Cloudflare Tunnel + Docker backend on home server + email (working ✅).
- Job hunting use case: CV content must be accurate before applications.
