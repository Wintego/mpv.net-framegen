# mpv.net-framegen

Portable mpv.net v7.1.2.0 x64 build with VapourSynth frame generation profiles.

This repository distributes a cleaned portable build based on the official mpv.net portable release, with the frame generation functionality migrated from the DW build.

## Download

Download the archive from Releases:

[mpv.net-v7.1.2.0-portable-x64-framegen.zip](https://github.com/Wintego/mpv.net-framegen/releases/download/framegen-v7.1.2.0/mpv.net-v7.1.2.0-portable-x64-framegen.zip)

SHA256:

```text
E81C49A9B282F15153E9F89B98FDD801ABABF9AC8601316158B9E660893B513E
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

- mpv.net v7.1.2.0 portable x64 (libmpv v0.41.0-60-g85bf9f4ff)
- VapourSynth portable runtime
- Embedded Python runtime required by VapourSynth
- mvtools and svpflow VapourSynth plugins
- Four frame generation `.vpy` profiles

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
