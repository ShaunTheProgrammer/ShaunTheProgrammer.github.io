# Academic CV site

A static academic homepage structurally matched to the Minimal Mistakes
layout used by [academicpages.github.io](https://academicpages.github.io) —
same fixed masthead, sticky author sidebar, page grid, font stack, and
heading scale — rebuilt as plain HTML/CSS/JS (no Jekyll/Ruby toolchain
required). The only intentional departure from the reference is color: an
indigo/cyan accent in place of that theme's teal.

No "About" or "Publications" page/section — the sidebar (avatar, name, bio,
links) carries identity on every page, and the CV itself is the home page.

## Structure

```
index.html          Home = CV (education, experience, skills, awards, teaching)
projects.html        Detailed project write-up, incl. the ncRNA-LUAD pipeline
contact.html         Contact details
css/style.css        All styling (accent hexes are CSS variables at the top)
js/main.js           Mobile nav toggle
assets/              Static files (drop your real CV PDF here)
```

## Customize

1. Replace every `[bracketed placeholder]` and "Your Name" / `you@example.edu`
   across the HTML files with your real information. The sidebar markup is
   duplicated on each page (no templating layer) — update all three.
2. Swap the "YN" avatar initials for a real photo if you want one — replace
   the `.author__avatar` div with `<img src="assets/photo.jpg" ...>` and drop
   the image in `assets/`.
3. Replace `assets/cv-placeholder.pdf` with your actual CV PDF (same filename,
   or update the download links).
4. Update the GitHub link in `projects.html` to your real repo URL.
5. Accent colors live as CSS variables at the top of `css/style.css`
   (`--accent`, `--accent-2`, etc.); neutral ink/border values are matched to
   the reference theme and shouldn't need touching.

## Preview locally

No build step needed — just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy to GitHub Pages

```bash
cd cv-website
git init
git add .
git commit -m "Initial academic CV site"
git branch -M main
git remote add origin https://github.com/<your-username>/<your-username>.github.io.git
git push -u origin main
```

Using the `<username>.github.io` repo name publishes it at
`https://<your-username>.github.io` automatically. For a project-named repo
instead, enable Pages in the repo's Settings → Pages and set the source to
the `main` branch.
