# ダウンロードして使えるデザインシステム 10選

Claude Design / Claude Code に読み込ませて「自社の部品で生成」を始めるための、デザイントークン集です。雰囲気の異なる10種類を用意しました。それぞれに `tokens.json`（デザイントークン）、`tokens.css`（すぐ使えるCSS変数）、`README.md`（説明とパレット一覧）が入っています。

- ライセンス: すべて CC0 / 自由利用（クレジット表記不要・改変可・商用可）
- 配色はオリジナル。実在ブランドの商標カラーは使用していません。
- 本文色（ink）は背景に対して読めるコントラストを基準に調整しています。

## 10システム一覧

| # | システム | 雰囲気 | 想定用途 | Primary | Accent | 背景 |
| --- | --- | --- | --- | --- | --- | --- |
| 1 | [minimal-saas](./minimal-saas/) | 清潔・中立・機能的 | BtoB SaaS / 管理画面 / ダッシュボード | `#4f46e5` | `#0ea5e9` | `#ffffff` |
| 2 | [warm-editorial](./warm-editorial/) | 落ち着き・知性・手触り | メディア / ブログ / インタビュー記事 | `#9a3412` | `#b45309` | `#fbf6ee` |
| 3 | [bold-startup](./bold-startup/) | エネルギッシュ・前向き | スタートアップLP / ローンチページ | `#7c3aed` | `#16a34a` | `#ffffff` |
| 4 | [corporate-trust](./corporate-trust/) | 誠実・安定・専門的 | 金融 / 士業 / コンサルのコーポレート | `#1e3a5f` | `#1d7a8c` | `#ffffff` |
| 5 | [playful-consumer](./playful-consumer/) | 明るい・かわいい・親しみ | 消費者向けアプリ / 教育 / D2C | `#e8557d` | `#f2a93b` | `#fffaf4` |
| 6 | [dark-developer](./dark-developer/) | クール・テクニカル | 開発者ツール / 管理コンソール / 技術ブログ | `#6ea8fe` | `#c08cff` | `#0d1117` |
| 7 | [luxury-premium](./luxury-premium/) | 重厚・優雅・特別 | 高級ブランド / ホテル / 会員制 | `#b8924f` | `#caa968` | `#0f0d0c` |
| 8 | [soft-wellness](./soft-wellness/) | おだやか・ナチュラル | ヨガ / スパ / オーガニック / クリニック | `#5f7a5b` | `#c98a76` | `#f7f4ee` |
| 9 | [neo-brutalist](./neo-brutalist/) | 直球・遊び心・自己主張 | クリエイティブ / インディー / Z世代向け | `#ffd400` | `#ff5a3c` | `#fdfdf6` |
| 10 | [wa-modern](./wa-modern/) | 静謐・端正・品格 | 和ブランド / 伝統工芸 / 文化施設 / 観光 | `#1f3a5f` | `#c0392b` | `#f6f4ef` |

## 各システムに含まれるファイル

```
design-systems/
  {slug}/
    tokens.json   … デザイントークン（color / typography / spacing / radius / shadow）
    tokens.css    … 上記を :root の CSS変数に落としたもの（コピペで使える）
    README.md     … 雰囲気・想定業種・使いどころ・配色の意図・パレット一覧
```

トークンのキー構成は10システム共通です。

- color: `primary` / `secondary` / `accent` / `bg` / `surface` / `ink` / `ink-mid` / `line` / `success` / `warning` / `danger`
- typography: `fontFamily`（heading / body、一部 mono）/ `size` / `weight` / `lineHeight`
- spacing: 4・8基準のスケール（`1`=4px 〜 `9`）
- radius: `none` / `sm` / `md` / `lg` / `pill`
- shadow: `sm` / `md` / `lg`

## Claude Design / Claude Code への読み込ませ方（5ステップ）

1. 使いたいシステムのフォルダを選ぶ（例: `minimal-saas`）。雰囲気・想定業種は各 `README.md` を参照。
2. そのフォルダの `tokens.json`（または `tokens.css`）を、Claude Design / Claude Code に渡す。Claude Code ならファイルをプロジェクトに置いて「このトークンを使って」と指示する。
3. 「このデザイントークンを唯一の正とし、色・余白・角丸・影・フォントはこの変数だけから選んで」と前提を与える。生の HEX 値を直書きさせず、変数（`--color-primary` など）経由で参照させるのがコツ。
4. 作りたい画面・部品を依頼する（例: 「このトークンで料金表セクションを作って。本文は ink、主要ボタンは primary」）。CSSなら `tokens.css` を読み込んだ上で `var(--color-primary)` の形で組ませる。
5. 出力をプレビューし、ずれていれば「primary を CTA だけに限定」「余白は spacing スケールから」のように、トークン名を使って微調整を指示する。必要なら `tokens.json` の値自体を編集して再生成する。

補足: `tokens.json` は構造化データとして「どんな部品を作るか」の判断に、`tokens.css` は実装にそのまま使えます。両ファイルは同じ値で一致しています。

## ライセンス

このコレクションのトークンおよびドキュメントは CC0 / 自由利用です。改変・再配布・商用利用すべて可、クレジット表記は不要です。
