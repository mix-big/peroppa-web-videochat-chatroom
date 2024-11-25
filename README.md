# File Upload and Email Notification

このプロジェクトは、Firebase Storageを使用してファイルをアップロードし、EmailJSを使ってそのファイルのリンクをメールで送信するウェブアプリケーションです。

## 概要

- ユーザーはフォームからメールアドレスとファイルを入力できます。
- ファイルはFirebase Storageにアップロードされ、そのURLがEmailJSを介して指定されたメールアドレスに送信されます。
- シンプルなUIで、FirebaseとEmailJSを活用して、ファイルアップロードと通知を実現します。

## 必要なもの

- Firebase アカウント
- EmailJS アカウント

## セットアップ

### 1. Firebase プロジェクトの作成

1. [Firebase コンソール](https://console.firebase.google.com/)で新しいプロジェクトを作成します。
2. Firebase Storage を有効化します。
3. Firebase コンソールの設定ページから API キー、プロジェクトID、アプリIDを取得します。
4. `index.html` 内の `firebaseConfig` セクションに取得した設定情報を入力します。

### 2. EmailJS アカウントの作成

1. [EmailJS](https://www.emailjs.com/)でアカウントを作成します。
2. サービスを作成し、テンプレートを設定します。
3. テンプレートに `{user_email}` と `{file_url}` を埋め込んでください。
4. サービスID、テンプレートID、ユーザーIDを取得し、`index.html` 内の `emailjs.init` メソッドに設定します。

### 3. Firebase と EmailJS 設定の追加

1. `firebaseConfig` オブジェクトにFirebaseの設定情報（APIキー、プロジェクトID、アプリIDなど）を入力します。
2. EmailJSの設定として、`emailjs.init` にユーザーIDを入力し、`emailjs.send` メソッドの引数にサービスIDとテンプレートIDを設定します。

### 4. GitHub Pagesでの公開

1. プロジェクトをGitHubにアップロードします。
2. GitHubのリポジトリ設定で、「GitHub Pages」を有効化します。
3. `index.html`を公開します。

## 使用方法

1. ブラウザでプロジェクトページを開きます。
2. メールアドレスを入力し、アップロードするファイルを選択します。
3. 「Upload and Send」ボタンをクリックすると、ファイルがFirebaseにアップロードされ、そのURLが指定されたメールアドレスに送信されます。

## プロジェクト構成

