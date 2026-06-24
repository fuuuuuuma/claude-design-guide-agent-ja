# Claude Design 用途別プロンプト50選

Claude Design は、言葉で指示すると Claude がデザイン（LP・スライド・1枚資料・プロトタイプ・UI・ドキュメント・アニメーション）を生成・編集できるツールです。本ファイルは、用途別にコピペしてそのまま使える依頼文を50本まとめた実用素材です。

**前提：これらのプロンプトは Claude の「デスクトップアプリ」の Claude Design に貼って使う想定です。** デスクトップアプリなら、ローカルのコード・GitHub・各種コネクタと連携でき、「デザインシステムを取り込む」系のプロンプトが活きます。

## おすすめの順番（この順で送る）

Claude Design は **いきなりデザインを作らず、① デザインシステム → ② ワイヤーフレーム → ③ デザイン → ④ ハンドオフ** の順で作ると崩れません。まずこの4本を「土台」として送ってから、用途別の50本を使ってください。

```
① このGitHubリポジトリ（またはローカルのコード）を読み込んで、色・タイポグラフィ・コンポーネントのデザインシステムを作って。
② {サービス}のワイヤーフレームを、今のデザインシステムに沿って作って。構成は{FV→課題→特徴→事例→申し込み}。
③ このワイヤーフレームをデザインに仕上げて。配色・余白・部品はデザインシステム準拠で。
④ 完成したらハンドオフ用にまとめて（実装は Claude Code へ）。
```

## このプロンプト集の使い方（3行）

1. 使いたいプロンプトの日本語版（または英語版）をコピーし、**デスクトップアプリの Claude Design** に貼り付ける。
2. `{業種}` `{ターゲット}` `{ブランド名}` のような波括弧の差し込み変数を、自分の情報に置き換える。
3. まず上の「おすすめの順番」で土台（デザインシステム→ワイヤーフレーム）を作り、用途別プロンプト → リファイン系（カテゴリ9）→ 書き出し系（カテゴリ10）の順で仕上げる。

---

## 1. LP・Webサイト制作

### p01 サービス紹介LPのファーストビュー設計

```
{業種}向けの{サービス名}を紹介するランディングページを作ってください。ターゲットは{ターゲット}です。ファーストビューにキャッチコピー、サブコピー、CTAボタン、信頼性を示す要素（導入社数や受賞など）を配置し、トンマナは{清潔感のある／親しみやすい／高級感のある}方向で。1ページのスクロール構成で、課題提起→解決策→特徴3点→料金→よくある質問→申し込みの順に並べてください。
```

```
Create a landing page that introduces {サービス名}, a service for {業種}. The target audience is {ターゲット}. In the first view, place a headline, subhead, CTA button, and trust elements (such as number of clients or awards). Keep the tone {clean / friendly / premium}. Use a single-page scroll structure ordered as: problem → solution → three key features → pricing → FAQ → sign-up.
```

💡 ファーストビューだけ先に作って合意を取ってから全体を生成すると、手戻りが減ります。

### p02 既存サイトのキャプチャを参考にしたリニューアル案

```
このWebサイトのキャプチャを取り込みました。同じ業種の{ブランド名}向けに、このトンマナを参考にしつつ独自性を出したリニューアル案を作ってください。情報設計は維持し、配色とタイポグラフィを{ブランドカラー（例：#1A3A6B）}基準に置き換え、余白を広めにとってモダンな印象に整えてください。
```

```
I've captured this website. For {ブランド名} in the same industry, create a redesign that references this tone while adding originality. Keep the information architecture, replace the color scheme and typography to be based on {ブランドカラー (例：#1A3A6B)}, and use generous whitespace for a modern feel.
```

💡 参考サイトはキャプチャ取り込みで読ませると、レイアウトの意図が伝わりやすくなります。

### p03 コンバージョン重視の申し込みフォーム周り

```
{サービス名}の申し込みページを作ってください。入力項目は{氏名・メール・電話・プラン選択}の4つに絞り、離脱を防ぐためステップ表示と入力補助を入れてください。完了画面まで含め、安心感を与えるコピーとマイクロコピーを添えてください。トンマナは信頼感重視で。
```

```
Create a sign-up page for {サービス名}. Limit the input fields to four: {name, email, phone, plan selection}. Add a step indicator and input assistance to reduce drop-off. Include the completion screen, with reassuring copy and microcopy throughout. Keep the tone trust-focused.
```

💡 フォームは項目を減らすほど完了率が上がるので、必須項目だけに絞る指示が効きます。

### p04 サービス比較セクション付きの料金ページ

```
{サービス名}の料金ページを作ってください。{ベーシック／スタンダード／プロ}の3プランを横並びの比較テーブルで見せ、おすすめプランを強調してください。各プランに含まれる機能、向いている人、月額・年額の切り替えを入れ、最下部に申し込みCTAを置いてください。トンマナは{ターゲット}に合わせて分かりやすく。
```

