# MelIyagi

**One downloader for Freenet (Hyphanet), I2P and BitTorrent — with torrents routed over Tor or I2P. Paste a link, and it knows which network to use.**

[English](README.md) · [한국어](README_ko.md)

## Why MelIyagi?

- **Three networks, one window.** Freenet keys, `.i2p` addresses, magnet links and `.torrent` files all go into the same box. MelIyagi detects the network and starts.
- **Torrents that don't show your IP.** New torrents start in **Tor mode** by default. Switch any torrent to I2P, direct, or run direct + Tor + I2P side by side — right-click to change.
- **See who you're talking to.** Peers are colored by route: direct, Tor (purple) or I2P (green).
- **Freenet made easy.** CHK, SSK, USK (follows the newest edition automatically) and KSK keys. Upload a file and get its CHK link copied for you.
- **Remembers your choices.** Connection modes are saved and restored after restart.

## Features

| Network | What you paste |
|---|---|
| Freenet / Hyphanet | `freenet:CHK@…`, `USK@…/site/0/` |
| I2P | `http://xxx.i2p/path/file.zip` |
| BitTorrent | `magnet:?xt=…`, `.torrent` |

**BitTorrent connection modes:** Direct · Tor · Direct + Tor · I2P · Direct + Tor + I2P

- Freenet upload (ClientPut) with automatic CHK link
- Preview (video › image › document), open folder, start seeding
- Open `.torrent` files from the title bar

## Download

**[⬇ Latest release](https://github.com/iyagicom/MelIyagi/releases/latest)**

| Your system | File to pick |
|---|---|
| Ubuntu 24.04 · Debian | `.deb` marked **ubuntu24.04** |
| Ubuntu 26.04 | `.deb` marked **ubuntu26.04** |
| Fedora · openSUSE | `.rpm` |
| Arch · Manjaro | `.pkg.tar.zst` |
| Any other Linux | `.AppImage` (run without installing) or `.zip` |

**What to run alongside** (only for the networks you use):

| For | Run | Default port |
|---|---|---|
| Freenet | a [Hyphanet](https://www.hyphanet.org) node | FCP `9481` |
| I2P | `i2pd` | SAM `7656`, HTTP `4444`, SOCKS5 `4447` |
| Tor | `tor` | SOCKS5 `9050` |

## ⚠️ Please note

- MelIyagi is a network client. It does not provide or host any content.
- Tor and I2P are separate services and are not included.
- Routing through Tor or I2P does not guarantee complete anonymity. A direct connection shows your IP to peers.
- You are responsible for following the laws and copyright rules that apply to you.
