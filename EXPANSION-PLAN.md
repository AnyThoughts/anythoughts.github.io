# Website expansion plan: The Gospel and Crimson Zion

Date: September 15, 2026  
Repository: AnyThoughts/anythoughts.github.io  
Working branch: `site-2026-redesign`  
Status: planning document saved; expansion implementation has not begun.

## Purpose

Give visitors a clear presentation of the gospel and a place to discover Crimson Zion, while retaining Daniel Goodwin's author website as their shared home. Continue the site's lightweight, hand-coded, responsive, dignified Christian character.

This plan covers the phase after the September 12 redesign release. `REDESIGN-PLAN.md` records the original modernization proposal; its old inventory and implementation status are historical.

## Starting point

The repository was inspected on September 15, 2026. The development branch and `main` currently contain identical files, despite having different commit histories:

- Live baseline: `0630fbd36f1d0c0baff8d300b2f28c0e447813fa`.
- Development baseline before this document: `ff36b25119312d1b29a3b8e49236a16f6dd7fbfc`.
- Existing files: `index.html`, `dgstylesheet.css`, `Header.jpg`, `Me.jpg`, `CNAME`, and `REDESIGN-PLAN.md`.
- Homepage: introduction, About, seven book projects, Faith & Service, and Contact.
- Existing navigation: author name/home, About, Books, Faith & Service, and Contact.
- Existing presentation: midnight/forest colors, gold and parchment accents, established fonts, decorative borders, and a responsive navigation bar.

This was a source inspection, not a rendered browser review.

## Working agreement

- Save planning and development work on `site-2026-redesign`. Keep the live site on `main` while the expansion is developed.
- This task authorizes saving the plan. Discuss content and visual direction with Dan before substantial implementation, one area at a time.
- Preserve the existing domain, HTTPS configuration, and `CNAME`.
- Carry forward Dan's settled choices: current fonts and loading method, hidden vertical scrollbar, tested Books widths, footer treatment, and generous desktop navigation spacing.
- Reuse the existing design where it fits. Scope new styles carefully so new pages do not change established homepage layouts.
- Prepare a reviewable preview and changes before asking Dan to approve publication. Approval of this planning document is not approval to merge or deploy.

## Proposed site structure

| Page | File | Purpose |
| --- | --- | --- |
| Home | `index.html` | Preserve the author introduction, biography, books, Faith & Service, and contact; add clear routes to the two new pages. |
| The Gospel | `gospel.html` | Explain the good news of Jesus Christ and invite visitors to respond and ask questions. |
| Music / Crimson Zion | `music.html` | Introduce the music, provide a Spotify listening experience, and present releases and their message. |

Use the existing shared `dgstylesheet.css`. Place new music artwork in `assets/music/` with simple, descriptive filenames.

These filenames and the navigation below are recommendations to settle before coding.

## Order of work

### 1. Settle the page structure and navigation

Recommended navigation: author name linking home, then About, Books, Music, The Gospel, and Contact.

Faith & Service remains on the homepage with its existing `#faith` destination. Its section gains a clear link to the gospel page; a footer link can keep it directly accessible from the new pages.

On the new pages, homepage section links must include the homepage path, such as `index.html#about` and `index.html#contact`. A bare `#about` would incorrectly look for that section on the current page.

Review mobile wrapping and fixed-header spacing before settling the menu. Add a modest Crimson Zion introduction on the homepage, provisionally between Books and Faith & Service.

**Complete when:** Dan is comfortable with the page names, menu, and homepage placement.

### 2. Write the gospel presentation

Develop the message before its decorative treatment. Use a welcoming, personal voice that a visitor unfamiliar with Christianity can understand. Explain theological terms and let Scripture support the message.

Proposed reading sequence:

1. God is our Creator, holy and worthy of our trust.
2. We have sinned and need forgiveness and reconciliation with Him.
3. Jesus Christ, the Son of God, lived without sin, died for our sins, and rose bodily from the grave.
4. Salvation is God's gift of grace through faith in Christ; His finished work is its foundation.
5. Respond in repentance and faith, trusting Jesus rather than personal merit.
6. Following Christ includes learning His Word, prayer, baptism, fellowship, and growing obedience; these flow from salvation.
7. Offer a clear invitation to contact Dan with questions.

Suggested passages to review while drafting: Romans 3:23; 6:23; 5:8; 1 Corinthians 15:3–4; Ephesians 2:8–10; Mark 1:15; John 3:16. Select a focused set rather than crowding the page.

