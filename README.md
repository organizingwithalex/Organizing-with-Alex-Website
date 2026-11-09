# organizingwithalex.com

A static site with plain HTML, CSS and a small JS file. It has no build step, framework or dependencies, and it's ready to deploy on Vercel.

## What's here
- `index.html`: the homepage
- `areas/`: an areas index, a Palm Beach County hub and 9 town pages
- `journal/`: the journal index and 16 posts (5 new, plus 11 carried over from Wix)
- `privacy/` and `terms/`: the legal pages
- `404.html`: the not-found page
- `images/`: every photo as optimized WebP, plus the logo
- `site.js`: the rotating headline, portfolio filters and floating call bar
- `sitemap.xml`, `robots.txt`, `llms.txt`: for search engines and AI assistants
- `vercel.json`: clean URLs, caching, and 42 permanent (301) redirects from old Wix URLs

Each page has its own title, meta description, canonical URL, Open Graph tags and JSON-LD:
- every page: LocalBusiness
- homepage: FAQPage
- town pages: Service
- posts: BlogPosting

## Deploy
1. Create a new GitHub repo (for example `organizingwithalex-site`) and push the contents of this folder to it, with `index.html` at the repo root.
2. In Vercel, go to **Add New → Project → Import** and pick the repo.
   - Framework preset: **Other**
   - Build command: *(leave empty)*
   - Output directory: *(leave empty, the root)*
3. Deploy, then check the `*.vercel.app` preview URL.
4. **Domain:** in Vercel, go to Settings → Domains and add `organizingwithalex.com` and `www.organizingwithalex.com`. Pick one as primary and redirect the other.
   - If the domain is registered through Wix, update its DNS records in Wix (or transfer the domain) to the values Vercel shows.
   - Keep the Wix site live until DNS has switched over.
5. **The day you switch:**
   - Visit a few old URLs (for example `/post/small-closet-solutions-for-miami-condos-maximize-every-inch`) and confirm they redirect.
   - In Google Search Console, verify the domain, submit `https://organizingwithalex.com/sitemap.xml`, and request indexing for the homepage and `/areas/*`.
   - Submit the same sitemap to Bing Webmaster Tools.
   - Add GA4 to every page `<head>`, and track `tel:` and `sms:` clicks plus form submits as conversions.

## Forms and booking
- **Consultation form:** posts to Formspree (`https://formspree.io/f/meaaboll`) and is delivered to organizingwithalex@gmail.com. After launch, send one test submission and confirm Formspree's verification email.
- **"Check availability":** opens the Google Calendar booking page.

## Before launch
- Replace the bracketed placeholder reviews (`[Name]`) on the homepage and town pages with real Google reviews.
- Before cutting DNS, crawl the old Wix site (Screaming Frog free, or Search Console's Pages report). Add any old URL that isn't in `vercel.json` to its `redirects`.

## Editing later
Edit the HTML directly. The design source lives in the Claude design canvas. Shared pieces (header, footer, booking form) are repeated in each page, so update them everywhere when you change one.
