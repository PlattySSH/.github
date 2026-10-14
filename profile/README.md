<div align="center">

<img src="https://plattyssh.github.io/assets/sol-256.png" alt="Sol" width="96" />

### Platty

A fast, native SSH client and terminal for Windows.

[Website](https://plattyssh.github.io) · [Docs](https://plattyssh.github.io/docs/) · [Download](https://github.com/PlattySSH/platty/releases)

</div>

We build Platty, an open-source SSH client written in Go that draws its whole interface on the GPU. No Electron and no web view: hosts, keys, tunnels, SFTP and snippets live in one calm window, encrypted on your PC.

The pieces that make it work are small Go libraries you can use on their own:

| Repository | What it is |
|---|---|
| [platty](https://github.com/PlattySSH/platty) | The app |
| [vt](https://github.com/PlattySSH/vt) | A VT terminal emulator with no GUI: parser, screen state, reflow and input encoding |
| [conpty](https://github.com/PlattySSH/conpty) | Start processes in a Windows pseudo console |
| [glyphs](https://github.com/PlattySSH/glyphs) | A cached glyph rasterizer with color emoji, font fallback and ligatures |
| [plattyssh.github.io](https://github.com/PlattySSH/plattyssh.github.io) | The website and documentation |

Everything is MIT licensed. Bug reports and ideas are welcome in [issues](https://github.com/PlattySSH/platty/issues).
