# Healthyi website

Website for Healthyi, a student-led organization by Youth Impact working to end neglected tropical diseases (NTDs).
Live at https://healthyi.co

## What's in this folder
- `index.html`: the homepage. The whole site (all pages, styles and scripts) is in this one file.
- `about/`, `members/`, `news/…` and the other folders: copies of the same page, one per address, so clean links like healthyi.co/about/ work and each page has its own title, description and link preview.
- `images/`: photos, logos, icons and the link-preview thumbnail (`og-image.jpg`).
- `favicon.ico`, `site.webmanifest`: browser tab and home-screen icons.
- `sitemap.xml`, `robots.txt`: help search engines find every page.
- `404.html`: shown for addresses that don't exist.
- `CNAME`: tells GitHub Pages to serve the site at healthyi.co.

## Publish with GitHub Pages
1. Create a repository and upload everything in this folder (keep all folders).
2. Go to Settings → Pages. Under "Build and deployment", choose "Deploy from a branch", then `main` and `/ (root)`, and click Save.
3. Under "Custom domain", check that it says `healthyi.co`, and turn on "Enforce HTTPS" once it's available.
4. At your domain registrar, add these DNS records for healthyi.co:
   - Four `A` records pointing to 185.199.108.153, 185.199.109.153, 185.199.110.153 and 185.199.111.153
   - A `CNAME` record for `www` pointing to `<your-github-username>.github.io`

## Contact form
Messages go through FormSubmit to bubble.youthimpact@gmail.com. The first time the form is used on the live site,
FormSubmit sends an activation email to that address. Click its link once; after that, messages arrive normally.

## Updating content
News, members, reports, event projects and activity materials are stored as JSON inside each page, in the
`<script type="application/json" id="site-data">` block. The easiest way to update is to ask for a rebuilt zip,
since every page folder holds a copy of the same content.
