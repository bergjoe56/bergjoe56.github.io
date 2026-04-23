# Joseph Berg — Architecture Portfolio

A minimal static website for Joseph Berg's architecture portfolio, ready to deploy on GitHub Pages.

---

## Folder Structure

```
joseph-berg-portfolio/
├── index.html              ← Homepage (hero with background video)
├── portfolio.html          ← 9-project thumbnail grid
├── about.html              ← About me + PDF links
├── style.css               ← All styles
├── projects/               ← One HTML file per project
│   ├── nexus-forum.html
│   ├── muir-environmental.html
│   ├── cream-city-commons.html
│   ├── obscene-matters.html
│   ├── miscellaneous.html
│   ├── professional.html
│   ├── paris.html
│   ├── amsterdam.html
│   └── british-isles.html
├── images/                 ← Create this folder, add your images here
│   ├── nexus-forum-thumb.jpg
│   ├── muir-thumb.jpg
│   └── ...
└── pdfs/                   ← Create this folder, add your PDFs here
    ├── joseph-berg-portfolio.pdf
    └── joseph-berg-resume.pdf
```

---

## Setup Guide (No Coding Required)

### Step 1 — Create a GitHub account
Go to https://github.com and sign up for a free account.

### Step 2 — Create a new repository
1. Click the green **New** button on your GitHub dashboard.
2. Name it exactly: `yourusername.github.io`  
   (replace "yourusername" with your actual GitHub username)
3. Set it to **Public**.
4. Click **Create repository**.

### Step 3 — Upload your files
1. On your new repository page, click **uploading an existing file**.
2. Drag and drop **all the files and folders** from this portfolio folder.
3. Click **Commit changes**.

### Step 4 — Enable GitHub Pages
1. Go to your repository **Settings** tab.
2. In the left sidebar, click **Pages**.
3. Under "Branch", select **main** and click **Save**.
4. Your site will be live at: `https://yourusername.github.io`

It may take 1–2 minutes to go live the first time.

---

## Adding Your Content

### Background video (homepage)
1. Upload your video to YouTube (set visibility to "Unlisted" if you prefer).
2. Get the video ID from the URL (the part after `?v=`, e.g. `dQw4w9WgXcQ`).
3. Open `index.html` in a text editor and replace the `<video>` tag with:
```html
<iframe id="hero-video"
  src="https://www.youtube.com/embed/YOUR_VIDEO_ID?autoplay=1&mute=1&loop=1&playlist=YOUR_VIDEO_ID&controls=0"
  frameborder="0"
  allow="autoplay; fullscreen"
  allowfullscreen>
</iframe>
```
4. Add this CSS to `style.css` to make the iframe behave like a video:
```css
#hero-video {
  position: absolute;
  inset: 0;
  width: 100%;
  height: 100%;
  border: none;
  opacity: 0.45;
  pointer-events: none;
}
```

### Thumbnail images (portfolio grid)
1. Create a folder called `images/` in your portfolio folder.
2. Add a thumbnail image for each project (JPG or PNG, recommend 800×600px).
3. Open `portfolio.html` and uncomment the `<img>` tag inside each project block, updating the filename.

### Project images
1. Inside `images/`, create a subfolder for each project, e.g. `images/nexus-forum/`.
2. Add your project photos there (JPG or PNG).
3. Open the corresponding file in `projects/` and uncomment the `<img>` tags, updating filenames.
4. Update the caption text below each image.
5. Copy/paste the image blocks to add more images (up to 40 per project).

### About page photo
1. Add your photo to `images/joseph-berg.jpg`.
2. Open `about.html`, find the comment that says "Replace the placeholder" and uncomment the `<img>` tag.
3. Delete the `<div class="about-photo-placeholder">` block.

### About page bio
Open `about.html` and replace the placeholder text inside `.about-bio` with your actual biography.

### PDF files
1. Create a folder called `pdfs/`.
2. Add your files named `joseph-berg-portfolio.pdf` and `joseph-berg-resume.pdf`.
3. The buttons on the About page will automatically link to them.

---

## Fonts Used
- **Cormorant** — headings and project titles (elegant serif)
- **Helvetica Neue** — body text and UI labels

Fonts are loaded from Google Fonts and require an internet connection to display correctly.

---

## Tips
- Keep image files under 2MB each for fast loading. Use https://squoosh.app to compress.
- Recommended thumbnail size: 800 × 600px (4:3 ratio).
- Recommended full project image width: 1600–2400px.
- Total site size should stay under 500MB to keep GitHub Pages happy.
- For videos, always use YouTube embed — never upload video files directly to GitHub.
