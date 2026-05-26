# 樫辺勒 公式サイト デザイン案

文学版・ポップ版の2デザインを並べて見比べてもらうための、デモ用一式です。

## ファイル構成

```
github/
├── index.html      ← 入口（バージョン選択ページ）
├── literary.html   ← 文学版（落ち着いた明朝デザイン）
├── pop.html        ← ポップ版（明るい丸ゴシックデザイン）
└── README.md       ← このファイル
```

訪問者は `index.html` で2バージョンから選び、それぞれの単体ページに進む流れです。各バージョンは内部に5ページぶん（ホーム／プロフィール／著作／お知らせ／お問い合わせ）を含んでいます。

---

## GitHub Pagesでの公開手順（非技術者向け）

GitHub Pagesを使えば、**無料**でこのサイトをインターネット上に公開できます。サーバー契約も独自ドメインも要りません。手順は以下のとおり。

### 1. GitHubアカウントを作る

[github.com](https://github.com) にアクセスして「Sign up」から無料登録します。メールアドレスとパスワードがあれば数分で完了します。

### 2. 新しいリポジトリ（=フォルダ）を作る

ログイン後、画面右上の「+」マークから「**New repository**」を選びます。

- **Repository name**: 好きな名前（例: `kashibe-roku-site`）
- **Public** を選択（※Private だと無料Pagesが使えません）
- 「Add a README file」にチェック
- 「Create repository」をクリック

### 3. 4つのファイルをアップロードする

作成したリポジトリの画面で「**Add file** → **Upload files**」を選び、このフォルダ内の **4ファイルすべて**（`index.html` / `literary.html` / `pop.html` / `README.md`）をドラッグ＆ドロップでアップロード。下のほうの「**Commit changes**」を押せば反映されます。

※ `README.md` は同名ファイルがすでにある場合、上書きを選んでください。

### 4. GitHub Pagesを有効化する

リポジトリ画面の上部メニューから「**Settings**」を開き、左サイドの「**Pages**」をクリック。

- **Source**: 「Deploy from a branch」
- **Branch**: 「main」「/(root)」を選んで「Save」

数分後、Pages欄の上部に `https://（ユーザー名）.github.io/（リポジトリ名）/` のようなURLが表示されます。これが公開URLです。

### 5. アクセスして確認

表示されたURLにアクセスすると、選択ページが開きます。「文学版」「ポップ版」を選んで両方の動きを確認してください。

---

## 内容を更新するには

GitHubの該当ファイル画面で右上の鉛筆アイコン（✏️ Edit this file）をクリックすると、ブラウザ上で直接コードを編集できます。書き換えて下部の「Commit changes」を押せば、数分でサイトに反映されます。

差し替えやすい主な箇所:
- **顔写真**: 各HTMLの `<div class="photo-placeholder">` 部分を `<img>` タグに置き換え
- **書影**: `<div class="cover-placeholder ...">` を `<img>` に置き換え
- **動画**: `<div class="video-placeholder">` をまるごと消し、コメントアウトされた `<iframe>` を有効化（YouTubeにアップ後）
- **SNS・Amazon・楽天URL**: `href="#"` を実URLに差し替え
- **本文テキスト**: HTML内のテキストを直接書き換え

画像をアップロードしたい場合は、リポジトリ内に `images/` フォルダを作ってそこに置き、`<img src="images/portrait.jpg">` のように参照します。

---

## 独自ドメイン（任意）

`https://kashibe-roku.com` のような独自ドメインを使いたい場合は、別途ドメイン取得サービス（お名前.com、ムームードメインなど）で年1,500円程度のドメインを購入し、GitHub Pagesの「**Custom domain**」設定欄に入力します。詳しくは [GitHub公式ヘルプ](https://docs.github.com/ja/pages/configuring-a-custom-domain-for-your-github-pages-site) を参照。

---

## 注意点

- **Publicリポジトリでないと無料Pagesは使えません**。中身のHTMLコードが全世界から閲覧可能になりますが、ウェブサイトの性質上もともと公開情報なので通常は問題ありません。パスワードや秘密情報はファイルに含めないでください。
- 反映には数分〜10分程度かかる場合があります。すぐ表示されなくても慌てずに。
- フォーム送信機能はデモのままなので、本番運用時は[Formspree](https://formspree.io)等のサービスにつないでください。

---

## ライセンス

このサイトのデザイン・コードはご自由にご利用ください。
