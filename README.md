# Edward Benavidez Portfolio (React + Vite)

Static, free-to-host portfolio. No API keys, no paid services.

## 1. Install tools (once)
Install Node.js LTS from https://nodejs.org (check with `node -v`).

## 2. Run locally
Open a terminal in this folder:
```
npm install
npm run dev
```
Open the address it prints (usually http://localhost:5173). Press Ctrl+C to stop.

## 3. Preview the production build
```
npm run build
npm run preview
```

## 4. Edit your content
Almost everything you will change is in `src/data.js`:
- `CONTACT_EMAIL`: your real email (email buttons and footer link appear only when set)
- `FORM_ENDPOINT`: where the contact form posts (see below)
- `SOCIALS`: real profile URLs
- `PROJECTS`: set `image` (e.g. `/projects/site.png`, file saved in `public/projects/`) and `href` for real work. Placeholders disappear automatically.
- `TOOLS`: adjust wording to match tools you have actually confirmed.
Replace the portrait placeholder in `src/App.jsx` (`<div className="portrait" ...>`) with an `<img>` once you have a photo.

## 5. Connect the contact form
The form validates, but sends nothing until `FORM_ENDPOINT` is set. Free option: create a form at https://formspree.io, copy its endpoint URL (`https://formspree.io/f/xxxx`), paste it into `FORM_ENDPOINT`. Check the provider's current free limits.

## 6. Upload to GitHub
1. Create a free account and a new empty repository at https://github.com/new.
2. In this folder run:
```
git init
git add .
git commit -m "Initial portfolio"
git branch -M main
git remote add origin https://github.com/YOUR-USERNAME/YOUR-REPO.git
git push -u origin main
```
(No Git? Use "uploading an existing file" on the GitHub repo page and drag in all files except `node_modules`.)

## 7. Deploy (free tiers; check current terms)
- **Netlify:** Add new site > Import from GitHub > pick repo. Build command `npm run build`, publish directory `dist`.
- **Vercel:** Add New Project > import repo. Vite is auto-detected.

## 8. Update after changes
Edit files, then `git add . && git commit -m "Update" && git push`. Netlify/Vercel redeploy automatically.

## Before going live
Add `og:image` and `og:url` meta tags in `index.html`, and swap placeholder previews for real screenshots.
