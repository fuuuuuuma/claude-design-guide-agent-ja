# dark-developer

濃いダークグレーを背景にした、開発者向けの近未来デザインシステム。コードや管理画面を長時間見ても疲れにくいよう、彩度を抑えた発光色のアクセントを採用しています。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

クール・テクニカル・集中。GitHub のダークUIに近いトーンをベースに、ブルー・ミント・パープルの3アクセントで状態や種別を出し分けます。等幅フォント（`--font-mono`）も用意。

## 想定業種・媒体

- 開発者向けツール / CLI・API ドキュメント
- SaaS の管理コンソール、ログ・監視ダッシュボード
- 技術ブログ、エンジニア採用ページ

## 使いどころ

- 背景 `bg` の上にカードを `surface` で重ね、区切りは `line`
- リンク・主要操作: `primary`（ブルー）
- 成功・差分追加など: `secondary`（ミント）/ `success`
- ハイライト・特別な種別: `accent`（パープル）
- コードブロック: `--font-mono` ＋ `surface` 背景

## 配色の意図

- 背景 `#0d1117` に対して本文 `ink (#e6edf3)` を乗せ、高コントラストかつ目に痛くない明度に調整
- アクセント色は彩度を抑えた「発光色」。暗い背景上で読めるよう明るめにしている
- `primary` などのアクセントを地色に使い、その上に小さい文字を乗せる場合は暗い文字（`bg`）を使う。明るいアクセント地に白文字は避ける
- `ink-mid` は補足・コメント用。暗背景に対しておよそ6:1のコントラストを確保

## 推奨フォント

- 見出し: Space Grotesk / Inter
- 本文: Inter
- コード: JetBrains Mono / SFMono-Regular
- 日本語は Hiragino Kaku Gothic ProN にフォールバック

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary | `--color-primary` | `#6ea8fe` |
| Secondary | `--color-secondary` | `#7ee7c7` |
| Accent | `--color-accent` | `#c08cff` |
| Background | `--color-bg` | `#0d1117` |
| Surface | `--color-surface` | `#161b22` |
| Ink（本文） | `--color-ink` | `#e6edf3` |
| Ink-mid（補足） | `--color-ink-mid` | `#9aa4b2` |
| Line（罫線） | `--color-line` | `#2a313c` |
| Success | `--color-success` | `#4ade80` |
| Warning | `--color-warning` | `#fbbf57` |
| Danger | `--color-danger` | `#ff6b6b` |

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
