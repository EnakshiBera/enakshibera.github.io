# Academic Website Template for Economics PhD Students

A clean, minimal personal academic website built with plain HTML and CSS —
no frameworks, no build tools, no backend. Designed to look professional
for the economics job market.

**Live example:** [enakshibera.github.io](https://enakshibera.github.io)

---

## What this template gives you

- A homepage with photo and bio
- A research page with expandable paper entries
- A teaching page with course listings
- A data page (optional)
- A CV download link
- Clean serif typography (EB Garamond) used widely on econ academic sites
- Navigation with your name on the left, links on the right
- Works on mobile

---

## Who this is for

PhD students in economics (or adjacent fields) who want a clean,
professional website for the job market without learning a web framework.
You only need to edit HTML and CSS — no programming knowledge required.

---

## File structure

```
your-repo/
├── index.html          ← Homepage (edit this first)
├── research.html       ← Research page
├── teaching.html       ← Teaching page
├── data.html           ← Data page (optional, delete if not needed)
├── style.css           ← All styling — fonts, colors, layout
├── YOUR_CV.pdf         ← Your CV (upload to root folder)
├── headshot.jpg        ← Your photo (upload to root folder)
└── syllabus_*.pdf      ← Any syllabi (optional)
```

---

## How to set it up (step by step)

### Step 1 — Create a GitHub Pages repo

1. Go to [github.com](https://github.com) and sign in
2. Click **New repository**
3. Name it exactly: `yourusername.github.io`
   (replace `yourusername` with your actual GitHub username)
4. Set it to **Public**
5. Click **Create repository**

Your site will be live at `https://yourusername.github.io`

---

### Step 2 — Upload the files

1. Go to your repo homepage
2. Click **Add file → Upload files**
3. Upload all files at once: all `.html` files, `style.css`, your CV PDF, your photo
4. Scroll down → click **Commit changes**

Wait 1–2 minutes → visit your site.

---

### Step 3 — Edit your homepage

Open `index.html` and find these parts to change:

```html
<!-- Your name in the nav -->
<a href="index.html" class="nav-name">Your Name Here</a>

<!-- Your photo — make sure the filename matches what you uploaded -->
<img src="headshot.jpg" alt="Your Name">

<!-- Your bio -->
<p>
  I am a [year]-year PhD student in Economics at [University].
  My research interests lie in [your fields].
</p>

<!-- Your email -->
<p>Email: <a href="mailto:you@university.edu">you@university.edu</a></p>

<!-- Your social links -->
<a href="https://twitter.com/YOUR_HANDLE" target="_blank">Twitter</a>
<a href="https://linkedin.com/in/YOUR_HANDLE" target="_blank">LinkedIn</a>

<!-- Your CV filename -->
<a href="YOUR_CV.pdf" target="_blank">CV</a>
```

---

### Step 4 — Edit your research page

Open `research.html`. Each paper uses this block — copy and paste it for each paper:

```html
<div class="accordion-item">
  <div class="accordion-header" onclick="toggle(this)">
    <div class="accordion-title">
      Your Paper Title Here
      <span class="paper-tag">&nbsp;(Working Paper)</span>
      <span class="paper-conf">Conference Name 2026</span>
    </div>
    <span class="accordion-arrow">&#8964;</span>
  </div>
  <div class="accordion-body">
    One paragraph description of your paper.
    <br>
    <a href="link-to-your-draft.pdf" target="_blank">Draft (PDF)</a>
  </div>
</div>
```

**Paper status options** — change the text inside `paper-tag`:
- `(Working Paper)`
- `(Work in Progress)`
- `(Job Market Paper)`
- `(Published)` — add journal name in `paper-conf`

---

### Step 5 — Edit your teaching page

Open `teaching.html`. Each course uses this block:

```html
<div class="teach-entry">
  <div><strong>ECON 101, Course Name</strong></div>
  <div class="teach-entry-right">Fall 2024, Spring 2025</div>
</div>
<div class="teach-sub">
  Brief description. &ensp;
  <a href="syllabus.pdf" target="_blank">Syllabus (PDF)</a>
</div>
```

---

### Step 6 — Update the nav on every page

**Important:** adding a new page does NOT automatically add it to the menu.
You must update the `<nav>` block in **every** HTML file manually.

The nav block looks like this — add or remove lines as needed:

```html
<nav>
  <a href="index.html" class="nav-name">Your Name</a>
  <div class="nav-links">
    <a href="index.html">Home</a>
    <span class="dot">&middot;</span>
    <a href="research.html">Research</a>
    <span class="dot">&middot;</span>
    <a href="teaching.html">Teaching</a>
    <span class="dot">&middot;</span>
    <a href="data.html">Data</a>
    <span class="dot">&middot;</span>
    <a href="YOUR_CV.pdf" target="_blank">CV</a>
  </div>
</nav>
```

Add `class="active"` to the link for the current page so it appears bold:
```html
<a href="research.html" class="active">Research</a>
```

---

### Step 7 — Customize colors and fonts

Open `style.css`. At the very top you'll find:

```css
:root {
  --accent: #3a5a7c;   /* navy blue — links, titles, rule line */
  --muted: #5a5a5a;    /* grey — subtitles, dates, descriptions */
  --border: #d8d8d8;   /* light grey lines */
}
```

Change `--accent` to any color you like. For example:
- `#8b0000` — dark red
- `#2e4a1e` — forest green
- `#1a1a1a` — plain black (most minimal)

To change the photo size, find `.home-photo img` and change the width:
```css
.home-photo img {
  width: 350px !important;   /* change this number */
}
```

---

## Common problems and fixes

| Problem | Fix |
|---|---|
| I edited a file but the site didn't change | You forgot to click **Commit changes** |
| My photo is huge / full screen | Your Jekyll theme is overriding the CSS — see below |
| New page doesn't appear in the menu | Update the `<nav>` block in every HTML file |
| CV link doesn't work | Check the filename matches exactly — case sensitive |
| Site looks unstyled | Make sure `style.css` is in the same folder as your HTML files |

### Fixing Jekyll theme conflicts

If your site looks wrong (photo too big, wrong fonts, extra headers),
your repo may have a Jekyll theme active. Fix it:

1. Find `_config.yml` in your repo
2. Open it and delete any line that says `theme:` or `remote_theme:`
3. Or replace the contents with just: `theme:`
4. Commit the change

---

## Deploying changes

Every change requires a **commit** to go live:

1. Open the file on GitHub → click the pencil ✏️ icon
2. Make your edits
3. Scroll down → click **Commit changes** → click the green button
4. Wait 1–2 minutes
5. Hard refresh your browser: **Ctrl+Shift+R** (Windows) or **Cmd+Shift+R** (Mac)

---

## Credits

Template designed for economics PhD students going on the job market.
Inspired by clean academic websites including those of PhD students at
UVa, IU Bloomington, Purdue, and other economics departments.

Font: [EB Garamond](https://fonts.google.com/specimen/EB+Garamond) via Google Fonts.

---

## License

Free to use and adapt for your own academic website.
No attribution required — though a link back is appreciated!
