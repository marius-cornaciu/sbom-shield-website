# SBOM-Shield — Presentation Website

Static website presenting **SBOM-Shield**, a free self-hosted Software Composition
Analysis platform distributed via Docker Hub — vulnerability scanning, secrets
detection, and AI/ML compliance (EU AI Act, OWASP LLM Top 10, MITRE ATLAS, NIST
AI RMF).

Built with plain HTML + CSS — no build step, no dependencies. Content is kept in
sync with the docs in the main sca-scanner repo (`README.md`, `AI-Compliance.md`,
`quick-start.md`, …) — re-check `index.html` against those whenever the product
changes materially. sca-scanner itself is private, so it isn't linked here.

## docker-compose.yml / env.prod.example

These are mirrored here **from sca-scanner on purpose**, not leftovers — sca-scanner
is private, so `raw.githubusercontent.com` can't serve files from it publicly. This
repo is the public download point every quickstart command (site + docs) points at:

```bash
curl -O https://raw.githubusercontent.com/marius-cornaciu/sbom-shield-website/main/docker-compose.yml
```

Re-copy both files here whenever they change in sca-scanner — there's no
automation keeping them in sync yet.

## Issues

Bug reports and feature requests for SBOM-Shield (the tool, not just this
site) are tracked here too — same reason as the compose file mirroring:
sca-scanner is private, so this is the only public repo that can host them.
Templates live in `.github/ISSUE_TEMPLATE/`. The site links to
[New Issue](https://github.com/marius-cornaciu/sbom-shield-website/issues/new/choose)
from its own "Found a Bug?" section.

## Preview locally

```bash
open index.html
# or serve it:
python3 -m http.server 8000
```

## Publish on GitHub Pages

This repo already tracks `origin` → `github.com/marius-cornaciu/sbom-shield-website`.
Push to `main` and GitHub Pages (**Settings → Pages → Source: Deploy from a branch →
`main` / root**) picks it up automatically — live at
`https://marius-cornaciu.github.io/sbom-shield-website/` within a minute or two.

```bash
git push origin main
```

## Authors

Built by Marius Cornaciu and Anca Beres.

## License

SBOM-Shield Website
Copyright (C) 2026 Marius Cornaciu, Anca Beres

This program is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

This program is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE. See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with this program. If not, see <https://www.gnu.org/licenses/>.

Full text: [`LICENSE`](LICENSE).
