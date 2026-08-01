# FlowConnect — Marketing Site

A single-file marketing site for **FlowConnect**, the effortless way to syndicate
channel data across the industrial supply chain to manufacturer, rep, and
distributor partners. Part of the Flow (FlowRMS) ecosystem.

## Contents

```
index.html          The entire site (HTML + CSS + JS, self-contained)
fc-shots/           Product screenshots used in the page
logos/              Partner/customer logos for the trust strip
```

Everything except the images lives in `index.html`. Fonts (Inter) load from Google
Fonts and the "Get a Demo" modal embeds a TidyCal booking calendar
(`flow/flow-connect`) — both require an internet connection to render.

## Run locally

Just open `index.html` in a browser, or serve the folder:

```bash
python3 -m http.server 8000
# then visit http://localhost:8000
```

## Deploy with GitHub Pages

1. Create a repo and push these files (with `index.html` at the repo root).
2. In the repo, go to **Settings → Pages**.
3. Under **Build and deployment**, set **Source: Deploy from a branch**,
   pick your branch (e.g. `main`) and folder `/ (root)`, then **Save**.
4. Your site publishes at `https://<username>.github.io/<repo>/`.

## Editing

- All copy, colors, and layout are in `index.html`.
- Brand palette (CSS variables near the top): blue `#2563eb`, orange `#f97316`,
  green `#10b981`. The "Get Data Flowing" cards are inline SVG mockups.
- To change the booking calendar, edit the `data-path` on the
  `.tidycal-embed` div near the bottom of `index.html`.
