# UJUG Sponsorship Page - Project Metadata

## What This Is
A static HTML page for the Utah Java Users Group (UJUG) sponsorship info, extracted from a WordPress database backup and prepared for deployment on GitHub Pages.

## Origin
- **Source**: WordPress database backup at `C:\Users\Don\Downloads\ujugorg_wp01.sql`
- **Post ID**: 650 (autosave revision of page 89, slug `sponsorship-info`)
- **Original date**: 2025-02-18
- **WordPress site**: ujug.org (previously hosted on shared hosting, domain now transferred to Porkbun)
- **Original WordPress files export**: `C:\Users\Don\Documents\public_html\` (includes wp-content, themes, plugins, updraft backups)

## File Structure
```
ujug-site/
  sponsorship-info/
    index.html          - The sponsorship info page (self-contained HTML+CSS)
    ujug_crowd_1.jpg    - Header image: panoramic photo of packed UJUG meeting
    ujug_logo.png       - UJUG green logo (retina version)
```

## Image Sources (from WordPress uploads)
- `ujug_crowd_1.jpg` copied from `public_html/wp-content/uploads/2025/01/ujug_crowd_1.jpg`
- `ujug_logo.png` copied from `public_html/wp-content/uploads/2015/06/ujug_flat_green_retina.png`

## Page Content Summary
- Dark theme (#2d2d2d background, white text, green accents rgb(90,185,79))
- UJUG logo centered at top
- Crowd photo banner
- "Support UJUG" section with mission description
- "Why do we need sponsors?" section (food, speaker fees, door prizes)
- 4 sponsorship tiers in a CSS grid:
  - **One-time Promotion**: $500 (promo email to 4000+ members, mention at 2 meetings, swag)
  - **Silver**: $500/year (logo at meetings, swag)
  - **Platinum**: $1,250/year (yearly address, twice yearly email, logo, swag)
  - **Diamond** (standout): $2,500/year (twice yearly address, quarterly email, logo, swag, special callout, max 2 sponsors)
- Footer with contact email: board@ujug.org (HTML entity encoded)

## Deployment Plan
- **Hosting**: GitHub Pages (free)
- **Domain**: ujug.org (registered on Porkbun)
- **Target URL**: ujug.org/sponsorship-info

### Steps to Deploy
1. Initialize git repo in `ujug-site/` folder
2. Create GitHub repo (e.g. `ujug-site`) and push
3. Enable GitHub Pages in repo Settings > Pages (source: main branch)
4. In Porkbun DNS settings, add:
   ```
   A     @    185.199.108.153
   A     @    185.199.109.153
   A     @    185.199.110.153
   A     @    185.199.111.153
   CNAME www  <github-username>.github.io
   ```
5. In GitHub repo Settings > Pages > Custom domain, enter `ujug.org`
6. Wait for DNS propagation and SSL cert provisioning

## Other WordPress Backups Available
- Updraft DB backups in `public_html/wp-content/updraft/` (2019-2024)
- Latest updraft full backup: 2024-12-05 (db, plugins, themes, uploads, others)
- Newer DB dump: `C:\Users\Don\Downloads\ujugorg_wp01.sql` (contains 2025 content)
- Tar backups: `public_html/Jan1011-backup.tar.gz`, `Jan1011-1840-backup.tar.gz`

## Other Pages in WordPress (from DB)
- Homepage (post 10) - meeting schedule, testimonials, sponsor logos
- Sponsorship Info (post 89/650) - THIS page
- Sponsors Overview (post ~203) - list of current sponsors with logos
- Contact page - email form (board@ujug.org)
- Mailing Lists page
- Various meeting event posts