```
Create a pricing page for {サービス名}. Show three plans ({Basic / Standard / Pro}) as a side-by-side comparison table, highlighting the recommended plan. For each plan, include the features, who it suits, and a monthly/annual toggle. Place a sign-up CTA at the bottom. Keep the tone clear and matched to {ターゲット}.
```

💡 おすすめプランを1つ強調すると選択の迷いが減り、表が読みやすくなります。

### p05 イベント・キャンペーン用の単発LP

```
{イベント名}の告知LPを作ってください。日時・場所・参加費・登壇者・申し込み締切を目立たせ、ファーストビューで開催概要が一目で分かるようにしてください。トンマナは{ワクワク感のある／落ち着いた}方向で、申し込みボタンをページ内に複数配置してください。
```

```
Create a promotional landing page for {イベント名}. Make the date, venue, fee, speakers, and registration deadline prominent, so the overview is clear at a glance in the first view. Keep the tone {exciting / calm}, and place the registration button in multiple spots on the page.
```

💡 締切やキャンペーン期限はファーストビューに置くと、行動を後押しできます。

---

## 2. スライド・ピッチデック

### p06 投資家向けピッチデックの骨子

```
{サービス名}の投資家向けピッチデックを作ってください。構成は、課題→解決策→市場規模→プロダクト→ビジネスモデル→トラクション→競合優位→チーム→資金使途→まとめの10〜12枚で。1枚1メッセージを徹底し、図やグラフのプレースホルダを入れてください。トンマナは{信頼感のある／勢いのある}方向で。
```

```
Create an investor pitch deck for {サービス名}. Structure it in 10–12 slides: problem → solution → market size → product → business model → traction → competitive edge → team → use of funds → summary. Enforce one message per slide and include placeholders for charts and diagrams. Keep the tone {trustworthy / energetic}.
```

💡 1枚1メッセージを明示すると、情報を詰め込みすぎないスライドになります。

### p07 セミナー・ウェビナー用スライド

```
{テーマ}についての60分ウェビナー用スライドを作ってください。対象は{ターゲット}で、導入（つかみ）→本編3章→まとめ→次のアクションの構成にしてください。文字は要点のみ、図解中心で。各章の冒頭に章扉スライドを入れ、トンマナは親しみやすく読みやすい方向で。
```

```
Create slides for a 60-minute webinar about {テーマ}. The audience is {ターゲット}. Structure it as: intro (hook) → three main chapters → summary → next action. Keep text to key points and lead with diagrams. Add a section-divider slide before each chapter, and keep the tone friendly and readable.
```

💡 章扉を入れると話の区切りが視聴者に伝わり、長尺でも迷子になりません。

### p08 文書アップロードからスライド化

```
このDOCX（またはPPTX）の内容を取り込みました。中身を要約しながら、{社内報告／顧客提案}用のスライドに作り直してください。冗長な文章は箇条書きに整理し、数値はグラフに置き換え、1枚あたりの情報量を抑えてください。トンマナは元資料のブランドカラーを踏襲してください。
```

```
I've imported this DOCX (or PPTX). Rebuild its content into slides for {internal reporting / a client proposal}, summarizing as you go. Turn verbose paragraphs into bullet points, convert figures into charts, and limit the information per slide. Keep the tone consistent with the brand colors of the original document.
```

💡 既存文書を読み込ませると、ゼロから書くより構成が早く固まります。

### p09 製品アップデート報告スライド

```
{プロダクト名}の四半期アップデート報告スライドを作ってください。今期リリースした主要機能{3〜5点}を、ビフォーアフターと利用シーンで見せてください。最後に次四半期のロードマップを1枚で。トンマナは{社内向けにフラット／顧客向けに前向き}な方向で。
```

```
Create a quarterly update report deck for {プロダクト名}. Present the {3–5} key features released this quarter using before/after comparisons and usage scenarios. End with a single roadmap slide for next quarter. Keep the tone {flat for internal / positive for customers}.
```

💡 ビフォーアフター形式は、機能改善の価値を直感的に伝えられます。

### p10 短時間プレゼン用ライトニングトークデック

```
{テーマ}についての5分間ライトニングトーク用スライドを5〜7枚で作ってください。1枚あたりのメッセージは1つ、大きな文字とシンプルな図で。冒頭は問いかけ、最後は持ち帰ってほしい一文で締めてください。トンマナは{勢いのある／淡々とした}方向で。
```

```
Create a 5–7 slide deck for a 5-minute lightning talk about {テーマ}. One message per slide, with large text and simple visuals. Open with a question and close with one takeaway line. Keep the tone {energetic / matter-of-fact}.
```

