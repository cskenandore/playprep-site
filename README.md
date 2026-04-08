# PlayPrep Website

This folder contains the PlayPrep marketing website, hosted on GitHub Pages at playprep.app.

## Files

- `index.html` — Landing page
- `privacy.html` — Privacy Policy (linked from App Store Connect)
- `terms.html` — Terms of Service (linked from App Store Connect)
- `logo.png` — App logo / favicon

## How to publish to GitHub Pages

1. Create a NEW GitHub repository named `playprep-site` (public)
2. Upload all files in this folder to that repo
3. Go to repo Settings → Pages → Source: Deploy from branch → Branch: main → folder: / (root)
4. Save — GitHub will give you a URL like `cskenandore.github.io/playprep-site`

## Connect your custom domain (playprep.app)

1. In your GitHub repo, go to Settings → Pages → Custom domain
2. Type `playprep.app` and save — this creates a CNAME file automatically
3. In Cloudflare (where you bought the domain):
   - Go to DNS → Add record
   - Type: CNAME, Name: @, Target: cskenandore.github.io
   - Also add: CNAME, Name: www, Target: cskenandore.github.io
4. Wait 10-30 minutes for DNS to propagate
5. Back in GitHub Pages settings, check "Enforce HTTPS"

## URLs that will work after setup

- https://playprep.app → landing page
- https://playprep.app/privacy.html → Privacy Policy
- https://playprep.app/terms.html → Terms of Service
- https://www.playprep.app → also works

## App Store Connect

Enter these URLs in App Store Connect → App Information:
- Privacy Policy URL: https://playprep.app/privacy.html

## Adding screenshots later

In index.html, find the `.screenshot-frame` divs and replace them with:
  <img src="screenshots/home.png" alt="Home screen" style="width:200px; border-radius:24px;" />

Put your screenshots in a /screenshots/ folder in this repo.
