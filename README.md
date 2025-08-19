# DryWet Landing Page (Static)

A minimal, fast landing page you can deploy to **Cloudflare Pages** in minutes.

## Deploy (no Git needed)

1. Go to Cloudflare Dashboard → **Pages** → **Create a project** → **Upload assets**.
2. Drag the **contents** of this folder (not the folder itself).
3. Once deployed, click **Custom domains** → add `drywetwipe.com` and `www.drywetwipe.com`.
4. In **DNS**, be sure there are CNAMEs or A/AAAA records pointing the apex and `www` to the Pages project (Cloudflare will suggest these automatically).
5. In **SSL/TLS**: set **Always Use HTTPS** and **Automatic HTTPS Rewrites** ON.
6. In **Rules → Redirects**: add `http://www.drywetwipe.com/*` → `https://drywetwipe.com/$1` (or the reverse) to pick a primary host.
7. (Optional) **Email Routing**: forward `hello@drywetwipe.com` to your inbox.
8. (Optional) **Web Analytics**: enable Pages Analytics for privacy‑friendly stats.

## Contact Form

This template uses a simple `<form data-static-form>` pattern. On Cloudflare Pages, you can wire this to a service (e.g., Pages Functions, a lightweight Worker, or a form backend like Basin/Formspree/Zapier). Until connected, the form will do a normal POST without processing.

## Customize

- Replace `/assets/hero-mock.png` with a product image.
- Update copy in `index.html` and styles in `styles.css`.
- Add legal pages: `/privacy.html`, `/terms.html` if needed.
