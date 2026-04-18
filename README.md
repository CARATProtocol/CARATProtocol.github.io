# CARAT GitHub Pages Kit

This folder is a ready-to-publish static GitHub Pages package for the public-facing CARAT GitHub site.

## What it is for

Use this as the **public product face** of CARAT on GitHub:

- project overview
- trust and methodology summaries
- official links
- Chrome extension install area
- roadmap and public docs links

Do **not** use this page for:

- VPS or deployment secrets
- internal endpoints
- infrastructure notes
- admin documentation
- anything operationally sensitive

## Recommended GitHub structure

For an organization page, GitHub Pages expects a repository named:

`CARATProtocol.github.io`

GitHub Docs reference:

- https://docs.github.com/en/pages/getting-started-with-github-pages/what-is-github-pages

## Suggested repo content

At minimum:

- `index.html`
- `styles.css`
- `assets/`
- optional `CNAME` if using a custom subdomain

## Suggested public links

- Main website: `https://caratprotocol.com`
- Engine: `https://caratprotocol.com/carat/engine`
- Extension privacy: `https://caratprotocol.com/carat/extension-privacy`
- GitHub org: `https://github.com/CARATProtocol`

## Publishing

1. Create the repo `CARATProtocol.github.io`
2. Upload the contents of this folder to the root of that repo
3. In GitHub repo settings, open `Pages`
4. Set publishing source to:
   - `Deploy from a branch`
   - branch: `main`
   - folder: `/ (root)`
5. Save

GitHub Docs reference:

- https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site

## Custom domain recommendation

Use a subdomain instead of your main production app domain.

Recommended:

- `docs.caratprotocol.com`

GitHub recommends subdomains with `CNAME` records for GitHub Pages:

- https://docs.github.com/pages/configuring-a-custom-domain-for-your-github-pages-site/about-custom-domains-and-github-pages

## Custom domain setup

1. In your DNS provider, create:
   - `CNAME`
   - host/name: `docs`
   - value/target: `caratprotocol.github.io`
2. In the GitHub repo:
   - `Settings -> Pages`
   - set custom domain to `docs.caratprotocol.com`
3. Wait for DNS to propagate
4. Enable HTTPS in GitHub Pages settings

GitHub Docs reference:

- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site
- https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages

## Updating the Add to Chrome button later

When the Chrome Web Store listing is approved:

1. Open `index.html`
2. Find the button text:
   - `Add to Chrome (coming soon)`
3. Replace the placeholder `href="javascript:void(0)"`
4. Use the real Chrome Web Store URL
5. Remove the `button-disabled` class