💡 枚数とメッセージ数の上限を先に指定すると、密度がちょうどよくなります。

---

## 3. 営業・提案・社内資料

### p11 顧客向け提案書（一式）

```
{業種}の見込み客{企業名}に向けた提案書を作ってください。構成は、現状の課題整理→提案概要→具体的な施策→導入スケジュール→費用→期待効果→会社紹介。先方の課題に寄り添う書き出しにし、費用は概算レンジで示してください。トンマナは{誠実で丁寧／推進力のある}方向で。
```

```
Create a proposal for {企業名}, a prospect in {業種}. Structure it as: current challenges → proposal overview → specific measures → implementation schedule → costs → expected impact → company introduction. Open by empathizing with their challenges, and show costs as approximate ranges. Keep the tone {sincere and polite / driving}.
```

💡 費用は確定額でなく概算レンジで提示すると、初回提案でも出しやすくなります。

### p12 営業1枚サマリー（リーブビハインド）

```
商談後に置いていく{サービス名}の1枚サマリーを作ってください。サービスの要点、導入メリット3つ、料金の目安、次のステップ、問い合わせ先を1ページに収めてください。読み手が後で見返しても伝わるよう、見出しと余白を整理してください。トンマナは信頼感重視で。
```

```
Create a one-page leave-behind summary for {サービス名} to hand out after a meeting. Fit the service overview, three benefits, a pricing guide, next steps, and contact info onto one page. Organize headings and whitespace so it still communicates when reviewed later. Keep the tone trust-focused.
```

💡 1枚に収める指示を入れると、情報の優先順位付けが自動的に整います。

### p13 社内稟議・意思決定資料

```
{施策名}を社内で承認してもらうための意思決定資料を作ってください。背景→目的→具体策→必要なコストとリソース→想定リスクと対策→期待効果→判断してほしい点、の順で。意思決定者が短時間で判断できるよう、結論先出しで作ってください。トンマナはフラットで簡潔に。
```

```
Create a decision-making document to get internal approval for {施策名}. Order it as: background → objective → specific plan → required cost and resources → anticipated risks and countermeasures → expected impact → decisions needed. Lead with the conclusion so decision-makers can judge quickly. Keep the tone flat and concise.
```

💡 「判断してほしい点」を最後に明記すると、会議が決裁で終わりやすくなります。

### p14 業務マニュアル・手順書

```
{業務名}の手順書を作ってください。対象は{新人／外部委託先}です。前提条件→準備するもの→ステップ（番号付き）→つまずきやすい点→完了確認、の構成で。各ステップは1アクション1文にし、スクリーンショットを入れる枠を用意してください。トンマナは分かりやすさ最優先で。
```

```
Create a procedure manual for {業務名}. The audience is {new hires / external contractors}. Structure it as: prerequisites → what to prepare → numbered steps → common pitfalls → completion check. Make each step one action per sentence, and provide frames for screenshots. Prioritize clarity in the tone.
```

💡 スクリーンショット枠をあらかじめ用意させると、後から画像を差し込みやすくなります。

### p15 月次レポート・実績報告

```
{部署／プロジェクト名}の月次レポートを作ってください。サマリー（今月のハイライト）→主要指標の推移（グラフ）→できたこと→課題→来月の重点、の構成で。数値は前月比・目標比が分かる見せ方にし、結論を冒頭に置いてください。トンマナは社内向けに簡潔で。
```

```
Create a monthly report for {部署／プロジェクト名}. Structure it as: summary (this month's highlights) → key metric trends (charts) → accomplishments → challenges → next month's priorities. Present numbers so month-over-month and vs-target are clear, and put the conclusion at the top. Keep the tone concise for internal use.
```

💡 前月比・目標比を併記させると、数値の良し悪しが一目で伝わります。

---

## 4. プロトタイプ・アプリUI/UX・ワイヤーフレーム

### p16 アプリ主要画面のワイヤーフレーム

```
{アプリ名}の主要画面のワイヤーフレームを作ってください。対象ユーザーは{ターゲット}、主な目的は{達成したいこと}です。ホーム・一覧・詳細・登録/編集・設定の5画面を、要素配置と導線が分かるグレースケールで。各画面に簡単な注釈を添えてください。装飾は最小限で構いません。
```

```
Create wireframes for the main screens of {アプリ名}. The target users are {ターゲット} and the main goal is {達成したいこと}. Produce five screens — home, list, detail, create/edit, settings — in grayscale showing element placement and flow. Add a short annotation to each screen. Keep decoration minimal.
```

💡 最初はグレースケール指定にすると、配色より構造の議論に集中できます。

### p17 機能のクリッカブルなプロトタイプ

```
{機能名}のクリッカブルなプロトタイプを作ってください。ユーザーが{開始→入力→確認→完了}の流れを体験できるように、画面遷移をつないでください。ボタンを押すと次の画面に進む形で、主要な分岐（成功・エラー）も用意してください。トンマナは{プロダクトの既存トーン}に合わせて。
```

