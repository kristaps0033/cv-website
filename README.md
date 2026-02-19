# CV Website - Kristaps Kaspars Tavars

A modern, responsive personal CV website built with HTML5, CSS3, and designed with a clean, professional Squarespace-inspired aesthetic.

## 🔗 Live Demo

Visit the repository: [https://github.com/kristaps0033/cv-website](https://github.com/kristaps0033/cv-website)

## 📋 Features

- **Responsive Design** - Works seamlessly on desktop, tablet, and mobile devices
- **Modern Layout** - Full-width sections with centered content containers
- **Clean Typography** - Roboto font family with optimized spacing and readability
- **Professional Color Scheme** - Orange accent color (hsl(17.82, 100%, 55.1%)) with neutral backgrounds
- **Four Page Structure**:
  - Home - Hero section with CTA buttons and feature highlights
  - About - Personal goals and strengths
  - Education - Timeline of education, work experience, and skills
  - Contact - Contact information and form

## 🛠️ Technologies Used

- HTML5
- CSS3 (Flexbox, Grid, Custom Properties)
- Google Fonts (Roboto)

## 🚀 Getting Started

### Clone the Repository

```bash
git clone https://github.com/kristaps0033/cv-website.git
cd cv-website
```

### View Locally

Simply open `index.html` in your browser, or use a local server:

```bash
# Using Python
python -m http.server 5500

# Using Node.js (http-server)
npx http-server -p 5500
```

Then visit `http://localhost:5500`

## 📁 Project Structure

```
cv-website/
├── index.html          # Homepage
├── about.html          # About page
├── education.html      # Education & experience page
├── contact.html        # Contact page
├── styles.css          # Main stylesheet
├── assets/            # Images and CV file
└── squeree space copy/ # Original Squarespace reference files
```

## 🎨 Design System

- **Font Family**: Roboto (400, 500, 700 weights)
- **Primary Color**: Orange (#FF7538 / hsl(17.82, 100%, 55.1%))
- **Backgrounds**: White (#ffffff), Light Gray (#f9fafb), Dark (#1a1a1a)
- **Max Width**: 1200px (content), 2000px (site)
- **Responsive Breakpoint**: 768px

## 📝 Customization

1. Update personal information in HTML files
2. Replace images in the `assets/` folder
3. Modify colors in `styles.css` CSS custom properties (`:root`)
4. Add your CV file to `assets/` and update the download link

## 🔄 Sync Between Multiple PCs

```bash
# Pull latest changes
git pull origin main

# Make changes and commit
git add .
git commit -m "Your commit message"
git push origin main
```

## 🌐 Deploy to Cloudflare Pages

1. Open Cloudflare Dashboard → Pages → Create a project → Upload assets
2. Select the `cv-website` folder as project root
3. Publish

You can add a custom domain (e.g., `cv.kristapshomelab.com`) via Pages → Custom domains

## 📄 License

This project is open source and available for personal use.

## 👤 Author

**Kristaps Kaspars Tavars**

- GitHub: [@kristaps0033](https://github.com/kristaps0033)

