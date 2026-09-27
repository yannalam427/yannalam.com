# yannalam.com

Portfolio of Yann Alam, electrical engineering student at NJIT (May 2027).
A static site: one `index.html` plus its images, fonts and `vendor/three.min.js`. Nothing is loaded from other servers.

## Launch (one time)

1. **Buy the domain** `yannalam.com` at any registrar (for example Cloudflare, Porkbun or Namecheap).
2. **Verify it with GitHub first** (protects against domain takeover):
   GitHub → your avatar → Settings → Pages → *Add a domain* → `yannalam.com`.
   GitHub shows one TXT record; add it at your registrar's DNS page, then click *Verify*.
3. **Create the repo**: GitHub → New repository → name it `yannalam.com` (any name works) → Public → Create.
4. **Upload the site**: in the new repo, *Add file → Upload files*, drag in **everything in this folder**
   (including `CNAME`, `.nojekyll`, `vendor/` and `fonts/`), then *Commit changes*.
   Hidden files: if your computer hides `.nojekyll`, the site still works without it.
5. **Turn on Pages**: repo → Settings → Pages → *Build and deployment* → Source: *Deploy from a branch* →
   Branch: `main`, folder `/ (root)` → Save. Under *Custom domain* it should already say `yannalam.com`
   (from the `CNAME` file); if not, type it and Save.
6. **Point the domain at GitHub** (registrar → DNS records):

   | Type  | Name / Host | Value                   |
   |-------|-------------|-------------------------|
   | A     | @           | 185.199.108.153         |
   | A     | @           | 185.199.109.153         |
   | A     | @           | 185.199.110.153         |
   | A     | @           | 185.199.111.153         |
   | AAAA  | @           | 2606:50c0:8000::153     |
   | AAAA  | @           | 2606:50c0:8001::153     |
   | AAAA  | @           | 2606:50c0:8002::153     |
   | AAAA  | @           | 2606:50c0:8003::153     |
   | CNAME | www         | yannalam427.github.io   |

   Delete any parking-page A/CNAME records the registrar added. On Cloudflare, set these records to *DNS only* (grey cloud).
7. **HTTPS**: once the DNS check in Settings → Pages turns green (minutes to a few hours), tick **Enforce HTTPS**.
8. **Check**: open https://yannalam.com and https://www.yannalam.com, then paste the link into a LinkedIn post draft to see the preview card.

## After launch

- **Google**: add the site in Google Search Console (Domain property, verified by a DNS TXT record) and submit `https://yannalam.com/sitemap.xml`.
- **LinkedIn**: add the site to your profile's *Contact info → Website* and to the *Featured* section.
- **Updating**: the source lives in the Claude project "Website Creation (yann)". Ask Claude for the change, then upload the new
  `index.html` (and any new files) to this repo the same way; Pages republishes in about a minute.