```
Create a clickable prototype for {機能名}. Connect the screen transitions so a user can experience the flow {start → input → confirm → complete}. Pressing a button should advance to the next screen, and include the main branches (success, error). Match the tone to {the product's existing tone}.
```

💡 主要な分岐（成功・エラー）まで作らせると、ユーザーテストにそのまま使えます。

### p18 既存画面の改善案（UX観点）

```
このアプリ画面のキャプチャを取り込みました。{ターゲット}にとっての使いやすさの観点で、改善案を3パターン作ってください。それぞれ何をどう変えたか、なぜ良くなるかを短く添えてください。情報量は維持しつつ、優先操作を目立たせる方向で。
```

```
I've imported a capture of this app screen. From the perspective of usability for {ターゲット}, create three improvement variations. For each, briefly note what changed and why it's better. Keep the information density while making the primary action more prominent.
```

💡 改善案を複数パターン出させ、根拠とセットで比較すると判断が速くなります。

### p19 オンボーディングフローの設計

```
{アプリ名}の初回オンボーディングフローを作ってください。初めてのユーザーが{コア体験}にたどり着くまでを、3〜4ステップの画面で設計してください。各ステップは説明1文＋イラスト枠＋次へボタン。スキップ導線も用意してください。トンマナは{ターゲット}に親しみやすく。
```

```
Create the first-run onboarding flow for {アプリ名}. Design 3–4 step screens that guide a first-time user to {コア体験}. Each step should have one explanatory sentence, an illustration frame, and a next button. Include a skip path. Keep the tone friendly for {ターゲット}.
```

💡 スキップ導線を入れさせると、慣れたユーザーの離脱を防げます。

### p20 ダッシュボードのUI設計

```
{用途}向けの管理ダッシュボードUIを作ってください。表示したい主要指標は{指標A・指標B・指標C}です。上部にKPIカード、中段に推移グラフ、下段にデータテーブルを配置し、期間フィルタを上部に置いてください。情報は詰め込みすぎず、視線の流れがZ字になるよう整えてください。
```

```
Create an admin dashboard UI for {用途}. The key metrics to show are {指標A, 指標B, 指標C}. Place KPI cards at the top, trend charts in the middle, and a data table at the bottom, with a date filter at the top. Avoid overcrowding and arrange it so the eye follows a Z-pattern.
```

💡 KPIカード・グラフ・テーブルの3段構成を指定すると、迷わず情報設計が決まります。

---

## 5. デザインシステム構築・ブランド統一

### p21 GitHubリポジトリからデザインシステムを取り込む

```
このGitHubリポジトリのコードベースを取り込んで、デザインシステムを抽出してください。色・タイポグラフィ・余白・ボタンやカードなどのコンポーネントを読み取り、再利用できる部品セットとして整理してください。抽出後は、これを使って{LP／管理画面}のサンプル画面を1枚生成してください。
```

```
Import this GitHub repository's codebase and extract a design system. Read the colors, typography, spacing, and components such as buttons and cards, and organize them into a reusable set of parts. After extraction, use it to generate one sample screen for {a landing page / an admin screen}.
```

💡 デザインシステムを先に取り込んでからプロジェクトを作ると、生成物が自社の部品で揃います。

### p22 ブランドガイドからトンマナを定義

```
{ブランド名}のブランドガイド（色・フォント・トーン）をまとめたデザインシステムを作ってください。メインカラー{#xxxxxx}、サブカラー{#xxxxxx}、見出しフォント{フォント名}、本文フォント{フォント名}を基準に、ボタン・見出し・カード・タグの標準スタイルを定義してください。良い例と避けたい例も添えてください。
```

```
Create a design system that captures {ブランド名}'s brand guide (colors, fonts, tone). Based on the main color {#xxxxxx}, sub color {#xxxxxx}, heading font {フォント名}, and body font {フォント名}, define standard styles for buttons, headings, cards, and tags. Include examples of good and to-avoid usage.
```

💡 良い例・避けたい例をセットで持たせると、チームでの運用がぶれにくくなります。

### p23 既存デザインファイルから部品を統一

```
このデザインファイルを取り込みました。バラバラになっているボタンや見出しのスタイルを洗い出し、統一されたコンポーネントセットに整理してください。重複や揺れ（似た色・似た余白）を指摘し、推奨の標準値にまとめてください。整理後の一覧を1枚にして見せてください。
```

```
I've imported this design file. Identify the inconsistent button and heading styles and organize them into a unified component set. Point out duplicates and drift (similar colors, similar spacing) and consolidate them into recommended standard values. Present the cleaned-up set on one page.
```

