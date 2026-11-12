# education-recap

Pages from the House of the People's education phase (Second Sitting on AI), served with GitHub Pages and embedded in the House of the People site on Webflow.

## What's here

| Path | What it is | On the site |
|---|---|---|
| `glossary/index.html` | The AI glossary: fourteen key words about AI, explained plainly, laid out like the glossary slide from Session 1. One self-contained page (fonts inlined, no outside requests). | `houseofthepeople.uk/ai-glossary` |
| `webflow/ai-glossary.html` | The snippet to paste into a Webflow Embed element on that page. It shows the glossary full height, and term links scroll the page. | |
| `recap/` | The members' recap, "What the House Heard": the education phase, Sessions 1–8. Built from the recap artifact: `recap.css` and `recap.js` (the page and its data), `slides/`, `thumbs/` and `img/` (pictures and clips), `links.json` (video playlists), and `index.html` (a standalone copy for checking, not indexed). | a members' page on Webflow |
| `webflow/recap-embed.html` | The snippet for one Webflow Code Embed element on that page. | |

## Publishing

1. In the repository's **Settings → Pages**, set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
2. The glossary is then at `https://yazash123.github.io/education-recap/glossary/`.
3. In Webflow, on the `/ai-glossary` page, add an **Embed** element and paste in `webflow/ai-glossary.html`. Publish the site.

A link such as `houseofthepeople.uk/ai-glossary#chatbot` opens the glossary at that term.

### The recap

The recap is too big for a Webflow embed (50,000-character cap), so the embed only loads `recap.css` and `recap.js` from GitHub Pages.

1. With Pages on (as above), the standalone copy is at `https://yazash123.github.io/education-recap/recap/`.
2. In Webflow, make the page and delete its navbar and footer. Add one **Code Embed** element **directly in the Body** (not in a Container) and paste in `webflow/recap-embed.html`. Nothing above it may have `overflow: hidden` or a transform, or the sticky parts stop sticking.
3. The Designer canvas does not run embeds, so it shows an empty box. **Publish to the `.webflow.io` address** and check it there before publishing to the main domain.
4. Links to a section work: `…/your-page#drivers`, `#futures`, `#s3`.

### Video playlists

`recap/links.json` holds the YouTube playlist for each session (`s1` … `s5`, `s6-7` for the weekend, `s8`) and `jacob_presentation` (the horizon-scan talk). A value can be a full YouTube link or just the playlist id. An empty value hides that button. The page reads this file each time it loads, so editing it on GitHub updates the site within a minute or two, with no Webflow change.

### Rebuilding

The recap is generated from the artifact's source by `build_web.py` (kept with the artifact source, not here). Don't hand-edit `recap.css` or `recap.js`; edit the source and rebuild.

## Privacy

Members are anonymous. Nothing in this repository names a member.
