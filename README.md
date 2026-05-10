# Academic Personal Website

A clean, professional academic personal website inspired by [andrewng.org](https://www.andrewng.org).  
Built with pure HTML, CSS, and vanilla JavaScript — no frameworks, no build tools. Ready for GitHub Pages.

---

## 📁 File Structure

```
academic-website/
├── index.html          ← Home page
├── about.html          ← About Me
├── research.html       ← Research Interests
├── publications.html   ← Publications
├── supervisor.html     ← Supervisors & Mentors
├── gallery.html        ← Gallery
├── blog.html           ← Blog listing
├── blog-post.html      ← Blog post template (duplicate for each post)
├── style.css           ← All shared styles
├── images/             ← Create this folder and put your photos here
│   ├── photo.jpg       ← Your profile photo
│   └── ...
└── cv.pdf              ← Your CV (optional)
```

---

## 🚀 How to Deploy on GitHub Pages

### Step 1 — Create a repository
1. Go to [github.com](https://github.com) and sign in.
2. Click **New repository**.
3. Name it: `your-username.github.io`  
   *(Replace `your-username` with your actual GitHub username — this gives you a free domain like `https://your-username.github.io`)*
4. Set it to **Public**. Click **Create repository**.

### Step 2 — Upload your files
**Option A — GitHub web interface (easiest):**
1. Open your new repository.
2. Click **Add file → Upload files**.
3. Drag and drop ALL the files from this folder.
4. Click **Commit changes**.

**Option B — Git command line:**
```bash
git init
git add .
git commit -m "Initial website commit"
git branch -M main
git remote add origin https://github.com/your-username/your-username.github.io.git
git push -u origin main
```

### Step 3 — Enable GitHub Pages
1. In your repository, go to **Settings → Pages**.
2. Under **Source**, select **Deploy from a branch**.
3. Choose branch: `main`, folder: `/ (root)`.
4. Click **Save**.
5. Wait 1–2 minutes, then visit `https://your-username.github.io`.

---

## ✏️ How to Customize

### Personal details
Search for `[Your Name]`, `[University Name]`, `your@email.com` etc. across all HTML files and replace with your real information.

### Profile photo
1. Add your photo to an `images/` folder.
2. In `index.html`, replace the placeholder div with:
   ```html
   <img src="images/photo.jpg" alt="Your Name" class="hero-photo" />
   ```
3. Do the same in `about.html`.

### Colors
Open `style.css` and edit the CSS variables at the top:
```css
:root {
  --accent: #1a3a5c;       /* Main color — change to your preference */
  --bg: #fafaf8;           /* Page background */
  --text: #1a1a1a;         /* Body text */
}
```

### Adding publications
In `publications.html`, copy a `<li class="pub-item">` block and fill in your paper's details.

### Adding blog posts
1. Duplicate `blog-post.html` and rename it (e.g., `blog-ml-tips.html`).
2. Edit the content inside the new file.
3. In `blog.html`, update the `href` of the relevant post's "Read more →" link to point to your new file.

### Adding gallery photos
In `gallery.html`, replace each `<div class="gallery-item-inner">` with an `<img>` tag:
```html
<div class="gallery-item" ...>
  <img src="images/conf1.jpg" alt="Conference photo" style="width:100%;height:100%;object-fit:cover;" />
  <div class="gallery-caption">Your caption here</div>
</div>
```

---

## 🎨 Design Features
- Clean, minimal aesthetic inspired by andrewng.org
- Responsive — works on mobile, tablet, and desktop
- Sticky navigation with active page highlighting
- Mobile hamburger menu
- Publication filter (Journal / Conference / Preprint)
- Blog category filter
- Gallery with lightbox popup
- Smooth hover animations
- Google Fonts (Lora + DM Sans)

---

## 📬 Contact Form (optional upgrade)
GitHub Pages only hosts static files, so server-side contact forms don't work natively.
Use [Formspree](https://formspree.io) for a free contact form — just replace the action URL:
```html
<form action="https://formspree.io/f/YOUR_FORM_ID" method="POST">
```

---

*Built for GitHub Pages hosting. No dependencies, no build step required.*