💡 既存ファイルの「揺れ」を洗い出させると、統一作業の抜け漏れが減ります。

### p24 ローカルコードベースから生成基盤を作る

```
このローカルのコードベースを取り込んで、ここで使われている色・タイポ・コンポーネントを土台にした生成設定を作ってください。今後この設定をベースに画面を作ると、既存プロダクトと見た目が揃うようにしてください。まずはサンプルとして{設定画面}を1枚生成してください。
```

```
Import this local codebase and create a generation setup based on the colors, typography, and components used here. From now on, screens built on this setup should match the look of the existing product. As a sample, generate one {settings screen}.
```

💡 ローカルのコードベース取り込みは、実装済みの見た目をそのまま流用できるのが利点です。

### p25 複数媒体のトンマナ統一ガイド

```
{ブランド名}のデザインシステムをもとに、LP・スライド・SNS・ドキュメントで使う際のトンマナ統一ガイドを作ってください。媒体ごとに、使う色の比率、見出しの大きさ、余白の取り方、避けたい表現を1枚ずつまとめてください。担当者が見て迷わないレベルの具体性で。
```

```
Based on {ブランド名}'s design system, create a tone-consistency guide for use across landing pages, slides, social, and documents. For each medium, summarize the color ratios, heading sizes, spacing approach, and expressions to avoid, one page each. Make it concrete enough that a team member won't be unsure.
```

💡 媒体別に1枚ずつ分けると、担当者が自分の領域だけ参照しやすくなります。

---

## 6. ロゴ・SNS素材・バナー・サムネ

### p26 ロゴのコンセプト案

```
{ブランド名}（{業種}）のロゴ案を3パターン作ってください。ブランドの印象は{キーワード3つ}です。シンボル＋ロゴタイプの組み合わせで、モノクロでも成立するシンプルな形を意識してください。各案にコンセプトの一言説明を添え、使用イメージ（名刺・看板）も小さく見せてください。
```

```
Create three logo concepts for {ブランド名} ({業種}). The brand impression is {キーワード3つ}. Use a symbol-plus-logotype combination and aim for simple forms that work in monochrome. Add a one-line concept note to each, and show small usage mockups (business card, signage).
```

💡 モノクロでも成立する形を条件にすると、用途を選ばない汎用的なロゴになります。

### p27 SNS投稿用カルーセル画像

```
{テーマ}についての{Instagram／X}向けカルーセル画像を{5}枚作ってください。1枚目は思わず止まるタイトル、2〜4枚目は要点を1つずつ、最後はまとめとフォロー誘導。文字は大きく、{ブランドカラー}で統一し、スマホで読める文字量に抑えてください。トンマナは{親しみやすい／専門的}方向で。
```

```
Create a {5}-image carousel for {Instagram / X} about {テーマ}. Slide 1 is a scroll-stopping title, slides 2–4 each cover one key point, and the last is a summary with a follow prompt. Use large text, unify with {ブランドカラー}, and keep the text amount readable on a phone. Keep the tone {friendly / professional}.
```

💡 スマホで読める文字量に、と条件を付けると詰め込みすぎを防げます。

### p28 キャンペーンバナー（複数サイズ）

```
{キャンペーン名}の告知バナーを作ってください。訴求は{オファー内容}、CTAは{今すぐ申し込む}です。{ブランドカラー}を基調に、視認性の高い配色で。同じデザインで{正方形・横長・縦長}の3サイズに展開してください。文字は離れて見ても読める大きさで。
```

```
Create a promotional banner for {キャンペーン名}. The appeal is {オファー内容} and the CTA is {今すぐ申し込む}. Base it on {ブランドカラー} with high-visibility coloring. Adapt the same design into three sizes: {square, landscape, portrait}. Keep text large enough to read from a distance.
```

💡 1デザインを複数サイズに展開させると、媒体ごとの作り直しが不要になります。

### p29 動画サムネイルのレイアウト

```
{動画タイトル}のサムネイル案を3パターン作ってください。視聴者は{ターゲット}、伝えたい一言は{キャッチ}です。クリックしたくなるよう、太い文字・高コントラスト・人物または象徴的なモチーフの配置を意識してください。スマホの一覧でも読める文字量に抑えてください。
```

```
Create three thumbnail concepts for {動画タイトル}. The viewers are {ターゲット} and the key phrase is {キャッチ}. Make them click-worthy with bold text, high contrast, and a person or symbolic motif. Keep the text amount readable even in a phone feed.
```

💡 同じ動画でも案を複数出させ、A/Bで比較するとクリック率の検証がしやすくなります。

### p30 プロフィール・ヘッダー画像セット

```
{個人名／ブランド名}のSNSプロフィールまわりを一式作ってください。アイコン（正方形）とヘッダー画像（横長）を、同じトンマナで揃えてください。発信テーマは{テーマ}、印象は{キーワード}です。各SNSの推奨比率に合わせ、主要要素が見切れないよう余白を確保してください。
```

