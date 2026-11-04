# OpsIdea Website — Backlog

Ideas and open threads for whenever this project picks back up. Nothing here is urgent — the site is live, stable, and fully verified as of 2026-11-04 (see `SESSION_HANDOFF.md`). This list exists so good ideas surfaced during the last session aren't lost, not as a new round-counting exercise.

## High priority — real, concrete

- [ ] **Add real GitHub repo descriptions.** `mail-guard`, `delete-guard`, `claude-webdesign-demo`, and `supplychain-sentinel-demo` currently show "No description yet." on the live site because that's genuinely true on GitHub. Set a real one-line description on each repo (GitHub repo Settings, or `gh repo edit <repo> --description "..."`) — the site pulls live from the API, so no code change is needed once set.
- [ ] **Decide on `Website_Building_AIS`.** It shows in the Recent Work grid as "OpsMind - DevOps & AI learning community landing page" — a different project name than the repo/site itself. Confirm whether it belongs in the public showcase, should be renamed, or excluded.

## Medium priority — worth considering

- [ ] **Verify the OG/Twitter preview card on real platforms.** This session confirmed `og-image.jpg` is live (HTTP 200) and the meta tags are correctly wired, but never ran it through Twitter's Card Validator or LinkedIn's Post Inspector against the actual live URL. Quick sanity check worth doing once, especially before sharing the link anywhere.
- [ ] **"Now Building" / writing section.** Floated early as a candidate direction and never built. If Stalin wants the site to be more than a static brochure (ongoing notes, a "what I'm building this week" blurb), this is real, honest content to add — not fabrication, since it would reflect real current work.
- [ ] **Re-run a full Lighthouse audit (desktop + mobile) before resuming work.** Confirms nothing regressed while the project was paused — GitHub API shape changes, Google Fonts CDN issues, etc. are all realistic drift sources for a site with live external dependencies.

## Low priority — optional hardening

- [ ] **Favicon PNG fallback.** Currently an inline SVG data URI. All current major browsers support SVG favicons, so this was deliberately deprioritized — only worth revisiting if a specific platform/tool is confirmed not to render it.
- [ ] **Split `index.html` into separate `/css` and `/js` files** if it grows meaningfully past its current ~620 lines. Not needed now — this was a soft ceiling noted in the original plan, not a current problem.
- [ ] **Privacy-friendly analytics** (e.g. Plausible) if Stalin wants visit data. Explicitly out of scope this session — would need a decision on provider and a signup, not something to add silently.
- [ ] **Expand `sitemap.xml`** if the site grows beyond a single page (e.g. a blog/notes section gets added).

## Explicitly rejected / not worth doing

- **Fabricated testimonials, stats, or project descriptions.** Ruled out as a hard constraint for the entire session — this is a real professional site, not a demo. Any future work should keep this rule.
- **Frameworks or a build step.** The site is intentionally plain static HTML/CSS/vanilla JS so it deploys as-is to GitHub Pages with zero tooling. Don't introduce React/Vue/a bundler/etc. without a real reason that outweighs that simplicity.

## Process note for next time

Two real bugs (a cramped 5-column repo grid, and a scroll-reveal section that could render fully invisible) were caught only by reviewing full-page screenshots — not by the per-round in-browser spot-checks done throughout most of the session. If resuming the "verify every round" discipline, make a full-page screenshot part of that check, not just a scrolled walkthrough.
