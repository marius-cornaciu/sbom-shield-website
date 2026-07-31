# SBOM Shield — Presentation Website

Static website presenting **SBOM Shield**, a free self-hosted SBOM platform distributed via Docker Hub.

Built with plain HTML + CSS — no build step, no dependencies. Ready for GitHub Pages.

## Preview locally

```bash
open index.html
# or serve it:
python3 -m http.server 8000
```

## Publish on GitHub Pages

1. Create a repo on GitHub (e.g. `sbom-shield-website`) and push this project:

   ```bash
   git remote add origin git@github.com:marius-cornaciu/sbom-shield-website.git
   git push -u origin main
   ```

2. On GitHub: **Settings → Pages → Source: Deploy from a branch → Branch: `main` / root → Save**.

3. Your site goes live at `https://marius-cornaciu.github.io/sbom-shield-website/` within a minute or two.

## Before publishing

Replace the placeholders in `index.html` and this README:

- `YOUR_DOCKERHUB_USER` — your Docker Hub username (used in `docker pull` commands and links)
- `marius-cornaciu` — your GitHub username (footer / links)

Also review the feature list, port number (`8080`), and FAQ answers so they match what your platform actually does.
