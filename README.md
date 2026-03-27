# CMU Vending Map

> A community-maintained map of vending machines on Carnegie Mellon University's Pittsburgh campus.

**Live site:** https://cmu-mapping-club.github.io/vending-machines-cmu/ 

---

## About

Born from the r/cmu posts asking ["where are the vending machines?"](https://www.reddit.com/r/cmu/comments/2m7f9d/where_are_vending_machines_on_campus/?share_id=mkrj1mqg-X0kUNFp9tkdz&utm_content=1&utm_medium=android_app&utm_name=androidcss&utm_source=share&utm_term=1) — this is an open, community-editable map so the answer is always findable and always up to date.

## Features

- Interactive dark-themed map (OpenStreetMap + CARTO tiles)
- Search by building or floor
- Filter by type: Snacks, Drinks, Combo
- Status indicators: Operational / Limited stock / Unknown
- Every popup links directly to the GitHub edit page

## Contributing

Found a machine that's missing? Moved? Broken? **Please update the map!**

→ See [CONTRIBUTING.md](./CONTRIBUTING.md) for a step-by-step guide. No coding required.

The entire dataset is one file: [`vending-machines.json`](./vending-machines.json)

## Deploying your own

```bash
git clone https://github.com/CMU-Mapping-Club/cmu-vending-map
cd cmu-vending-map
# Open index.html in a browser - it works locally too!
```

To deploy to GitHub Pages:
1. Push to GitHub
2. Go to repo **Settings → Pages**
3. Set source to **Deploy from branch: main / (root)**
4. Done — live at `https://CMU-Mapping-Club.github.io/cmu-vending-map`

## Tech stack

| Layer | Tool | Cost |
|-------|------|------|
| Hosting | GitHub Pages | Free |
| Map tiles | CARTO Dark (OpenStreetMap) | Free |
| Map library | Leaflet.js | Free / MIT |
| Database | `vending-machines.json` in this repo | Free |
| CI/CD | GitHub Actions (optional) | Free |

---

*Maintained by the CMU community. Not affiliated with Carnegie Mellon University.*
