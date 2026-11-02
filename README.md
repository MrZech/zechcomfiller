# zechender.com

A small personal website for Iain Zechender. Plain HTML and CSS, system fonts, no JavaScript, dependencies, tracking, or build step.

## Preview locally

From this directory, run:

```sh
python3 -m http.server 8000 --bind 127.0.0.1
```

Open http://127.0.0.1:8000. Stop the server with Ctrl+C.

## Publish on GitHub Pages

1. Create a GitHub repository and upload these files to its root, including `.nojekyll` and `CNAME`. You can use any repository name when using a custom domain.
2. In the repository, open **Settings → Pages**.
3. Under **Build and deployment**, choose **Deploy from a branch**, then select **main** and **/ (root)**. Save.
4. Under **Custom domain**, enter **zechender.com** and save. The included `CNAME` file also declares this domain.
5. At your DNS provider, point the root domain (`@`) to GitHub Pages using these four **A** records:

   | Type | Name | Value |
   | --- | --- | --- |
   | A | @ | 185.199.108.153 |
   | A | @ | 185.199.109.153 |
   | A | @ | 185.199.110.153 |
   | A | @ | 185.199.111.153 |

6. For `www.zechender.com`, add a **CNAME** record with name `www` pointing to **YOUR-GITHUB-USERNAME.github.io** (replace the username, without a repository path).
7. Replace old web-hosting records for `@` or `www` that conflict with these records. Keep unrelated email records. If old `AAAA` records point to the disconnected server, remove those or update them using GitHub's IPv6 instructions.
8. Once GitHub validates the domain and provisions its certificate, enable **Enforce HTTPS** in Pages settings. DNS changes can take up to 24 hours.

GitHub recommends verifying your domain in account settings before attaching it to a repository. Follow the account-specific TXT record instructions in [GitHub's domain verification guide](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/verifying-your-custom-domain-for-github-pages).

Reference: [GitHub Pages publishing settings](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site) and [custom domain setup](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site).

## Edit the site

- `index.html`: name, introduction, employer link, and page metadata.
- `styles.css`: colors, typography, spacing, and mobile layout.
- `favicon.svg`: browser tab icon.
- `CNAME`: custom domain for GitHub Pages.

The site is ready to upload; GitHub Pages and DNS still need to be configured before it is live on the domain.
