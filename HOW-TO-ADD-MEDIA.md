# How to Add Images & Videos to Your Portfolio Site
## Angelica Del Priore — AngelicaDelPriore.com

---

## YOUR FILE STRUCTURE

When you unzip `portfolio-site.zip`, you get:

```
portfolio-site/
├── index.html          ← your website
└── images/             ← your portfolio images
    ├── bm-packaging.jpg
    ├── bm-products.jpg
    ├── bm-guidelines.jpg
    ├── tf-display.jpg
    ├── tf-products.jpg
    ├── tf-soleil.jpg
    ├── tf-packaging.jpg
    ├── tf-production.jpg
    ├── rf-brand.jpg
    ├── rf-campaign.jpg
    ├── rf-concept.jpg
    ├── zo-peptide.jpg
    ├── zo-campaign.jpg
    ├── zo-content.jpg
    ├── vr-experiential.jpg
    ├── vr-packaging.jpg
    └── vr-display.jpg
```

Upload EVERYTHING inside `portfolio-site/` to your GitHub repository.
Do NOT upload the outer `portfolio-site/` folder itself — just its contents.

Your GitHub repo should look like:
```
your-repo/
├── index.html
└── images/
    ├── bm-packaging.jpg
    ├── ...etc
```

---

## IMAGES — Already Working!

The 17 images are already embedded in the code. They were extracted
from your PDF and optimized for web (72 quality JPEG, 1200px wide).

### To SWAP an image:
1. Name your new image the SAME filename (e.g., `bm-packaging.jpg`)
2. Drop it into the `images/` folder, replacing the old one
3. Done — no code changes needed

### To ADD a new image:
1. Save your image in the `images/` folder (e.g., `images/my-new-photo.jpg`)
2. Open `index.html` in any text editor (TextEdit on Mac, Notepad on Windows)
3. Find the case study section where you want it
4. Add this line where you want the image:

```html
<img src="images/my-new-photo.jpg" alt="Description of image" loading="lazy"/>
```

To make it span the full width (2 columns), add class="span-2":
```html
<img src="images/my-new-photo.jpg" alt="Description" class="span-2" loading="lazy"/>
```

---

## VIDEOS — Three Options

### OPTION A: YouTube or Vimeo (Easiest — Recommended)

Upload your videos to YouTube or Vimeo, then replace the placeholder
code in `index.html`.

**FIND this in the code** (example — bareMinerals Mineralist video):
```html
<div class="video-placeholder">
  <div class="play-icon"></div>
  <div class="video-label">Mineralist Lipstick — Coming Soon</div>
</div>
```

**REPLACE IT with this** (paste your YouTube embed URL):
```html
<iframe
  src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
  style="width:100%;aspect-ratio:16/9;border:none;border-radius:2px"
  allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope"
  allowfullscreen>
</iframe>
```

For Vimeo:
```html
<iframe
  src="https://player.vimeo.com/video/YOUR_VIDEO_ID"
  style="width:100%;aspect-ratio:16/9;border:none;border-radius:2px"
  allow="autoplay; fullscreen"
  allowfullscreen>
</iframe>
```

**How to get the embed URL:**
- YouTube: Go to your video → Share → Embed → copy the `src="..."` URL
- Vimeo: Go to your video → Share → Embed → copy the `src="..."` URL


### OPTION B: Self-Hosted Video File

If you have .mp4 files and want to host them yourself:

1. Create a `videos/` folder next to `index.html`
2. Put your .mp4 files in it
3. Replace the placeholder with:

```html
<video controls style="width:100%;border-radius:2px"  poster="images/my-thumbnail.jpg">
  <source src="videos/my-video.mp4" type="video/mp4">
</video>
```

Note: Video files can be large. GitHub has a 100MB file limit.
For large videos, YouTube/Vimeo is better.


### OPTION C: Google Drive Video Link

If your videos are on Google Drive:

```html
<iframe
  src="https://drive.google.com/file/d/YOUR_FILE_ID/preview"
  style="width:100%;aspect-ratio:16/9;border:none;border-radius:2px"
  allow="autoplay"
  allowfullscreen>
</iframe>
```

---

## VIDEO PLACEHOLDERS — Where They Are in the Code

Here's every video placeholder and what to search for in `index.html`:

| Brand          | Label in Code                              | Search For                    |
|----------------|--------------------------------------------|-------------------------------|
| bareMinerals   | Mineralist Lipstick — Coming Soon          | "Mineralist Lipstick"         |
| bareMinerals   | Bare Your Best Skin — Coming Soon          | "Bare Your Best Skin"         |
| bareMinerals   | POG Store Design — Coming Soon             | "POG Store Design"            |
| Tom Ford       | Tom Ford Brand Video — Coming Soon         | "Tom Ford Brand Video"        |
| Rodan + Fields | Rodan + Fields Brand Video — Coming Soon   | "Rodan + Fields Brand Video"  |
| Rodan + Fields | Best Line Story — Coming Soon              | "Best Line Story"             |
| ZO Skin Health | ZO Peptide Campaign — Coming Soon          | "ZO Peptide Campaign"         |
| ZO Skin Health | ZO Hydro Mist — Coming Soon               | "ZO Hydro Mist"               |

---

## QUICK EDITING TIPS

- Use **TextEdit** (Mac) or **Notepad** (Windows) to edit `index.html`
  - On Mac: Right-click → Open With → TextEdit → Format → Make Plain Text
- Use **Cmd+F** (Mac) or **Ctrl+F** (Windows) to search for text
- After editing, save the file and refresh your browser to preview
- Push changes to GitHub and they go live in ~1 minute

---

## NEED HELP?

Come back to Claude anytime with your video URLs and I can generate
the exact code swaps for you!
