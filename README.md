# education-recap

Pages from the House of the People's education phase (Second Sitting on AI), served with GitHub Pages and embedded in the House of the People site on Webflow.

## What's here

| Path | What it is | On the site |
|---|---|---|
| `glossary/index.html` | The AI glossary: fourteen key words about AI, explained plainly, laid out like the glossary slide from Session 1. One self-contained page (fonts inlined, no outside requests). | `houseofthepeople.uk/community-glossary` |
| `webflow/community-glossary.html` | The snippet to paste into a Webflow Embed element on that page. It shows the glossary full height, and term links scroll the page. | |

Still to come: the members' recap ("What the House Heard"), once its edits are finished.

## Publishing

1. In the repository's **Settings → Pages**, set the source to **Deploy from a branch**, branch `main`, folder `/ (root)`.
2. The glossary is then at `https://yazash123.github.io/education-recap/glossary/`.
3. In Webflow, on the `/community-glossary` page, add an **Embed** element and paste in `webflow/community-glossary.html`. Publish the site.

A link such as `houseofthepeople.uk/community-glossary#chatbot` opens the glossary at that term.

## Privacy

Members are anonymous. Nothing in this repository names a member.
