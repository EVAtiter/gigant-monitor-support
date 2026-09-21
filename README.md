# Gigant Monitor — Support

**Gigant Monitor** は、macOS のシステム状況を紫×黄の液体メーターで表現する
メニューバー常駐ユーティリティです。70 年代アニメ計器を思わせるアートワークで、
CPU 使用率・ネットワークトラフィック・ディスク I/O を「眺めて楽しむ」ためのツールです。

このリポジトリは Gigant Monitor の **サポート / 質問 / 要望 / 不具合報告** の窓口です。
下記 2 つの配布版に共通の窓口で、ソースコードの公開は行っていません。

---

## 入手

**2 通りの配布があります。どちらも無料で、機能の大半は共通です。**

### Mac App Store 版 —「Gigant Monitor」

https://apps.apple.com/app/gigant-monitor/id6777906549

Apple Silicon（M1 以降）専用。App Sandbox 有効。更新は App Store から届きます。

### 直接配布版 —「Gigant Monitor Plus」

Apple の公証済みバイナリを GitHub Releases と Homebrew で配布しています。

```
brew install --cask EVAtiter/tap/gigant-monitor-plus
```

- ダウンロード（zip）: https://github.com/EVAtiter/gigant-monitor-pro-release/releases/latest
- **Apple Silicon (arm64) 専用**です

App Store 版のすべての機能に加えて、**消費電力の表示**が使えます。

- **消費電力メーター**: CPU ウィンドウの表示内容を「CPU 使用率 ↔ 消費電力」で切り替え
- **電力・CPU タイムライン**: 上段に CPU 使用率、下段に消費電力の推移
  （App Store 版のタイムラインは CPU のみ）

Mac の SoC 全体の消費電力を読むには App Store のサンドボックスでは使えない API が必要なため、
この機能は直接配布版に限られます。逆に言うと、**消費電力に興味がなければ App Store 版で十分**です。

## 質問・要望・不具合報告

