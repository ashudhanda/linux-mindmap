# Linux Mastery — Interactive Mind Map

An animated, monochrome (Vercel-style black & white) interactive mind map of the **complete Linux syllabus** — 19 modules, from absolute zero to DevOps-ready.

**Live site:** https://ashudhanda.github.io/linux-mindmap/

## What's inside

- **5 phases, 19 modules**, flowing top-to-bottom
- Every module expands into **topics → subtopics → key points** (4 levels deep)
- Each module also carries its **essential commands**, a **hands-on lab** with the **expected outcome**, and the **top DevOps interview question** with a strong-answer guide
- **Search** across every topic and command
- **Touch:** drag to pan on touch screens
- **Scroll to zoom** works the same in Firefox (line scrolling) as in Chrome (pixel scrolling)
- **Reduced motion:** with `prefers-reduced-motion` on, clicking the root box expands it at once instead of playing the ignite animation
- **Box counter** — the bottom-right pill counts how many boxes are currently shown (rendered nodes; panning them off-screen does not change the count). Per-module progress tracking is not implemented.
- **Panels stay out of the way** — centring a search or deep-link target and Fit both use the area left of the open details panel, so the target is never hidden behind it. On a narrow screen, where the panel covers almost the whole viewport, Fit and centring frame the full map instead, so it is laid out sensibly once the panel closes.
- **Theme** — the browser chrome colour (theme-color) follows the light/dark theme.
- **Deep links** (`#m7`), light-on-dark monochrome design with full motion

## Keyboard, deep links & search

- **Keyboard:** Tab to any box and press Enter/Space to expand it or open its details, just like clicking. Screen readers hear whether a box is expanded or collapsed. Esc closes the details panel and returns focus to the box that opened it — even if you opened another module's details while it was already open.
- **Deep links:** link straight to a module, e.g. `https://ashudhanda.github.io/linux-mindmap/#m7` opens module M7 on load — and changing the hash while the page is already open works too. An unknown id (e.g. `#m99`) says so in a toast instead of silently doing nothing. A phase/topic target also moves keyboard focus onto the box, so Enter/Space can expand it right away.
- **Search (Enter):** matches topic names, phase taglines, module summaries, essential commands, hands-on labs, expected outcomes, interview Q&A, and subtopic key points. Enter jumps to the first match and moves keyboard focus onto it, so Enter/Space can expand it right away. Pressing Enter again in the search box steps to the next match (the toast counts, e.g. Match 2 of 5); a new query starts over at the first match. Esc in the search box clears the query (with an empty query, Esc closes the details panel instead).

## Structure

```
index.html          → the site (single page, no build step)
data/syllabus.json  → all content: phases → modules → topics → subtopics → points
```

## Run locally

Just open `index.html` in a browser (the JSON loads via `fetch`, so serve over HTTP if your browser blocks `file://` fetches):

```bash
python3 -m http.server -d . 8000
# → http://localhost:8000
```

## Curriculum source

Topic order verified against RHCSA EX200 objectives, LFCS domains, KodeKloud, freeCodeCamp, Linux Journey, OverTheWire Bandit, and KillerKoda Linux scenarios.
