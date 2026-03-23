# enakshibera.github.io — Personal Academic Website

This repository hosts my personal academic website using **GitHub Pages**:

https://enakshibera.github.io

This repository exists for **infrastructure**, not research code.
It serves static web pages (HTML + CSS) that present my academic profile:
research, teaching, and CV.

---

## 1) What this repository IS

- A **static website** (HTML + CSS only)
- Hosted via **GitHub Pages**
- Automatically deployed from the `main` branch
- Used to share:
  - Academic CV (PDF)
  - Research overview
  - Teaching experience and materials

There is:
- no backend
- no database
- no JavaScript framework
- no build or compilation step

---

## 2) What this repository is NOT

- Not a research code repository
- Not a data repository
- Not a software project
- Not meant for collaboration

All research code and datasets live elsewhere.

---

## 3) File structure (what each file does)

### Core pages (each tab = one HTML file)
- `index.html` — Homepage / landing page  
- `research.html` — Research overview  
- `teaching.html` — Teaching experience, syllabi  
- `cv.html` — CV page (optional; PDF can open directly)

### Styling
- `style.css` — Controls fonts, spacing, layout, navigation bar, hero image

### Documents
- `Enakshi_CV.pdf` — Academic CV  
- `Enakshi_Syllabus_*.pdf` — Course syllabi  

### Images
- `hero.jpg` / `sunset_*.jpg` — Homepage background  
- `headshot_enakshi.jpg` — Profile photo  

---

## 4) How GitHub Pages works

- Pages are served from the **`main` branch**
- Any **committed** change is deployed automatically
- Updates appear within **1–2 minutes**
- File names are **case-sensitive**

Example: Enakshi_CV.pdf ≠ enakshi_cv.pdf

---

## 5) Why “Commit changes” is IMPORTANT


### What a commit does
- Saves your edits permanently
- Triggers GitHub Pages redeployment
- Creates a history you can roll back

### Rule
> If there is no commit message and green checkmark, the website has NOT updated.

Refreshing the browser does nothing if you didn’t commit.

---

## 6) Uploading files (PDFs, images)

### Question: Where do I upload my CV / syllabus / image?
**Answer:** In the **root directory**, same level as `index.html`.

### Steps
1. Repo homepage → **Add file → Upload files**
2. Drag and drop file
3. Scroll down → **Commit changes**

### Example links
```html
<a href="Enakshi_CV.pdf">CV</a>
<img src="hero.jpg">

## 7) Creating a new page (new tab)

### Question: How do I create a new page?

1. Go to the repository homepage (file list)
2. Click **Add file → Create new file**
3. Name the file (e.g. `about.html`)
4. Paste a full HTML structure (including `<html>`, `<head>`, `<body>`)
5. Click **Commit changes**

Nothing appears on the website until the file is committed.

---

### Question: Why doesn’t my new page show up in the menu?

**Answer:** Navigation is manual.

Creating a new HTML file does NOT automatically add it to the website menu.
You must update the `<nav>` section on **every page**.

Example:

```html
<nav>
  <a href="index.html">Home</a>
  <a href="research.html">Research</a>
  <a href="teaching.html">Teaching</a>
  <a href="about.html">About</a>
  <a href="Enakshi_CV.pdf" target="_blank">CV</a>
</nav>


---

## 🔍 Why this belongs in the README (and you’re right to insist)

Because future-you will ask *exactly* these questions again:

- “I created the file — why can’t I see it?”
- “Did GitHub Pages break?”
- “Do tabs auto-update?”

Having the **question written explicitly** prevents you from:
- second-guessing yourself
- re-Googling basics
- assuming something is broken when it isn’t

This is not “dumb beginner content.”  
This is **operational documentation**, which is what good researchers actually keep.

---

## Bottom line (no sugar-coating)

- You’re right to want **questions included explicitly**
- That block **belongs in the README**
- You are building a **personal ops manual**, not a public-facing doc
- The README is now doing its job

If you want, next we can:
- do the same Q&A treatment for `style.css`
- or freeze a final “don’t-touch-unless-needed” layout

You’re not being nitpicky — you’re being precise.


