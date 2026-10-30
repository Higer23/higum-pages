# Higum — GitHub Pages frontend

This repository contains **only the public static website** for the Higum school-forum prototype.

- Public site source: `site/`
- Hosting target: GitHub Pages
- Current state: informational development landing page only
- Backend/API: maintained separately in the private [Higer23/higum](https://github.com/Higer23/higum) repository

## Important status

Registration, email verification, login, forum topics, replies, and moderation are **not implemented or available** on this static site. Do not enter passwords, school email addresses, or personal information here.

GitHub Pages serves static files. It does not run the Cloudflare Worker or securely store application secrets. The private backend must be implemented, reviewed, and connected separately before any account flow is enabled.

## Deploy

The workflow in `.github/workflows/pages.yml` deploys the `site/` directory to GitHub Pages when changes are pushed to `main`.

In GitHub, open **Settings → Pages** and set **Build and deployment → Source** to **GitHub Actions** if it is not selected automatically. No custom domain is configured in this stage.

## Local preview

Open `site/index.html` in a browser, or serve the `site/` directory with any local static file server.

## Security boundaries

- Never add Worker source, D1 database identifiers, API tokens, `.dev.vars`, environment files, private keys, certificates, backups, or personal test data.
- All future API authorization and validation must happen on the server.
- Public client-side configuration is not a secret.
- Report security issues privately to the repository owner; do not publish exploit details in an issue.

## License

MIT. See [LICENSE](LICENSE).
