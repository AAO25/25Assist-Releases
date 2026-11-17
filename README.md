# 25Assist-Releases

Game data mirror for the [25Assist launcher](https://github.com/AAO25/25assist-launcher)
(America's Army 2.5 Assist).

The launcher downloads game files from this repository's **latest release** first, then
AAO25.com, then SourceForge:

```
https://github.com/AAO25/25Assist-Releases/releases/latest/download/<file>
```

## Release contents

| Asset | Purpose |
|---|---|
| `AAFiles.txt` | File list with MD5 hashes, used to verify and repair installs |
| `animations.7z`, `maps.7z`, `sounds.7z`, `textures.7z`, … | Full-game archives |
| `system-win.7z`, `system-lin.7z`, `alpulse.7z` | Windows and Linux system files |
| `dxweb.7z` | DirectX web setup |
| `AAFiles.<path>.7z` | Single-file repair archives. The game path's `\` becomes `.`, e.g. `Maps\Bridge.aao` → `AAFiles.Maps.Bridge.aao.7z` |

Release assets can't be in folders, so repair archives sit next to the full-game archives
instead of in an `AAFiles/` folder as on the other mirrors.

## Updating

Publish a new release marked **Latest** with the complete set of files. The launcher always
reads the latest release, so older releases can stay as history. Keep `AAFiles.txt` and the
archives in the same release so the hashes match the files.
