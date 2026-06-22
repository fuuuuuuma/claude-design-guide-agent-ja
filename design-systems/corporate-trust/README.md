# corporate-trust

深いネイビーとグレーを基調にした、信頼感重視の企業向けデザインシステム。金融・士業・コンサルティングなど「堅実さ」が問われる業種に向けて、落ち着いた配色と整然としたレイアウトで構成しています。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

誠実・安定・専門的。彩度を抑えたネイビーで保守的な信頼感を出しつつ、ティール寄りのアクセントで古臭くなりすぎないバランスを取っています。角丸は控えめ、影も浅めで端正に。

## 想定業種・媒体

- 金融機関・保険・証券のコーポレートサイト
- 税理士・弁護士・社労士など士業の事務所サイト
- コンサルティング・BtoBサービスの会社案内、IR・採用ページ

## 使いどころ

- グローバルヘッダー・フッター: `primary`（ネイビー）地に白文字
- 見出し: `primary` または `ink`
- 主要アクション（資料請求・問い合わせ）: `primary` の塗りボタン＋白文字
- リンク・補助強調: `accent`（ティール）
- 表・カードの段差: `surface`、区切りは `line`

## 配色の意図

- `primary (#1e3a5f)` は十分に暗く、白文字を乗せて高コントラストを確保できる
- 本文 `ink (#1a2230)` は白背景で読みやすく、`ink-mid` は補足情報用（白地に対しおよそ4.9:1）
- アクセント `accent (#1d7a8c)` はリンク文字として白背景で読める明度。地色に小さい白文字を乗せる用途には使わない
- `danger` / `warning` も彩度を抑え、画面全体のトーンを乱さない

## 推奨フォント

- 見出し・本文ともに Noto Sans JP（または Helvetica Neue / Arial）
- 可読性重視のため、装飾的な書体は避ける

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary | `--color-primary` | `#1e3a5f` |
| Secondary | `--color-secondary` | `#39557a` |
| Accent | `--color-accent` | `#1d7a8c` |
| Background | `--color-bg` | `#ffffff` |
| Surface | `--color-surface` | `#f1f4f8` |
| Ink（本文） | `--color-ink` | `#1a2230` |
| Ink-mid（補足） | `--color-ink-mid` | `#56606e` |
| Line（罫線） | `--color-line` | `#d7dde6` |
| Success | `--color-success` | `#1f7a4d` |
| Warning | `--color-warning` | `#a96512` |
| Danger | `--color-danger` | `#a72c3a` |

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
