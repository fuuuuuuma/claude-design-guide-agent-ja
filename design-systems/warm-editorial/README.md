# warm-editorial

クリーム色の紙のような地に、セリフ（明朝・ローマン体）の見出しを合わせた温かいエディトリアル系デザインシステム。読み物としての心地よさを重視し、行間を広めに取って長文でも疲れにくい設計です。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

落ち着き・知性・手触り。白ではなくわずかに黄みのある地色を使うことで、画面でも紙に近い柔らかさが出ます。テラコッタ（焼き物のような赤茶）を差し色にして、上品さと温度感を両立。

## 想定業種・媒体

- オウンドメディア / ブログ / インタビュー記事
- 出版・ライフスタイル・食・旅のコンテンツ
- ブランドストーリーやコラムを読ませたいコーポレートサイト

## 使いどころ

- 記事本文: `bg` のクリーム地に `ink` で組み、行間 `line-height-normal (1.8)` を基本に
- 見出し: セリフフォント＋`ink` または `primary`
- 引用・補足ブロック: `surface` を背景に、左罫を `accent`
- リンク・強調: `primary`（テラコッタ）

## 配色の意図

- 地色をクリーム `#fbf6ee` にすることで白の眩しさを抑え、長文の可読性を上げる
- 本文 `ink (#2b2118)` はほぼ黒に近い焦茶で、クリーム地に対して高コントラスト
- `ink-mid` はキャプションや日付などの補足に。地色に対しておよそ4.7:1を確保
- アクセントの `primary` / `accent` に白文字を乗せる場合は見出しサイズ以上で使用し、小さなラベルには使わない

## 推奨フォント

- 見出し: Noto Serif JP / Georgia（セリフ）
- 本文: Noto Serif JP / Hiragino Mincho ProN（明朝）
- 欧文中心なら Georgia 単体でも成立

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary | `--color-primary` | `#9a3412` |
| Secondary | `--color-secondary` | `#7c5c3b` |
| Accent | `--color-accent` | `#b45309` |
| Background | `--color-bg` | `#fbf6ee` |
| Surface | `--color-surface` | `#f4ead9` |
| Ink（本文） | `--color-ink` | `#2b2118` |
| Ink-mid（補足） | `--color-ink-mid` | `#6b5d4d` |
| Line（罫線） | `--color-line` | `#e2d4bf` |
| Success | `--color-success` | `#3f6212` |
| Warning | `--color-warning` | `#a16207` |
| Danger | `--color-danger` | `#b1402b` |

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
