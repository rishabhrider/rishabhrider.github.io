# Deploy DecideWise AI on GitHub Pages with Namecheap

Domain: `decidewiseai.me`

## 1. Create a GitHub repository

Recommended repository name:

```text
decidewiseai-website
```

Upload all files from this folder into the repository root:

```text
index.html
privacy.html
terms.html
CNAME
.nojekyll
robots.txt
sitemap.xml
README.md
DEPLOYMENT.md
```

## 2. Enable GitHub Pages

1. Open your repository on GitHub.
2. Go to **Settings → Pages**.
3. Under **Build and deployment**, select:
   - Source: **Deploy from a branch**
   - Branch: **main**
   - Folder: **/ (root)**
4. Save.
5. Under **Custom domain**, enter:

```text
decidewiseai.me
```

GitHub may create or update a `CNAME` file. This package already includes the correct `CNAME` file.

## 3. Configure Namecheap DNS

In Namecheap:

1. Go to **Domain List**.
2. Click **Manage** next to `decidewiseai.me`.
3. Open **Advanced DNS**.
4. Remove conflicting records for `@` or `www` if they exist, especially URL Redirect, parked records, old A records, or old CNAME records.
5. Add these records:

| Type | Host | Value | TTL |
|---|---|---|---|
| A Record | @ | 185.199.108.153 | Automatic |
| A Record | @ | 185.199.109.153 | Automatic |
| A Record | @ | 185.199.110.153 | Automatic |
| A Record | @ | 185.199.111.153 | Automatic |
| CNAME Record | www | YOUR-GITHUB-USERNAME.github.io | Automatic |

Replace `YOUR-GITHUB-USERNAME` with your actual GitHub username.

Example:

```text
rishabhathiya.github.io
```

Do **not** include the repository name in the CNAME value.

## 4. Wait for DNS propagation

Namecheap records can start working in about 30 minutes, but GitHub notes DNS changes can take up to 24 hours.

## 5. Enable HTTPS

After GitHub confirms the domain, return to **Settings → Pages** and enable:

```text
Enforce HTTPS
```

It can take some time for the SSL certificate to become available.

## 6. Test URLs

Test:

```text
https://decidewiseai.me
https://www.decidewiseai.me
```

If you configure the apex domain as the GitHub Pages custom domain, GitHub Pages should redirect `www.decidewiseai.me` to `decidewiseai.me` after DNS and HTTPS are correctly configured.

## 7. Optional: make the lead form fully serverless

GitHub Pages cannot process forms by itself. To collect leads directly:

1. Create a Formspree form.
2. Copy the endpoint URL.
3. Open `index.html`.
4. Replace:

```js
const LEAD_ENDPOINT='';
```

with:

```js
const LEAD_ENDPOINT='https://formspree.io/f/your_form_id';
```

Then commit and push the updated file.
