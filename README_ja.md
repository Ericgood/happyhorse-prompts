[![English](https://img.shields.io/badge/English-Switch-blue)](README.md) [![简体中文](https://img.shields.io/badge/简体中文-切换-blue)](README_zh.md) [![한국어](https://img.shields.io/badge/한국어-전환-blue)](README_ko.md) [![Español](https://img.shields.io/badge/Español-Cambiar-blue)](README_es.md)

<div align="center">
  <img src="assets/logo.png" alt="HappyHorse Logo" width="200">

  # 🐴 HappyHorse プロンプト集

  **[HappyHorse](https://happyhorses.io) AI動画生成プロンプトのコミュニティキュレーションコレクション**

  [![Awesome](https://awesome.re/badge.svg)](https://awesome.re)
  [![GitHub stars](https://img.shields.io/github/stars/Ericgood/happyhorse-prompt?style=social)](https://github.com/Ericgood/happyhorse-prompt)
  [![License: CC BY 4.0](https://img.shields.io/badge/License-CC%20BY%204.0-lightgrey.svg)](https://creativecommons.org/licenses/by/4.0/)
  [![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg)](https://github.com/Ericgood/happyhorse-prompt/pulls)

</div>

---

> **注意：** これはコミュニティ主導のプロジェクトです。著作権を侵害するコンテンツを見つけた場合は、[Issue を作成](https://github.com/Ericgood/happyhorse-prompt/issues)してください。

## 🐴 HappyHorse とは？

**HappyHorse-1.0** は、テキストから動画と音声を同時に生成する150億パラメータの統一Transformerモデルです。後処理のアフレコは不要です。2026年4月初旬に [Artificial Analysis](https://artificialanalysis.ai/) Video Arena リーダーボードに匿名で登場し、Seedance 2.0、Kling 3.0、PixVerse V6 などの既存モデルを超えて **第1位** を獲得しました。

### 主な特長

- 🏆 **AI Video Arena 第1位** — Elo 1333（テキスト→動画）、Elo 1392（画像→動画）
- 🧠 **150億パラメータ** — 40層シングルストリームTransformer、クロスアテンションなし
- 🎬 **動画＋音声同時生成** — ダイアログ、環境音、フォーリーを動画フレームと同時に生成
- 🗣️ **多言語リップシンク** — 中国語、英語、日本語、韓国語、ドイツ語、フランス語、広東語
- ⚡ **8ステップデノイジング** — DMD-2蒸留による高速推論、CFG不要
- 📖 **オープンソース** — ベースモデル、蒸留モデル、超解像モジュール、推論コード（商用利用権付き）

### アーキテクチャ

**シングルストリーム自己注意Transformer** を採用。テキストトークン、参照画像の潜在表現、ノイズ付き動画・音声トークンを1つのシーケンスで同時にデノイズします。最初と最後の4層はモダリティ固有のプロジェクションを使用し、中間の32層は全モダリティでパラメータを共有します。

> *「オープンソースコミュニティで、ゼロから本当の音声・動画の同時事前学習を行ったのは誰もいませんでした。」*
>
> — [36Kr HappyHorse レポート](https://eu.36kr.com/en/p/3757826958635781)

### リーダーボードランキング

| カテゴリ | Elo スコア | 順位 |
|:---|:---:|:---:|
| テキスト→動画（音声なし） | **1333** | 🥇 第1位 |
| 画像→動画（音声なし） | **1392** | 🥇 第1位 |
| テキスト→動画（音声あり） | 1205 | 🥈 第2位 |
| 画像→動画（音声あり） | 1161 | 🥈 第2位 |

*データ出典：[Artificial Analysis Video Arena](https://artificialanalysis.ai/)、2026年4月*

### 競合比較

| モデル | T2V Elo | 備考 |
|:---|:---:|:---|
| **HappyHorse-1.0** | **1333** | オープンソース、音声・動画同時生成 |
| Seedance 2.0 (720p) | 1273 | ByteDance、音声同期で優位 |
| SkyReels V4 | 1244 | $7.20/分 |
| Kling 3.0 1080p Pro | 1241 | $13.44/分 |
| PixVerse V6 | 1239 | $5.40/分 |

### 謎の正体

HappyHorse-1.0 の開発者は公式に確認されていません。Artificial Analysis は **「匿名」モデル** と説明しています。コミュニティの調査では、オープンソースの [daVinci-MagiHuman](https://github.com/BrightXiaoHan/MagiHuman) モデルに基づく反復最適化であり、Sand.ai や上海の GAIR ラボとの関連が示唆されています。命名は2026年が中国の干支で **午年（馬年）** であることと一致しています。

> *出典：[36Kr](https://eu.36kr.com/en/p/3757826958635781) · [WaveSpeed AI](https://wavespeed.ai/blog/posts/what-is-happyhorse-1-0-ai-video-model/) · [Apiyi 分析](https://help.apiyi.com/en/happyhorse-model-mystery-ai-video-lmarena-analysis-en.html)*

---

## 📊 統計

| プロンプト総数 | 注目 | 最終更新 |
|:---:|:---:|:---:|
| 7 | 7 | 2026年4月 |

---

## 🏆 公式デモ — HappyHorse で生成

これらのプロンプトは、HappyHorse の能力を示す公式デモです：物理認識モーション、流体力学、キャラクターアニメーション、時間的一貫性、同期音声生成。

---

### 1. 🎯 フラフープの子供

![注目](https://img.shields.io/badge/⭐_注目-公式デモ-FF4D00)

> 物理認識モーション — フープが腰から胸へ上がり、膝に下がり、床に落ちる。リアルな重量感と運動量。

#### 📝 プロンプト

```
A hula hoop spinning on a kid's waist, gradually climbing to their chest, then dropping
to knees, then clattering to the floor. They pick it up to try again.
```

<div align="center">
  <a href="videos/hula-hoop-kid.mp4">
    <img src="assets/thumbnails/hula-hoop-kid.jpg" width="700" alt="フラフープの子供 - プレビュー">
  </a>
  <br>
  <a href="videos/hula-hoop-kid.mp4">📥 動画をダウンロード</a> ・ <a href="https://x.com/i/status/2041591993386856448">🐦 ソース</a>
</div>

---

### 2. ⛳ ゴルフボールパット

![注目](https://img.shields.io/badge/⭐_注目-公式デモ-FF4D00)

> キャラクターの感情と物理の同期 — ゴルファーのボディランゲージがボールの各回転に合わせて変化。

#### 📝 プロンプト

```
A golf ball in a cup rolling around the rim three times before finally dropping in.
The golfer's body language matches each rotation. Audio: Ball rattle, exhale, plop.
```

<div align="center">
  <a href="videos/golf-ball-putt.mp4">
    <img src="assets/thumbnails/golf-ball-putt.jpg" width="700" alt="ゴルフボールパット - プレビュー">
  </a>
  <br>
  <a href="videos/golf-ball-putt.mp4">📥 動画をダウンロード</a> ・ <a href="https://x.com/i/status/2041591995106521352">🐦 ソース</a>
</div>

---

### 3. 🐱 猫とトースターの反射

![注目](https://img.shields.io/badge/⭐_注目-公式デモ-FF4D00)

> 反射レンダリング + 動物アニメーション — 猫がクロムのトースター表面を叩くと、歪んだ反射が叩き返す。

#### 📝 プロンプト

```
A cat staring at its own reflection in a toaster, paw tapping the chrome surface.
The distorted cat reflection taps back. Audio: Paw taps, confused meow.
```

<div align="center">
  <a href="videos/cat-toaster-reflection.mp4">
    <img src="assets/thumbnails/cat-toaster-reflection.jpg" width="700" alt="猫とトースター - プレビュー">
  </a>
  <br>
  <a href="videos/cat-toaster-reflection.mp4">📥 動画をダウンロード</a> ・ <a href="https://x.com/i/status/2041591996754903188">🐦 ソース</a>
</div>

---

### 4. ☕ バリスタラテアート

![注目](https://img.shields.io/badge/⭐_注目-公式デモ-FF4D00)

> 流体力学の傑作 — ミルクがクレマの下に沈み、突き破り、正確な手首の動きでロゼッタパターンを形成。

#### 📝 プロンプト

```
A barista creating latte art by pouring steamed milk into espresso. The white milk
submerges beneath the brown crema initially, then breaks through the surface as the
cup fills. The barista's wrist makes precise oscillating movements, creating a rosetta
pattern. The milk and espresso maintain their distinct colors while interacting at
the boundary. Audio: The gentle pour of liquid, the hiss of the steam wand in the
background.
```

<div align="center">
  <a href="videos/barista-latte-art.mp4">
    <img src="assets/thumbnails/barista-latte-art.jpg" width="700" alt="バリスタラテアート - プレビュー">
  </a>
  <br>
  <a href="videos/barista-latte-art.mp4">📥 動画をダウンロード</a> ・ <a href="https://x.com/i/status/2041591999061758171">🐦 ソース</a>
</div>

---

### 5. 🌸 花の開花と枯れのタイムラプス

![注目](https://img.shields.io/badge/⭐_注目-公式デモ-FF4D00)

> 2週間にわたる時間的一貫性 — 同じ花瓶、同じ窓、同じ角度。光は天候とともに自然に変化。

#### 📝 プロンプト

```
A flower blooming and wilting over two weeks, one photo per day. Same vase, same window,
same angle. Light changes with weather. Audio: Quiet domestic.
```

<div align="center">
  <a href="videos/flower-bloom-timelapse.mp4">
    <img src="assets/thumbnails/flower-bloom-timelapse.jpg" width="700" alt="花のタイムラプス - プレビュー">
  </a>
  <br>
  <a href="videos/flower-bloom-timelapse.mp4">📥 動画をダウンロード</a> ・ <a href="https://x.com/i/status/2039462980715524457">🐦 ソース</a>
</div>

---

## 🤝 コントリビュート方法

プロンプトの投稿を歓迎します！

### Pull Request で提出

1. このリポジトリを **Fork**
2. **プロンプトを追加** — 適切な `prompts/<category>/` フォルダに Markdown ファイルを作成
3. **PR を提出** — レビューしてマージします！

### Issue で提出

PR が面倒ですか？[Issue を作成](https://github.com/Ericgood/happyhorse-prompt/issues/new)してプロンプトを添付するだけで、こちらで追加します！

### ガイドライン

- ✅ オリジナルまたは共有許可のあるプロンプト
- ✅ 使用モデルを明記（例：HappyHorse）
- ✅ 期待される出力の説明を追加
- ✅ 動画/画像プレビューを強く推奨
- ❌ NSFW コンテンツ禁止
- ❌ 著作権キャラクターの複製禁止

## 📜 ライセンス

本プロジェクトは [CC BY 4.0](https://creativecommons.org/licenses/by/4.0/) ライセンスの下で公開されています。適切なクレジットを表示すれば、自由に共有・改変できます。

## 🌐 リンク

- 🐴 [HappyHorse 公式サイト](https://happyhorses.io)
- 📰 [36Kr：HappyHorse 詳細分析](https://eu.36kr.com/en/p/3757826958635781)
- 📊 [Artificial Analysis Video Arena](https://artificialanalysis.ai/)
- 💬 [ディスカッション](https://github.com/Ericgood/happyhorse-prompt/discussions)
- 🐛 [問題を報告](https://github.com/Ericgood/happyhorse-prompt/issues)

---

<div align="center">

**役に立ったら ⭐ をお願いします！**

HappyHorse コミュニティが ❤️ を込めて作成

</div>
