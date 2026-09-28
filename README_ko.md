# MelIyagi

**Freenet(Hyphanet)·I2P·BitTorrent 를 하나로 받는 다운로더 — 토렌트는 Tor·I2P 로 돌려서. 링크만 붙여 넣으면 어느 네트워크인지 알아서 압니다.**

[English](README.md) · [한국어](README_ko.md)

## 왜 MelIyagi 인가

- **네트워크 셋, 창 하나.** Freenet 키, `.i2p` 주소, 마그넷 링크, `.torrent` 파일을 모두 같은 칸에 넣습니다. MelIyagi 가 네트워크를 알아보고 받기 시작합니다.
- **내 IP 가 드러나지 않는 토렌트.** 새 토렌트는 기본이 **Tor 모드**입니다. 토렌트마다 I2P·직접 연결로 바꾸거나 직접 + Tor + I2P 를 동시에 돌릴 수 있습니다 — 오른쪽 클릭으로 바꿉니다.
- **누구와 연결됐는지 보입니다.** 상대가 경로별로 색이 다릅니다 — 직접, Tor(보라), I2P(초록).
- **Freenet 을 쉽게.** CHK·SSK·USK(최신판을 알아서 따라감)·KSK 키. 파일을 올리면 CHK 링크를 만들어 복사해 줍니다.
- **고른 것을 기억합니다.** 연결 모드는 저장돼 다시 켜도 그대로입니다.

## 기능

| 네트워크 | 붙여 넣는 것 |
|---|---|
| Freenet / Hyphanet | `freenet:CHK@…`, `USK@…/site/0/` |
| I2P | `http://xxx.i2p/path/file.zip` |
| BitTorrent | `magnet:?xt=…`, `.torrent` |

**BitTorrent 연결 모드:** 직접 · Tor · 직접 + Tor · I2P · 직접 + Tor + I2P

- Freenet 올리기(ClientPut), CHK 링크 자동 생성
- 미리보기(영상 › 이미지 › 문서), 폴더 열기, 시딩 시작
- 제목 표시줄에서 `.torrent` 바로 열기

## 다운로드

**[⬇ 최신 버전 받기](https://github.com/iyagicom/MelIyagi/releases/latest)**

| 내 시스템 | 받을 파일 |
|---|---|
| Ubuntu 24.04 · 데비안 | **ubuntu24.04** 가 붙은 `.deb` |
| Ubuntu 26.04 | **ubuntu26.04** 가 붙은 `.deb` |
| 페도라 · openSUSE | `.rpm` |
| 아치 · 만자로 | `.pkg.tar.zst` |
| 그 밖의 리눅스 | `.AppImage`(설치 없이 실행) 또는 `.zip` |

**함께 켜 둘 것** (쓰는 네트워크만):

| 용도 | 실행할 것 | 기본 포트 |
|---|---|---|
| Freenet | [Hyphanet](https://www.hyphanet.org) 노드 | FCP `9481` |
| I2P | `i2pd` | SAM `7656`, HTTP `4444`, SOCKS5 `4447` |
| Tor | `tor` | SOCKS5 `9050` |

## ⚠️ 알아 두세요

- MelIyagi 는 네트워크 클라이언트입니다. 어떤 콘텐츠도 제공하거나 보관하지 않습니다.
- Tor 와 I2P 는 별도 서비스이며 들어 있지 않습니다.
- Tor·I2P 를 거쳐도 완전한 익명이 보장되지는 않습니다. 직접 연결은 상대에게 내 IP 가 보입니다.
- 적용되는 법과 저작권 규정을 지키는 책임은 사용자에게 있습니다.
