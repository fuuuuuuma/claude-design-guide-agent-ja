# bold-startup

高彩度のパープルとピンクを軸に、極太の見出しで勢いを出す大胆なスタートアップ向けデザインシステム。ランディングページのファーストビューで一気に印象づけたい場面に向いています。

- ライセンス: CC0 / 自由利用（クレジット表記不要・改変可・商用可）

## 雰囲気

エネルギッシュ・前向き・若い。極太（black 900）の大見出しと、彩度の高いアクセントで「動き」を感じさせます。余白も大きめに取り、要素を堂々と配置するのがコツ。

## 想定業種・媒体

- 資金調達期のスタートアップLP / プロダクトローンチページ
- アプリの紹介サイト、キャンペーンページ
- イベント・カンファレンスの告知ページ

## 使いどころ

- ヒーロー見出し: `font-size-4xl` ＋ `font-weight-black` ＋ `ink`
- 主要CTA: `primary` の塗りボタン＋白文字、角丸 `radius-lg`
- 第2のCTA・タグ: `secondary`（ピンク）
- ポジティブ訴求（無料・成長など）: `accent`（グリーン）

## 配色の意図

- `primary (#7c3aed)` と `secondary (#db2777)` は彩度が高く、グラデーションの起点にも使える
- これらの地色に乗せる文字は白で、見出し・ボタンラベルなど太め・大きめの文字に限定（小さい注釈を白で乗せない）
- 本文 `ink (#160a2e)` は白背景で高コントラスト。長文は黒に寄せて読みやすさを確保
- 影 `shadow-md` / `shadow-lg` は primary 由来の色を含ませ、浮遊感を出す

## 推奨フォント

- 見出し: Poppins / Montserrat（ジオメトリックな太ゴシック）
- 本文: Inter
- 日本語は Hiragino Kaku Gothic ProN / Meiryo にフォールバック

## カラーパレット（HEX）

| 役割 | 変数 | HEX |
| --- | --- | --- |
| Primary | `--color-primary` | `#7c3aed` |
| Secondary | `--color-secondary` | `#db2777` |
| Accent | `--color-accent` | `#16a34a` |
| Background | `--color-bg` | `#ffffff` |
| Surface | `--color-surface` | `#f4f1fb` |
| Ink（本文） | `--color-ink` | `#160a2e` |
| Ink-mid（補足） | `--color-ink-mid` | `#574a6b` |
| Line（罫線） | `--color-line` | `#e4def0` |
| Success | `--color-success` | `#15803d` |
| Warning | `--color-warning` | `#c2410c` |
| Danger | `--color-danger` | `#be123c` |

## ファイル

- `tokens.json` — デザイントークン（JSON）
- `tokens.css` — CSSカスタムプロパティ（`:root`）
