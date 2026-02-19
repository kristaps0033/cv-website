# CV Website Project

**Purpose:** Professional online presence & job hunting tool. Modern, responsive static site with live form backend.

**Current Status (2026-02-19):** ✅ **COMPLETE** — Design, content, responsive layout, images, form backend live.

**Completed (Urgency %, Progress +%)**
- ✅ Design + CSS (100%, +100%)
- ✅ Deploy to Cloudflare Pages (100%, +100%)
- ✅ Form backend live on server (100%, +100%) — Node.js/Express + SQLite, Docker auto-restart, email notifications working.
- ✅ Content accuracy (100%, +100%) — Real education, experience, skills. Ready for job hunting.
- ✅ Mobile responsiveness (100%, +100%) — Images stack below text on mobile, technical skills definition box, navigation responsive.
- ✅ Images + grid layouts (100%, +100%) — About/Education pages with professional image placement.

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

**Deployment (2026-02-19)**
- **Frontend:** GitHub → Cloudflare Pages auto-sync. Live: https://cv.kristapshomelab.com
- **Backend:** Home server Docker container (persistent).\n  - `cv-website-backend` port 3001 (host) → 3000 (container).\n  - Exposed via Cloudflare Tunnel: form submissions → email to tavarskristaps@gmail.com ✅.\n- **Dev:** localhost:5500 (frontend), localhost:3001 (backend).

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
