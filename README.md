# Hakkyun Kim — Personal Website

Clean, minimal academic portfolio site. Built with plain HTML/CSS/JS. No frameworks, no build step.

## File Structure

```
hakkyun-site/
├── index.html          ← Homepage
├── css/
│   └── style.css       ← All styles + dark/light mode tokens
├── js/
│   └── theme.js        ← Theme toggle + active nav link logic
├── pages/
│   ├── about.html
│   ├── research.html
│   ├── projects.html
│   ├── cv.html
│   └── hobbies.html
├── files/
│   └── hakkyun_kim_cv.pdf   ← Add your CV PDF here
└── img/
    └── photo.jpg            ← Add your headshot here
```

## Deploying to GitHub Pages

1. Create a new GitHub repo (e.g. `hakkyun-kim.github.io` or just `portfolio`)
2. Push all files:
   ```bash
   git init
   git add .
   git commit -m "initial site"
   git remote add origin https://github.com/YOUR_USERNAME/REPO_NAME.git
   git push -u origin main
   ```
3. In repo Settings → Pages → set source to `main` branch, root `/`
4. Your site goes live at `https://YOUR_USERNAME.github.io/REPO_NAME`

## Connecting Your Custom Domain

1. In your domain registrar (GoDaddy, Namecheap, etc.), add these DNS records:
   ```
   A     @    185.199.108.153
   A     @    185.199.109.153
   A     @    185.199.110.153
   A     @    185.199.111.153
   CNAME www  YOUR_USERNAME.github.io
   ```
2. In GitHub repo Settings → Pages → Custom domain → enter your domain
3. Check "Enforce HTTPS" once DNS propagates (can take up to 24 hrs)

## Customizing Content

### Things to update before going live:
- [ ] Replace `you@email.com` in every footer and about.html
- [ ] Replace LinkedIn and GitHub URLs in every footer
- [ ] Add your headshot to `img/photo.jpg` and update about.html avatar
- [ ] Add your CV PDF to `files/hakkyun_kim_cv.pdf`
- [ ] Fill in real project/research descriptions where placeholders exist
- [ ] Update the hero tagline on index.html if desired

### Adding a new project (projects.html):
Copy the comment template block and fill it in.

### Dark/light mode:
Handled automatically by `js/theme.js` using `localStorage`. The toggle button is in every page's `<nav>`.
