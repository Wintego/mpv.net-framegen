# mpv.net-framegen

Portable mpv.net v7.1.2.0 x64 build with VapourSynth frame generation profiles.

This repository distributes a cleaned portable build based on the official mpv.net portable release, with the frame generation functionality migrated from the DW build.

## Download

Download the archive from Releases:

[mpv.net-v7.1.2.0-portable-x64-framegen.zip](https://github.com/Wintego/mpv.net-framegen/releases/download/framegen-v7.1.2.0/mpv.net-v7.1.2.0-portable-x64-framegen.zip)

SHA256:

```text
BBEC1A15176AA440507F4EFCF88D5907D636146B4CDCD0AFAFA70D0DB2AEBACF
```

## Frame Generation Hotkeys

Start playback in `mpvnet.exe`, then use:

| Hotkey | Mode |
| --- | --- |
| `Ctrl+1` | mvtools x2 LQ |
| `Ctrl+2` | mvtools 60 fps |
| `Ctrl+3` | svpflow LQ |
| `Ctrl+4` | svpflow PRO |
| `Ctrl+0` | Disable filters |

Recommended default: `Ctrl+2` for a balanced 60 fps mode. Use `Ctrl+1` for lower load, especially with heavy 4K video.

## Included Components

- mpv.net v7.1.2.0 portable x64
- VapourSynth portable runtime
- Embedded Python runtime required by VapourSynth
- mvtools and svpflow VapourSynth plugins
- Four frame generation `.vpy` profiles

The archive was cleaned to remove unrelated tools and AI upscaling assets from the source DW package.

## Notes

This is an unofficial portable build. The original mpv.net project is available at:

[https://github.com/mpvnet-player/mpv.net](https://github.com/mpvnet-player/mpv.net)
