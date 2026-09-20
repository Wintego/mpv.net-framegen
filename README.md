# mpv.net-framegen

Portable mpv.net v7.1.2.0 x64 build with VapourSynth frame generation.

This repository distributes a cleaned portable build based on the official mpv.net portable release, with the frame generation functionality migrated from the DW build and reduced to a single tuned preset.

## Download

Download the archive from Releases:

[mpv.net-v7.1.2.0-portable-x64-framegen.zip](https://github.com/Wintego/mpv.net-framegen/releases/download/framegen-v7.1.2.0-memc-x2/mpv.net-v7.1.2.0-portable-x64-framegen.zip)

SHA256:

```text
856AC287BC5A150BF000C0D515039992CEB441ED429DA4732FD92A6D1774CBFE
```

## Frame Generation Hotkeys

Start playback in `mpvnet.exe`, then use:

| Hotkey | Mode |
| --- | --- |
| `Ctrl+1` | `MEMC_X2` — fps doubling at source resolution |
| `Ctrl+0` | Disable filters |

`MEMC_X2` doubles the frame rate at the source resolution on the CPU: 24 → 48, 25 → 50, 30 → 60. Sources at 32 fps and above bypass the filter, and frames above 1440p are downscaled before interpolation.

The preset settings were picked by measurement, not by guesswork: about thirty mvtools and svpflow configurations were compared on an objective reconstruction test and on measured power draw. The full write-up, including the results table and the three tunable parameters, ships in the archive as `portable_config/vs/README-memc.md`.

## Included Components

- mpv.net v7.1.2.0 portable x64 (libmpv v0.41.0-60-g85bf9f4ff)
- VapourSynth R70 portable runtime
- Embedded Python 3.12 runtime required by VapourSynth
- mvtools VapourSynth plugin (`libmvtools.dll` plus its required `libfftw3f-3.dll`)
- One frame generation profile, `MEMC_X2.vpy`

### Bundled portable_config

- `mpv.conf` - gpu-next / d3d11 renderer, HDR passthrough, night-mode audio compressor
- `input.conf` - frame generation hotkeys and menu entries
- `scripts/modernx.lua` + `thumbfast.lua` - modern OSC with seekbar thumbnails
- `scripts/auto-hdr.lua` + `bin/HDRCmd.exe` - automatic Windows HDR switching (from HDRTray)
- `scripts/long-video-rules.lua` - resume position for videos longer than 15 minutes, filter reset on file change
- `scripts/auto-close.lua` - close the player after the last file

The archive was cleaned to remove unrelated tools and AI upscaling assets from the source DW package. Personal data (watch history, shader cache, window state) is not included.

## Notes

This is an unofficial portable build. The original mpv.net project is available at:

[https://github.com/mpvnet-player/mpv.net](https://github.com/mpvnet-player/mpv.net)
