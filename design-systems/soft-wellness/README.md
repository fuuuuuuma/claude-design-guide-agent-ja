# soft-wellness

セージグリーンとベージュを基調にした、やさしいウェルネス向けデザインシステム。自然素材のような落ち着いた色合いと、ゆったりした行間・余白で、心地よさと安心感を伝えます。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

おだやか・ナチュラル・癒し。彩度の低いアースカラーでまとめ、テラコッタ寄りのアクセントで温度感を添えます。角丸はやや大きめ、影はごく浅く。

## 想定業種・媒体

- ヨガ・瞑想・フィットネス、スパ・サロン
- オーガニック食品、スキンケア・コスメ
- クリニック・カウンセリング・健康関連サービス

## 使いどころ

- 背景 `bg`（オフホワイト）に `surface` のベージュでセクションを分ける
- 見出し: セリフまたは丸ゴシック ＋ `ink` / `primary`
- 主要アクション: `primary`（セージ）の塗りボタン＋オフホワイト文字
- 強調・差し色: `accent`（テラコッタ）。淡いので白文字は避け、`ink` を乗せる

## 配色の意図

- 地色をわずかに暖色の `#f7f4ee` にして、自然光のような柔らかさを出す
- 本文 `ink (#2f352c)` は黒すぎないダークオリーブで、地色に対して高コントラスト
- `primary (#5f7a5b)` は十分に暗いセージで、白文字を乗せても読める
- `accent` は明るめのテラコッタのため、白文字を避けて `ink` を乗せる
- `ink-mid` は補足用で、地色に対しおよそ4.8:1を確保

## 推奨フォント

- 見出し: Noto Serif JP / Zen Maru Gothic（穏やかな印象）
- 本文: Noto Sans JP
- 読みやすさ重視のため、本文はゴシックでも可

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary | `--color-primary` | `#5f7a5b` |
| Secondary | `--color-secondary` | `#a98b6f` |
| Accent | `--color-accent` | `#c98a76` |
| Background | `--color-bg` | `#f7f4ee` |
| Surface | `--color-surface` | `#ece7dc` |
| Ink（本文） | `--color-ink` | `#2f352c` |
| Ink-mid（補足） | `--color-ink-mid` | `#62695c` |
| Line（罫線） | `--color-line` | `#dcd5c6` |
| Success | `--color-success` | `#4f7a4a` |
| Warning | `--color-warning` | `#a9762a` |
| Danger | `--color-danger` | `#b4584e` |

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
