# Obsidian Vault Sync — OAuth information pages

Static site for the personal rclone OAuth client used with Obsidian and Google Drive. These files are intended for a public GitHub Pages site. Do not add the vault, notes, attachments, `rclone.conf`, OAuth client secrets, or tokens to this repository.

## Files

- `index.html` — application homepage
- `privacy.html` — privacy notice
- `terms.html` — use terms
- `assets/site.css` — shared responsive styling

## GitHub Pages

Use a dedicated public repository for these pages. After enabling Pages from the `main` branch and repository root, the user-site address will be `https://<username>.github.io/`; privacy and terms are `/privacy.html` and `/terms.html`. GitHub Pages makes the site public.

## Google OAuth domain requirement

Before setting the OAuth app to Production, Google requires the homepage and privacy page to use an authorized domain that is verified and controlled by the app owner. Do not assume the default `username.github.io` host will qualify. Verify control of the exact host in Search Console first. If Google will not accept it as an authorized domain, use a domain you control or leave the app in Testing, which requires reauthorization every 7 days for the Drive scope.

Once the exact host is verified, enter the real homepage, privacy, and terms URLs in Google Auth Platform → Branding, register the authorized domain, and only then consider changing Publishing status. Reconnect rclone afterward so it receives a new OAuth token.