```
Create a full set of social profile assets for {個人名／ブランド名}. Make the icon (square) and header image (landscape) consistent in tone. The content theme is {テーマ} and the impression is {キーワード}. Match each platform's recommended aspect ratio and leave margins so key elements aren't cropped.
```

💡 アイコンとヘッダーを同時に作らせると、トンマナが自然に揃います。

---

## 7. ドキュメント・1枚資料・インフォグラフィック

### p31 サービス概要の1枚資料

```
{サービス名}の概要が一目で分かる1枚資料を作ってください。何ができるか、誰向けか、3つの特徴、料金の目安、導入の流れを1ページに収めてください。読み手は{ターゲット}です。図解中心で文字は最小限、視線が上から下へ自然に流れる構成にしてください。トンマナは信頼感重視で。
```

```
Create a one-page sheet that conveys {サービス名} at a glance. Fit what it does, who it's for, three features, a pricing guide, and the onboarding flow onto one page. The reader is {ターゲット}. Lead with diagrams and keep text minimal, with a layout where the eye flows naturally top to bottom. Keep the tone trust-focused.
```

💡 「1ページに収める」と明示すると、自然に要素の優先順位が決まります。

### p32 数値を見せるインフォグラフィック

```
{テーマ}に関するインフォグラフィックを作ってください。盛り込む数値は{数値A・数値B・数値C}です。各数値を大きく見せ、意味が直感的に伝わるアイコンや簡易グラフを添えてください。出典の記載欄も用意してください。トンマナは{専門的／カジュアル}方向で、SNSでも共有しやすい縦長で。
```

```
Create an infographic about {テーマ}. The numbers to include are {数値A, 数値B, 数値C}. Show each number large with icons or simple charts that make the meaning intuitive. Provide a space for source citations. Keep the tone {professional / casual}, and use a portrait orientation that's easy to share on social.
```

💡 出典欄を用意させると、公開資料でも数値の信頼性を担保できます。

### p33 比較表でまとめる検討資料

```
{選択肢A}と{選択肢B}（必要なら{選択肢C}）を比較する1枚資料を作ってください。比較軸は{価格・機能・サポート・向いている人}です。表形式で見やすくまとめ、どんな人にどちらが向くかを最後に一言で示してください。中立的なトンマナで、判断材料として使える形に。
```

```
Create a one-page comparison sheet for {選択肢A} vs {選択肢B} (add {選択肢C} if needed). The comparison axes are {price, features, support, who it suits}. Present it as a clear table, and end with one line on who each option suits. Keep a neutral tone, formatted to serve as decision material.
```

💡 比較軸を先に指定すると、表の列がぶれず公平な比較になります。

### p34 手順を図解するフロー図資料

```
{プロセス名}の流れを図解した1枚資料を作ってください。開始から完了までを{4〜6}ステップのフロー図で表し、各ステップに担当・所要時間・成果物を添えてください。分岐がある場合は条件も示してください。トンマナは業務資料として読みやすい方向で。
```

```
Create a one-page sheet that diagrams the flow of {プロセス名}. Represent start to finish as a {4–6}-step flow diagram, with the owner, duration, and deliverable noted at each step. If there are branches, show the conditions. Keep the tone readable as a work document.
```

💡 各ステップに担当と所要時間を入れさせると、運用ドキュメントとして実用的になります。

### p35 用語集・チートシート

```
{分野}の初心者向けチートシートを作ってください。よく使う用語{10〜15}個を、用語名＋一言の意味＋使う場面の3点セットで一覧にしてください。関連する用語はグループ分けし、印刷して手元に置ける1枚に収めてください。トンマナは初心者に優しく簡潔に。
```

```
Create a beginner cheat sheet for {分野}. List {10–15} common terms as a three-part set: term + one-line meaning + when it's used. Group related terms and fit it onto one page that can be printed and kept at hand. Keep the tone beginner-friendly and concise.
```

💡 「用語＋意味＋使う場面」の3点セットにすると、暗記でなく実用で覚えられます。

---

## 8. Claude Code連携・コードへのハンドオフ

### p36 ターミナルからデザインシステムを取り込む

```
Claude Code のターミナルで /design-sync を使い、このリポジトリのデザインシステム（色・タイポ・コンポーネント）を取り込んでください。取り込んだ内容を要約し、以降のデザイン生成でこの部品を使う前提に設定してください。不足している定義（例：エラー色やフォーカス状態）があれば指摘してください。
```

```
In the Claude Code terminal, use /design-sync to import this repository's design system (colors, typography, components). Summarize what was imported and set it as the basis for future design generation. Point out any missing definitions (e.g., error colors or focus states).
```

