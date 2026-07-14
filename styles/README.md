# Map Styles

This folder contains the seven Maptoolkit vector basemap styles, served at `https://styles.maptoolkit.org/`.

## The seven styles

| Style | Root file |
|-------|-----------|
| Summer (default) | `summer.json` |
| Light | `light.json` |
| Hiking | `hiking.json` |
| Winter | `winter.json` |
| Dark | `dark.json` |
| Street | `street.json` |
| Cycling | `cycling.json` |

Each style comes in three flavors: **default**, **language**, and **3D**.

## Default styles (this folder's root)

`summer.json`, `light.json`, `hiking.json`, `winter.json`, `dark.json`, `street.json`, `cycling.json`

Labels show the local language of the area. When a place name uses a non-Latin script (Cyrillic, Arabic, CJK, etc.), the label gets a second line with a Latin-script name, using whichever of `name_en` / `name_fr` / `name_es` / `name_de` is available first.

Served at:

```
https://styles.maptoolkit.org/summer.json
```

## Language versions (`ar/`, `cs/`, `de/`, `en/`, `es/`, `fr/`, `hi/`, `hu/`, `it/`, `ja/`, `ko/`, `pl/`, `zh/`)

Each of these 13 folders holds the same 7 styles, renamed with the language suffix, e.g. `en/summer-en.json`.

Labels use the translated name (`name_<lang>`) where a translation exists, otherwise fall back to the local `name`. Unlike the default styles, language versions show a single label line — no Latin-script subtitle.

Served at:

```
https://styles.maptoolkit.org/summer-en.json
https://styles.maptoolkit.org/hiking-ja.json
```

## 3D versions (`3d/`)

`3d/` holds the same 7 styles with terrain enabled — `terrain.source` points at the `rgb-tiles` raster-DEM source, with `exaggeration: 1`. Everything else, including labels, is identical to the default styles (local language, Latin-script subtitle for non-Latin names).

Served at:

```
https://styles.maptoolkit.org/summer-3d.json
```

## Deployment note

Regardless of the subfolder a file lives in here, every variant is served flat from the root of `styles.maptoolkit.org` — there is no `/en/` or `/3d/` path segment in the served URL, only in this repo.

## License

Please note the copyrights and terms of use for these styles: [License.md](../LICENSE.md)
