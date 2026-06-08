# awesome-motion.md

![awesome-motion.md animated logo](assets/logo-motion.svg)

AI Agent が視覚的に印象的で退屈ではない UI アニメーションを生成できるようにする、`MOTION.md` ファイルの厳選コレクションです。

[English](README.md) | [中文版](README.zh-CN.md) | [한국어](README.ko.md) | [العربية](README.ar.md)

## プレビューギャラリー

各プレビューは同じ UI 要素を使用しながら、それぞれの `MOTION.md` に基づいて異なるビジュアルスタイルとモーション動作を生成しています。

<table width="100%">
  <tr><td width="100%"><strong>Material Expressive</strong><br /><img src="assets/previews/material-expressive.gif" alt="Material Expressive preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Apple Fluid</strong><br /><img src="assets/previews/apple-fluid.gif" alt="Apple Fluid preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Fluent Productive</strong><br /><img src="assets/previews/fluent-productive.gif" alt="Fluent Productive preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Carbon Enterprise</strong><br /><img src="assets/previews/carbon-enterprise.gif" alt="Carbon Enterprise preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Linear Snappy</strong><br /><img src="assets/previews/linear-snappy.gif" alt="Linear Snappy preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Stripe Polished</strong><br /><img src="assets/previews/stripe-polished.gif" alt="Stripe Polished preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Vercel Minimal</strong><br /><img src="assets/previews/vercel-minimal.gif" alt="Vercel Minimal preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Framer Spring</strong><br /><img src="assets/previews/framer-spring.gif" alt="Framer Spring preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>GSAP Cinematic</strong><br /><img src="assets/previews/gsap-cinematic.gif" alt="GSAP Cinematic preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Game Impact</strong><br /><img src="assets/previews/game-impact.gif" alt="Game Impact preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Glitch Cyberpunk</strong><br /><img src="assets/previews/glitch-cyberpunk.gif" alt="Glitch Cyberpunk preview" width="100%" /></td></tr>
  <tr><td width="100%"><strong>Editorial Scroll</strong><br /><img src="assets/previews/editorial-scroll.gif" alt="Editorial Scroll preview" width="100%" /></td></tr>
</table>

## これは何ですか？

`MOTION.md` は、Cursor、Claude Code、OpenCode などの AI コーディング Agent のためのモーションデザイン・ルールブックです。

AI に単に「アニメーションを追加して」と依頼して一般的なフェード表現で終わらせるのではなく、イージングカーブ、 duration token、入場アニメーション、ホバー状態、スクロールトリガー、終了トランジション、アクセシビリティルール、アンチパターンまで含む具体的なモーション仕様を渡します。

## プロジェクト構成

```txt
awesome-motion-md/
├── assets/                # デモ GIF とビジュアルアセット
├── motion-md/            # モーションスタイルのルールブック
├── docs/                 # ガイドとサンプル
├── README.md             # 英語 README
├── README.zh-CN.md       # 中国語 README
├── README.ja.md          # 日本語 README
├── README.ko.md          # 韓国語 README
└── README.ar.md          # アラビア語 README
```

## モーションスタイル

モーションスタイルは `motion-md/` に配置され、各スタイルは独立した完全な `MOTION.md` ルールブックとして提供されます。

利用可能なスタイル:

```txt
motion-md/
├── material-expressive/MOTION.md
├── apple-fluid/MOTION.md
├── fluent-productive/MOTION.md
├── carbon-enterprise/MOTION.md
├── linear-snappy/MOTION.md
├── stripe-polished/MOTION.md
├── vercel-minimal/MOTION.md
├── framer-spring/MOTION.md
├── gsap-cinematic/MOTION.md
├── game-impact/MOTION.md
├── glitch-cyberpunk/MOTION.md
└── editorial-scroll/MOTION.md
```

| スタイル | 説明 |
| --- | --- |
| `material-expressive` | Material Design の expressive spring system に基づく、物理感のあるモーション。 |
| `apple-fluid` | Apple の空間的で直接操作感のある体験に着想を得た、静かで連続的なプレミアムモーション。 |
| `fluent-productive` | 生産性 UI 向けの高速で機能的、階層が明確なモーション。 |
| `carbon-enterprise` | 複雑なエンタープライズ製品に適した、正確でアクセシブルなモーション。 |
| `linear-snappy` | 小さな移動距離と明確な状態変化を持つ、超高速 SaaS モーション。 |
| `stripe-polished` | 奥行き、スタッガー、商用品質の洗練を重視したランディングページ向けモーション。 |
| `vercel-minimal` | ダーク UI と細かなフィードバックに適した、控えめな開発者ツール向けモーション。 |
| `framer-spring` | スプリング、ジェスチャー、レイアウトアニメーションを中心としたモーションパターン。 |
| `gsap-cinematic` | 高インパクトなマーケティングページ向けのタイムラインベースのシネマティックモーション。 |
| `game-impact` | 予備動作、インパクト、報酬表現を含むゲーム的なフィードバックモーション。 |
| `glitch-cyberpunk` | アクセシビリティ制約を含む、ネオン、スキャンライン、グリッチモーション。 |
| `editorial-scroll` | 記事、ローンチ、スクロールストーリーテリング向けのナラティブなスクロールモーション。 |

## 目標

AI が生成する UI を、意図があり、表現力があり、生き生きとしたものにすること。
