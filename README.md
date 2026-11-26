# Hex Design

Portfolio and studio website for **Hex Design** — an independent design studio based in Dhaka, Bangladesh, focused on brand identity, social media posters, YouTube thumbnails, tech content production, and UI/UX design.

Built as a single, self-contained static HTML file with no build step or bundler required.

## Overview

The site covers the full studio presence in one page:

- **Hero & Client Marquee** — Display typography (`Cal Sans` / `Manrope`), subtle scroll parallax portrait, availability status, and an infinite client logo ticker.
- **About & Workflow** — Studio overview, four-stage design process, and core disciplines (Graphics Design, Tech Content Creation, UI/UX Design, Photography).
- **Selected Work** — Behance portfolio supporting both a hover-preview list layout and a card grid view, with an in-site Behance embed modal.
- **Tech Content** — Switchable `16:9` full videos and `9:16` YouTube Shorts grids with an embedded popup player.
- **Services & Testimonials** — Expandable dark-surface services accordion and a keyboard-navigable client review slider.
- **Resume** — Work history, education, and toolkit with a dedicated `@media print` layout for clean PDF export (or an external CV URL).
- **Pricing** — Fixed-scope packages with a live `BDT (৳)` / `USD ($)` currency toggle that pre-selects the chosen package in the contact form.
- **Tutorials & Blogs** — Filterable design resources with an in-site essay reader modal and video player.
- **Contact** — Project brief composer that formats and opens inquiries directly in WhatsApp or the default email client, plus one-click email copy.

## Stack

- **Markup & Logic:** Vanilla HTML5, CSS3, JavaScript (ES6+)
- **Styling:** Custom CSS variables and animations + [Tailwind CSS](https://tailwindcss.com/) via CDN
- **Smooth Scroll:** [Lenis](https://github.com/darkroomengineering/lenis) (`1.1.18`) with native scroll fallback
- **Typography:** `Cal Sans`, `Manrope`, and `Inter` via Google Fonts

## Structure

```text
.
├── index.html   # Complete markup, design tokens, styles, data, and scripts
└── README.md
```

## Local Preview

No installation or build step is needed. Open `index.html` directly in a browser, or run a local static server:

```bash
# Python
python -m http.server 8000

# Node
npx serve .
```

## Updating Content

All dynamic content is centralized in the `PORTFOLIO_DATA` object inside `index.html` (around line 2247):

- `cvUrl` — Add a public PDF link (e.g. Google Drive) for the **Download CV** button. Leaving it empty triggers the built-in print-to-PDF resume view.
- `contact` — Email address and WhatsApp number used by the brief composer and footer links.
- `clients` — Client names and Google Drive file IDs for the marquee logos.
- `behanceProjects` — Project metadata, Behance IDs (for modal embeds), URLs, and cover image IDs.
- `techFullVideos` / `techShorts` — Paste any YouTube URL or 11-character video ID into `youtubeUrl` to automatically load thumbnails and enable popup playback.
- `services`, `reviews`, `resources` — Accordion entries, testimonials, tutorials, shorts, and blog essays.

Images hosted on Google Drive use a multi-step fallback loader (`drive.google.com/thumbnail` -> `lh3.googleusercontent.com/d/` -> monochrome placeholder).

## Deployment

Because the project is purely static, it can be deployed directly to **GitHub Pages**, **Vercel**, **Netlify**, or **Cloudflare Pages** with the repository root as the publish directory and no build command.

## Links

- **Behance:** [behance.net/shaonshah](https://www.behance.net/shaonshah)
- **LinkedIn:** [linkedin.com/in/shaon36](https://www.linkedin.com/in/shaon36/)
- **Instagram:** [@h3x_design6](https://www.instagram.com/h3x_design6/)
- **Email:** shaonshah36@gmail.com
