# 689713.me — site files (GitHub Pages)

This folder is published as-is to the public repo `kprajesh-ms/689713.me` (branch `main`, root), served by GitHub Pages at `https://689713.me/`. Add future apps as sibling folders of `netscan/` and a card on `index.html`.

| URL | File |
|---|---|
| `/` | `index.html` — company landing |
| `/netscan/` | `netscan/index.html` — product page (Support/Marketing URL in both stores) |
| `/netscan/privacy` | `netscan/privacy.html` (Pages resolves extensionless URLs to `.html`) |
| `/netscan/buy` | `netscan/buy.html` |
| `/netscan/appcast.json` | update feed for direct builds — bump `build` when a direct build ships |

`CNAME` holds the custom domain; `.nojekyll` keeps Pages from processing the files.

DNS at GoDaddy for the apex + www:

```
A     @    185.199.108.153
A     @    185.199.109.153
A     @    185.199.110.153
A     @    185.199.111.153
CNAME www  kprajesh-ms.github.io
```

Then GitHub › repo Settings › Pages › Custom domain `689713.me`, tick "Enforce HTTPS" once the certificate is issued (10–60 min after DNS propagates).

Publishing from the main repo: `scripts/publish-site.sh` copies `docs/site/` into a checkout of the site repo and pushes.
