---
marp: true
theme: default
paginate: true
size: 16:9
style: |
  @import url('https://fonts.googleapis.com/css2?family=BIZ+UDPGothic:wght@400;700&family=Noto+Sans+JP:wght@400;700&display=swap');

  :root {
    --color-background: #ffffff;
    --color-foreground: #1a1a2e;
    --color-accent: #0969da;
    --color-accent-light: #dbeafe;
    --color-section: #f0f6ff;
    --font-latin: 'Aptos Display', 'Segoe UI', sans-serif;
    --font-ja: 'BIZ UDPGothic', 'Noto Sans JP', 'Meiryo UI', 'Meiryo', sans-serif;
  }

  section {
    background: var(--color-background);
    color: var(--color-foreground);
    font-family: var(--font-ja);
    font-size: 22px;
    padding: 48px 64px;
    line-height: 1.7;
  }

  h1, h2, h3 {
    font-family: var(--font-latin), var(--font-ja);
    color: var(--color-foreground);
  }

  h1 {
    font-size: 2.0em;
    font-weight: 700;
    border-bottom: 3px solid var(--color-accent);
    padding-bottom: 0.2em;
    margin-bottom: 0.6em;
  }

  h2 {
    font-size: 1.5em;
    font-weight: 700;
    color: var(--color-accent);
    margin-top: 0.4em;
    margin-bottom: 0.4em;
  }

  h3 {
    font-size: 1.1em;
    font-weight: 700;
    color: var(--color-foreground);
  }

  ul, ol {
    padding-left: 1.4em;
  }

  li {
    margin-bottom: 0.3em;
  }

  strong {
    color: var(--color-accent);
    font-weight: 700;
  }

  code {
    background: var(--color-section);
    padding: 0.1em 0.4em;
    border-radius: 4px;
    font-size: 0.9em;
    font-family: 'Cascadia Code', 'Consolas', monospace;
  }

  table {
    border-collapse: collapse;
    width: 100%;
    font-size: 0.85em;
  }

  th {
    background: var(--color-accent);
    color: #ffffff;
    padding: 8px 14px;
    text-align: left;
  }

  td {
    border-bottom: 1px solid #e0e0e0;
    padding: 7px 14px;
  }

  tr:nth-child(even) td {
    background: var(--color-section);
  }

  footer {
    font-size: 0.7em;
    color: #888;
  }

  /* Title slide */
  section.title {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    background: var(--color-background);
  }

  section.title h1 {
    font-size: 2.2em;
    border-bottom: none;
    line-height: 1.3;
    margin-bottom: 0.3em;
  }

  section.title .subtitle {
    font-size: 1.0em;
    color: #555;
    margin-top: 0.5em;
  }

  section.title .date {
    font-size: 0.85em;
    color: #888;
    margin-top: 1.5em;
  }

  /* Chapter title slide */
  section.chapter {
    display: flex;
    flex-direction: column;
    justify-content: center;
    background: var(--color-accent);
    color: #ffffff;
  }

  section.chapter h1 {
    color: #ffffff;
    border-bottom: 3px solid rgba(255,255,255,0.4);
    font-size: 2.0em;
  }

  section.chapter h2 {
    color: rgba(255,255,255,0.85);
    font-size: 1.2em;
  }

  /* Tag/badge */
  .tag {
    display: inline-block;
    background: var(--color-accent);
    color: #fff;
    font-size: 0.7em;
    padding: 2px 8px;
    border-radius: 10px;
    margin-right: 4px;
    vertical-align: middle;
  }

  .tag-ga {
    background: #1a7f37;
  }

  .tag-preview {
    background: #9a6700;
  }
---

<!-- _class: title -->
<!-- _paginate: false -->

# GitHub Copilot &amp; GitHub 最新アップデート

<div class="subtitle">GitHub Universe 2025 以降の動向まとめ</div>
<div class="date">2026年3月</div>

