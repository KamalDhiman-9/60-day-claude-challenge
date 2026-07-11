# Kamal Dhiman — AI/ML Portfolio Website

A single-file, responsive personal portfolio built with HTML, Tailwind CSS (CDN), and vanilla JavaScript — generated from resume data and tailored for an AI/ML Engineer profile.

---

## 📄 Generated File

- **File:** `kamal-dhiman-portfolio.html`
- **Stack:** HTML5, Tailwind CSS (CDN), Vanilla JS, Google Fonts (Space Grotesk, Inter, JetBrains Mono)
- **Type:** Single-file, no build step required

---

## 🖼️ Screenshots

> Add screenshots here after opening the file locally or visiting the live URL.
> Recommended: hero section (dark + light mode), skills section, projects grid, mobile view.

| Section | Screenshot |
|---|---|
| Hero (Dark) | `![Hero Dark](./screenshots/hero-dark.png)` |
| Hero (Light) | `![Hero Light](./screenshots/hero-light.png)` |
| Skills | `![Skills](./screenshots/skills.png)` |
| Projects | `![Projects](./screenshots/projects.png)` |
| Mobile View | `![Mobile](./screenshots/mobile.png)` |

**How to capture:**
1. Open `kamal-dhiman-portfolio.html` in a browser (or visit the live URL below).
2. Use your browser's screenshot tool, or `Cmd+Shift+4` (Mac) / `Win+Shift+S` (Windows).
3. Save into a `screenshots/` folder next to this file, then update the paths above.

---

## 🌐 Live Portfolio URL

> _Not yet deployed — add your live link here once deployed._

```
https://your-project-name.vercel.app
```
or
```
https://your-project-name.netlify.app
```

**Quickest deploy path (Netlify, drag-and-drop — no CLI needed):**
1. Go to [app.netlify.com/drop](https://app.netlify.com/drop)
2. Drag `kamal-dhiman-portfolio.html` (renamed to `index.html`) into the browser window
3. Netlify gives you a live URL instantly — copy it here

**Vercel (CLI path):**
```bash
npm i -g vercel
cd portfolio-folder
vercel --prod
```

---

## 🔗 GitHub Commit URL

> _Add your commit URL here once pushed._

```
https://github.com/KamalDhiman-9/<repo-name>/commit/<commit-hash>
```

**Steps to get this:**
```bash
mkdir kamal-portfolio && cd kamal-portfolio
# copy kamal-dhiman-portfolio.html into this folder, rename to index.html
git init
git add index.html
git commit -m "Add AI/ML portfolio website"
git branch -M main
git remote add origin https://github.com/KamalDhiman-9/kamal-portfolio.git
git push -u origin main
```
Then grab the commit URL from the GitHub repo's "Commits" tab and paste it above.

---

## 🧠 Key Learnings

- **Resume-to-web pipeline:** Structuring resume content (experience, projects, skills) into clean, reusable sections made it straightforward to generate recruiter-friendly copy directly from ATS-style resume data.
- **Single-file architecture:** Keeping HTML, Tailwind config, and vanilla JS in one file removed any build step — useful for fast iteration and zero-friction deployment on static hosts like Netlify/Vercel.
- **Design restraint:** Rather than defaulting to generic "AI gradient" aesthetics, the site uses one deliberate signature element (an animated neural-network canvas in the hero) and keeps the rest of the UI quiet and disciplined — teal/violet accents on a dark ink palette, restrained motion, and a monospace accent font for a technical feel.
- **Performance-conscious animation:** Scroll reveals and skill-bar fills use `IntersectionObserver` instead of scroll event listeners, and the canvas respects `prefers-reduced-motion` for accessibility.
- **Deployment simplicity:** Static single-file sites deploy in seconds on Netlify/Vercel with zero configuration — no package.json, no build pipeline, just drag-and-drop or a single CLI command.

---

## 📁 Project Structure

```
kamal-portfolio/
├── index.html          # Single-file portfolio (rename from kamal-dhiman-portfolio.html)
├── screenshots/         # Add screenshots here
└── PORTFOLIO_SUBMISSION.md
```
