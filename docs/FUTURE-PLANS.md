# CV Website Future Plans

## Phase 2: Polish & Integration (Parked)
- Analytics: Google Analytics or Plausible (page views, referral sources).
- SEO optimization: proper Open Graph tags, sitemap.xml, robots.txt.
- Dark mode toggle: CSS custom properties ready, just needs UI control.
- Portfolio section: showcase past projects (linked from homelab ecosystem).
- Blog integration: write-ups on tech work, project notes (static or headless CMS).

## Phase 3: Advanced (Parked)
- Email subscription: newsletter signup for project updates.
- Dynamic project showcase: auto-render projects from GitHub API (wot-replay-analyzer, homelab-portal, etc.).
- Admin panel: edit CV, manage inquiries, publish blog posts.
- Multi-language support: Latvian + English toggle already in place conceptually.
- Performance audits: Lighthouse optimization, image lazy loading, critical CSS inlining.

## Integration with Homelab Ecosystem (Future)
- Embed homelab projects on portfolio page (GitHub card + description).
- Link WoT stats dashboard (if Phase 2 of wot-stats-tracker ready).
- Showcase discord-bot commands or homelab-portal features.
- Use cv-website as "public face" for other projects (attracts collaborators, employers).

## Form Backend Scaling (Pending Decision)
**Option A: Formspree (Free Tier)**
- Pros: instant setup, email inbox, no backend needed.
- Cons: 50 forms/month limit, paid plans required for higher volume.
- Fit: good for early job hunting phase; upgrade if volume grows.

**Option B: CloudFlare Tunnel + Local Backend**
- Pros: unlimited submissions, full control, integrates with homelab infra.
- Cons: requires local server uptime, need to build + maintain backend.
- Fit: better long-term, aligns with homelab automation philosophy.

**Option C: Hybrid**
- Run local backend via CloudFlare Tunnel (limit outages).
- Fallback to Formspree if tunnel down (redundancy).
- Fit: production-grade, for long-term public presence.

## Non-Core Parking
- CMS migration: move from static HTML to headless CMS (Strapi, Contentful) — defer until content volume justifies it.
- Mobile app: PWA or native app version — post-job-success phase.
- Multilingual i18n: full Latvian/English/Russian UI — nice-to-have, not blocking job hunting.
