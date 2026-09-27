# PRD: Personal Site (v1)

## Goal
A personal identity site that works as both a fast, credible signal for recruiters
and a deeper personal story for friends and acquaintances — showing who Olympia
is, what she has built, and the life and interests behind the work. Static site
(HTML, CSS, a little JavaScript) hosted on GitHub Pages.

## Audience and key action
- **Primary audience:** recruiters / hiring managers, who need a fast, scannable
  read on background, work, and trajectory.
- **Secondary audience:** friends and personal connections, who want more depth
  and story.
- **Key action:** on Home, a visitor scans an interactive timeline of Olympia's
  journey (education, work, achievements) and clicks any point to expand it
  in place (accordion-style — no navigation away). From there, projects and
  hobbies are one click away on their own pages, and the resume is one click
  away from Contact.

## Pages
Five pages, all reachable from a persistent top nav bar.

1. **Home** — the scrolling teaser and centerpiece.
   - Hero/intro: short headline, one line on who Olympia is.
   - Interactive timeline: click a point to expand achievement/job/project
     detail inline (accordion-style, no page change).
   - Work preview: a few featured projects, linking out to the full Projects
     page.
   - Hobbies preview: a few highlights (exchange, hackathon, sports), linking
     out to the full Gallery page.
   - Scroll-triggered reveal: images/text fade or slide in as they enter the
     viewport while scrolling down through the sections above.
   - CTA to Contact.

2. **About** — the deep dive. Full bio/story text: background, cultural
   exposure (exchange), hackathon experience, cross-industry work, values,
   what motivates her. More narrative than the Home timeline.

3. **Projects** — full portfolio. For each project: name, short description,
   the problem/goal, tools/technologies used, outcome/learnings, links
   (demo/repo/case study).

4. **Gallery** — photos from life, travel, and hobbies (exchange, hackathon,
   sports, everyday moments), with brief captions.

5. **Contact** — email address and LinkedIn/GitHub links shown directly on
   the page (LinkedIn/GitHub-style display, not a form), plus a downloadable
   resume PDF button.

## Navigation
A single persistent top nav bar on all five pages, linking to Home, About,
Projects, Gallery, Contact. On Home, the nav bar stays visible/sticky as the
visitor scrolls through the timeline, work preview, and hobbies preview
sections.

## Content (have / missing / from whom)
| Item | Status | From whom |
|---|---|---|
| Resume PDF | **Have** — ready to drop in | Olympia |
| Gallery photos (2 experience photos, 1 skiing photo) | **Have** — 3 photos ready; captions/labels still needed | Olympia |
| About bio text | **Missing** — to be written, using themes: exchange/cultural exposure, hackathon, cross-industry work, competitive sports | Olympia |
| Timeline entries (title, date, short description per point) | **Missing** — to be drafted alongside the bio | Olympia |
| Project write-ups (names, descriptions, tech, outcomes, links) | **Missing** — count and details not yet decided | Olympia |
| Contact details (email address, LinkedIn URL, GitHub URL) | **Missing** — need the actual links/address to display | Olympia |
| Additional gallery photos beyond the initial 3 | **Missing** — see Later | Olympia |

## Look (as values for a `:root` block)
Sunset-inspired gradient, cool-to-warm; clean modern sans-serif base. Provisional — refine exact shades once rendered.

```css
:root {
  /* palette */
  --color-blue: #2F6FED;
  --color-light-blue: #7FC7E8;
  --color-green: #4FBFA0;
  --color-yellow: #FFD866;
  --color-light-orange: #FFB067;
  --color-orange: #FF7A45;

  /* gradient, cool to warm */
  --gradient-sunset: linear-gradient(
    135deg,
    var(--color-blue),
    var(--color-light-blue),
    var(--color-green),
    var(--color-yellow),
    var(--color-light-orange),
    var(--color-orange)
  );

  /* base */
  --color-bg: #FFFDF9;
  --color-text: #1F2430;
  --color-text-muted: #5B6270;

  /* type */
  --font-base: "Inter", system-ui, -apple-system, sans-serif;
}
```

## Checks
A visitor must be able to:
1. On Home, click any point on the timeline and see it expand inline with
   detail, without leaving the page.
2. Click through from Home's work preview to the full Projects page and read
   at least one project's description, tech, and link.
3. Reach the Contact page from any other page via the nav bar and download
   the resume PDF.
4. Use the nav bar from any page to reach all five pages with no broken
   links.
5. Scroll down the Home page and see images/text reveal (fade/slide in) as
   they enter view, with the layout holding up at mobile width.

## Out of scope
- User accounts or logins
- Any server, database, or backend
- A content-management system for editing content without touching code
- A contact form that saves or emails submissions server-side (Contact page
  is static links + a mailto address instead)
- Comments or visitor-generated content
- Site search
- Multi-language support

## Later
- Code-free content editing (CMS), if wanted after v1
- A hosted form service (e.g. Formspree) for the Contact page, if submission
  tracking becomes desirable
- Expanding the Gallery beyond the initial 3 photos
- Adding more timeline entries as new achievements happen
- Upgrading scroll-triggered reveal to full layered parallax, if desired
- A writing/notes section or favorite books/music/inspiration page
- Visitor analytics