💡 `/design-sync` で先に取り込んでおくと、`/design` で作る画面が実装と揃います。

### p37 /design で画面を作って同期する

```
Claude Code で /design を使い、取り込み済みのデザインシステムをベースに{画面名}を作成してください。要件は{主要な機能と表示要素}です。作成後はデザイン側と双方向同期し、実装に渡せる状態にしてください。既存コンポーネントで足りる部分は新規作成せず流用してください。
```

```
In Claude Code, use /design to create {画面名} based on the imported design system. The requirements are {主要な機能と表示要素}. After creating it, sync bidirectionally with the design side and get it ready to hand to implementation. Reuse existing components where they suffice rather than creating new ones.
```

💡 既存コンポーネントの流用を指示すると、実装時の差分が小さく済みます。

### p38 実装ハンドオフ用バンドルにまとめる

```
作成した{画面名／フロー}を、Claude Code に実装を渡すためのハンドオフ用バンドルにまとめてください。各画面のレイアウト意図、使っているコンポーネント、状態（通常・ホバー・エラーなど）、必要なデータ項目を整理して含めてください。実装者がそのまま着手できる粒度にしてください。
```

```
Bundle the {画面名／フロー} I created into a handoff bundle for passing implementation to Claude Code. Include the layout intent of each screen, the components used, the states (default, hover, error, etc.), and the required data items. Make the granularity such that an implementer can start right away.
```

💡 状態（ホバー・エラー等）まで含めると、実装側の確認往復が減ります。

### p39 デザインとコードの差分を解消する

```
このデザインと、Claude Code 側の実装にズレが出ています。色・余白・コンポーネントの差分を洗い出し、どちらに合わせるべきかの判断材料とともに整理してください。デザインを正とする場合は実装への修正指示を、実装を正とする場合はデザインの更新案をまとめてください。
```

```
There's drift between this design and the implementation on the Claude Code side. Identify the differences in colors, spacing, and components, and organize them with material for deciding which to align to. If the design is the source of truth, summarize fix instructions for the implementation; if the implementation is, summarize design update proposals.
```

💡 双方向同期は「どちらを正とするか」を先に決めると判断が速くなります。

### p40 デザイン変更を実装タスクに翻訳する

```
{画面名}のデザインを{変更内容}に更新しました。この変更を Claude Code で実装するためのタスクリストに翻訳してください。変更が影響するコンポーネント、修正すべきスタイル、確認すべき画面を箇条書きで。優先度と想定の影響範囲も添えてください。
```

```
I've updated the design of {画面名} with {変更内容}. Translate this change into a task list for implementing it in Claude Code. List the affected components, the styles to fix, and the screens to verify, as bullet points. Include priority and the expected scope of impact.
```

💡 デザイン変更をタスクリスト化させると、実装の抜け漏れチェックに使えます。

---

## 9. リファイン・修正・canvas編集

### p41 要素の整列と余白の調整

```
この画面の要素を整列させてください。ボタンや見出しの左端を揃え、カード間の余白を均等にし、グループごとの間隔を整理してください。情報のまとまりが視覚的に伝わるよう、近いものは近く、違うものは離して配置してください。色や文言は変えず、レイアウトだけ整えてください。
```

```
Align the elements on this screen. Align the left edges of buttons and headings, make the spacing between cards even, and organize the gaps between groups. Place related items close and unrelated items apart so the information grouping reads visually. Don't change colors or wording — adjust only the layout.
```

💡 canvas上でドラッグ・リサイズした後、整列指示で仕上げると手作業のズレが消えます。

### p42 トンマナを別の方向に振り直す

```
このデザインのトンマナを{現状の印象}から{目指す印象（例：高級感のある落ち着いた方向）}に振り直してください。配色・フォント・余白・装飾の強さを調整し、レイアウトと情報は維持してください。変更前後で何を変えたかを短くまとめてください。
```

```
Shift the tone of this design from {現状の印象} to {目指す印象 (例：a premium, calm direction)}. Adjust the color scheme, fonts, spacing, and decoration intensity while keeping the layout and information. Briefly summarize what changed before and after.
```

💡 「レイアウトは維持」と添えると、トンマナだけ変わり構成は壊れません。

### p43 特定要素だけ部分修正

```
この画面の{修正対象（例：ヘッダーのCTAボタン）}だけを修正してください。{変更内容（例：色を{#xxxxxx}に、文言を「無料で試す」に、サイズをひと回り大きく）}にしてください。他の要素には一切手を加えないでください。修正後の見え方を確認させてください。
```

```
Modify only the {修正対象 (例：the CTA button in the header)} on this screen. Make it {変更内容 (例：color {#xxxxxx}, label "無料で試す", one size larger)}. Do not touch any other elements. Let me check how it looks after the change.
```

💡 「他の要素には手を加えない」と明記すると、意図しない巻き込み修正を防げます。

