# Hosting & Website Strategy — Brainstorming Notes

## Current Setup
- 8-chapter interactive HTML textbook (Trichology for GP)
- Static files, no backend — self-contained HTML/CSS/JS
- Hosted on GitHub (public repo): github.com/Samanvay96/Trichology-for-GP

## Recommended Architecture
- **Main site** (jayantkarambhe.com or similar): WordPress on Hostinger (~$35-50/yr)
  - Landing page, about, contact, blog posts, course promotion pages
  - Visual editor so Dad can update content independently
  - Unlimited pages, plugins for SEO/analytics/forms
- **Courses subdomain** (courses.domain.com): GitHub Pages (free)
  - Hosts the interactive HTML courses
  - CNAME DNS record pointing to samanvay96.github.io
  - Free HTTPS via Let's Encrypt

## How It Connects
- Course cards/buttons on WordPress link to courses.domain.com
- Chapter pages already have built-in navigation (prev/next, chapter index)
- Feels seamless to the user

## If Courses Need to Be Paid
- **Gumroad / LemonSqueezy** — lightweight checkout, redirect to course URL after purchase
- **Teachable / Thinkific** ($30-80/month) — full course platform, overkill for now
- **Squarespace Member Areas** ($7-35/month add-on) — gated content

## Alternatives Considered
| Platform | Cost/yr | Notes |
|----------|---------|-------|
| Carrd | $19 | Great for single-page, too limited for blog |
| WordPress.com (free) | $0 | Shows their branding, limited |
| WordPress.com (Personal) | ~$48 | Custom domain, no ads |
| Hostinger + WordPress | ~$35-50 | Best value for multi-page site ← chosen |
| Squarespace | ~$192 | Polished but expensive |
| Wix | ~$120-200 | Similar to Squarespace |

## GitHub Pages Setup (TODO)
- Enable Pages in repo settings (Settings > Pages > Source: main)
- Add CNAME file with the subdomain
- Configure DNS: `courses` CNAME → `samanvay96.github.io`
- Free HTTPS auto-provisioned

## Notes
- Repo can stay public (content is CC BY-NC-ND licensed)
- If private repo needed: Cloudflare Pages (free) or GitHub Pro ($4/month)
- Domain renewal is ~$10-15/yr on top of hosting
