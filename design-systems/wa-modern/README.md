# wa-modern

藍・墨・朱を基調に、余白を広く取った和モダンデザインシステム。明朝体と大きな余白で「間」を活かし、伝統的な落ち着きと現代的な洗練を両立します。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

静謐・端正・品格。余白（spacingスケールが大きめ）と細い罫線、明朝体で和の佇まいを作ります。朱（あけ）は差し色として点で使い、引き締めます。

## 想定業種・媒体

- 旅館・料亭・和菓子・日本茶などの和ブランド
- 伝統工芸・文化施設・美術館、地域・観光のサイト
- 老舗企業のブランドサイト、品位を求めるLP

## 使いどころ

- 背景 `bg`（生成り）に本文 `ink`（墨）で組み、余白を大きく取って「間」を作る
- 見出し: 明朝体 ＋ `ink` または `primary`（藍）
- 主要アクション: `primary`（藍）の塗りボタン＋生成り文字
- 差し色・強調: `accent`（朱）を限定的に。判子や見出しのアクセントに

## 配色の意図

- 地色を白ではなく生成り `#f6f4ef` にして、和紙のような温度を出す
- 本文 `ink (#1b1b1a)` は墨色で、生成り地に対して高コントラスト
- 藍 `primary (#1f3a5f)` は十分暗く、生成り文字を乗せても読める
- 朱 `accent (#c0392b)` は面積を抑えて使う差し色。小さな白文字を乗せる用途には使わず、見出しサイズ以上に限定
- `ink-mid` は補足・キャプション用で、地色に対しおよそ5.6:1を確保

## 推奨フォント

- 見出し: Shippori Mincho / Noto Serif JP（明朝）
- 本文: Noto Serif JP / Yu Mincho
- 縦組みや約物の美しさを活かすなら明朝で統一

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary（藍） | `--color-primary` | `#1f3a5f` |
| Secondary（松葉） | `--color-secondary` | `#3c5a4a` |
| Accent（朱） | `--color-accent` | `#c0392b` |
| Background（生成り） | `--color-bg` | `#f6f4ef` |
| Surface | `--color-surface` | `#ece7dc` |
| Ink（墨・本文） | `--color-ink` | `#1b1b1a` |
| Ink-mid（補足） | `--color-ink-mid` | `#5a574f` |
| Line（罫線） | `--color-line` | `#d8d2c5` |
| Success | `--color-success` | `#3f6b46` |
| Warning | `--color-warning` | `#a8742a` |
| Danger | `--color-danger` | `#a73228` |

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
