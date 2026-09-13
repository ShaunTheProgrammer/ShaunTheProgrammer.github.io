# Academic CV site

A static academic homepage structurally matched to the Minimal Mistakes
layout used by [academicpages.github.io](https://academicpages.github.io) —
same fixed masthead, sticky author sidebar, page grid, font stack, and
heading scale — rebuilt as plain HTML/CSS/JS.

## Structure

```
index.html          Home = CV (education, experience, skills, awards, teaching)
projects.html        Detailed project write-up, incl. the ncRNA-LUAD pipeline
contact.html         Contact details
css/style.css        All styling (accent hexes are CSS variables at the top)
js/main.js           Mobile nav toggle
assets/              Static files (drop your real CV PDF here)
```

## Preview locally

No build step needed — just open `index.html` in a browser, or serve it:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