### p44 情報量の調整（増やす・減らす）

```
この{スライド／画面}は情報が{多すぎる／少なすぎる}ので調整してください。{減らす場合：要点を3つに絞り、補足は削るか別ページへ}／{増やす場合：根拠となるデータや具体例を1つずつ加える}。1画面あたりの読みやすさを優先し、トンマナは維持してください。
```

```
This {slide / screen} has {too much / too little} information, so adjust it. {If reducing: narrow to three key points and cut or move supplements to another page} / {If adding: add one piece of supporting data or a concrete example each}. Prioritize per-screen readability and keep the tone.
```

💡 増減の方向と上限（例：要点3つ）を具体的に指定すると、ちょうどよい密度になります。

### p45 アクセシビリティ・可読性の改善

```
このデザインの可読性とアクセシビリティを改善してください。文字と背景のコントラストを十分に確保し、小さすぎる文字を読めるサイズに、リンクやボタンが押せると分かる見た目に整えてください。色だけに頼らず形やラベルでも区別できるようにしてください。レイアウトの大枠は維持で。
```

```
Improve the readability and accessibility of this design. Ensure sufficient text-to-background contrast, bump up text that's too small to a readable size, and make links and buttons look clearly tappable. Don't rely on color alone — distinguish by shape and labels too. Keep the overall layout.
```

💡 色だけでなく形やラベルでも区別、と指示すると、色覚の差にも配慮できます。

---

## 10. 書き出し・他ツール連携

### p46 PDFで書き出す

```
このデザインをPDFで書き出してください。{用途（例：印刷して配布する／メールで送る）}を想定し、{1枚資料は1ページ／スライドは1スライド1ページ}でまとめてください。文字が切れたり潰れたりしていないか確認し、配布に適した形にしてください。
```

```
Export this design as a PDF. Assuming {用途 (例：printing for distribution / sending by email)}, lay it out as {one page for a one-pager / one slide per page for slides}. Check that no text is cut off or crushed, and make it suitable for distribution.
```

💡 書き出し前に、文字切れや潰れがないかを確認させると配布事故を防げます。

### p47 PowerPointで書き出して編集を引き継ぐ

```
このスライドをPowerPoint（PPTX）で書き出してください。書き出し後に{担当者}が文言や数値を差し替えられるよう、テキストは編集可能な状態を保ってください。フォントや配色が崩れていないかも確認してください。{社内テンプレート}に合わせる必要があれば指摘してください。
```

```
Export these slides as PowerPoint (PPTX). Keep the text editable so {担当者} can swap wording and numbers after export. Check that fonts and colors aren't broken. If they need to match {社内テンプレート}, point that out.
```

💡 PPTX書き出しはテキスト編集可能を条件にすると、相手側で修正してもらえます。

### p48 Canva / Figma系へ受け渡す

```
このデザインを{Canva／Figma系のツール}に受け渡してください。受け渡し後に色やコンポーネントを編集しやすいよう、要素ごとに分けた状態を保ってください。受け渡し先で崩れやすい部分があれば事前に指摘し、必要なら受け渡し用に整えてから連携してください。
```

```
Hand this design off to {Canva / a Figma-family tool}. Keep elements separated so colors and components are easy to edit after the handoff. Point out in advance any parts likely to break on the destination, and if needed, clean it up for handoff before connecting.
```

💡 連携先で崩れやすい箇所を先に確認させると、受け渡し後の修正が減ります。

### p49 Webに公開する（Vercel等）

```
このデザインを{Vercel等の公開先}に渡せる形にしてください。LPやプロトタイプとして公開する前提で、各セクションの構造と必要なコンテンツを整理し、実装・公開に必要な情報をまとめてください。公開後に差し替えやすいテキスト・画像の箇所も示してください。
```

```
Prepare this design to hand off to {a publishing destination such as Vercel}. Assuming it goes live as a landing page or prototype, organize each section's structure and required content, and summarize what's needed for implementation and publishing. Indicate which text and images will be easy to swap after launch.
```

💡 公開系の操作は最終的に人が承認する前提で、まずは渡せる形に整える指示が安全です。

### p50 複数フォーマットへ一括展開

```
完成したこの{資料／デザイン}を、用途別に複数フォーマットへ展開してください。{配布用にPDF、編集用にPPTX、Webプレビュー用に共有リンク}を想定しています。各フォーマットで文字切れや崩れがないか確認し、どのファイルがどの用途向けかを一覧にして示してください。
```

```
Take this finished {document / design} and adapt it into multiple formats by use case. I'm assuming {PDF for distribution, PPTX for editing, and a share link for web preview}. Check each format for text cutoff or breakage, and present a list of which file is for which use.
```

💡 用途とフォーマットの対応を一覧で出させると、配布時に取り違えません。
