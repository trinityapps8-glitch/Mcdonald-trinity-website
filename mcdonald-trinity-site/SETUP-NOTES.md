# McDonald Trinity — site handoff notes

## Deploying on Netlify
1. Drag the whole `site` folder into Netlify (Sites → Add new site → Deploy manually), or connect it to a Git repo.
2. Netlify will serve `index.html`, `about.html`, `innovation.html`, `company.html`, `contact.html` automatically — no build step needed, it's plain HTML/CSS/JS.
3. The contact form on `contact.html` uses Netlify Forms (`data-netlify="true"`). Once deployed on Netlify this works with zero backend — submissions show up in Site settings → Forms.
4. Once you have your real Netlify/custom domain, replace every instance of `https://mcdonaldtrinity.netlify.app/` in the five HTML files (canonical tags, og:url, sitemap.xml) with your real live URL — a quick find-and-replace.

## Getting it indexed on Google (Search Console)
This needs your own Google account, so it can't be done from here — but it's quick:
1. Go to https://search.google.com/search-console and add your site (use the "URL prefix" method with your live Netlify URL).
2. Verify ownership the easy way for a static Netlify site: Search Console will give you a line like
   `<meta name="google-site-verification" content="XXXXXXXX" />`
   Paste that into the `<head>` of `index.html` (right under the other `<meta>` tags), redeploy, then click Verify.
3. Once verified, submit `sitemap.xml` under Search Console → Sitemaps (it's already built and live at `/sitemap.xml`).
4. `robots.txt` is already in place and points Google at the sitemap automatically.

## What's already done for SEO
- Unique `<title>` and meta description on every page
- Open Graph + Twitter card tags so links preview nicely when shared
- JSON-LD structured data (Person, Organization, Article) so Google can understand who Trinity, Emtrixz, and the Stanbic programme are
- Canonical URLs, `robots.txt`, and `sitemap.xml`

## The one open item: the exact "Bootcamp Prototype Showcase" video
I confirmed the Stanbic National Schools Championship is Uganda's national school **innovation and entrepreneurship** programme (not sport) from Stanbic Bank Uganda's own programme site and independent press coverage, and found that Stanbic Bank Uganda's official YouTube channel (@StanbicBankUganda) does publish bootcamp/prototype-showcase style videos each season. I wasn't able to pull up the specific "Bootcamp Prototype Showcase" video or its transcript through search, so `innovation.html` currently links out to the channel rather than embedding a specific video.

Send me the exact YouTube link and I'll swap in a real embed and tighten the copy around exactly what was shown/said in it.
