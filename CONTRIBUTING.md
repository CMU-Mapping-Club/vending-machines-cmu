# Contributing to CMU Vending Map 🤝

Thanks for helping keep this map accurate! All the vending machine data lives in a single JSON file — no coding knowledge required to add or update a machine.

## How to add or update a machine

### Option A — GitHub web editor (easiest, no setup needed)

1. Open [`vending-machines.json`](./vending-machines.json) in this repo
2. Click the **pencil ✏️ icon** (top right of the file view)
3. Make your changes following the format below
4. Scroll down and click **"Propose changes"**
5. Submit the pull request — a maintainer will review and merge it!

### Option B — Pull request the normal way

```bash
git clone https://github.com/YOUR_USERNAME/cmu-vending-map
cd cmu-vending-map
# Edit vending-machines.json
git checkout -b add-my-building-machine
git commit -am "Add vending machine in My Building"
git push origin add-my-building-machine
# Then open a PR on GitHub
```

---

## JSON format

Each machine entry in `vending-machines.json` looks like this:

```json
{
  "id": "building-floor",
  "name": "Human-readable name",
  "building": "Full building name",
  "floor": "Floor and location hint",
  "type": "combo",
  "lat": 40.4433,
  "lng": -79.9436,
  "status": "operational",
  "hours": "24/7",
  "notes": "Optional notes like payment methods, restock schedule"
}
```

### Field reference

| Field | Required | Values |
|-------|----------|--------|
| `id` | ✅ | Unique slug, e.g. `"wean-3f"` |
| `name` | ✅ | Short display name |
| `building` | ✅ | Full building name |
| `floor` | ✅ | Floor + location description |
| `type` | ✅ | `"snack"` `"drink"` `"combo"` `"healthy"` |
| `lat` / `lng` | ✅ | GPS coordinates (right-click on Google Maps → "What's here?") |
| `status` | ✅ | `"operational"` `"limited"` `"out_of_order"` `"unknown"` |
| `hours` | — | e.g. `"24/7"` or `"8am–10pm"` |
| `notes` | — | Payment info, restock schedule, etc. |

### Machine types

- **`snack`** — Chips, candy, crackers, etc.
- **`drink`** — Water, soda, juice, coffee
- **`combo`** — Both snacks and drinks
- **`healthy`** — Protein bars, nuts, low-sugar options

---

## Finding coordinates

The easiest way to get lat/lng:

1. Go to [Google Maps](https://maps.google.com) and find the building entrance
2. Right-click the exact spot → click the coordinates that appear
3. They're copied to your clipboard!

For CMU buildings, you can also use the [CMU Campus Map](https://www.cmu.edu/about/visit/campus-map.html).

---

## Tips for good contributions

- **Be specific** with the floor/location — "3rd floor, near the elevator bank" is better than "3rd floor"
- **Update `lastUpdated`** at the top of the JSON to today's date (YYYY-MM-DD)
- **Mark status as `unknown`** if you're not sure — don't guess `operational`
- **One machine per PR** keeps reviews fast

---

## Code of conduct

Be kind! This is a community project run by students for students. If you see something wrong, just fix it. If something's broken, open an issue.
