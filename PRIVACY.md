# Gigant Monitor — プライバシーポリシー

**最終更新日**: 2026 年 6 月

## 概要

Gigant Monitor（以下「本アプリ」といいます）は、ユーザーから一切のデータを
収集しません。個人情報、利用状況、計測値のいずれも、本アプリの開発者および
第三者に送信されることはありません。

## 収集しない情報

本アプリは以下のいずれの情報も収集・送信しません:

- 氏名、メールアドレス、その他の個人を識別できる情報
- 位置情報
- 連絡先・カレンダー・写真・ファイル等のユーザーデータ
- 利用ログ、クラッシュレポート、解析データ
- アプリが計測した CPU 使用率・ネットワーク使用量の数値
- ネットワークパケットの内容、接続先、通信履歴

## 本アプリが読み取る情報

可視化のために以下の OS 提供 API をローカルで呼び出しますが、得た数値は
画面表示のみに使い、外部に送信しません。

- **CPU 使用率**: `host_processor_info` API（カーネルの CPU 負荷カウンタを取得）
- **ネットワークトラフィック**: `getifaddrs` + `if_data` API
  （インターフェイス全体の累積バイト数とリンク速度を取得。個別のパケットや
  接続先には一切アクセスしません）
- **プライマリインターフェイス名**: `SCDynamicStoreCopyValue` API
  （Wi-Fi / 有線の切替検知用に「en0」等のインターフェイス名のみ取得）

## ローカル保存

本アプリの設定（ウィンドウ位置・サイズ・透明度等）は、お使いの Mac の
**ユーザーごとの設定領域（UserDefaults / Sandbox コンテナ）にのみ**
保存されます。これらの設定値が外部に送信されることはありません。

## 通信

本アプリ自身は外部サーバーと通信しません。Mac App Store 経由のアプリ
アップデート時には Apple の標準的な仕組みが使われますが、これは Apple
社の管理下にあり本アプリの動作には含まれません。

## 子供の利用

本アプリは特定の年齢層を対象としていませんが、いずれの利用者からも
情報を収集しないため、子供を含むすべての利用者に対して同じ動作をします。

## 連絡先

プライバシーに関する質問は本リポジトリの
[Discussions](https://github.com/EVAtiter/gigant-monitor-support/discussions)
までお願いします。

---

# Gigant Monitor — Privacy Policy

**Last updated**: June 2026

## Overview

Gigant Monitor (the "App") **collects no data** of any kind. No personal
information, usage data, or measured values are transmitted to the developer
or any third party.

## What we do NOT collect

The App does not collect or transmit any of the following:

- Name, email address, or any personally identifiable information
- Location data
- Contacts, calendars, photos, files, or any user content
- Usage logs, crash reports, or analytics
- The CPU usage or network throughput numbers that the App measures
- Network packet contents, destinations, or connection history

## What the App reads locally

The App calls the following OS APIs locally for visualization. The values
are used only for on-screen display and are never transmitted externally.

- **CPU usage**: `host_processor_info` (reads kernel-level CPU load counters)
- **Network throughput**: `getifaddrs` + `if_data` (reads aggregate per-interface
  byte counters and link speed; individual packets and destinations are never
  inspected)
- **Primary interface name**: `SCDynamicStoreCopyValue` (reads only the
  interface name such as "en0" to detect Wi-Fi/Ethernet switching)

## Local storage

App settings (window position, size, opacity, etc.) are stored only in your
Mac's per-user preferences area (UserDefaults / sandbox container). These
values are never sent off the device.

## Network communication

The App itself does not communicate with any external server. App updates
go through Apple's standard Mac App Store mechanism, which is operated by
Apple Inc. and is not part of the App's own behavior.

## Contact

For privacy-related questions, please use this repository's
[Discussions](https://github.com/EVAtiter/gigant-monitor-support/discussions).
