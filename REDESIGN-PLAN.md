# Author website: 2026 redesign plan

Status: proposed direction; implementation has not started.

## Scope

Modernize Daniel Goodwin's existing hand-coded author website while preserving its Christian message, lightweight structure, responsiveness, and ease of maintenance.

- Production branch: `main`.
- Development branch: `site-2026-redesign`.
- Inspection baseline: `d3779487dd8e0139b9b87826da7812bb9d8279c1`.
- Preserve the existing custom domain in `CNAME`: `www.dgoodwin.us`.
- Keep development on the redesign branch. Merge and release only after Daniel's approval.

## Existing site

The repository contains `index.html`, `dgstylesheet.css`, `Header.png`, `Me.png`, and `CNAME`.

The page includes the statement "By His grace and for His glory.", a Christian author biography, four book entries, email and social links, and a June 2025 footer.

Current book listings:
- The Pendragon Legacy: Book One – The Light and the Lion: Coming Soon.
- Princess Rebecca and the Mirror in the Tower: Available Now, with an Amazon link.
- Princess Rebecca and the Sunshine Who Lost Her Way: In Development.
- The Pendragon Legacy: Book Two: In Development.

Review these statuses and the biography with Daniel before updating their factual content.

Source findings:
- Missing mobile viewport metadata and responsive breakpoints.
- Float-based layouts, fixed widths, and repeated line breaks for spacing.
- Footer positioned beyond the page width.
- jQuery is loaded but unused.
- Header artwork is 1536 × 1024 and about 2.78 MB; portrait is 1024 × 1024 and about 1.82 MB.
- This inspection covered source and image assets; browser testing has not been performed.

## Proposed direction

1. Retain a single HTML page and shared stylesheet, with no required JavaScript or framework.
2. Refine the existing identity using deep forest green, restrained gold, readable light text, dignified serif headings, and consistent spacing.
3. Reuse the existing artwork and portrait, preserving the Christian statement.
4. Arrange content as introduction, books, author biography, and contact.
5. Replace the book table with responsive entries that distinguish available and forthcoming works.
6. Replace floats and fixed layout dimensions with flexible layouts and readable text widths.
7. Improve semantic structure, link labels, image descriptions, keyboard focus, and touch usability.
8. Optimize image delivery while retaining original assets.
9. Organize CSS with shared color and spacing variables, and add concise maintenance instructions.

## Review and release

Check mobile and desktop layouts, keyboard navigation, links, image loading, and overflow before release. Confirm book statuses and biography accuracy. Present the redesign for Daniel's review before merging into `main` or changing the live deployment.
