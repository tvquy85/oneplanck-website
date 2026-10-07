# OnePlanck website

Static corporate landing page for `oneplanck.com`, designed for GitHub Pages.

## Important before publishing

The contact button currently uses:

`founder@oneplanck.com`

If your actual mailbox is different, open `index.html` and replace every occurrence of `founder@oneplanck.com` with the email you created.

The Research Credentials section deliberately avoids inventing publication titles or venues. Add only publications that are already public/accepted and that you are comfortable displaying.

## Deploy on GitHub Pages

1. Create a new **public** GitHub repository, e.g. `oneplanck-website`.
2. Upload all files in this folder to the root of the repository.
3. Commit to the `main` branch.
4. Open **Settings → Pages**.
5. Under **Build and deployment**, choose **Deploy from a branch**.
6. Select `main` and `/ (root)`, then Save.
7. Under **Custom domain**, enter `oneplanck.com` and Save.

This repository already includes a `CNAME` file containing `oneplanck.com`.

## GoDaddy DNS for GitHub Pages

In GoDaddy → Domains → oneplanck.com → DNS, add these A records for the root domain:

| Type | Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |

Add this CNAME for `www`:

| Type | Name | Value |
|---|---|---|
| CNAME | www | YOUR-GITHUB-USERNAME.github.io |

Replace `YOUR-GITHUB-USERNAME` with your GitHub username.

### Critical email warning

Do **not** delete or alter GoDaddy email records such as MX, SPF/TXT, DKIM, or other mail-related DNS records. Only modify/add the website records needed for GitHub Pages.

## HTTPS

After GitHub verifies the custom domain, enable **Enforce HTTPS** in Settings → Pages. DNS propagation can take from a few minutes to several hours.

## Suggested Claude Startups consistency

Use the same company identity everywhere:

- Website: `https://oneplanck.com`
- Company email: your `@oneplanck.com` founder email
- Claude Console account: same company email
- Startup application: same company email and website

## Local preview

Double-click `index.html`, or run a basic local server from this directory:

```bash
python -m http.server 8000
```

Then open `http://localhost:8000`.
