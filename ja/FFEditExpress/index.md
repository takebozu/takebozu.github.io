---
layout: default
title: FFEdit Express (macOS) — ffmpegによるロスレス動画トリミング
description: >-
  FFEdit Expressは、In点とOut点を指定して、その区間だけをffmpegの
  ロスレスコピーで書き出せる、シンプルなmacOS向け動画トリミングツールです。
image: /img/og/ffeditexpress.png
lang: ja
alternate_lang: en
alternate_url: /FFEditExpress/
---

# <img src="/img/icons/ffeditexpress_logo.png" height="32" align="top" alt="FFEdit Expressアイコン"> FFEdit Express (macOS)

FFEdit Express は、ffmpeg を使ったシンプルな動画トリミングツールです。In 点と Out 点を指定して、指定区間だけをロスレスコピーで書き出せます。再エンコードを行わないため高速で、画質の劣化もありません。

## スクリーンショット

<img src="/img/screenshots/ffeditexpress/main.png" alt="FFEdit Expressのスクリーンショット: タイムラインでIn点・Out点を設定し、ffmpegのロスレスコピーで区間を書き出し" style="max-width:720px; width:100%; height:auto; border-radius:8px;">

各操作の詳しい説明は[操作ガイド](/ja/FFEditExpress/guide-ja.html)をご覧ください。

## 主な機能

- **ロスレス書き出し** — 選択区間を ffmpeg の `-vcodec copy -acodec copy` で書き出し。再エンコードしないため高速で、画質の劣化もありません
- **タイムライン操作** — 再生ヘッド・In 点・Out 点をタイムライン上で直接ドラッグ。ドラッグ開始位置に最も近いハンドルが自動的に選ばれます
- **In / Out 点** — 「Set In」「Set Out」で現在位置を設定し、「Go to In」「Go to Out」で各点へジャンプ。In 点と Out 点の間の長さが画面に表示されます
- **細かい移動** — 0.1 秒から 30 秒まで、決まった刻みで前後に移動。現在位置を最も近い整数秒にスナップも可能
- **B/W フレームスキャン** — 0.5 秒以上続く白黒フレーム（シーン転換）を自動検出してタイムラインにマーカー表示。「Prev」「Next」で前後のマーカーへ移動できます
- **ffmpeg コマンドのコピー** — 表示される `ffmpeg …` コマンドをクリップボードにコピーし、ターミナルでそのまま実行することも可能
- **出力ファイル名の自動付与** — `_cut` 付きの出力パスを自動提案。同名ファイルが存在する場合は `_1`, `_2` … と自動的に連番を付与

## 必要環境

- macOS 14 以降
- ffmpeg（Homebrew でのインストール推奨: `brew install ffmpeg`）

## ダウンロード

[FFEdit Express v1.0 をダウンロード（.zip）](/downloads/FFEditExpress_v1.0.zip)

1. ダウンロードした ZIP を展開します。
2. **FFEdit Express.app** を**アプリケーション**フォルダに移動します。
3. アプリケーションフォルダから起動します。初回起動時に macOS がブロックする場合は、アプリを右クリックして「**開く**」を選択してください。

動作には ffmpeg が必要です（上記「[必要環境](#必要環境)」を参照）。

[← Lucid Worksトップへ戻る](/ja/)
