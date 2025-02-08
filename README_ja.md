# Dify Electron アプリ

## 概要

Difyは、`http://localhost/apps`からウェブページを表示するElectronベースのアプリケーションです。このアプリケーションはmacOS上で動作し、指定されたウェブページを表示するためのシンプルなインターフェースを提供します。

## 特徴

- `http://localhost/apps`からウェブページを表示
- 標準的なmacOSのタイトルバーを含む（最小化、最大化、閉じるボタン）

## インストール

1. `dist`ディレクトリから`.dmg`ファイルをダウンロードします。
2. `.dmg`ファイルを開き、`dify`アプリをアプリケーションフォルダにドラッグします。
3. アプリケーションフォルダから`dify`アプリを起動します。

## 使用方法

1. `http://localhost/apps`でウェブサーバーが動作していることを確認します。
2. `dify`アプリを開きます。
3. アプリは`http://localhost/apps`からウェブページを表示します。

## エンドポイントの変更

Difyアプリがアクセスするエンドポイントを変更するには、以下の手順に従ってください：

1. プロジェクトディレクトリ内の`main.js`ファイルを開きます。
2. `win.loadURL`メソッドのURLを設定する行を見つけます：
   ```javascript
   win.loadURL('http://localhost/apps');
   ```
3. `'http://localhost/apps'`を希望するエンドポイントURLに置き換えます。例えば：
   ```javascript
   win.loadURL('http://your-new-endpoint.com');
   ```
4. `main.js`の変更を保存します。
5. アプリケーションを再ビルドします：
   ```bash
   npm run build
   ```

## 開発

### 前提条件

- Node.js v22.13.1
- npm 10.9.2

### セットアップ

1. リポジトリをクローンします。
2. 依存関係をインストールします：
   ```bash
   npm install
   ```

### アプリの実行

開発モードでアプリを実行するには：
```bash
npm start
```

### アプリのビルド

macOS用にアプリをビルドするには：
```bash
npm run build
```

ビルドされた`.dmg`ファイルは`dist`ディレクトリに配置されます。

## ライセンス

このプロジェクトはMITライセンスの下でライセンスされています。
