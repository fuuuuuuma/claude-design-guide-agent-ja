# luxury-premium

漆黒の背景にゴールドとボルドーを差した、上質な高級感を狙うデザインシステム。広い余白と細い罫線、セリフ書体で「静かな贅沢」を表現します。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

重厚・優雅・特別。色数を絞り、ゴールドを点として効かせることで品位を出します。余白（spacingスケールは大きめ）と細いライン、控えめな角丸が鍵。

## 想定業種・媒体

- 高級ブランド / ジュエリー・時計・コスメ
- ファインダイニング、ホテル・スパ、会員制サービス
- ハイエンド不動産、プレミアム商品のLP

## 使いどころ

- 背景 `bg`（漆黒）に本文 `ink`（オフホワイト）で組み、余白を大きく取る
- 見出し: セリフ書体 ＋ `ink` または `primary`（ゴールド）
- 主要アクション: `primary` の細枠ボタン（地色は透明＋ゴールド枠＋ゴールド文字）または `surface` 塗り
- 強い差し色: `secondary`（ボルドー）を限定的に

## 配色の意図

- 背景を完全な黒ではなく `#0f0d0c` の温黒にし、紙のような深みを出す
- 本文 `ink (#f2ece1)` は暖色のオフホワイトで、黒背景に対して高コントラスト
- ゴールド `primary (#b8924f)` は文字・枠・小面積の装飾向け。広い面に敷くと安っぽく見えやすいので点で使う
- ゴールド地に文字を乗せる場合は暗い文字（`bg`）を使い、白文字は避ける
- `ink-mid` はキャプション用。黒背景に対しおよそ7:1を確保

## 推奨フォント

- 見出し: Cormorant Garamond（ハイコントラストなセリフ）
- 本文: Noto Serif JP / Georgia
- 欧文の細さを活かすため、見出しは light〜regular ウェイト推奨

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary | `--color-primary` | `#b8924f` |
| Secondary | `--color-secondary` | `#7a1f33` |
| Accent | `--color-accent` | `#caa968` |
| Background | `--color-bg` | `#0f0d0c` |
| Surface | `--color-surface` | `#1b1715` |
| Ink（本文） | `--color-ink` | `#f2ece1` |
| Ink-mid（補足） | `--color-ink-mid` | `#b3a896` |
| Line（罫線） | `--color-line` | `#3a322c` |
| Success | `--color-success` | `#7fae6e` |
| Warning | `--color-warning` | `#d4a445` |
| Danger | `--color-danger` | `#c75c5c` |

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
