# DecideWise AI — GitHub Pages Landing Website

This folder contains a static, GitHub-Pages-ready landing website for **DecideWise AI**, founded by **Rishabh Athiya**.

## Files included

- `index.html` — main landing page
- `privacy.html` — privacy policy page
- `terms.html` — terms page
- `CNAME` — custom domain file for GitHub Pages (`decidewiseai.me`)
- `.nojekyll` — prevents Jekyll processing issues
- `robots.txt` and `sitemap.xml` — basic SEO files
- `DEPLOYMENT.md` — GitHub Pages + Namecheap setup instructions

## Contact details used

- Founder: Rishabh Athiya
- Email: founder@decidewiseai.me
- Mobile: +91 90395 59323

## Important form behavior

GitHub Pages is static hosting, so it cannot receive form submissions by itself. The lead form currently works by preparing an email request and copying the request as fallback. If you want direct form submission without email, create a Formspree endpoint and paste it into this line in `index.html`:

```js
const LEAD_ENDPOINT='';
```

Example:

```js
const LEAD_ENDPOINT='https://formspree.io/f/your_form_id';
```

## Local preview

Open `index.html` directly in your browser, or run:

```bash
python -m http.server 8000
```

Then visit `http://localhost:8000`.