- 雑談・要望・使い方の質問 → **[Discussions](https://github.com/EVAtiter/gigant-monitor-support/discussions)**
- 明確な不具合 → **[Issues](https://github.com/EVAtiter/gigant-monitor-support/issues)**

日本語・英語どちらでも歓迎です。

## 主な機能

- **3 つの液体メーター**: CPU / ネットワーク (上り・下り) / ディスク (読み込み・書き込み)
- **3 つのタイムライン**: CPU / ネットワーク / ディスク の推移を、なめらかな曲線の面で表示。
  右端が現在で、左へ流れていきます（既定はオフ）
  - ネットワークは中心線から上へ「上り」、下へ「下り」
  - ディスクは中心線から上へ「Read」、下へ「Write」
- **初期配置は指標ごとに 1 列**。液体メーターの真下に対応するタイムラインが並ぶので、
  同じ指標の「いま」と「これまで」が縦に揃います
- 10 種の配色テーマをメニューから切り替え。液体の色・液体の透明度・パネルの透明度も調整でき、
  テーマごとに設定を保持します
- 各ウィンドウはサイズ・位置固定を個別に設定。全ウィンドウ共通で
  「常に最前面」「壁紙に貼り付ける」を切り替え
- **壁紙に貼り付ける**: ウィンドウをデスクトップ壁紙の一部のように振る舞わせ、
  Finder のアイコン配置を妨げません
- **画面下端で呼び出す**: 画面のいちばん下にマウスを 0.5 秒置くと、表示中のウィンドウを
  一時的に最前面へ（既定オフ）
- ネットワーク / ディスクは「直近のスライディングウィンドウ最大」をピークとして可視化
  （5 分 / 15 分 / 30 分 / 1 時間 / 無制限 から選択可能）
- マルチモニター環境ではディスプレイ別に位置を記憶
- メニューを開くと、現在値と直近ピークを数値でも確認できます
- 日本語 / 英語 UI 対応
- 低消費電力設計: アイドル時は自動でフレームレートを下げ、画面スリープ中や
  他のウィンドウに完全に隠れている間は描画を止めます
- アプリ自身は外部通信を一切行いません

## メーターの見た目（0 〜 100%）

値が増えるとメーターは「メタボール → 壁 → ギザギザ波形 → 赤い過負荷」と段階的に
変化します。各段階のスクリーンショットは [percent/README.md](percent/README.md) に
まとめてあります。

## プライバシー

Gigant Monitor は **データを一切収集しません**。詳細は [PRIVACY.md](PRIVACY.md) を参照してください。

## 動作要件

- macOS 14.0 Sonoma 以降
- Apple Silicon（M1 以降）専用

---

# Gigant Monitor — Support (English)

**Gigant Monitor** is a menu bar utility for macOS that visualizes your system
status through purple-and-yellow liquid meters inspired by 1970s anime
instrument panels. It's about atmosphere, not precision — a way to enjoy
watching CPU, network, and disk activity flow.

This repository is the **support / questions / requests / bug reports**
channel for Gigant Monitor. It serves both editions listed below.
Source code is not published here.

## Get the app

**Two editions are available. Both are free, and they share almost every feature.**

### Mac App Store — "Gigant Monitor"

https://apps.apple.com/app/gigant-monitor/id6777906549

Requires a Mac with Apple silicon (M1 or later). Sandboxed. Updates arrive through the App Store.

### Direct download — "Gigant Monitor Plus"

Notarized builds are distributed via GitHub Releases and Homebrew.

```
brew install --cask EVAtiter/tap/gigant-monitor-plus
```

- Download (zip): https://github.com/EVAtiter/gigant-monitor-pro-release/releases/latest
- **Apple Silicon (arm64) only**

It has everything the App Store edition has, plus **power consumption**:

- **Power meter**: switch the CPU window between CPU usage and power draw
- **Power & CPU timeline**: CPU usage on top, power draw below
  (the App Store edition's timeline shows CPU only)

Reading whole-SoC power draw requires an API that is not available inside the App Store
sandbox, so this is limited to the direct-download edition. If power draw isn't something
you care about, **the App Store edition is all you need**.

## Features

- **Three liquid meters**: CPU / Network (up & down) / Disk (read & write)
- **Three timelines**: CPU / Network / Disk history drawn as smooth filled curves.
  The right edge is now, and history flows to the left (off by default)
  - Network grows from a center line: upload above, download below
  - Disk grows from a center line: read above, write below
- **The default layout gives each metric its own column**, with the liquid meter on top
  and its timeline right below, so "now" and "recently" line up vertically
- 10 color themes; liquid color, liquid transparency, and panel transparency are all
  adjustable and stored per theme
- Per-window size and position lock; shared "Always on Top" and "Pin to Wallpaper" toggles
- **Pin to Wallpaper**: blend windows into the desktop wallpaper layer so Finder icons
  can be placed freely on top
- **Quick Reveal**: rest the cursor at the bottom of the screen for half a second to bring
  visible windows to the front (off by default)
- Network and disk are visualized against a sliding-window peak
  (5 / 15 / 30 min / 1 hour / unlimited)
- Per-display position memory for multi-monitor setups
- Open the menu to read current values and recent peaks as numbers
- Japanese / English UI
- Battery-conscious: reduces frame rate when idle, and stops drawing while the display
  sleeps or the window is fully hidden behind others
- The app itself makes no network connections of its own

## Ask questions / send feedback

- General discussion, feature requests, usage questions →
  **[Discussions](https://github.com/EVAtiter/gigant-monitor-support/discussions)**
- Clear-cut bugs → **[Issues](https://github.com/EVAtiter/gigant-monitor-support/issues)**

Posts in Japanese or English are both welcome.

## What the meter looks like (0–100%)

The meter progresses through stages — metaballs, a connected "wall", a jagged
sawtooth, and finally a red overload waveform — as the value climbs. See
[percent/README.md](percent/README.md) for a stage-by-stage gallery.

## Privacy

Gigant Monitor **collects no data of any kind**. See [PRIVACY.md](PRIVACY.md) for details.

## System requirements

- macOS 14.0 Sonoma or later
- Requires a Mac with Apple silicon (M1 or later).
