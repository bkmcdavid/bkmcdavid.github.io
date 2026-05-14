# Site refresh — update notes

## What's in this update

```
site_update/
├── index.html                  ← replaces /index.html
├── css/
│   └── style.css               ← replaces /css/style.css
├── research/
│   └── index.html              ← replaces /research/index.html
├── teaching/
│   └── index.html              ← replaces /teaching/index.html
├── wine/
│   └── index.html              ← replaces /wine/index.html
└── img/
    ├── atheniancoins.jpg       ← replaces /img/atheniancoins.jpg (cropped border)
    └── olivegrove.jpg          ← replaces /img/olivegrove.jpg (cropped border)
```

Drop these into the repo in matching locations. Everything else (other images, PDFs, CNAME, habits/, syllbuild/) is untouched.

## What changed this round

- **Homepage bio updated.** Added second paragraph announcing the January 2027 move to the Hamilton School at University of Florida. First paragraph (Chapman / Smith Institute / "values, organization, productivity, and the good life") is kept verbatim.
- **Workshop callout repurposed** from submission solicitation to a pointer. CTA button is now "Details" linking to the meeting page.
- **Contact email updated** to bmcdavid at gmail dot com.
- **Removed the "Philosophy · Chapman University" eyebrow** above your name on the homepage.
- **Removed the page titles** ("Areas of inquiry" / "Courses" / etc.) from the research, teaching, and wine pages — they now begin directly with the first section block.
- **Footer text** changed to "Chapman University Smith Institute for Political Economy and Philosophy" on all four pages.

## Research page — bigger structural change

The research page is now dramatically shorter. Each area shows:

1. A short 1–2 sentence summary (no more "Read more" toggles)
2. The list of papers (no more "Abstract" toggles either — the papers and journals are visible directly, just click through for the PDF)

The summaries I wrote for you, drawing from your existing prose:

- **Ancient Political Economy** — *My research in this area focuses on the economic insights of Plato, with one project developing a thread through Aristotle as well (draft available upon request).*
- **Plato's Theory of Human Nature** — *Most scholars have focused on the* Republic*'s account of nurture and education at the expense of its account of nature. My research in this area explores how Plato conceives of nature as a cause prior to nurture.*
- **Adam Smith's Eudaimonism** — *Scholars agree Smith was an avid reader of classical philosophy, but disagree about which ideas he adopted and to which school he was most loyal. My research in this area focuses on Smith's use of ancient frameworks for constructing his own moral theory.*
- **Trust in AI** — *The benefits of AI tools are on the far side of fostering trust between human principals and their AI agents. My research in this area explores that trust relationship in human-AI iterations of principal-agent relationships.*

The longer descriptions (your "contentious view" paragraph, the Aristotle "political animal" passage, the "three primary kinds of people" framing, etc.) are gone from the page. They still exist in the old version of the file if you want to bring any of them back. I'd be happy to reinstate any specific piece, or restructure further.

## Images

The atheniancoins.jpg and olivegrove.jpg files had thin baked-in dark borders that were showing as visible bands when displayed at the section-image aspect ratio. I auto-cropped them — the olive grove dropped from 800×635 to 782×625, the Athenian coins from 1280×851 to 1228×535.

I also changed the section-image CSS from fixed-height with background-image to aspect-ratio with proper `<img>` tags and `object-fit: cover`. This is more reliable and handles odd image dimensions more gracefully.

## Things I didn't touch (carrying over from previous notes)

- **City of Pigs page range** still shows `pp. 57–594` in the research entry. Probably `pp. 574–594`. Flagging again.
- **Headshot** still uses McDavidheadshot.jpg.
- **habits/** and **syllbuild/** untouched.
- **No favicon** added.

## Preview & deploy

Run a local server from the repo root to preview before pushing:

```
python3 -m http.server 8000
```

Then open http://localhost:8000/ in a browser. Absolute paths like `/img/...` only resolve under a real server, not `file://`.
