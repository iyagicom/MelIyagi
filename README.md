# MelIyagi v1.18.0

**Freenet + I2P + BitTorrent Integrated Downloader (Tor / I2P Routing Support)**

MelIyagi provides a unified downloader for Freenet, I2P, and BitTorrent, with optional Tor and I2P routing support.

Simply paste a URI, and MelIyagi automatically detects the network and starts the download.

> ### ⚠️ Usage Notice
>
> - MelIyagi is a network client and does not provide or host downloaded content.
> - Tor and I2P are external network services and are not included with MelIyagi.
> - Routing traffic through Tor or I2P does not guarantee complete anonymity.
> - Users are responsible for complying with all applicable laws, regulations, and copyright requirements.
> - The developer does not control or determine how users use external networks or downloaded content.

---

## Key Features

### Supported Networks

| Network | URI Example | Description |
|---|---|---|
| **Freenet** | `freenet:CHK@abc...` `USK@pub.../site/0/` | Decentralized immutable storage |
| **I2P** | `http://xxx.i2p/path/file.zip` | Anonymous network routing |
| **BitTorrent** | `magnet:?xt=...` `.torrent` | P2P downloading with multiple connection modes |

### BitTorrent Connection Modes

Connection modes can be switched using the right-click menu.

| Mode | Description | Network |
|---|---|---|
| Direct | UPnP/DHT/LSD enabled | Direct connection |
| Tor | Via SOCKS5 (9050) | Tor |
| Parallel Direct + Tor | Two sessions simultaneously | Direct + Tor |
| I2P | Via SOCKS5 (4447), `.i2p` only | I2P |
| Full Direct + Tor + I2P | Three sessions simultaneously | Direct + Tor + I2P |

Peer sessions are identified as **Direct**, **Tor (Purple)**, or **I2P (Green)**.

> **Note:** Direct connections may expose the user's IP address to peers.
> Users should select the connection mode appropriate for their intended use.

### Supported Freenet Key Types

- `CHK` — Content Hash Key (file downloads)
- `SSK` — Signed Subspace Key (sites)
- `USK` — Updatable Subspace Key (automatically tracks the latest edition)
- `KSK` — Keyword Signed Key

### Freenet Upload

Right-click a file → **ClientPut** → Automatically generate a CHK URI → Copy to clipboard.

### File Management

Right-click a completed or downloaded item to:

- **Preview** — Opens the first available file using the default application, with video > image > document priority
- **Open Folder** — Opens the download folder in the file manager
- **Start Seeding** — Manually resumes seeding of a completed torrent

### Connection Mode Persistence

- New torrents use **Tor mode by default**.
- The selected connection mode is saved in the session file and restored after restarting the application.
- `.torrent` files can be opened quickly using the 📂 button in the title bar.

---

## Installation

### Prerequisites

**For Freenet downloads:**

