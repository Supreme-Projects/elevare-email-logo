# Elevare Investments — Email Logo Host

A minimal static site for hosting a single PNG logo for **Microsoft 365 (Outlook)** signatures.

## Files
- `assets/logo-email@2x.png` — Retina (recommend this URL in signatures, set width=320)
- `assets/logo-email.png` — Standard (1x, height 80px)
- `index.html` — Preview page
- `netlify.toml` — Cache headers

## Deploy (GitHub → Netlify)
1. Create a new GitHub repo (e.g., `elevare-email-logo`).
2. Add these files, commit, and push:
   ```bash
   git add .
   git commit -m "Add email logo host"
   git push origin main
   ```
3. In **Netlify**: *Add new site* → **Import from Git** → select your repo.
   - Build command: _(leave empty)_
   - Publish directory: `.`
4. Deploy. Your direct image URL will be:
   - `https://YOUR-SITE.netlify.app/assets/logo-email@2x.png`

## Use in Microsoft 365 (Outlook on the web)
1. Go to **Settings → Mail → Compose and reply → Email signature**.
2. Click **Insert pictures inline**.
3. Paste the image URL:  
   `https://YOUR-SITE.netlify.app/assets/logo-email@2x.png`
4. With the image selected, set **Width = 320** (height auto).  
   This serves the 2x image crisply on Retina displays.
5. Optionally set **Alt text**: "Elevare Investments".

> Note: Some recipients block remote images. If your org prefers embedded images (CID), use a signature tool or Outlook desktop to attach the image instead.
