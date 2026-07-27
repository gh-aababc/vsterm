# Changelog

All notable releases are published as binaries on
[GitHub Releases](https://github.com/vesaaa/vsterm/releases).

Source development is private; tags that trigger CI live in this repository.
On each `v*` tag, CI also syncs `README.md`, `README.zh-CN.md`, `CHANGELOG.md`,
and `LICENSE` to the public `vesaaa/vsterm` main branch, and copies this file’s
section for that version into the GitHub Release notes.

## [1.1.8] — 2026-07-27

### Added
- Toolbox **IP Quality Check**: queries `api.ibxq.com` fraud data (risk score bar, operator/line, location, IP type, cloud vendor identity, blacklists, bots, proxies).
- Local public IPv4/IPv6 chips next to Check (via `curl` / `ipv4.ip.sb` · `ipv6.ip.sb`); click to fill the target field.
- Path Trace is toolbox-only (no longer a top tab); Toolbox also keeps Traceroute.

### Changed
- IP Quality layout polish: paired ISP/Org and postcode/timezone rows; IP-type chips (yes-only, centered); vendor / blacklist chip grids.

### 中文
- **新增**：工具箱「IP质量检测」（欺诈分、运营商、地理位置、IP 类型、大厂身份、外部黑名单、Bot、代理）；本机公网 IPv4/IPv6 标签可点击填入；路径追踪仅保留工具箱入口。
- **改进**：IP 质量面板排版（双字段对齐、类型色块居中、黑名单方框+尾部色块等）。

## [1.1.7] — 2026-07-27

### Changed
- Path Trace default target is `8.8.4.4` (was `www.baidu.com`).
- CI: public `vesaaa/vsterm` Release and docs sync only after **all** platform builds succeed (draft staging; incomplete builds are aborted).

### 中文
- **改进**：路径追踪默认目标改为 `8.8.4.4`；Release CI 等全部平台构建成功后再公开发布与同步文档，避免缺包。

## [1.1.6] — 2026-07-26

### Added
- Preferences: when setting a master password for the first time, **Screen lock** is checked by default (and persisted after a successful set).
- Preferences → Data directory: help text notes that the default folder is `.vsterm`; the path field supports typing/paste and a right-click Copy/Paste menu.
- Fresh installs default the desk pet to the **bottom-edge dog**.

### Changed
- Session tree folders use a macOS-style `>` disclosure chevron (rotates when open).
- Left-click a folder icon/name expands or collapses children; right-click still opens the context menu (add server, rename, …).

### Fixed
- Folder name hover no longer shows the text I-beam cursor (arrow cursor instead).

### 中文
- **新增**：首次设置主密码时默认勾选屏幕锁；数据目录说明标明默认 `.vsterm`，路径可粘贴；首次安装默认启用底部小狗桌面宠物。
- **改进**：文件夹折叠箭头改为 macOS 风格 `>`；左键点名称展开/收起，右键可添加服务器等。
- **修复**：服务器列表里文件夹名悬停光标恢复为箭头。

## [1.1.5] — 2026-07-26

- CI: run release asset upload with bash on all runners (fixes Windows PowerShell failing on `set -euo pipefail`); bump actions/checkout to v5.

## [1.1.4] — 2026-07-26

- CI: tag releases upload assets directly to the public Release (skip Actions artifacts; avoids storage-quota failures).

## [1.1.3] — 2026-07-26

- Cut idle CPU: vsync on real GPUs (WARP still AutoNoVsync); stop tooltip popups from scheduling 60 fps redraws.
- macOS Dock / Launchpad icon: 10% transparent margin; runtime Dock glyph uses the same padded asset.
- macOS releases ship as drag-install DMGs; `tools/` (ip2region) lives inside `VsTerm.app/Contents/Resources`.

## [1.1.2] — 2026-07-24

- Verify private CI publishes Release assets (and docs) to public `vesaaa/vsterm`.

## [1.1.0] — 2026-07-24

- Fix terminal drag selection starting late (anchor at press origin so fast drags no longer skip the first characters).

## [1.0.49] — 2026-07-24

- SSH tunnels: one shared forward set per host across tabs; UI polish (icons, SOCKS5 defaults, panel height).

## [1.0.48] — 2026-07-23

- Six-locale UI, release polish, bilingual README.

## [1.0.47] — 2026-07-22

- Dual geo providers for path trace; network-connections filter refresh.

## [1.0.46] — 2026-07-21

- Commands panel: folders, icons, multi-line paste.

## Earlier

See [Releases](https://github.com/vesaaa/vsterm/releases) for the full history (`v1.0.0` … `v1.0.45`).