---

<!-- _paginate: false -->

## アジェンダ

1. **GitHub Copilot の概要**
2. **GitHub Universe 2025 の発表とその後の動向**
3. **GitHub Copilot アップデート情報のピックアップ**
　（GitHub Universe 2025 以降）
4. **その他の GitHub 関連情報のピックアップ**

---

<!-- _class: chapter -->
<!-- _paginate: false -->

# 1
## GitHub Copilot の概要

---

## GitHub Copilot とは

> *"GitHub Copilot is an AI coding assistant that helps you write code faster and with less effort. Then, you can focus more energy on problem solving and collaboration."*
> — docs.github.com

### 利用できる場所
- **IDE**：VS Code、Visual Studio、JetBrains IDE、Eclipse、Xcode、Vim/Neovim
- **GitHub.com**（Web）
- **GitHub Mobile**（チャットインターフェース）
- **コマンドライン**：GitHub CLI（Copilot CLI）

> 出典：[docs.github.com](https://docs.github.com/en/copilot/about-github-copilot/what-is-github-copilot)

---

## 主な機能

### 💻 IDE 上で使う機能
- **Inline suggestion**：コンテキストを読み取り次のコードをリアルタイム提案
- **Copilot Chat**：コードについて自然言語で質問・生成・説明を依頼

### 🤖 エージェントとして使う機能
- **Copilot coding agent**：Issue をアサインするだけで、ブランチ作成・コード変更・PR 作成まで **自律実行**
- **Copilot code review**：PR のコード変更を AI がレビューし、改善提案を提供

### 🌐 GitHub.com で使う機能
- **Copilot Chat**（GitHub.com）：Web 上でコードについて質問・生成・説明を依頼
- **PR サマリー自動生成**：PR のコード変更の説明文を自動生成
- **Copilot Spaces**：コンテキストを整理・共有してより関連性の高い回答を取得

> 出典：[docs.github.com](https://docs.github.com/en/copilot/about-github-copilot/what-is-github-copilot)

---

## 利用プランの概要

| プラン | 対象 | 主な特徴 |
|--------|------|----------|
| **Copilot Free** | 個人（無料） | 限定的な機能・リクエスト数で AI コーディングを体験 |
| **Copilot Student** | 学生（無料） | 無制限の補完、プレミアムモデル、coding agent |
| **Copilot Pro** | 個人（有料） | 無制限の補完、プレミアムモデル、coding agent |
| **Copilot Pro+** | 個人（有料） | Pro の全機能 ＋ より多いプレミアムリクエスト、全モデルアクセス |
| **Copilot Business** | 組織 | coding agent、集中管理・ポリシー制御 |
| **Copilot Enterprise** | 大規模企業 | Business の全機能 ＋ エンタープライズグレードの機能 |

- 教員・OSS メンテナーは Copilot Pro への無料アクセスが得られる場合あり
- **Copilot Student** プランは、GitHub Education の特典からプランとして切り出された（2026年3月〜）

> 出典：[docs.github.com](https://docs.github.com/en/copilot/about-github-copilot/subscription-plans-for-github-copilot)

---

<!-- _class: chapter -->
<!-- _paginate: false -->

# 2
## GitHub Universe 2025 の発表と<br>その後の動向

---

## GitHub Universe 2025 とは

- **開催日**：2025年10月28〜29日
- **場所**：Fort Mason Center, San Francisco
- GitHub が年に一度開催する開発者向けカンファレンス

### コンテンツトラック（3つ）
1. 🚀 **Build faster, stay in flow** — AI ネイティブツールで開発ライフサイクルを変革
2. 🔐 **Secure every commit** — AI 活用の脆弱性検出とシームレスなセキュリティ
3. ⚡ **Automate and scale with confidence** — CI/CD 最適化と GitHub Copilot の ROI 測定

<br>

> *"Build what's next on GitHub, the place for anyone from anywhere to build anything."*

> 出典：[github.blog](https://github.blog/news-insights/company-news/github-universe-2025-heres-whats-in-store-at-this-years-developer-wonderland/)

---

## GitHub Universe 2025 発表まとめ

### 公式レポートページ

<br>

> 🔗 **https://github.com/events/universe/recap?locale=ja**

<br>

GitHub Universe 2025 の全発表内容は、上記の公式レポートページにまとめられています。  
基調講演・セッション・デモのハイライトを日本語でご覧いただけます。

---

## Universe 2025 発表（1）：Mission Control

### Copilot coding agent のタスク管理を刷新
- セッションログを **Overview** / **Files changed** タブの横に表示
- コミットの根拠をリアルタイムで確認しながら進捗をモニタリング

### リアルタイムステアリング
- エージェントが動作中でも **リアルタイムにガイダンス** を提供可能
- チャット入力、または Files changed ビュー内のコメントから直接フィードバック

### タスク管理の集約
- タスクステータスを一覧で把握、Copilot が確認を求める際に素早く対応
- Codespaces・VS Code・GitHub CLI からシームレスに作業継続

> 出典：[github.blog/changelog](https://github.blog/changelog/2025-10-28-a-mission-control-to-assign-steer-and-track-copilot-coding-agent-tasks/)

---

## Universe 2025 発表（2）：カスタムエージェント

### `.github/agents` 設定ファイルでエージェントをカスタマイズ
- リポジトリまたは組織の `.github/agents` にマークダウンの設定ファイルを追加
- エージェントのペルソナ・プロンプト・ツール選択・MCP サーバーを定義

### 主なメリット
- チームのワークフロー・規約・ニーズに特化したエージェントを定義
- 組織固有・チーム固有のエージェントを共有リポジトリで管理
- Copilot coding agent（github.com）、Copilot CLI で動作（VS Code は今後対応）

### 活用例
- Frontend エンジニア向けサブエージェント（React/Vue の規約を強制）
- GitHub CLI の MCP を使ってカスタムタスクを自動化するエージェント

> 出典：[github.blog/changelog](https://github.blog/changelog/2025-10-28-custom-agents-for-github-copilot/)

---

## Universe 2025 発表（3）：Slack 連携 / コード品質

### Copilot coding agent × Slack
- Slack の GitHub アプリで `@GitHub` にメンションするだけで PR を生成
- バックグラウンドで動作し、完成したら Slack スレッドに返信
- Microsoft Teams との連携も GA 済み（2025年9月〜）

### GitHub Code Quality（パブリックプレビュー）
- PR をコード品質改善の機会に変換
- CodeQL ベースの品質ルールで保守性・信頼性の問題を検出
  - 対応言語：Java、C#、Python、JavaScript、Go、Ruby
- **ワンクリック Copilot 修正**でインライン表示の指摘をすぐに対処
- 信頼性・保守性スコアで技術的負債の優先順位を把握

> 出典：[github.blog/changelog](https://github.blog/changelog/2025-10-28-work-with-copilot-coding-agent-in-slack/) / [github.blog/changelog](https://github.blog/changelog/2025-10-28-github-code-quality-in-public-preview/)

---

## Universe 2025 発表（4）：その他のアップデート

### Immutable Releases（GA）
- リリースのアセット・タグを公開後に改ざんできないよう保護
- ソフトウェアサプライチェーンセキュリティの新たな層

### ホームダッシュボードの刷新（パブリックプレビュー）
- 最重要タスクを一画面で把握・アクションできるよう改善

### Visual Studio — October 2025 Update
- 新しいモデル選択肢の追加
- よりプロジェクトを理解した Copilot の提案
- Copilot Chat での **プランニング機能** の導入

> 出典：[github.blog/changelog](https://github.blog/changelog/month/10-2025/) / [github.blog/changelog](https://github.blog/changelog/2025-10-27-github-copilot-in-visual-studio-october-update/)

---

<!-- _class: chapter -->
<!-- _paginate: false -->

# 3
## GitHub Copilot<br>アップデート情報のピックアップ
### （GitHub Universe 2025 以降）

---

## 2025年12月のアップデート

### Copilot Memory（プレビュー）
- Copilot Pro / Pro+ 向けにパブリックプレビュー開始
- coding agent とコードレビューでリポジトリ固有のメモリをサポート
- コードベースから重要な知見を蓄積し、エージェントの精度を向上

### Agent Skills
- **Agent Skills**：タスクを特定・繰り返し可能な方法で実行するよう Copilot に教える仕組み
- スキルはフォルダー構成（インストラクション・スクリプト・リソース）
- プロンプトに関連すると判断したとき自動的にロード
- coding agent・Copilot CLI・VS Code のエージェントモードで動作

### API から Issue を Copilot にアサイン
- GraphQL・REST API 経由でイシューを Copilot にアサイン可能に

> 出典：[github.blog/changelog](https://github.blog/changelog/2025-12-19-copilot-memory-early-access-for-pro-and-pro/) / [github.blog/changelog](https://github.blog/changelog/2025-12-18-github-copilot-now-supports-agent-skills/)

---

## 2026年1月のアップデート

### Agents タブ（リポジトリ内）
- Copilot coding agent のタスク管理がリポジトリ内の **Agents タブ** に統合
- コード・PR・イシューと並んでセッションを管理
- セッションログのグルーピングが改善、ファイル変更の diff をワンクリックで展開
- **Copilot CLI** でセッションを継続する機能を追加

### Copilot SDK（テクニカルプレビュー）
- Copilot CLI へのプログラムアクセスを提供する言語別 SDK
- 対応言語：**Node.js / Python / Go / .NET**

### ACP（Agent Client Protocol）のサポート（Copilot CLI）
- AI エージェントとクライアント間の業界標準プロトコルを実装
- サードパーティツール・IDE・自動化システムから Copilot CLI を統合可能に

> 出典：[github.blog/changelog](https://github.blog/changelog/2026-01-26-introducing-the-agents-tab-in-your-repository/) / [github.blog/changelog](https://github.blog/changelog/2026-01-14-copilot-sdk-in-technical-preview/)

---

## 2026年2月のアップデート

### Copilot CLI — GA（2026年2月25日）
- ターミナルネイティブなコーディングエージェントとして **正式リリース**
- Plan モード / Autopilot モード / 内蔵専門エージェント（Explore・Task・Code Review 等）
- MCP・プラグイン・Agent Skills でカスタマイズ可能
- セッションを超えた **リポジトリメモリ**（過去のコンテキストを記憶）
- macOS / Linux / Windows 対応、GitHub Codespaces にも標準搭載

### Copilot メトリクス — GA
- Copilot の採用状況・利用トレンドを一元管理

### Web 上の Copilot での Web 検索改善
- 特定モデルでモデルネイティブの Web 検索が利用可能に

### Zed エディタサポート — GA
- GitHub Copilot が Zed を公式サポート（Pro・Pro+・Business・Enterprise）

> 出典：[github.blog/changelog](https://github.blog/changelog/2026-02-25-github-copilot-cli-is-now-generally-available/)

---

## 2026年2月のアップデート（続き）

### Copilot coding agent — Windows プロジェクト対応
- Windows プロジェクトで Copilot coding agent が利用可能に

### Copilot coding agent — コード参照対応
- エージェントが生成したコードがパブリックリポジトリのコードと一致する場合、一致したコードのリンクを表示

### Visual Studio — January Update（2026年2月4日公開）
- Copilot Chat の構文ハイライト付き補完
- 部分的なコード提案の承認（Partial Acceptance）
- デバッグ・テスト・モダナイゼーション連携の強化

> 出典：[github.blog/changelog](https://github.blog/changelog/2026-02-18-use-copilot-coding-agent-with-windows-projects/) / [github.blog/changelog](https://github.blog/changelog/2026-02-18-copilot-coding-agent-supports-code-referencing/)

---

## 2026年3月のアップデート（1）

### GPT-5.4 — GA（2026年3月5日）
- OpenAI の最新エージェントコーディングモデル
- 実世界・エージェント・ソフトウェア開発タスクで新たな成功率を達成
- 強化された論理推論と複雑なマルチステップタスクの実行能力
- VS Code / Visual Studio / JetBrains / Xcode / Eclipse / github.com / GitHub Mobile / CLI / coding agent で利用可能

### エージェントセッションへの画像追加（2026年3月5日）
- github.com の Agents タブなどで画像からエージェントセッションを開始
- ペースト・ドラッグ&ドロップ・アイコンクリックで画像を添付

### Visual Studio — February Update（2026年3月4日公開）
- 拡張されたエージェント機能
- よりスマートな inline suggestion
- デバッグ・テスト・モダナイゼーションワークフロー全体への深い統合

> 出典：[github.blog/changelog](https://github.blog/changelog/2026-03-05-gpt-5-4-is-generally-available-in-github-copilot/)

---

## 2026年3月のアップデート（2）

### GPT-5.3-Codex — LTS（長期サポート）モデル（2026年3月18日）
- エンタープライズ向けに **12ヶ月間** の安定サポートを保証
- 2026年2月5日リリース → 2027年2月4日まで Business / Enterprise で利用可能
- GPT-4.1 に替わる **新しいベースモデル** として採用
- エンタープライズで高いコードサバイバルレートを記録

### Copilot coding agent の検証ツール設定（2026年3月18日）
- coding agent がコードを書いたとき自動的に以下を実行：
  - プロジェクトのテスト・リンター
  - CodeQL・GitHub Advisory Database・シークレットスキャン・Copilot コードレビュー
- **リポジトリ管理者**が実行する検証ツールを設定できるように

### GitHub CLI から Copilot コードレビューをリクエスト（2026年3月11日）
- `gh pr edit --add-reviewer @copilot` でターミナルから直接 Copilot にレビューを依頼

> 出典：[github.blog/changelog](https://github.blog/changelog/2026-03-18-gpt-5-3-codex-long-term-support-in-github-copilot/) / [github.blog/changelog](https://github.blog/changelog/2026-03-18-configure-copilot-coding-agents-validation-tools/)

---

## 2026年3月のアップデート（3）

### Copilot Student プラン（2026年3月13日）
- **GitHub Education の特典からプランとして切り出され**、新しい **Copilot Student プラン** として提供開始
- 長期的・持続可能な学生向け Copilot 体験に向けたモデルラインナップを更新

> 出典：[github.blog/changelog](https://github.blog/changelog/2026-03-13-updates-to-github-copilot-for-students/)

---

<!-- _class: chapter -->
<!-- _paginate: false -->

# 4
## その他の GitHub 関連情報<br>のピックアップ

---

## GitHub Actions のアップデート

### 環境をデプロイなしで利用可能に（2026年3月19日）
- `deployment: false` キーで環境を設定すると、デプロイメントを作成せずにシークレット・変数を使用可能
- デプロイ不要なシークレット・変数管理だけに環境を使いたいケースを解決

### スケジュールワークフローのタイムゾーン対応（2026年3月19日）
- cron スケジュールに IANA タイムゾーンを指定可能に（例：`timezone: "America/New_York"`）
- UTC に縛られず、現地時間でワークフローを実行

### Actions Runner Controller 0.14.0 — GA（2026年3月19日）
- **マルチラベルサポート**：ランナースケールセット向け
- `actions/scaleset` ライブラリクライアントに移行
- リソースカスタマイズオプションの追加

> 出典：[github.blog/changelog](https://github.blog/changelog/2026-03-19-github-actions-late-march-2026-updates/) / [github.blog/changelog](https://github.blog/changelog/2026-03-19-actions-runner-controller-release-0-14-0/)

---

## セキュリティ関連のアップデート

### Dependabot — npm マルウェア検出（2026年3月17日）
- npm パッケージの悪意あるバージョンを検出する **Dependabot アラート** が利用可能に
- GitHub Advisory Database のマルウェアアドバイザリと照合
- CVE ベースの脆弱性アラートと別カテゴリーで管理

### GitHub Advanced Security — セットアップ簡素化（2026年3月17日）
- 組織での Advanced Security 設定を簡単にするガイド付き体験
- 設定・リポジトリターゲティングをより速く編集可能に
- GitHub Enterprise Cloud で利用可能（GHES 3.22 でリリース予定）

### シークレットスキャン パターン更新（2026年3月10日）
- **28種** の新しいシークレット検出器（15プロバイダー：Lark、Vercel、Snowflake、Supabase 等）
- **39種**の検出器でプッシュ保護がデフォルト有効化（Airtable、Databricks、Heroku 等）
- Airtable / DeepSeek / npm / Pinecone / Sentry トークンへの **有効性チェック** 追加

> 出典：[github.blog/changelog](https://github.blog/changelog/2026-03-17-dependabot-now-detects-malware-in-npm-dependencies/) / [github.blog/changelog](https://github.blog/changelog/2026-03-10-secret-scanning-pattern-updates-march-2026/)

---

## 開発者体験・プラットフォームのアップデート

### REST API バージョン 2026-03-10（2026年3月12日）
- カレンダーベースのバージョニングで **初めて破壊的変更** を含むバージョンをリリース
- `2022-11-28` は今後 24ヶ月以上サポート継続
- `X-GitHub-Api-Version: 2026-03-10` ヘッダーで新バージョンに移行

### リポジトリダッシュボード — GA（2026年2月24日）
- アクセス可能なリポジトリを見つけ・フィルタリングし・カスタムビューを保存する機能が正式リリース

### Immutable Releases — GA（2025年10月28日 @Universe）
- リリースのアセット・タグを公開後に改ざん不可能に保護
- ソフトウェアサプライチェーンの信頼性を強化

> 出典：[github.blog/changelog](https://github.blog/changelog/2026-03-12-rest-api-version-2026-03-10-is-now-available/) / [github.blog/changelog](https://github.blog/changelog/2025-10-28-immutable-releases-are-now-generally-available/)

---

## まとめ

### GitHub Copilot の進化
- **コード補完ツール** から **自律的なコーディングエージェント** へ
- Copilot CLI GA・Agent Skills・Copilot Memory など、エージェント基盤が着実に強化
- GPT-5.4 GA・GPT-5.3-Codex LTS など、モデル選択肢と安定性も向上

### GitHub Universe 2025 のポイント
- **Mission Control** による Copilot coding agent タスクの一元管理
- **Custom Agents**（`.github/agents/`）でチーム固有のエージェントを定義
- Slack 連携・GitHub Code Quality など、開発ワークフロー全体を AI でカバー

### 2026年に注目のトレンド
- Copilot coding agent の検証ツール設定など、**エージェントの信頼性・ガバナンス** の強化
- Dependabot マルウェア検出など、**セキュリティの自動化** がさらに深化
- REST API の新バージョンリリースなど、**プラットフォーム API の進化** が続く

---

<!-- _paginate: false -->

## 参照情報

- **The GitHub Blog** — [github.blog](https://github.blog)
- **GitHub Changelog** — [github.blog/changelog](https://github.blog/changelog)
- **GitHub Docs** — [docs.github.com](https://docs.github.com)
- **GitHub Universe** — [githubuniverse.com](https://githubuniverse.com)

<br>

> ※ 本スライドの情報は上記 4 つの公式ソースのみを参照しています。

