# Critters-Crawlers-v.1

Static website for Critters and Crawlers.

## Publish with GitHub Pages

The repository is prepared to deploy from the `main` branch using the workflow in
`.github/workflows/deploy.yml`.

1. Add the site files and deployment configuration to a commit and push it to
   `main`.
2. In the repository, open **Settings → Pages** and set the build and deployment
   source to **GitHub Actions**.
3. At the DNS provider for `crittersandcrawlerswildlife.com`, point the apex
   domain to GitHub Pages with these A records:

   - `185.199.108.153`
   - `185.199.109.153`
   - `185.199.110.153`
   - `185.199.111.153`

   Set `www` to a CNAME for `SanderTank878.github.io`. Remove conflicting
   parking records for the apex and `www`; leave unrelated email records (such
   as MX and mail-related TXT records) unchanged.
4. After DNS updates propagate and the first Pages deployment succeeds, check
   **Settings → Pages** for the custom-domain and HTTPS status. The canonical
   site address is `https://www.crittersandcrawlerswildlife.com/`.

The included `CNAME` file sets the custom domain for Pages deployments. The
GitHub Pages workflow deploys the static site whenever changes are pushed to
`main`, and can also be run manually from the repository's Actions tab.
