# Marneh John Luceñara — Portfolio Site

A single-page portfolio site for showcasing EA work, testimonials, and contact info. Deploys free on Vercel in under 2 minutes.

---

## 📁 What's in this folder

```
portfolio/
├── index.html                           ← The entire site (one file)
├── Marneh_John_Lucenara_Resume.pdf      ← Linked from the hero "Download resume" button
├── headshot.jpg                         ← ADD THIS: your professional headshot
└── README.md                            ← This file
```

---

## 🚀 Deploy to Vercel (2 minutes, free)

1. Create a GitHub account if you don't have one (github.com)
2. Create a new repository → call it `portfolio` → drag this entire folder into it
3. Go to **vercel.com** → sign up with GitHub
4. Click **Add New Project** → import your `portfolio` repo
5. Click **Deploy** (no settings needed — Vercel auto-detects a static site)
6. You'll get a URL like `marnehlucenara.vercel.app` — that's your portfolio

To use a custom domain later (e.g., `marnehlucenara.com`):
- Buy the domain on Namecheap or Porkbun (~$10/year)
- In Vercel project settings → Domains → add the domain → follow the DNS instructions

---

## ✏️ Things to customize before launch

### 1. Add your headshot
Drop `headshot.jpg` in this folder. If the file isn't found, the site falls back to a stylized "MJL" monogram — so the site won't break, but a real photo is way more impactful.

Ideal photo specs:
- Portrait orientation (4:5 ratio ideal)
- Warm, natural lighting if possible — matches the site's tone
- Minimum 800×1000 pixels

### 2. Wire up the contact form
The form uses **Formspree** (free, 50 submissions/month):

1. Sign up at **formspree.io**
2. Create a new form → copy your form ID (looks like `xyzabc123`)
3. In `index.html`, find the line:
   ```html
   <form class="contact-form reveal" action="https://formspree.io/f/YOUR_FORMSPREE_ID" method="POST">
   ```
4. Replace `YOUR_FORMSPREE_ID` with your actual ID

Form submissions will be emailed to whatever address you used to sign up for Formspree.

### 3. Add video testimonials (when ready)
Currently the testimonial section has 3 cards with placeholder video frames. When you're ready to add real videos:

**Option A — YouTube (unlisted, easiest):**
Upload the video to YouTube, set to "Unlisted," copy the video ID from the URL.
Then in `index.html`, find each `<div class="video-frame placeholder">` block and replace with:

```html
<div class="video-frame">
  <iframe width="100%" height="100%" style="border-radius: 4px;"
          src="https://www.youtube.com/embed/YOUR_VIDEO_ID"
          frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</div>
```

**Option B — Direct MP4 hosting:**
Upload videos to the same folder as `index.html` and replace the placeholder div with:

```html
<div class="video-frame">
  <video controls width="100%" height="100%" style="border-radius: 4px; object-fit: cover;">
    <source src="abby-testimonial.mp4" type="video/mp4">
  </video>
</div>
```

### 4. Polish the "former Athena manager" testimonial
Right now it says *"Former Athena Manager"* — once you confirm who's appearing in the video, swap that for their actual name and title.

### 5. Review copy
The site currently uses "Dutch global DTC brand (smart wallets and tech accessories)" — this matches the anonymized resume. If/when Olivier gives permission, do a find-and-replace across the whole file:
- `Dutch Global DTC Brand` → `Ekster`
- `Dutch global direct-to-consumer brand` → `Ekster`
- `the CMO` → `Olivier Momma, CMO`
- `a Dutch global direct-to-consumer brand (smart wallets and tech accessories)` → `Ekster`

---

## 🎨 Design notes

- **Fonts:** Fraunces (display serif) + Inter Tight (body) — both free via Google Fonts, pre-loaded
- **Palette:** Cream (#F5EFE3) + terracotta (#B8543A) + dark green (#2D4A3E) + charcoal ink
- **Aesthetic:** "Modern boutique consultancy" — intentionally different from the corporate-navy look of the PDF resume
- **Responsive:** Works from 360px mobile up to 1400px desktop
- **Performance:** Single file, no JS frameworks, loads in under a second

---

## 📎 Where to use your new URL

Once deployed, paste the URL everywhere:
- **LinkedIn profile** → Contact info → Website
- **LinkedIn headline** → "EA to founders · portfolio at marnehlucenara.vercel.app"
- **Email signature**
- **Upwork, Athena, Persona profiles**
- **Cold outreach messages** → replace "resume attached" with "portfolio: [your URL]"

The URL is especially powerful in cold outreach — a polished portfolio signals seriousness in a way a PDF attachment can't.

---

Questions or tweaks? Good luck shipping it.
