# Soil Hydrology & Physics Lab website

Website for Dr. Kang Liang's lab at North Dakota State University, to be served at **https://soilhydrolab.com** through GitHub Pages.

## Files

- `index.html` – the whole site (Home, Team, Research, Publications, News, Contact)
- `CNAME` – tells GitHub Pages to serve the site at soilhydrolab.com

## Updating content

Most updates only touch the lists near the bottom of `index.html`:

| To change | Edit this list |
|---|---|
| Papers | `PUBS` |
| Presentations | `PRES` |
| News items | `NEWS` (newest first; the home page shows the top 4) |
| Projects / grants | `PROJECTS` |
| Featured papers on the home page | `FEATURED` |

Team members, research themes, and contact details are written directly in the HTML sections with matching names (`v-team`, `v-research`, `v-contact`).

You can also ask Claude to make the change, for example "add this paper to the publications list."

## One-time setup

### 1. Buy the domain
Search for `soilhydrolab.com` at a registrar (Namecheap, Cloudflare, Porkbun, Squarespace Domains) and buy it if it is available.

### 2. Put the site on GitHub
1. Create a free account at github.com.
2. Create a new **public** repository, for example `soilhydrolab`.
3. Upload `index.html`, `CNAME`, and this `README.md` (Add file → Upload files → Commit).
4. Go to **Settings → Pages**. Under "Build and deployment," choose **Deploy from a branch**, branch `main`, folder `/ (root)`, and save.
5. In the same page, under **Custom domain**, enter `soilhydrolab.com` and save.

### 3. Point the domain to GitHub
In your registrar's DNS settings, add these records:

| Type | Host / Name | Value |
|---|---|---|
| A | @ | 185.199.108.153 |
| A | @ | 185.199.109.153 |
| A | @ | 185.199.110.153 |
| A | @ | 185.199.111.153 |
| AAAA | @ | 2606:50c0:8000::153 |
| AAAA | @ | 2606:50c0:8001::153 |
| AAAA | @ | 2606:50c0:8002::153 |
| AAAA | @ | 2606:50c0:8003::153 |
| CNAME | www | YOUR-GITHUB-USERNAME.github.io |

Remove any existing "parking" A or CNAME records for `@` and `www` first.

### 4. Turn on HTTPS
DNS changes can take up to 24 hours. Once GitHub shows the domain as verified, return to **Settings → Pages** and tick **Enforce HTTPS**.

Source: [GitHub Docs – Managing a custom domain for your GitHub Pages site](https://docs.github.com/en/pages/configuring-a-custom-domain-for-your-github-pages-site/managing-a-custom-domain-for-your-github-pages-site)
