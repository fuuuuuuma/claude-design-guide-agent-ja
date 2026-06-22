# playful-consumer

パステル調のピンク・水色に、丸ゴシック書体を合わせた陽気なコンシューマー向けデザインシステム。大きめの角丸と柔らかい影で、親しみやすく楽しい雰囲気を作ります。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

明るい・かわいい・親しみやすい。鋭さを減らした丸い角と、淡い背景にビビッドめのアクセントを置く配色。子ども・ファミリー・趣味の領域でも浮かないトーンです。

## 想定業種・媒体

- 消費者向けアプリ（家計簿・健康・学習・趣味など）
- 子ども・教育・ファミリー向けサービス
- D2Cブランド、食品・スイーツ、キャンペーンサイト

## 使いどころ

- カード・ボタン: 角丸大きめ（`radius-md` / `radius-lg`）＋ `shadow-md`
- 主要アクション: `primary`（ローズピンク）の塗りボタン＋白文字
- 補助・情報系: `secondary`（水色）
- 強調バッジ・キャンペーン: `accent`（マンゴーイエロー）。淡いので白文字は避け、`ink` を乗せる

## 配色の意図

- 背景はわずかに暖色の `#fffaf4`、面の段差は淡いピンク `surface` で「やさしさ」を演出
- 本文 `ink (#3a2a33)` は黒すぎないダークプラムで、白背景に対し高コントラストかつ柔らかい印象
- `primary (#e8557d)` は彩度を保ちつつ十分暗く、白文字を乗せても読める（大きめラベル向け）
- `accent` は明るい黄色のため、白文字は使わず `ink` を乗せてコントラストを確保

## 推奨フォント

- 見出し・本文: M PLUS Rounded 1c（丸ゴシック）
- 欧文は Quicksand
- フォールバックに Hiragino Maru Gothic ProN

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary | `--color-primary` | `#e8557d` |
| Secondary | `--color-secondary` | `#5bb8d4` |
| Accent | `--color-accent` | `#f2a93b` |
| Background | `--color-bg` | `#fffaf4` |
| Surface | `--color-surface` | `#ffeef2` |
| Ink（本文） | `--color-ink` | `#3a2a33` |
| Ink-mid（補足） | `--color-ink-mid` | `#7a6670` |
| Line（罫線） | `--color-line` | `#f3dbe2` |
| Success | `--color-success` | `#2f8f5b` |
| Warning | `--color-warning` | `#c47713` |
| Danger | `--color-danger` | `#d23f57` |

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
