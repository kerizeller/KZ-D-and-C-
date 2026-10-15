# Putting the new KZ site live (WordPress.com domain + Google email)

Your setup today: kzdandc.com is registered at WordPress.com and uses WordPress.com nameservers. Email for kzdandc.com and kzdevelopmentandconsulting.com runs on Google. Keep the domain at WordPress.com and only change the website records. Do NOT change the nameservers.

## Before you start
1. Download your logo and the team photos from WordPress (Media > Library). Send them to Claude to replace the initials.
2. Take a screenshot of the current DNS records page (step 3 shows where). This is your backup.

## Step 1. Create the repository
- On github.com, click New repository. Name it kzdandc-site. Set it to Public. Click Create.
- Click "uploading an existing file". Drag in everything from this folder (including the resources folder, CNAME, and style.css). Click Commit changes.

## Step 2. Turn on GitHub Pages
- Settings > Pages. Source: Deploy from a branch. Branch: main, folder: / (root). Save.
- In "Custom domain", type kzdandc.com and Save. (It will show a DNS warning until step 3 is done.)

## Step 3. Change the website records at WordPress.com
- Log in to WordPress.com. Go to Upgrades (or Manage) > Domains > kzdandc.com > DNS records.
- Add four A records, name @ (or blank):
  185.199.108.153 · 185.199.109.153 · 185.199.110.153 · 185.199.111.153
- Add a CNAME record: name www, value YOUR-GITHUB-USERNAME.github.io
- If WordPress.com still shows its own default A records (192.0.78.x) or a www record, delete them. If it will not let you, contact WordPress.com support and ask them to point the domain to GitHub Pages.
- Leave these alone: the MX record (smtp.google.com) and any TXT records (SPF, google-site-verification, DKIM). They keep your email working.

## Step 4. Finish
- Wait up to a few hours, then in GitHub Settings > Pages click "Check again" and tick "Enforce HTTPS".
- Test on mobile data (your work network blocks GitHub-hosted custom domains).
- Send a test email to info@kzdandc.com and info@kzdevelopmentandconsulting.com.

## Step 5. The WordPress.com plan
- In WordPress.com Purchases, make sure the domain kzdandc.com is set to auto-renew on its own.
- Only cancel the website plan after the new site works. Cancelling the plan does not need to cancel the domain, but check the domain is still listed afterwards.

## Step 6. Tell Google (do this the same week the site goes live)
- Google Search Console (search.google.com/search-console): Add property > Domain > kzdandc.com. Google gives you a TXT record. Add it in WordPress.com > Domains > kzdandc.com > DNS records as a TXT record on @. Then click Verify.
- In Search Console, open Sitemaps and submit: sitemap.xml
- Use URL Inspection on the home page and click "Request indexing".

## Step 7. Google Business Profile (the most important step for local searches)
- Go to business.google.com and create a profile for KZ Development & Consulting.
- Category: "Educational consultant" as primary; add "Business management consultant" or "Corporate training" if offered.
- Service area: Abu Dhabi and Dubai (you can hide the street address if you work from home).
- Website: https://kzdandc.com. Phone: +971 50 198 6469.
- Add the services from the website, and photos once you have them.
- Ask partner schools and colleagues to leave honest Google reviews.

## Step 8. Make the name consistent everywhere
- Use exactly "KZ Development & Consulting", the same phone number, and https://kzdandc.com on LinkedIn (create a company page), Google Business Profile, Clutch, and any directory listing.
