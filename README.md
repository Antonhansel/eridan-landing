# eridan-landing

Static marketing landing page for **[eridan-labs.com](https://eridan-labs.com)**.

Served via GitHub Pages from the `main` branch.

## Content

- `index.html` — single self-contained page (all CSS, SVGs, images inlined). Source: Eridan Labs brand synthesis landing.
- `CNAME` — custom domain config for GitHub Pages.

## Analytics

**Plausible** (privacy-friendly, cookie-free, GDPR-compliant without a consent banner).

To activate:
1. Sign up at <https://plausible.io>
2. Add `eridan-labs.com` as a site
3. Data starts flowing on the next page load — the `<script>` is already in `index.html`.

If you'd rather use Google Analytics 4, there's a commented-out `gtag` snippet at the top of `index.html`. Uncomment, replace `G-XXXXXXXXXX` with your Measurement ID, and be aware you'll need a cookie consent banner for EU visitors.

## Updating the page

```sh
# Edit index.html, then:
git commit -am "update landing copy"
git push
```

GitHub Pages rebuilds in ~30s.

## DNS (OVH)

At apex `eridan-labs.com`, set A records pointing to GitHub Pages:

```
@  A  185.199.108.153
@  A  185.199.109.153
@  A  185.199.110.153
@  A  185.199.111.153
```

And for `www`:

```
www  CNAME  antonhansel.github.io.
```

Then in GitHub repo Settings → Pages → Custom domain, enter `eridan-labs.com` and wait for HTTPS cert provisioning (a few minutes).
