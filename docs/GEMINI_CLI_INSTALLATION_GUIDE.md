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

### 1. ターミナル/PowerShellを開く方法

**詳細な手順は別ページで確認できます:**
📖 **[ターミナル・PowerShell 起動ガイド](./TERMINAL_POWERSHELL_GUIDE.md)**
- Mac：ターミナルの開き方（Spotlight、Launchpad、Finderから）
- Windows：PowerShell の開き方（管理者権限での起動方法も含む）
- 基本的な使い方とトラブルシューティング

#### 🍎 **Mac の場合（簡略版）**
1. `Command + Space` を押す
2. 「ターミナル」と入力して `Enter`

#### 🪟 **Windows の場合（簡略版）**
1. スタートメニューで「PowerShell」を検索
2. 「Windows PowerShell」をクリック

### 2. Node.js のインストール確認

**詳細な確認・インストール手順は別ページで確認できます:**
📖 **[Node.js バージョン確認・インストールガイド](./NODEJS_VERSION_CHECK.md)**
- バージョン確認の詳しい方法
- OS別インストール手順
- トラブルシューティング
- バージョン管理ツールの使い方

#### 簡易確認手順

ターミナル/PowerShellで以下を実行：

```bash
node --version
```

**結果の見方:**
- `v18.x.x` 以上が表示 → ✅ インストール済み
- エラーが出る → ❌ インストールが必要

### 3. Node.js のインストール（必要な場合のみ） {#nodejs-のインストール}

Node.jsが未インストールの場合は、詳細ガイドをご覧ください：

📖 **[Node.js バージョン確認・インストールガイド](./NODEJS_VERSION_CHECK.md)**

**簡略手順:**
1. https://nodejs.org/ にアクセス
2. 「LTS」版をダウンロード
3. インストーラーを実行
4. ターミナル/PowerShellを再起動
5. `node --version` で確認

---

## 📦 インストール手順

### ステップ1: ターミナル/PowerShellを開く

詳しい手順は：📖 **[ターミナル・PowerShell 起動ガイド](./TERMINAL_POWERSHELL_GUIDE.md)**

**簡略手順:**
- **Mac**: `Command + Space` → 「ターミナル」と入力 → `Enter`
- **Windows**: スタートメニューで「PowerShell」を検索

> 💡 **すでに開いている場合**: そのまま次のステップに進んでOKです

### ステップ2: Gemini CLI をインストール

#### インストールコマンドを入力

以下のコマンドを**正確に**入力するか、コピー&貼り付けしてください：

```bash
npm install -g @google/gemini-cli
```

#### コピー&貼り付けの方法

**🍎 Mac の場合**
1. 上記のコマンドをドラッグして選択
2. `Command + C` でコピー
3. ターミナル画面で `Command + V` で貼り付け
4. `Enter`キーを押して実行

**🪟 Windows の場合**
1. 上記のコマンドをドラッグして選択
2. `Ctrl + C` でコピー  
3. PowerShell画面で**右クリック**して貼り付け（または `Ctrl + V`）
4. `Enter`キーを押して実行

#### インストール中の画面

正常にインストールが進むと、以下のような表示が出ます：
```
npm WARN deprecated ...
added 123 packages in 15s
```

**⏰ 時間**: 通常1-3分程度かかります。気長に待ちましょう。

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
- **GitHub**: [google-gemini/gemini-cli](https://github.com/google-gemini/gemini-cli)
- **公式リポジトリ**: 最新情報、Issue報告、機能追加要望はこちら

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