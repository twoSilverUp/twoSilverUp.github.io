# How to deploy this site on GitHub Pages

## 1. Create the repository
On GitHub, create a new repository named exactly:

```
yourusername.github.io
```

(Replace `yourusername` with your actual GitHub username — it must match exactly, or Pages won't auto-publish.)

## 2. Folder structure
Upload these files keeping this exact structure:

```
yourusername.github.io/
├── index.html
└── assets/
    ├── Eunsang_Lee_CV.pdf      ← already included
    ├── profile.jpg             ← add your own photo here
    └── paper_a.png             ← add a thumbnail for your paper (optional)
```

- `index.html` must sit at the **root** of the repo (not inside a subfolder).
- Everything referenced by `src="assets/..."` inside `index.html` must live in an `assets` folder right next to `index.html`.

## 3. Add your photo
Put a square-ish photo (e.g. 400×400px) at `assets/profile.jpg`. If you want a different filename, update this line in `index.html`:

```html
<img src="assets/profile.jpg" alt="Profile photo of Eunsang Lee">
```

## 4. Add a paper thumbnail (optional)
The Publications section expects a small image at `assets/paper_a.png` (a figure from the paper, or any 1:1 thumbnail). If you don't have one yet, you can either:
- drop in a placeholder image, or
- remove the `<img>` line and change `.pub` grid in the CSS to a single column for that entry.

## 5. Fill in remaining links
In `index.html`, search for and replace:
- `https://github.com/yourgithub` → your real GitHub URL
- `https://linkedin.com/in/yourlinkedin` → your real LinkedIn URL
- Any `#` placeholders under Publications (`Paper` / `Code` / `Project` links)

## 6. Push and check
```bash
git init
git add .
git commit -m "first deploy"
git branch -M main
git remote add origin https://github.com/yourusername/yourusername.github.io.git
git push -u origin main
```

Then go to **Settings → Pages** in the repo to confirm it's building. After a minute or two, your site will be live at:

```
https://yourusername.github.io
```
