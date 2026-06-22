# minimal-saas

白基調に1色のアクセント（インディゴ）を効かせた、ミニマルなSaaS向けデザインシステム。情報密度が高い管理画面やダッシュボードでも視線が散らからないよう、彩度を抑えた配色と十分な余白で構成しています。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

清潔・中立・機能的。装飾を削ぎ落とし、コンテンツとデータそのものを主役にするトーン。アクセントは原則1色だけに絞り、ボタンやリンクなど「操作できる場所」に集中させます。

## 想定業種・プロダクト

- BtoB SaaS / 業務管理ツール / 管理画面（ダッシュボード）
- スタートアップのプロダクトサイト、ドキュメントサイト
- API・開発者向けの設定画面やコンソール

## 使いどころ

- 表・カード・フォームが多い画面: `surface` を背景の段差に、`line` を区切りに使う
- 主要アクション（保存・申し込み）: `primary` の塗りボタン＋白文字
- 補助アクション: `ink` の文字＋`line` の枠線（白背景の枠ボタン）
- リンクや軽い強調: `accent`

## 配色の意図

- 背景は純白 `#ffffff`、段差は `surface` のごく淡いグレーで「面」を分け、影に頼りすぎない
- 本文 `ink (#111827)` は白背景に対して高コントラストで長文も読みやすい
- `ink-mid` は補足テキスト・プレースホルダー用。白背景に対してコントラスト比およそ4.8:1を確保し、本文以外でも読める水準に
- アクセント地色（`primary` / `accent`）に小さい文字を乗せる場合は白文字を使い、文字サイズは14px以上を推奨

## 推奨フォント

- 見出し・本文ともに Inter（または system-ui / Helvetica Neue）
- 日本語は Hiragino Kaku Gothic ProN / Meiryo にフォールバック

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary | `--color-primary` | `#4f46e5` |
| Secondary | `--color-secondary` | `#6366f1` |
| Accent | `--color-accent` | `#0ea5e9` |
| Background | `--color-bg` | `#ffffff` |
| Surface | `--color-surface` | `#f7f8fa` |
| Ink（本文） | `--color-ink` | `#111827` |
| Ink-mid（補足） | `--color-ink-mid` | `#5b6472` |
| Line（罫線） | `--color-line` | `#e3e6eb` |
| Success | `--color-success` | `#15803d` |
| Warning | `--color-warning` | `#b45309` |
| Danger | `--color-danger` | `#b91c1c` |

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
