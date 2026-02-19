# CV Website Project

**Purpose:** Professional online presence & job hunting tool. Modern, responsive Squarespace-inspired static site showcasing IT/web development skills.

**Current Status:** MVP ready for content refinement and device-specific polish.

**Core TODOs (Urgency %, Progress +%)**
- ✅ Define Squarespace design baseline (100%, +100%)
- ✅ Build responsive HTML/CSS structure (100%, +100%)
- ✅ Deploy to Cloudflare Pages (100%, +100%)
- **Setup form backend** (90%, +80%) — Node.js Express + SQLite local receiver, Cloudflare Tunnel + Formspree fallback.
- **Content accuracy review** (90%, +30%) — fix text descriptions to match real experience.
- **Mobile responsiveness polish** (80%, +25%) — visual consistency across 375px/768px/desktop.

**Non-essentials** (defer until core content/design locked)
- Analytics integration (page views, referral tracking).
- SEO optimization & sitemap.
- Blog/portfolio section (phase 2).
- Dark mode toggle.

**Tech Stack**
- HTML5, CSS3 (Flexbox, Grid, custom properties).
- Static hosting: Cloudflare Pages (auto-deploys from GitHub on push).
- **Form backend:** Node.js/Express + SQLite (local) + Nodemailer (email notifications).
- **Deployment:** CloudFlare Tunnel for backend (subdomain: e.g. api.yourdomain.com) + Formspree fallback.
- Favicon: SVG (orange circle + white center, dark bg).

**Deployment**
- GitHub repos: https://github.com/kristaps0033/cv-website (frontend) + cv-website-backend (backend, local+tunnel).
- Frontend: Cloudflare Pages (auto-synced from `main` branch above).
- Backend: Local machine running `cv-website-backend/server.js` + exposed via CloudFlare Tunnel.
- Live preview (local): http://localhost:5500 (frontend), http://localhost:3000 (backend, dev only).

**Known Issues**
- Form endpoint placeholder (`formspree.io/f/your-id`) — needs real backend.
- Content text inaccurate (updated design hasn't synced with real CV yet).
- Mobile nav spacing to finalize (768px breakpoint).

**Next Actions**
1. Decide: Formspree (50 forms/month free, paid plans) vs CloudFlare Tunnel + local backend (unlimited, full control)?
2. If CloudFlare Tunnel: build minimal Node/Python form receiver, expose via tunnel, test end-to-end.
3. Update form endpoint in `contact.html`.
4. Refactor CV content (education, experience, skills) to match real background.
5. Visual polish on mobile (css adjustments, spacing consistency).
