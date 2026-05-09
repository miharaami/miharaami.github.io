# 三原あみ 作曲家公式サイト

`miharaami.github.io` 用の静的サイト一式です。

## ファイル構成

```
miharaami/
├── index.html      ─ トップページ（あなたの人生に、一曲を）
├── profile.html    ─ 紹介ページ（作曲家としての歩み）
├── works.html      ─ 作品集（ジャンル別フィルタリング機能付）
├── kids.html       ─ 子どもの音楽 専門ページ
├── order.html      ─ 作曲依頼ページ（4グレード料金表＋フォーム）
├── style.css       ─ 全ページ共有スタイル
├── works.json      ─ 楽曲データベース（拡張用）
└── README.md       ─ このファイル
```

## デザイン仕様

### カラーパレット
- クリーム：`#FAF6F0`（背景主役）
- 深い藍：`#1F3A5F`（強調・信頼）
- 桜色：`#E8B4B8`（柔らかなアクセント）
- 朱赤：`#C84C3D`（情熱・受賞）
- 金色：`#C9A961`（品格）

### タイポグラフィ
- 和文：游明朝・游ゴシック（OS標準フォント）
- 欧文：Cormorant Garamond（Google Fonts）

### デザイン哲学
- 姓名科学サイトとは独立したブランドとして設計
- 演歌・歌謡曲・童謡すべてに馴染む日本的情緒
- 古びない品格、依頼のハードルを下げる温かさ

## GitHub Pagesへの配置手順

### 手順1：リポジトリ作成
1. GitHubにログインし、`miharaami.github.io` という名前で新しいリポジトリを作成
2. 公開設定（Public）にする
3. README追加・gitignore追加はスキップ

### 手順2：ファイルアップロード
以下のファイルをすべてリポジトリのルートに配置：
- index.html
- profile.html
- works.html
- kids.html
- order.html
- style.css
- works.json

### 手順3：GitHub Pages設定
1. リポジトリのSettings → Pages へ
2. Source：Deploy from a branch
3. Branch：main / root
4. Save
5. 数分後、`https://miharaami.github.io/` にアクセスして確認

## 楽曲の追加方法

新曲が公開された場合、`works.json` の `works` 配列に以下の形式で追記するだけで作品集ページに自動反映されます：

```json
{
  "id": "unique-id",
  "title": "曲名",
  "lyricist": "作詞者",
  "singer": "歌唱者",
  "youtube": "YouTube動画ID（11文字）",
  "genre": "kayou",
  "year": 2025,
  "tags": ["タグ1", "タグ2"],
  "description": "短い解説（100字程度）"
}
```

ジャンル指定：
- `kayou` 歌謡曲
- `enka` 演歌
- `ballad` バラード
- `doyou` 童謡
- `musical` ミュージカル
- `other` その他

## 段階的な拡張計画

### フェーズ1（公開時、現在の状態）
- 全5ページの基盤公開
- 既存14曲のYouTube埋込
- 受賞4年連続・カワイ出版3年連続採用の記載
- メールリンク方式のお問い合わせフォーム

### フェーズ2（2ヶ月目）
- Stripe決済の追加（ライセンス販売3,000円〜）
- 月額会員機能（月額980円）
- 楽譜PDF販売

### フェーズ3（3〜4ヶ月目）
- JASRAC登録曲整理
- YouTube収益化
- 配信プラットフォーム展開

### フェーズ4（5〜6ヶ月目以降）
- 作詞コンテスト企画
- UCAブロックチェーン著作権連携
- 姓名科学サイトとの相互送客

## メンテナンス・更新時の注意

### 編集時
- `style.css` を変更すれば全ページに反映されます
- 新ページ追加時は、ナビゲーションを5ファイル全てで更新する必要があります
- 楽曲追加は `works.json` のみ

### 動作環境
- 純粋HTML+CSS+JS、サーバー不要
- すべてのモダンブラウザで動作
- スマホ・タブレット対応済み（レスポンシブ）

## 制作

- 企画・制作：三原嘉明（yymm77）
- デザイン・実装協力：Claude
- 作曲家：三原あみ

---

© 三原あみ Composer Office
