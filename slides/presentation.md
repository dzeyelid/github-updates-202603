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

  /* Highlight box */
  .highlight {
    background: var(--color-accent-light);
    border-left: 4px solid var(--color-accent);
    padding: 12px 16px;
    border-radius: 0 6px 6px 0;
    margin: 0.6em 0;
  }

  /* Two-column layout */
  .columns {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 2em;
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
3. **GitHub Copilot アップデート情報のピックアップ**<br>　（GitHub Universe 2025 以降）
4. **その他の GitHub 関連情報のピックアップ**

---

<!-- _class: chapter -->
<!-- _paginate: false -->

# 1
## GitHub Copilot の概要

---

## GitHub Copilot とは

- **GitHub と OpenAI が共同開発** した AI ペアプログラミングツール
- コードの補完・生成・説明・レビューを AI がアシスト
- **2022年6月** に一般提供開始、現在は大幅に機能拡張

<br>

> *"GitHub Copilot is your AI pair programmer."*
> — github.blog

<br>

- 50以上のプログラミング言語に対応
- VS Code / Visual Studio / JetBrains / Neovim / Xcode 等に対応

---

## 主な機能

### 🤖 コード補完・生成
- インライン補完：コードを書きながらリアルタイムに次のコードを提案
- チャット（Copilot Chat）：自然言語でコードの質問・生成・説明を依頼

### 🛠 エージェント機能
- **Copilot coding agent**：Issue をアサインするだけで、ブランチ作成・コード変更・PR作成まで自律実行
- **Copilot Workspace**：アイデアからコード変更計画・実装まで一貫サポート

### 🔒 セキュリティ
- 脆弱なコードの提案フィルタリング
- セキュリティ脆弱性の自動検出・修正提案

---

## 利用プランの概要

| プラン | 対象 | 主な特徴 |
|--------|------|----------|
| **Free** | 個人（無料） | 月2,000回のコード補完、月50回のチャット |
| **Pro** | 個人 $10/月 | 無制限の補完、月300回のプレミアムリクエスト |
| **Pro+** | 個人 $39/月 | 全モデル利用可、月1,500回のプレミアムリクエスト |
| **Business** | 組織 $19/ユーザー/月 | 組織管理・ポリシー制御、SSO対応 |
| **Enterprise** | 大企業 $39/ユーザー/月 | カスタム設定・社内コードベース連携 |

<br>

- 学生・教職員・OSS開発者向けの **無料プラン** あり
- 2026年3月より **Copilot Student プラン** 開始

---

## 対応モデル・エコシステム

- **マルチモデル対応**：OpenAI、Anthropic、Google のモデルから選択可能
  - GPT-5.x-Codex シリーズ、Claude Sonnet/Opus、Gemini Pro 等
- **Auto モード**：タスクに最適なモデルを自動選択

<br>

### 主要な統合先
- IDE：VS Code、Visual Studio、JetBrains、Neovim、Eclipse、Xcode
- プラットフォーム：GitHub.com、GitHub Mobile、GitHub CLI
- 外部ツール：Slack、Microsoft Teams、Azure Boards、Linear 等

---

<!-- _class: chapter -->
<!-- _paginate: false -->

# 2
## GitHub Universe 2025 の発表と<br>その後の動向

---

## GitHub Universe 2025 とは

- **開催日**：2025年10月28〜29日（San Francisco）
- GitHub が年に一度開催する開発者向けカンファレンス
- 2025年は「**AI エージェント時代**」をテーマに多数のアップデートを発表

<br>

### キーメッセージ

> *"Developers drive the AI agent era with GitHub."*

<br>

- AI による自動化の焦点が「コード補完」から「**自律的なコーディングエージェント**」へ
- 開発者がエージェントを管理・統制する時代への移行を宣言

> 出典：[github.blog](https://github.blog/news-insights/company-news/github-universe-2025-heres-whats-in-store-at-this-years-developer-wonderland/)

---

## 主な発表（1）：Agent HQ & ミッションコントロール

### Agent HQ
- 複数の AI エージェントを一元管理するプラットフォーム
- GitHub、OpenAI、Anthropic、Google 等のエージェントを統合
- GitHub、VS Code、CLI、モバイルを横断した管理が可能

### Mission Control
- エージェントへのタスク割り当て・進捗追跡の一元ダッシュボード
- エージェントのアイデンティティ管理・競合解消
- **カスタムコーディングエージェント**の構築・デプロイが可能
  - `AGENTS.md` でコーディング規約・振る舞いをリポジトリ単位で定義

> 出典：[github.blog](https://github.blog)

---

## 主な発表（2）：ワークフロー統合の強化

### 外部ツールとの深い連携
- Slack / Microsoft Teams / Azure Boards / Linear からエージェントにタスクを割り当て可能
- タスク完了通知や自動サマリーを各ツールに配信

### Copilot コーディングエージェントの機能拡張
- **セルフホストインフラ**での実行対応（Enterprise 向け）
- Web 検索による最新ドキュメントの参照
- コンテキストを考慮したブランチ名・PR タイトルの自動生成
- CodeQL を活用したセキュリティ脆弱性の自動検出・修正

### MCP（Model Context Protocol）Registry
- VS Code から Stripe、Figma、Sentry 等の外部サービスと直接連携

> 出典：[github.blog](https://github.blog)

---

## 主な発表（3）：IDE の強化

### VS Code
- **Plan モード**：実装計画の立案と AI エージェントとの対話的な仕様確認
- **AGENTS.md**：リポジトリ固有のコーディング規約をエージェントに自動適用
- Copilot の **ワークスペースレベル設定**：モデル・インストラクション・機能のカスタマイズ

### JetBrains IDE
- Copilot のタスク割り当てと実行が JetBrains 内で可能に
- IntelliJ IDEA / その他 JetBrains 製品への対応拡充

### Visual Studio
- スムーズな補完と改善されたワークフロー統合

> 出典：[github.blog](https://github.blog)

---

## 主な発表（4）：コード品質・エンタープライズ

### Code Quality ダッシュボード
- コードの保守性・信頼性・テストカバレッジを可視化
- 組織全体での Copilot 利用状況・エージェント活動のダッシュボード
- リーダーシップ向けに AI 活用の ROI を可視化

### エンタープライズ向け AI ガバナンス
- エージェントの監査可能性・バージョン管理
- 組織ポリシーに基づくエージェント制御
- AI 活用のリスク管理と効果測定

> 出典：[github.blog](https://github.blog)

---

<!-- _class: chapter -->
<!-- _paginate: false -->

# 3
## GitHub Copilot<br>アップデート情報のピックアップ
### （GitHub Universe 2025 以降）

---

## 2025年11月のアップデート

### コーディングエージェント
- セルフホストインフラへの対応が正式化
- Copilot coding agent による自動コードレビュー機能

### Copilot Spaces
- **パブリック共有**：Spaces を直リンクで公開可能に
- **ファイル追加の簡略化**：github.com のコードビューアから直接 Spaces へ追加
- **ロールベース制御**：Space・リポジトリレベルでのアクセス権管理

### CLI の強化
- セマンティックコードベース検索に対応
- 主要な全モデルを CLI から利用可能に

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

## 2025年12月のアップデート

### モデルの拡充

<span class="tag tag-preview">Preview</span> **GPT-5.1-Codex-Max** が Copilot Pro/Business/Enterprise 向けに公開プレビュー

<span class="tag tag-ga">GA</span> **Claude Opus 4.5** / **Gemini 3 Pro** の統合

### カスタムエージェントの拡充
- JetBrains IDE / Eclipse / Xcode でカスタムエージェントの作成・デプロイが可能に

### エンタープライズ向け
- BYOK（Bring Your Own Key）：Anthropic・OpenAI・xAI・Foundry の自前キー利用
- データ保管場所（Data Residency）の設定が可能に

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

## 2026年1月のアップデート

### Copilot SDK（テクニカルプレビュー）
- Node.js / Python / Go / .NET から Copilot をプログラムから活用可能に

### 新モデル
<span class="tag tag-ga">GA</span> **GPT-5.2-Codex** が VS Code・Web・CLI 等で一般提供開始

### エージェントの記憶（Agentic Memory）
- リポジトリ固有のコンテキストを **28日間** 保持
- プロジェクト構造やチームの好みを学習・記憶してより的確な提案へ

### パフォーマンス分析ダッシュボード
- Enterprise/Pro ユーザー向けに Copilot の採用状況・生産性への影響を可視化

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

## 2026年2月のアップデート

### 新モデルの追加
<span class="tag tag-ga">GA</span> **Claude エージェント** / **Codex エージェント** が Business/Enterprise 向けに提供開始

### 使用状況メトリクスの拡充
- エンタープライズレベルで **CLI アクティビティ** の追跡が可能に
- チーム全体の Copilot 活用状況の見える化

### モバイル対応
- GitHub Mobile で **Copilot coding agent のライブ通知** を受信可能に

### Visual Studio の改善
- シンタックスハイライト付きのコード補完
- 部分的なコード提案の承認（Partial Acceptance）
- Copilot Chat のマークダウンプレビュー強化

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

## 2026年3月のアップデート（前半）

### コーディングエージェントの強化
<span class="tag tag-ga">GA</span> **エージェントの検証ツール**：エージェントが行う検証の設定オプション追加

<span class="tag tag-ga">GA</span> **GPT-5.3-Codex** のサポート開始

<span class="tag tag-preview">Preview</span> **Copilot for Jira**：Jira のイシューに Copilot コーディングエージェントを割り当て可能に

### リポジトリ探索機能
- Web 上の Copilot Chat で **ファイルツリーの閲覧・参照** が可能に

### JetBrains IDE 向け改善
- エージェント機能の強化
- **Auto モデル選択**（タスクに応じた自動モデル切替）対応

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

## 2026年3月のアップデート（後半）

### 新モデルの追加

<span class="tag tag-ga">GA</span> **GPT-5.4 Mini**：高速なコード補完向け軽量モデル

### Copilot Student プラン
- 学生向け無料プランを **Copilot Student プラン** として再編
- 一部プレミアムモデルは Auto モードでのみ利用可能に
- GitHub Student Developer Pack 経由で引き続き Copilot Pro を提供

### セキュリティの強化
- MCP サーバー経由の AI コーディングエージェントに **シークレットスキャン**対応
  - エージェントが誤ってシークレット情報を漏洩するリスクを軽減

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

<!-- _class: chapter -->
<!-- _paginate: false -->

# 4
## その他の GitHub 関連情報<br>のピックアップ

---

## GitHub Actions の主なアップデート

### インフラ・ランナーの強化
- **カスタムランナーオートスケーリング**（パブリックプレビュー）
  - Kubernetes 不要でコンテナ・VM・ベアメタルで自動スケール可能
  - マルチラベルジョブ割り当て・リアルタイムジョブテレメトリ対応

### ワークフロー構文の改善
- **タイムゾーン指定** が cron スケジュールで利用可能に
- **環境（Environments）**：デプロイメントをトリガーせずに使用可能に
  → シークレット・変数の管理のみに利用するユースケースが可能に

### Copilot エージェントとの連携
- Copilot エージェントが起動する Actions ワークフローに対して**承認をスキップ**するオプション

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

## セキュリティ関連のアップデート

### シークレットスキャン（2026年3月）
- **28種** の新しいパターン検出器を追加
- **39種**の検出器でプッシュ保護がデフォルト有効化
  - 例：Airtable、Databricks、Heroku、Shopify、Vercel など
- プッシュ保護の**除外設定**：チーム・ロール・アプリ単位で設定可能

### GitHub Advanced Security
- 組織・リポジトリへの Advanced Security 設定の**ガイド付き導入体験**
- コード品質の権限設定を**管理者専用**へ変更（セキュリティマネージャーロールからは削除）

### Pull Request のセキュリティ改善
- コードとコメントの並列表示（Side-by-side ビュー）
- バッチコード品質改善提案の適用機能

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

## GitHub Enterprise Server 3.20

<span class="tag tag-ga">GA</span> **2026年3月 一般提供開始**

### 主な改善点
- **コードセキュリティ**の強化
  - 最新のシークレットスキャン・コードスキャンとの同期
- **ポリシー管理**の改善
  - エンタープライズポリシーの細かな制御が可能に
- **マージエクスペリエンス**の向上
  - よりスムーズな PR マージフロー

### エージェント制御プレーン
- AI エージェントのガバナンス・監査・効果測定をエンタープライズで管理

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

## REST API & 開発者向けアップデート

### REST API バージョン 2026-03-10
- **カレンダーバージョニング**方式を採用
- 破壊的変更と新機能の詳細なアップグレードガイドを提供

### コード品質ダッシュボード
- 組織全体のコード品質メトリクス（保守性・信頼性・テストカバレッジ）を可視化
- エンジニアリングリーダー向けに AI 活用の定量的効果を提示

### 開発者体験の改善
- イシューへの Copilot エージェント割り当てを REST API 経由でプログラムから制御可能
- より細かいリポジトリ・エージェント動作の制御オプション

> 出典：[github.blog/changelog](https://github.blog/changelog)

---

## まとめ

### GitHub Copilot の進化
- **コード補完ツール** → **自律的なコーディングエージェントプラットフォーム** へ
- 複数の AI モデルを選択・自動切替し、より的確な支援が可能に
- エージェントの記憶機能でプロジェクト固有の文脈を継続的に学習

### GitHub Universe 2025 のポイント
- **Agent HQ** による複数エージェントの統一管理
- `AGENTS.md` によるリポジトリ固有のエージェント制御
- Slack / Teams / Jira 等の外部ツールとのシームレスな統合

### 今後の注目点
- Copilot for Jira などエージェントの適用範囲のさらなる拡大
- エンタープライズ向けの AI ガバナンス・コンプライアンス強化
- マルチエージェント協調による大規模タスクの自律実行

---

<!-- _paginate: false -->

## 参照情報

- **The GitHub Blog** — [github.blog](https://github.blog)
- **GitHub Changelog** — [github.blog/changelog](https://github.blog/changelog)
- **GitHub Docs** — [docs.github.com](https://docs.github.com)
- **GitHub Universe** — [githubuniverse.com](https://githubuniverse.com)

<br>

> ※ 本スライドの情報は上記 4 つの公式ソースのみを参照しています。

