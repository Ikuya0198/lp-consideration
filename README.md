# Avisail Technologies - 新LP構成案（lp-consideration）

## プロジェクト概要

このディレクトリは、Avisail Technologies の新しいランディングページ（LP）の構成案です。既存のLPとは完全に切り離して開発を進めています。

**目的:**
- 情報量を増やし、整理する
- 何をしている会社か明確にする
- 商材への案内をスムーズに
- 課金までの導線を作る

**ベース:**
- `lp-consideration.md` の詳細構成案
- 既存LPのデザインシステムを踏襲
- ChatGPTが作成したHTMLアイデアを参考（改善済み）

---

## ディレクトリ構造

```
lp-consideration/
├── index.html                  # メインランディングページ
├── ja/
│   └── legal/
│       ├── privacy-policy.html # プライバシーポリシー
│       ├── terms.html          # 利用規約
│       ├── cookies.html        # クッキーポリシー
│       └── security.html       # セキュリティ方針
├── images/
│   └── README.md               # 画像プレースホルダー説明
├── lp-consideration.md         # LP構成案の詳細ドキュメント
└── README.md                   # このファイル
```

---

## ファイル説明

### index.html

新しいメインランディングページ。以下のセクションで構成：

1. **Hero（ヒーロー）** - ファーストビュー、スローガン、メッセージ
2. **Purpose & Passion** - 会社の存在意義と情熱
3. **Our Business** - 4つの事業領域（Trading / Investment / Security / AI & Development）
4. **Technology Foundation** - AIによる統合技術基盤の説明
5. **Proven Results** - 実績・技術力の証明（数字、技術スタック）
6. **Use Cases** - 活用事例（3つのケーススタディ）
7. **Why Choose Avisail** - 選ばれる3つの理由
8. **Explore Solutions** - 各事業への大型カードリンク
9. **FAQ** - よくある質問（7項目）
10. **Contact & Resources** - お問い合わせフォームとリソースリンク
11. **Footer** - フッター情報

### 法的ページ（ja/legal/）

4つの法的ページで構成。商業レベルの信頼性を確保：

- **privacy-policy.html** - データ収集、利用目的、第三者提供など
- **terms.html** - サービス利用条件、禁止事項、免責事項など
- **cookies.html** - クッキーの種類、管理方法など
- **security.html** - セキュリティ対策、インシデント対応など

---

## デザインシステム

### カラーパレット

```css
--primary-gradient: linear-gradient(135deg,#6aa6ff,#7ef0d4);
--accent-teal: #7ef0d4;
--accent-blue: #6aa6ff;
--bg-dark: #0a0f1a;
--bg-darker: #05080f;
--text-primary: #e9f0ff;
--text-secondary: #cfe2ff;
--text-muted: #9fb0cc;
```

### タイポグラフィ

- **フォント:** Inter（英数字）、Noto Sans JP（日本語）
- **見出し階層:** H1 (2.8-4.5rem) → H2 (2rem) → H3 (1.4rem)
- **本文:** 1.05-1.15rem、行間 1.7-1.9

### コンポーネント

- **カード:** 半透明背景、ぼかし効果、ホバーアニメーション
- **ボタン:** .btn（アウトライン）、.cta（グラデーション）
- **グリッド:** .grid-2, .grid-3, .grid-4

---

## レスポンシブ対応

### ブレークポイント

- **980px以下:** グリッドを1カラムに、ナビゲーション非表示
- **640px以下:** 統計グリッドを1カラムに、ヒーローサイズ調整

### メディアクエリ

```css
@media(max-width:980px) { /* タブレット */ }
@media(max-width:640px) { /* モバイル */ }
```

---

## 画像について

現在、画像ファイルはプレースホルダーです。
詳細は `images/README.md` を参照してください。

**必要な画像（合計9枚）:**
- hero-bg.jpg（ヒーロー背景）
- vessel-trading.jpg（事業カード）
- investment.jpg（事業カード）
- security.jpg（事業カード）
- ai-development.jpg（事業カード）
- vessel-trading-hero.jpg（大型カード）
- investment-hero.jpg（大型カード）
- security-hero.jpg（大型カード）
- ai-development-hero.jpg（大型カード）

