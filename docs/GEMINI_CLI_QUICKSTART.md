# 🚀 Gemini CLI クイックスタートガイド

## 5分でできる！最速インストール

### 📋 前提条件チェックリスト
- [ ] パソコンがある（**Mac推奨**、Windows対応）
- [ ] インターネットに接続している
- [ ] Googleアカウントを持っている
- [ ] ターミナル（Mac）またはPowerShell（Windows）を開ける

---

## ⚡ 3ステップインストール

### 1️⃣ ターミナル/PowerShellを開く（30秒）

**Mac**: `Command + Space` → 「Terminal」で検索 → Enter  
**Windows**: スタートメニュー → 「PowerShell」で検索 → クリック

### 2️⃣ Node.js 確認・インストール（1分）

```bash
node --version
```

**バージョンが表示される**: OK！次へ  
**エラーが出る**: https://nodejs.org/ から「LTS」版をダウンロードしてインストール

### 3️⃣ Gemini CLI インストール（30秒）
以下をコピー&貼り付けして実行：
```bash
npm install -g @google/gemini-cli
```

**Mac**: `Command+C` → `Command+V` → Enter  
**Windows**: `Ctrl+C` → 右クリック貼り付け → Enter

### 4️⃣ 初回起動と認証（30秒）
```bash
gemini
```
→ ブラウザが開く → Googleアカウントでログイン → 完了！

---

## 🎯 最初の3つのコマンド

### 1. 挨拶してみる
```bash
gemini "こんにちは！自己紹介をして"
```

### 2. プログラミングの質問
```bash
gemini "Pythonで1から10までの合計を計算するコードを書いて"
```

### 3. 対話モードを試す
```bash
gemini
> 今日の天気について教えて
> exit  # 終了するとき
```

---

## 🔥 よく使う便利コマンド集

### コード生成
```bash
# Webサイトのテンプレート
gemini "シンプルなHTMLのランディングページを作って"

# 関数の作成
gemini "JavaScriptで配列をシャッフルする関数を作って"

# データベース操作
gemini "MySQLでユーザーテーブルを作成するSQLを書いて"
```

### ファイル操作
```bash
# ファイルの説明
gemini "package.jsonファイルの役割を説明して"

# コードレビュー
gemini "このコードの問題点を指摘して" --file mycode.py

# リファクタリング
gemini "このコードをより効率的に書き直して" --file old.js
```

### 学習サポート
```bash
# 概念の説明
gemini "REST APIとは何か初心者向けに説明して"

# エラー解決
gemini "TypeError: Cannot read property 'length' of undefined の解決方法"

# ベストプラクティス
gemini "Reactのベストプラクティスを5つ教えて"
```

---

## 💡 プロのテクニック

### 1. エイリアス設定（ショートカット）

**Mac/Linux** (`~/.bashrc` または `~/.zshrc` に追加):
```bash
alias g="gemini"
alias gcode="gemini 'このコードを説明して' --file"
```

**Windows** (PowerShellプロファイルに追加):
```powershell
function g { gemini $args }
```

使用例:
```bash
g "Hello World"
```

### 2. 履歴の活用
```bash
# 前回の会話を続ける
gemini --continue

# 履歴をクリア
gemini --clear-history
```

### 3. 出力の保存
```bash
# ファイルに保存
gemini "README.mdのテンプレートを作って" > README.md

# クリップボードにコピー（Mac）
gemini "gitignoreファイルの内容" | pbcopy

# クリップボードにコピー（Windows）
gemini "gitignoreファイルの内容" | clip
```

---

## 🆘 困ったときは？

### Q: 「command not found」エラー
```bash
# 再インストール
npm uninstall -g @google/gemini-cli
npm install -g @google/gemini-cli
```

### Q: 認証エラー
```bash
# キャッシュクリア
gemini --clear-auth
gemini  # 再認証
```

### Q: 遅い・反応しない
```bash
# バージョン確認
gemini --version

# 最新版にアップデート
npm update -g @google/gemini-cli
```

---

## 📊 利用制限

| 項目 | 無料枠 |
|------|--------|
| 1分あたり | 60回 |
| 1日あたり | 1,000回 |
| 1回の文字数 | 約32,000文字 |

---

## 🎓 次のステップ

1. **詳細ガイド**: `GEMINI_CLI_INSTALLATION_GUIDE.md` を読む
2. **公式ドキュメント**: https://github.com/google-gemini/gemini-cli
3. **コミュニティ**: Google AI Community に参加

---

## 🎉 おめでとう！

Gemini CLIの設定が完了しました！
今すぐターミナルで `gemini` と入力して、AIアシスタントを使い始めましょう！

---

**作成日**: 2025年8月21日
**対応バージョン**: Gemini CLI 最新版