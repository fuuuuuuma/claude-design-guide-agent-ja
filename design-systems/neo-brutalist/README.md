# neo-brutalist

原色・太い黒罫・ぼかさないハードシャドウで構成する、ネオブルータリズム系デザインシステム。角丸ゼロ、はっきりしたコントラストで「作為的な荒さ」を演出します。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

直球・遊び心・自己主張。装飾を「あえて」生のまま見せるスタイル。黄・青・赤の原色を太い黒の枠で囲み、影は黒のソリッド（ぼかし無し）でずらして置きます。

## 想定業種・媒体

- クリエイティブスタジオ / デザイン・アート系のポートフォリオ
- インディーゲーム、音楽・イベント、Z世代向けブランド
- 個性を出したいキャンペーン・告知ページ

## 使いどころ

- すべての面に太い黒枠（`--border-width: 3px` ＋ `--border-color`）を付ける
- カード・ボタン: `surface` 地 ＋ 黒枠 ＋ `shadow-md`（ソリッド影）、角丸は使わない
- 主要アクション: `primary`（イエロー）または `secondary`（ブルー）の塗り
- 強調・注意喚起: `accent`（オレンジレッド）

## 配色の意図

- 黄 `primary (#ffd400)` の上には `ink`（黒）の文字を乗せる。黄地に白文字は読めないため避ける
- 青 `secondary (#2563ff)` の上には白文字、赤系 `accent (#ff5a3c)` の上も白または黒で大きめのラベルに限定
- 本文 `ink (#0a0a0a)` はほぼ黒で、明るい背景に対して最大級のコントラスト
- 罫線と影は同一の黒 `#0a0a0a` で統一し、輪郭の強さを揃える

## 推奨フォント

- 見出し: Archivo / Anton（極太・コンデンス）
- 本文: Space Grotesk / Inter
- アクセントに Space Mono（等幅）を混ぜると雰囲気が出る

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary | `--color-primary` | `#ffd400` |
| Secondary | `--color-secondary` | `#2563ff` |
| Accent | `--color-accent` | `#ff5a3c` |
| Background | `--color-bg` | `#fdfdf6` |
| Surface | `--color-surface` | `#ffffff` |
| Ink（本文） | `--color-ink` | `#0a0a0a` |
| Ink-mid（補足） | `--color-ink-mid` | `#444444` |
| Line（罫線） | `--color-line` | `#0a0a0a` |
| Success | `--color-success` | `#15a34a` |
| Warning | `--color-warning` | `#d97706` |
| Danger | `--color-danger` | `#e11d2e` |

補足: `--border-width: 3px` / `--border-color: #0a0a0a` をボタン・カードの枠に使い、影は `--shadow-*`（ソリッド）を組み合わせると様式が完成します。

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
