# CDN

Images extracted from the global (GL) Dissidia Final Fantasy Opera Omnia client, served by GitHub Pages at <https://dffoogg.github.io/cdn/>. The art belongs to Square Enix. Do not edit these files by hand; the scripts below write them from the [game](https://github.com/dffoogg/game) archive.

| Folder | What it holds | Written by |
|---|---|---|
| `characters/<image_id>.png` | Each character's head from `stl_chara_event_<image_id>`, trimmed and at half size. `image_id` is in [resources](https://github.com/dffoogg/resources)' `characters.json`. | `npm run extract` in [resource-extractor](https://github.com/dffoogg/resource-extractor) |
| `field-maps/NNN.png` | Each field's painting. The display scales are in the field editor's `src/lib/field-maps.json`. | `npm run field-maps` in [field-editor](https://github.com/dffoogg/field-editor) |
| `game-icons/<name>.png` | The map markers and hex frames from `FieldMap_Hex.g1t`, with `manifest.json`. | `npm run game-icons` in [omnia-ui](https://github.com/dffoogg/omnia-ui) |

Each script writes into `../dffoogg-cdn`, this repo checked out next to it; `DFFOO_CDN_DIR` overrides that. Commit and push here afterwards, then the Pages workflow publishes the files.
