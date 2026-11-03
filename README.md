# Binder Medical - Neighborhood Medical Store Website
**Location:** Ludhiana, Punjab, India  
**Project Type:** College Cloud Computing Project (Static Cloud Web Application)

A fast, lightweight, and authentic static frontend website built for a real, single-owner neighborhood pharmacy and medical shop called **"Binder Medical"** located in **Ludhiana, Punjab, India**.

---

## 🎯 Key Project Principles & Rules Followed
1. **100% Authentic (No Fake Media):** No AI-generated images, no stock photos, and no placeholder people. Sections needing real photography display neutral placeholder boxes with target filenames documented in [`MISSING_PHOTOS.md`](MISSING_PHOTOS.md).
2. **Zero Fabricated Facts:** No fake reviews, testimonials, customer counts, or invented license numbers. Items needing confirmation from the real owner are clearly tagged as `[TODO: ...]` and cataloged in [`TODO_INFO.md`](TODO_INFO.md).
3. **Local Community Focus:**
   - Multilingual toggle: **English**, **ਪੰਜਾਬੀ (Punjabi)**, and **हिंदी (Hindi)**.
   - Dynamic real-time **Open Now / Closed** badge based on current Indian Standard Time (IST) and shop hours.
   - Zero-backend **WhatsApp Medicine Availability Flow**: customers can type a medicine name to immediately open WhatsApp with a prefilled inquiry (`wa.me/`).
   - Honest medical disclaimer: *"Please consult a doctor before taking any medicine. Prescription medicines are sold only against a valid prescription."*
   - Embedded Google Map of Ludhiana with a direct "Get Directions" link.
4. **Cloud-Ready Static Architecture:** Pure HTML5, CSS3, and Vanilla JavaScript. Fast, zero build step required, no paid APIs, and deployable to any major cloud provider in under 2 minutes.

---

## 📁 Project Directory Structure

```
cc project/
├── index.html            # Main semantic single-page layout (multilingual, responsive, accessible)
├── 404.html              # Custom, friendly 404 error page with quick contact buttons
├── favicon.svg           # Scalable SVG medical pharmacy cross icon
├── robots.txt            # Search engine crawl rules
├── sitemap.xml           # XML sitemap for SEO
├── netlify.toml          # Netlify cloud hosting config with security & cache headers
├── firebase.json         # Firebase Hosting static deployment configuration
├── MISSING_PHOTOS.md     # Checklist of real photos to be provided by the shop owner
├── TODO_INFO.md          # Checklist of real shop details to be confirmed
├── README.md             # Project documentation and deployment guide
├── css/
│   └── styles.css        # Mobile-first CSS (calm medical green/teal palette, responsive 320px–1440px)
├── js/
│   └── app.js            # Vanilla JS (multilingual engine, live IST calculator, WhatsApp flow, lightbox)
└── assets/
    └── images/           # Storage for real photos (storefront.jpg, owner.jpg, counter.jpg, etc.)
```

---

## 💻 How to Run Locally

Because this is a pure static frontend, you have several quick ways to run it:

### Option A: Direct Browser Opening (No server needed)
Double-click `index.html` in Windows Explorer or your file manager. It will open in Google Chrome, Microsoft Edge, Firefox, or Safari immediately.

### Option B: Using Node.js (Recommended)
Open PowerShell or Terminal in the project root:
```bash
npx serve .
```
Then visit `http://localhost:3000` in your browser.

### Option C: Using Python
```bash
# Python 3
python -m http.server 8080
```
Then open `http://localhost:8080`.

---

## ☁️ Cloud Static Hosting Deployment Guides

This project is optimized for deployment on all major cloud static hosting platforms:

### 1. Netlify (Recommended - Fast & Free)
The repository includes a ready-to-use [`netlify.toml`](netlify.toml) configured with asset caching, security headers, and custom 404 handling.
- **Drag & Drop:**
  1. Go to [app.netlify.com](https://app.netlify.com).
  2. Drag and drop the `cc project` folder into the "Sites" dashboard.
  3. Your site is live immediately on a free `*.netlify.app` subdomain with global CDN and SSL.
- **Via Git CLI:**
  ```bash
  npm install -g netlify-cli
  netlify deploy --prod --dir=.
  ```

### 2. Firebase Hosting (Google Cloud Platform)
The repository includes a preconfigured [`firebase.json`](firebase.json).
```bash
# 1. Install Firebase CLI
npm install -g firebase-tools

# 2. Login & initialize
firebase login
firebase init hosting   # Select existing project; use '.' as public directory

# 3. Deploy
firebase deploy --only hosting
```

### 3. GitHub Pages
1. Push this folder to a GitHub repository (e.g., `github.com/username/binder-medical`).
2. In GitHub repository settings, go to **Pages** > **Build and deployment**.
3. Under **Branch**, select `main` (or `master`) and folder `/ (root)`, then click **Save**.
4. The site is published automatically at `https://<username>.github.io/<repo>/`.

### 4. AWS (S3 Static Website + CloudFront CDN)
1. **Create an S3 Bucket:** e.g., `binder-medical-ludhiana` with Public Read access enabled.
2. **Enable Static Website Hosting:** Set index document to `index.html` and error document to `404.html`.
3. **Upload Files:** Upload all files maintaining directory structure (`css/`, `js/`, `assets/images/`).
4. **CloudFront CDN:** Create a CloudFront distribution pointing to the S3 bucket origin for global HTTPS, low latency, and Edge caching.

---

## 📝 Checklists to Complete Real Store Setup

Before presenting or submitting the project, review the two checklists:
1. **[`MISSING_PHOTOS.md`](MISSING_PHOTOS.md):** Take real photos of the Binder Medical shop in Ludhiana (`storefront.jpg`, `owner.jpg`, `counter.jpg`, `shelves.jpg`, `products.jpg`, `street-view.jpg`) and drop them into `assets/images/`.
2. **[`TODO_INFO.md`](TODO_INFO.md):** Fill in the owner's name, exact Ludhiana street address, PIN code, 10-digit mobile/WhatsApp number, and Drug License number (`DL No.`).
