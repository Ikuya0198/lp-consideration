# 画像ファイル - プレースホルダー説明

このディレクトリには、LP（ランディングページ）で使用する画像ファイルを配置します。

## 必要な画像ファイル一覧

### メインヒーロー画像

**ファイル名:** `hero-bg.jpg`
- **推奨サイズ:** 1920x1080px以上
- **用途:** トップページのヒーロー背景
- **イメージ:** 船舶、海、航海、先進技術、グローバルネットワークなど
- **スタイル:** ダーク調、プロフェッショナル、モダン

---

### 事業領域サムネイル（4枚）

#### 1. Trading（船舶売買）
**ファイル名:** `vessel-trading.jpg`
- **推奨サイズ:** 800x600px
- **イメージ:** 船舶、港、国際貿易、コンテナ、グローバル物流
- **カラー:** ブルー系、プロフェッショナル

#### 2. Investment（投資）
**ファイル名:** `investment.jpg`
- **推奨サイズ:** 800x600px
- **イメージ:** グラフ、チャート、データ分析、金融市場、成長曲線
- **カラー:** グリーン/ブルー系、ビジネス的

#### 3. Security（セキュリティ）
**ファイル名:** `security.jpg`
- **推奨サイズ:** 800x600px
- **イメージ:** サイバーセキュリティ、ネットワーク、デジタルロック、データ保護
- **カラー:** ティール/ブルー系、技術的

#### 4. AI & Development（AI・技術開発）
**ファイル名:** `ai-development.jpg`
- **推奨サイズ:** 800x600px
- **イメージ:** AI、コーディング、ニューラルネットワーク、技術革新
- **カラー:** パープル/ブルー系、未来的

---

### Explore Solutions（大型カード用）

#### 1. Vessel Trading Hero
**ファイル名:** `vessel-trading-hero.jpg`
- **推奨サイズ:** 1200x800px
- **用途:** 「Explore Solutions」セクションの大型カード背景
- **イメージ:** vessel-trading.jpgと同じテーマだが、より高品質・大型

#### 2. Investment Hero
**ファイル名:** `investment-hero.jpg`
- **推奨サイズ:** 1200x800px
- **用途:** 「Explore Solutions」セクションの大型カード背景
- **イメージ:** investment.jpgと同じテーマだが、より高品質・大型

#### 3. Security Hero
**ファイル名:** `security-hero.jpg`
- **推奨サイズ:** 1200x800px
- **用途:** 「Explore Solutions」セクションの大型カード背景
- **イメージ:** security.jpgと同じテーマだが、より高品質・大型

#### 4. AI & Development Hero
**ファイル名:** `ai-development-hero.jpg`
- **推奨サイズ:** 1200x800px
- **用途:** 「Explore Solutions」セクションの大型カード背景
- **イメージ:** ai-development.jpgと同じテーマだが、より高品質・大型

---

## 画像取得方法

### オプション1: Unsplash（無料）
高品質な無料画像サイト: https://unsplash.com/

推奨検索キーワード:
- Hero背景: "ship sailing", "ocean voyage", "global shipping"
- Trading: "cargo ship", "container port", "shipping industry"
- Investment: "financial charts", "stock market", "data analytics"
- Security: "cybersecurity", "network security", "digital protection"
- AI & Development: "artificial intelligence", "neural network", "coding"

### オプション2: 既存の画像を使用
`/avisail/images/` ディレクトリに既に存在する画像を参照して使用することも可能です。

### オプション3: カスタム画像
- デザイナーに依頼してオリジナル画像を作成
- 実際の事業に関連する写真を撮影

---

## 一時的な対応（開発段階）

開発段階では、以下の方法で画像を代替できます：

### 方法1: CSS Gradientで代替
```css
background: linear-gradient(135deg, #6aa6ff, #7ef0d4);
```

### 方法2: Unsplash API経由で直接読み込み
```html
<div style="background-image:url('https://images.unsplash.com/photo-[ID]?w=1200');">
```

### 方法3: プレースホルダーサービス
```html
<div style="background-image:url('https://via.placeholder.com/800x600/1a1f3a/7ef0d4?text=Trading');">
```

---

## 画像最適化の推奨事項

実際の画像を配置する際は、以下の点に注意してください：

1. **ファイルサイズ:** 各画像を200KB以下に圧縮（WebP形式推奨）
2. **遅延読み込み:** `loading="lazy"` 属性を追加
3. **レスポンシブ:** 複数サイズを用意（srcset属性）
4. **Alt属性:** アクセシビリティのため必ず記載
5. **WebP + JPEG:** 両形式を用意してブラウザ対応

---

## 作成日
2025年12月2日
