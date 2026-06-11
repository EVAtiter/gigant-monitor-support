# Gigant Monitor — Support

**Gigant Monitor** は、macOS のシステム状況を紫×黄の液体メーターで表現する
メニューバー常駐ユーティリティです。80 年代アニメ計器を思わせるアートワークで、
CPU 使用率とネットワークトラフィックを「眺めて楽しむ」ためのツールです。

このリポジトリは Gigant Monitor の **サポート / 質問 / 要望 / 不具合報告** の窓口です。
ソースコードやバイナリの配布は行っていません。配布は Mac App Store 経由です。

---

## 入手

- Mac App Store: _(coming soon — リンクは公開後に追加)_

## 質問・要望・不具合報告

- 雑談・要望・使い方の質問 → **[Discussions](https://github.com/EVAtiter/gigant-monitor-support/discussions)**
- 明確な不具合 → **[Issues](https://github.com/EVAtiter/gigant-monitor-support/issues)**

日本語・英語どちらでも歓迎です。

## 主な機能

- 3 つの独立メーター: CPU / 下り (受信) / 上り (送信)
- 各メーターはサイズ・透明度・常時最前面・位置固定を個別に調整可能
- ネットワークは「直近 5 分のスライディングウィンドウ最大」をピークとして可視化
  （5 分 / 15 分 / 30 分 / 1 時間から選択可能）
- マルチモニター環境ではディスプレイ別に位置を記憶
- メニューバーにも数値を表示
- 日本語 / 英語 UI 対応
- アプリ自身は外部通信を一切行いません

## メーターの見た目（0 〜 100%）

値が増えるとメーターは「メタボール → 壁 → ギザギザ波形 → 赤い過負荷」と段階的に
変化します。各段階のスクリーンショットは [percent/README.md](percent/README.md) に
まとめてあります。

## プライバシー

Gigant Monitor は **データを一切収集しません**。詳細は [PRIVACY.md](PRIVACY.md) を参照してください。

## 動作要件

- macOS 14.0 Sonoma 以降
- Apple Silicon / Intel Mac 両対応（CPU メーターは公開 Mach API、
  ネットワークは `getifaddrs` ベースなのでアーキテクチャに依存しません）

---

# Gigant Monitor — Support (English)

**Gigant Monitor** is a menu bar utility for macOS that visualizes your system
status through purple-and-yellow liquid meters inspired by 1980s anime
instrument panels. It's about atmosphere, not precision — a way to enjoy
watching CPU usage and network traffic flow.

This repository is the **support / questions / requests / bug reports**
channel for Gigant Monitor. Source code and binaries are not distributed
here; the app is available exclusively via the Mac App Store.

## Get the app

- Mac App Store: _(coming soon)_

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
- Apple Silicon and Intel Macs are both supported.
