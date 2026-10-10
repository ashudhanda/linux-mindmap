# Linux Mastery — Interactive Mind Map

An animated, monochrome (Vercel-style black & white) interactive mind map of the **complete Linux syllabus** — 19 modules, from absolute zero to DevOps-ready.

**Live site:** https://ashudhanda.github.io/linux-mindmap/

## What's inside

- **5 phases, 19 modules**, flowing top-to-bottom
- Every module expands into **topics → subtopics → key points** (4 levels deep)
- Each module also carries its **essential commands**, a **hands-on lab**, and the **top DevOps interview question** with a strong-answer guide
- **Search** across every topic and command
- **Progress tracking** — modules you've opened are counted (saved in your browser)
- **Expand all / collapse all**, deep links (`#m7`), light-on-dark monochrome design with full motion

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
