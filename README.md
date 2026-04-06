# Brand Assets — Logo Library

A self-contained static brand asset page for the Lunar Rails group of companies. All logo files are embedded directly in the page — no server, no CDN, no dependencies.

---

## Deploy to Netlify via GitHub

### 1. Push to GitHub

```bash
# From inside this folder
git init
git add .
git commit -m "Initial commit"

# Create a new repo on github.com, then:
git remote add origin https://github.com/YOUR_ORG/logo-assets.git
git push -u origin main
```

### 2. Connect to Netlify

1. Go to [app.netlify.com](https://app.netlify.com) → **Add new site → Import an existing project**
2. Choose **GitHub** and select your repo
3. Build settings are auto-detected from `netlify.toml` — no changes needed
4. Click **Deploy site**

### 3. Set the site name

1. Netlify Dashboard → **Site configuration → Site details → Change site name**
2. Enter `logo-assets` → the site will be live at **logo-assets.netlify.app**

---

## Update logos

Edit `index.html` directly — all assets are base64-encoded inside the `FILES` object near the bottom of the file. After editing, commit and push; Netlify will redeploy automatically.

---

## Project structure

```
.
├── index.html      # The entire site — self-contained, no build step
├── netlify.toml    # Netlify deploy config + cache/security headers
├── .gitignore
└── README.md
```