Use NKJV for quotations and verify wording and references before publication. Preserve consistency with the existing What I Believe statement. Present any suggested prayer as an expression of faith, never as a formula that earns salvation.

Working title: **The Hope Behind the Stories**. Navigation label: **The Gospel**. Both remain open for discussion.

**Complete when:** Dan has reviewed the full text, Scripture selection, title, and closing invitation.

### 3. Design and build the gospel page

Create a calm reading experience with short sections, clear headings, readable paragraph widths, and restrained use of existing gold/parchment decoration.

Use a compact page introduction and a clear contact link. Keep the gospel freely readable with no account, form submission, or music playback needed.

Build with semantic HTML and shared styles. Check existing broad selectors, including headings and header decorations, before reusing them on a new page.

**Complete when:** the reviewed message is readable and usable in a development preview on phone and desktop.

### 4. Prepare and build Crimson Zion's page

Give Crimson Zion a recognizable musical identity while retaining a visible connection to Daniel's site.

Proposed page sequence:

- Artwork, name, and a brief introduction to its Christian classic rock/hard rock sound.
- **Hear Crimson Zion:** one prominent Spotify embed.
- Releases: cover art, a short description, and verified Spotify and Amazon Music links.
- Behind the music: the message, inspiration, and an accurate account of Dan's creative process, including AI's role and his writing, direction, and final mixing.
- Contact and a natural link to the gospel presentation.

Recommended starting player: a small playlist of tracks Dan selects as the best introduction. An album or artist embed remains an option if it better fits his preferences.

Gather the final artwork, current release list, artist/release URLs, and chosen Spotify embed before building this page. Verify titles and destinations; do not invent identifiers or publish placeholder links.

Use Spotify's standard embed code. Keep direct listening links alongside it so visitors can continue if the player does not load. Let visitors initiate playback. Describe the action as **Listen** without promising a fixed preview length or full-song access for everyone.

Keep the player responsive and defer loading it until near the viewport where practical. Spotify supplies its own player resources; the surrounding site can remain ordinary HTML/CSS without custom player JavaScript.

**Complete when:** Dan has reviewed the music content and appearance, and the real player and release links have been checked.

### 5. Connect the pages and check the whole site

Add the homepage introductions, agreed navigation, and consistent footer links. Give each new page its own descriptive title and search description.

Check:

- Homepage links and cross-page links reach the intended section or page.
- The fixed navigation does not obscure headings or anchor destinations.
- Layouts work on narrow phones, tablets, and wide desktops, including Dan's monitor.
- Text remains readable at increased browser zoom; content does not overflow horizontally.
- Keyboard navigation and focus are visible; new images have meaningful descriptions and the player has a descriptive title.
- Spotify works as available in a regular window and a signed-out/private window; direct links remain usable when the embed is unavailable.
- Assets and embedded resources use HTTPS, and no audio starts unexpectedly.
- Existing About, Books, Faith & Service, Contact, fonts, and footer retain their intended behavior.

Use an available development preview and Dan's browser checks. Do not change the production Pages source merely to preview the branch.

**Complete when:** concrete layout or functional problems are resolved and Dan has reviewed the connected site.

### 6. Publish and leave maintenance notes

Prepare a pull request from `site-2026-redesign` to `main`, summarizing the expansion and the checks actually performed. Resolve any differences from intervening changes to `main` before release.

Publish after Dan approves the finished result. Verify the new public page URLs, navigation, artwork, listening links, and HTTPS after deployment.

Add a short maintenance guide covering where to edit gospel text, add a release, replace artwork, update the Spotify selection, and keep shared navigation/footer copies consistent. Keep HTML and CSS clearly organized with useful comments.

**Complete when:** the approved expansion is live and Dan can confidently make routine updates.

## Immediate next step

Discuss the proposed navigation and homepage placement, then draft the gospel presentation together. Music assets and listening links can be gathered when we reach the Crimson Zion phase; they do not block planning or gospel work.

## Spotify references

Official documentation checked September 15, 2026:

- [Creating an embed](https://developer.spotify.com/documentation/embeds/tutorials/creating-an-embed): supports tracks, albums, artists, and playlists using copied HTML.
- [Embed overview](https://developer.spotify.com/documentation/embeds): player sizing and presentation options.
- [Playback troubleshooting](https://developer.spotify.com/documentation/embeds/tutorials/troubleshooting): some situations limit playback to a preview under 30 seconds; preserve the generated player permissions and test actual behavior.
