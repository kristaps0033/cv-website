# Conversation Notes - CV Website

## Goal
Rebuild a CV website to match a Squarespace-inspired design and keep it easy to continue work across multiple PCs.

## Current Status
- The site was rebuilt from scratch using a new HTML structure and a full CSS system.
- The repository is pushed to GitHub: https://github.com/kristaps0033/cv-website
- Pages updated: index.html, about.html, education.html, contact.html, styles.css.
- Assets and the original Squarespace export are in assets/ and squeree space copy/.

## Recent Fixes
- Removed the "IT & Web" feature card because it claimed experience that is not accurate.
- Changed the "Sazinies ar mani" button on the homepage to link to contact.html.
- Cleaned duplicate header/footer markup that was lingering in education.html.
- Updated CSS layout to keep the footer at the bottom using flex layout on body.

## Known Issues / Verify
- Download CV button: currently points to assets/Kristaps-Kaspars-Tavars-CV.pdf, but the repo has a .docx file. Decide whether to add a PDF or update the link to the .docx file.
- Live Server not working: use a simple local server (see below).
- Check that no duplicate markup remains in education.html (it previously had old content after </html>).

## How to Run Locally
Option 1: Open index.html directly in a browser.

Option 2: Python server (recommended):
- Run: python -m http.server 5500
- Visit: http://localhost:5500

## Suggested Next Steps
1. Confirm the Download CV file path (PDF vs DOCX).
2. Verify all pages render correctly and the footer/header are single and consistent.
3. Fix any remaining layout or content issues.
4. Publish (GitHub Pages or Cloudflare Pages).

## Key Files
- index.html
- about.html
- education.html
- contact.html
- styles.css
- assets/
- squeree space copy/ (reference only)

## Git Sync (Multiple PCs)
- Pull: git pull origin main
- Push: git add . ; git commit -m "message" ; git push origin main
