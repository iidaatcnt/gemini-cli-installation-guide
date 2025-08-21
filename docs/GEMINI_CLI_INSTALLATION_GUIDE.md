# 🤖 Gemini CLI インストール完全ガイド（初心者向け）

## 📌 目次
1. [Gemini CLIとは？](#gemini-cliとは)
2. [必要なものの準備](#必要なものの準備)
3. [インストール手順](#インストール手順)
4. [初回設定](#初回設定)
5. [使い方の基本](#使い方の基本)
6. [トラブルシューティング](#トラブルシューティング)

---

## 🤔 Gemini CLIとは？

**Gemini CLI**は、Googleが提供する**AI アシスタント**をターミナル（コマンドライン）で使えるようにするツールです。

### 💡 できること
- プログラミングの質問に答えてもらう
- コードの修正・改善の提案
- ファイルの操作や編集
- コマンドの実行サポート
- Web検索と情報取得

### 📊 無料利用枠
- **1分間に60回**まで質問可能
- **1日1,000回**まで無料で利用可能

---

## 🔧 必要なものの準備

### 1. Node.js のインストール確認

#### まずは確認
ターミナル（Macの場合）またはコマンドプロンプト（Windowsの場合）を開いて、以下のコマンドを入力：

```bash
node --version
```

#### 結果の見方
- `v18.x.x` や `v20.x.x` など表示される → **すでにインストール済み！** [次のステップへ](#インストール手順)
- `command not found` などエラーが出る → **Node.jsのインストールが必要**

### 2. Node.js のインストール（必要な場合のみ）

#### 🍎 **Mac の場合**

**方法1: 公式サイトから（推奨）**
1. https://nodejs.org/ にアクセス
2. 「LTS」版（緑色のボタン）をクリック
3. ダウンロードしたファイルをダブルクリック
4. 画面の指示に従ってインストール

**方法2: Homebrew を使う（上級者向け）**
```bash
# Homebrewがインストール済みの場合
brew install node
```

#### 🪟 **Windows の場合**

1. https://nodejs.org/ にアクセス
2. 「LTS」版（緑色のボタン）をクリック
3. ダウンロードした `.msi` ファイルをダブルクリック
4. 以下の手順でインストール：
   - 「Next」をクリック
   - 規約に同意して「Next」
   - インストール先はそのままで「Next」
   - すべてデフォルトのまま「Next」を続ける
   - 「Install」をクリック
   - 完了したら「Finish」

#### 🐧 **Linux の場合**

```bash
# Ubuntu/Debian
sudo apt update
sudo apt install nodejs npm

# CentOS/RHEL/Fedora
sudo yum install nodejs npm
```

### 3. インストール確認

再度ターミナルで確認：
```bash
node --version
npm --version
```

両方ともバージョン番号が表示されればOK！

---

## 📦 インストール手順

### ステップ1: ターミナルを開く

#### Mac の場合
1. `Command + Space` を押す
2. 「ターミナル」または「Terminal」と入力
3. Enterキーを押す

#### Windows の場合
1. `Windows + R` を押す
2. 「cmd」と入力
3. Enterキーを押す

### ステップ2: Gemini CLI をインストール

以下のコマンドをコピーして、ターミナルに貼り付けて実行：

```bash
npm install -g @google/gemini-cli
```

**💡 ヒント**: 
- コピー: `Command+C`（Mac）または `Ctrl+C`（Windows）
- 貼り付け: `Command+V`（Mac）または `右クリック→貼り付け`（Windows）

### ステップ3: インストール完了の確認

インストールが完了したら、以下のコマンドで確認：

```bash
gemini --version
```

バージョン番号が表示されれば成功！

---

## 🔐 初回設定

### ステップ1: Gemini CLI を起動

ターミナルで以下を入力：

```bash
gemini
```

### ステップ2: 認証方法を選択

初回起動時に認証が必要です。3つの方法から選べます：

#### 🌟 **方法1: Googleアカウントでログイン（推奨）**

1. ブラウザが自動的に開きます
2. Googleアカウントでログイン
3. 「許可」をクリック
4. 認証完了のメッセージが表示される

#### 🔑 **方法2: APIキーを使う**

1. https://makersuite.google.com/app/apikey にアクセス
2. 「Create API Key」をクリック
3. キーをコピー
4. 以下のコマンドを実行：

**Mac/Linux:**
```bash
export GOOGLE_API_KEY="ここにAPIキーを貼り付け"
gemini
```

**Windows:**
```cmd
set GOOGLE_API_KEY=ここにAPIキーを貼り付け
gemini
```

---

## 🎯 使い方の基本

### 基本的な質問

```bash
gemini "Pythonでhello worldを表示する方法を教えて"
```

### ファイルの内容について質問

```bash
gemini "このファイルの内容を説明して" --file example.py
```

### コードの改善を依頼

```bash
gemini "このコードをリファクタリングして" --file old_code.js
```

### Web検索を含む質問

```bash
gemini "2024年の最新のJavaScriptフレームワークを教えて"
```

### 対話モードで使う

```bash
gemini
# プロンプトが表示されたら、質問を入力
> JavaScriptの配列の使い方を教えて
# 回答が表示される
> 終了するには exit と入力
```

---

## 🚨 トラブルシューティング

### よくある問題と解決方法

#### ❌ 「command not found: gemini」エラー

**原因**: インストールが完了していない
**解決方法**:
```bash
npm install -g @google/gemini-cli
```

#### ❌ 「EACCES: permission denied」エラー

**原因**: 管理者権限が必要
**解決方法**:

Mac/Linux:
```bash
sudo npm install -g @google/gemini-cli
```

Windows（管理者権限でコマンドプロンプトを開く）:
1. スタートメニューで「cmd」を検索
2. 「管理者として実行」を選択
3. インストールコマンドを実行

#### ❌ 「npm: command not found」エラー

**原因**: Node.jsがインストールされていない
**解決方法**: [必要なものの準備](#必要なものの準備)に戻ってNode.jsをインストール

#### ❌ 認証エラー

**原因**: APIキーが正しくない、または期限切れ
**解決方法**:
1. 新しいAPIキーを生成
2. 環境変数を再設定
3. Gemini CLIを再起動

---

## 📚 さらに詳しく学ぶ

### 公式ドキュメント
- GitHub: https://github.com/google-gemini/gemini-cli
- ドキュメント: https://geminicli.work/docs/

### おすすめの使い方
1. **コード生成**: 「〇〇する関数を作って」
2. **バグ修正**: 「このエラーを修正して」
3. **説明**: 「このコードの動作を説明して」
4. **最適化**: 「このコードを高速化して」

### 💡 プロのヒント
- 質問は具体的に書く
- コンテキストを提供する
- ファイルパスは正確に指定する
- エラーメッセージは全文コピーして質問する

---

## 🎉 インストール完了！

おめでとうございます！これでGemini CLIが使えるようになりました。

### 最初に試してみるコマンド：

```bash
gemini "今日の日付を教えて"
```

```bash
gemini "簡単なPythonスクリプトを作って"
```

```bash
gemini "GitHubの使い方を初心者向けに説明して"
```

---

## 📞 サポート

問題が解決しない場合：
1. GitHubのIssues: https://github.com/google-gemini/gemini-cli/issues
2. Stack Overflow: タグ「gemini-cli」で検索
3. Google AI Community: https://discuss.ai.google.dev/

---

**最終更新**: 2025年8月21日
**バージョン**: Gemini CLI 最新版対応

---

## 📝 メモ欄

インストール日時: _______________
APIキー（安全に保管）: _______________
よく使うコマンド: _______________