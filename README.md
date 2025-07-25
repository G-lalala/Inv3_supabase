# Inv3_supabase

Supabase を使用したローカル開発環境のプロジェクトです。

## 概要

このプロジェクトは、Supabase のローカル開発環境を設定し、REST API のテストを行うためのセットアップが含まれています。

## 前提条件

以下のソフトウェアがインストールされている必要があります：

- [Node.js](https://nodejs.org/) (推奨: v18 以上)
- [Git](https://git-scm.com/)
- [Docker](https://www.docker.com/) (Supabase ローカル環境用)

## 環境構築手順

### 1. リポジトリのクローン

```bash
git clone <repository-url>
cd Inv3_supabase
```

### 2. 依存関係のインストール

```bash
npm install
```

### 3. Supabase CLI の確認

```bash
npx supabase --version
```

### 4. Supabase ローカル環境の起動

```bash
npx supabase start
```

初回実行時は、Docker コンテナのダウンロードとセットアップに時間がかかる場合があります。

## プロジェクト構成

```
Inv3_supabase/
├── .gitignore          # Git除外設定
├── package.json        # Node.jsプロジェクト設定
├── package-lock.json   # 依存関係ロックファイル
├── sample.http         # REST APIテストファイル
├── supabase/           # Supabase設定ディレクトリ
│   ├── config.toml     # Supabase設定ファイル
│   └── .gitignore      # Supabase用除外設定
└── README.md           # このファイル
```

## トラブルシューティング

### Supabase ローカル環境が起動しない場合

1. Docker が起動していることを確認
2. ポート 54321 が使用されていないことを確認
3. 以下のコマンドでログを確認：
   ```bash
   npx supabase status
   ```

### API テストが失敗する場合

1. Supabase ローカル環境が起動していることを確認
2. 認証トークンが有効であることを確認
3. エンドポイントの URL が正しいことを確認

## ライセンス

ISC

## 作者

G-lalala
