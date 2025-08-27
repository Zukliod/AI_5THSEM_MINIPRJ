## Project overview

This repository is a small web project (see `INDEX.HTML`) that collects and displays place-related data and images. The site organizes imagery under `img/` (subfolders: `curr/`, `future/`, `past/`) and is intended to be paired with a community-maintained "placedata" dataset of place objects.

## What the placedata dataset is

The placedata dataset is a simple, shareable collection of place objects describing locations that appear (or should appear) on the site. Each placedata object documents a place with location, descriptive, and attribution fields so the site and downstream tools can use them consistently.

Example placedata object (JSON):

```
{
        "name": "India Gate",
        "lat": 28.6129,
        "lon": 77.2295,
        "demographics": "A landmark surrounded by open space and a memorial.",
        "changes": "The surrounding area has evolved to include more recreational facilities and better public infrastructure over decades.",
        "significance": "A war memorial honoring Indian soldiers, it's a major tourist attraction and a key symbol of the city.",
        "historicalImageUrl": "img/past/india_gate_1960s.png",
        "currentImageUrl": "img/curr/india_gate_2024.png",
        "futureImageUrl": "img/future/india_gate_2030.png"
}
```

Suggested fields (recommended):
- name (string)
- latitude (number)
- longitude (number)
- demographics (string)
- changes (string)
- images(array of file paths or URLs)

Keep objects small and focused. If you have many places, submit them as an array or multiple files.

## Why contribute

- Help make the site more useful and geographically comprehensive.
- Improve local knowledge, historical coverage, and image-to-data linking.
- Contributors receive credit in the dataset and (optionally) on the site.

## How to contribute

1. Fork this repository.
2. Add or edit placedata entries as JSON files under a `data/` folder (create it if missing). Options:
   - Single file: `data/placedata.json` containing an array of objects.
   - Per-place files: `data/places/<id>.json` (one object per file).
3. Include image files (if any) under `img/` and reference their relative path in the `images` field.
4. Open a Pull Request with a short description of what you added and the source of the data.

If you prefer, open an issue with a CSV, GeoJSON, or a link to a dataset and a short explanation and maintainers will help convert it.

## Contribution guidelines (quick)

- Use UTF-8 and valid JSON.
- Provide a source field and at least one of: coordinates or a verifiable name.
- Keep personally-identifying or private information out of the dataset.
- Prefer open-licensed imagery and data (CC-BY, CC0, OSM-compatible). If data is not open, note any restrictions in the `source` field.

## Validation and review

Contributions will be reviewed by maintainers for:
- JSON syntax and basic schema compliance
- Reasonable coordinates (valid lat/lon ranges)
- Image paths that point to existing files in the repo (or public URLs)

If you want automated checks, mention it in your PR and we can add a lightweight validator (JSON Schema or a small script).

## License and credit

By contributing via pull request you confirm you have the right to share the data under an open license. Please state the license or source in your PR (e.g., CC0, CC-BY 4.0, public domain).

Contributors will be listed in a `CONTRIBUTORS.md` or in the dataset metadata if requested.

## Contact / Questions

Open an issue for questions, dataset coordination, or bulk uploads. Maintainers will respond and help with formatting.

---

Thank you for considering a contribution — your place knowledge makes the project better and more useful for everyone.