- Run a [Hyphanet](https://www.hyphanet.org) node separately.
- Default FCP address: `127.0.0.1:9481`

**For I2P routing:**

- Install and run `i2pd` separately.
- Default I2P SAM port: `7656`
- Default I2P HTTP proxy port: `4444`
- Default I2P Torrent SOCKS5 port: `4447`

**For Tor routing:**

- Install and run Tor separately.
- Default Tor SOCKS5 port: `9050`

### Ubuntu / Debian

Install the provided `.deb` package:

```bash
sudo dpkg -i meliyagi_1.18.0_amd64.deb
meliyagi
```

No source code or compiler is required to run the distributed package.

---

## Usage

1. Launch MelIyagi.
2. Start `i2pd` separately when using I2P.
3. For Freenet, run a Hyphanet node separately.
4. Start Tor separately when Tor routing is required.
5. Paste a Freenet, I2P, or magnet URI into the URI input field, or open a `.torrent` file.
6. Right-click a torrent to select the connection mode:

   * Direct
   * Tor
   * Parallel Direct + Tor
   * I2P
   * Full Direct + Tor + I2P
7. After the download is complete, right-click the item and select **Preview** or **Open Folder**.

---

## Settings

| Setting                    | Default          | Description                                  |
| -------------------------- | ---------------- | -------------------------------------------- |
| Freenet FCP                | `127.0.0.1:9481` | Local Freenet node                           |
| I2P SAM                    | `127.0.0.1:7656` | i2pd SAM port                                |
| I2P HTTP Proxy             | `4444`           | i2pd HTTP proxy                              |
| I2P Torrent SOCKS5         | `4447`           | i2pd SOCKS port                              |
| Tor SOCKS5                 | `9050`           | Tor proxy                                    |
| Default Torrent Mode       | Tor              | Default connection mode for new torrents     |
| Route Trackers Through Tor | Disabled         | Routes trackers through Tor when enabled     |
| Maximum Peers              | 200              | Maximum simultaneous connections per session |
| Direct Mode Port           | 6881             | BitTorrent listening port                    |
| Download / Upload Limit    | Unlimited        | KB/s                                         |
| Default Download Folder    | `~/Downloads`    | Default download location                    |

---

## License

Copyright (c) 2026 IYAGI-INC. All rights reserved.

This software is distributed **in executable form only**.

The source code is not publicly available.

### Linux Version

The Linux version may be freely used, installed, packaged, and redistributed for:

* Personal use
* Commercial use
* Educational use
* Government use
* Organizational use

No source code is provided with the distributed binaries.

### Windows Version

The Windows version is distributed through the Microsoft Store.

Usage and licensing for the Windows version are managed through the Microsoft Store.

> ⚠️ **Usage Notice**
>
> Freenet and I2P are communication networks that may be subject to different laws and regulations depending on your jurisdiction.
>
> Users are responsible for complying with all applicable laws, regulations, and copyright requirements.

---

# 한국어

### 한국어 README

# MelIyagi v1.18.0

**Freenet + I2P + BitTorrent 통합 다운로더 (Tor / I2P 라우팅 지원)**

MelIyagi는 Freenet, I2P, BitTorrent를 하나의 다운로더에서 사용할 수 있도록 지원하며, 선택적으로 Tor 및 I2P 라우팅을 사용할 수 있습니다.

URI를 붙여넣으면 네트워크를 자동으로 감지하여 다운로드를 시작합니다.

> ### ⚠️ 사용 고지
>
> - MelIyagi는 네트워크 클라이언트이며 다운로드되는 콘텐츠를 제공하거나 호스팅하지 않습니다.
> - Tor와 I2P는 MelIyagi에 포함되어 있지 않으며 별도의 네트워크 서비스로 사용됩니다.
> - Tor 또는 I2P를 통한 라우팅이 완전한 익명성을 보장하는 것은 아닙니다.
> - 사용자는 모든 관련 법률, 규정 및 저작권 규정을 준수할 책임이 있습니다.
> - 개발자는 사용자의 외부 네트워크 이용 방법이나 다운로드한 콘텐츠를 통제하지 않습니다.

---

## 주요 기능

### 지원 네트워크

| 네트워크 | URI 예시 | 설명 |
|---|---|---|
| **Freenet** | `freenet:CHK@abc...` `USK@pub.../site/0/` | 분산 불변 스토리지 |
| **I2P** | `http://xxx.i2p/path/file.zip` | 익명 네트워크 라우팅 |
| **BitTorrent** | `magnet:?xt=...` `.torrent` | 다양한 연결 모드를 지원하는 P2P 다운로드 |

### BitTorrent 연결 모드

우클릭 메뉴에서 연결 모드를 변경할 수 있습니다.

| 모드 | 설명 | 네트워크 |
|---|---|---|
| 직접 연결 | UPnP/DHT/LSD 활성화 | 직접 연결 |
| Tor | SOCKS5 (9050) 경유 | Tor |
| 병렬 직접 + Tor | 두 세션 동시 사용 | 직접 + Tor |
| I2P | SOCKS5 (4447) 경유, `.i2p` 전용 | I2P |
| 전체 직접 + Tor + I2P | 세 세션 동시 사용 | 직접 + Tor + I2P |

피어 세션은 **직접**, **Tor (보라색)**, **I2P (초록색)**으로 구분됩니다.

> **참고:** 직접 연결에서는 사용자의 IP 주소가 피어에게 노출될 수 있습니다.
> 사용자는 자신의 목적에 적합한 연결 모드를 선택해야 합니다.

### 지원하는 Freenet 키 타입

- `CHK` — 콘텐츠 해시 키 (파일 다운로드)
- `SSK` — 서명된 서브스페이스 키 (사이트)
- `USK` — 업데이트 가능한 서브스페이스 키 (최신 에디션 자동 추적)
- `KSK` — 키워드 서명 키

### Freenet 업로드

파일 우클릭 → **ClientPut** → CHK URI 자동 생성 → 클립보드 복사

### 파일 관리

다운로드 항목을 우클릭하여 다음 기능을 사용할 수 있습니다.

- **미리보기** — 동영상 > 이미지 > 문서 순으로 첫 번째 파일을 기본 앱으로 열기
- **폴더 열기** — 다운로드 폴더를 파일 관리자에서 열기
- **시딩 시작** — 완료된 토렌트의 시딩을 수동으로 재개

### 연결 모드 저장

- 신규 토렌트는 **Tor 모드**를 기본으로 사용합니다.
- 선택한 연결 모드는 세션 파일에 저장되며 프로그램을 재시작해도 유지됩니다.
- 타이틀바의 📂 버튼으로 `.torrent` 파일을 빠르게 열 수 있습니다.

---

## 설치

### 사전 준비

**Freenet 다운로드:**

- [Hyphanet](https://www.hyphanet.org) 노드를 별도로 실행해야 합니다.
- 기본 FCP 주소: `127.0.0.1:9481`

**I2P 라우팅:**

- `i2pd`를 별도로 설치하고 실행해야 합니다.
- 기본 I2P SAM 포트: `7656`
- 기본 I2P HTTP 프록시 포트: `4444`
- 기본 I2P Torrent SOCKS5 포트: `4447`

**Tor 라우팅:**

- Tor를 별도로 설치하고 실행해야 합니다.
- 기본 Tor SOCKS5 포트: `9050`

### Ubuntu / Debian

제공된 `.deb` 패키지를 설치합니다.

```bash
sudo dpkg -i meliyagi_1.18.0_amd64.deb
meliyagi
```

배포된 패키지를 실행하는 데 **소스 코드나 컴파일러는 필요하지 않습니다.**

---

## 사용 방법

1. MelIyagi를 실행합니다.
2. I2P를 사용하는 경우 `i2pd`를 별도로 실행합니다.
3. Freenet을 사용하는 경우 Hyphanet 노드를 별도로 실행합니다.
4. Tor 라우팅을 사용하는 경우 Tor를 별도로 실행합니다.
5. URI 입력란에 Freenet, I2P 또는 magnet URI를 붙여넣거나 `.torrent` 파일을 엽니다.
6. 토렌트를 우클릭하여 연결 모드를 선택합니다.

   * 직접 연결
   * Tor
   * 병렬 직접 + Tor
   * I2P
   * 전체 직접 + Tor + I2P
7. 다운로드 완료 후 항목을 우클릭하여 **미리보기** 또는 **폴더 열기**를 선택합니다.

---

## 설정

| 항목                 | 기본값              | 설명                |
| ------------------ | ---------------- | ----------------- |
| Freenet FCP        | `127.0.0.1:9481` | 로컬 Freenet 노드     |
| I2P SAM            | `127.0.0.1:7656` | i2pd SAM 포트       |
| I2P HTTP Proxy     | `4444`           | i2pd HTTP 프록시     |
| I2P Torrent SOCKS5 | `4447`           | i2pd SOCKS 포트     |
| Tor SOCKS5         | `9050`           | Tor 프록시           |
| 기본 토렌트 모드          | Tor              | 신규 토렌트의 기본 연결 방식  |
| 트래커 Tor 경유         | 해제               | 활성화하면 트래커도 Tor 경유 |
| 최대 피어 수            | 200              | 세션당 최대 동시 연결 수    |
| 직접 연결 포트           | 6881             | BitTorrent 리스닝 포트 |
| 다운로드 / 업로드 제한      | 무제한              | KB/s 단위           |
| 기본 저장 폴더           | `~/Downloads`    | 기본 다운로드 위치        |

---

## 라이선스

Copyright (c) 2026 IYAGI-INC. All rights reserved.

본 소프트웨어는 **실행 파일 형태로만 배포됩니다.**

소스 코드는 공개되지 않습니다.

### Linux 버전

Linux 버전은 다음 모든 목적으로 자유롭게 사용, 설치, 패키징 및 재배포할 수 있습니다.

* 개인 사용
* 상업적 사용
* 교육 목적
* 정부 및 공공기관 사용
* 단체 및 조직 사용

배포되는 바이너리에는 소스 코드가 제공되지 않습니다.

### Windows 버전

Windows 버전은 Microsoft Store를 통해 배포됩니다.

Windows 버전의 사용 및 라이선스는 Microsoft Store에서 관리됩니다.

> ⚠️ **사용 고지**
>
> Freenet 및 I2P는 관할 지역에 따라 서로 다른 법률과 규정이 적용될 수 있는 통신 네트워크입니다.
>
> 사용자는 모든 관련 법률, 규정 및 저작권 규정을 준수할 책임이 있습니다.