---

## 次のステップ

### 1. 画像の準備
- Unsplashから適切な画像を選定
- または既存の画像を使用
- または一時的にグラデーション背景で代替

### 2. コンテンツの微調整
- 実際の数字・実績に更新
- ケーススタディを具体化（可能であれば）
- FAQを追加・調整

### 3. リンク先ページの作成
各事業の詳細ページ：
- `/ja/services/trading.html`
- `/ja/services/investment.html`
- `/ja/services/security.html`
- `/ja/services/ai-development.html`

### 4. フォーム機能の実装
お問い合わせフォームの送信先を設定：
- メール送信サービス（SendGrid, Mailgunなど）
- または独自のバックエンド

### 5. アナリティクスの設定
- Google Analytics
- ヒートマップツール（Hotjar等）

### 6. SEO最適化
- メタタグの最適化
- 構造化データ（Schema.org）
- サイトマップ生成

---

## ローカル確認方法

### シンプルな方法（ブラウザで直接開く）

```bash
open lp-consideration/index.html
```

または、ブラウザのアドレスバーに以下をドラッグ＆ドロップ：
```
/Users/ikuyaodaka/Desktop/Avisail/Codes/InitProject/lp-consideration/index.html
```

### ローカルサーバーで確認（推奨）

```bash
# Python 3の場合
cd lp-consideration
python3 -m http.server 8000

# Node.jsのlive-serverを使う場合
npx live-server lp-consideration
```

その後、ブラウザで `http://localhost:8000` にアクセス。

---

## GitHubへのアップロード準備

### 新規リポジトリ作成時

```bash
cd lp-consideration
git init
git add .
git commit -m "Initial commit: New LP structure"
git branch -M main
git remote add origin https://github.com/YOUR_USERNAME/lp-consideration.git
git push -u origin main
```

### GitHub Pagesでの公開

1. GitHubリポジトリの Settings → Pages
2. Source: "Deploy from a branch"
3. Branch: main / (root)
4. Save

数分後、`https://YOUR_USERNAME.github.io/lp-consideration/` でアクセス可能になります。

---

## 重要な変更点（既存LPとの違い）

### 構成の改善

1. **4事業の平等な扱い** - 全事業を同じ重みで提示
2. **Technology Foundationセクション** - AIが全事業を支える構造を明確化
3. **実績セクションの追加** - 技術的実績にフォーカス（組織情報は避ける）
4. **Use Casesの具体化** - 抽象的だが業種・課題・ソリューションを明示
5. **法的ページの充実** - 4ページで信頼性を担保

### デザインの改善

1. **レスポンシブ対応** - モバイル・タブレットで崩れない
2. **アクセシビリティ** - label、適切なコントラスト、セマンティックHTML
3. **アニメーション** - スクロールインジケーター、ホバー効果
4. **統一感** - 既存LPのデザインシステムを踏襲しながら拡張

### コンテンツの改善

1. **情報量の増加** - 各セクションに十分な説明
2. **導線の明確化** - Hero → Business → Details → Contact という流れ
3. **FAQの充実** - 商業レベルの7項目
4. **CTAの配置** - 適切な位置に行動喚起ボタン

---

## 制約事項と対応

### 制約1: 法人設立前
**対応:** 具体的な組織情報（人数、住所）は記載せず、技術的実績にフォーカス

### 制約2: 画像が未準備
**対応:** プレースホルダーパスを使用。`images/README.md` に詳細説明を記載

### 制約3: リンク先ページが未作成
**対応:** `href="#"` で一旦対応。後ほど各事業の詳細ページを作成予定

---

## 連絡先

プロジェクトに関する質問や提案は、お問い合わせフォームまたはGitHub Issuesにて。

---

## ライセンス

© 2025 Avisail Technologies — All rights reserved.

---

## 作成日

2025年12月2日

Claude Code (Sonnet 4.5) により作成
