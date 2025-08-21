# 📦 Node.js バージョン確認・インストールガイド

## 📌 このページについて

Node.jsのバージョン確認方法と、インストール手順を詳しく解説します。

---

## 🔍 Node.js バージョンの確認方法

### 前準備: ターミナル/PowerShellを開く

まず、コマンドラインツールを起動します。
- 📖 [ターミナル・PowerShell起動ガイド](./TERMINAL_POWERSHELL_GUIDE.md)を参照

### バージョン確認コマンド

#### 基本コマンド
```bash
node --version
```

または短縮形：
```bash
node -v
```

#### 実行例と結果の見方

**✅ インストール済みの場合**
```bash
$ node --version
v20.11.0
```
- `v20.11.0` のようなバージョン番号が表示される
- `v18.0.0` 以上であればGemini CLIに対応

**❌ インストールされていない場合**

Mac/Linux:
```bash
$ node --version
-bash: node: command not found
```

Windows:
```powershell
PS> node --version
'node' は、内部コマンドまたは外部コマンド、
操作可能なプログラムまたはバッチ ファイルとして認識されていません。
```

### npm のバージョン確認

Node.jsと一緒にインストールされるnpmも確認：

```bash
npm --version
```

または短縮形：
```bash
npm -v
```

**実行例:**
```bash
$ npm --version
10.2.4
```

---

## 📥 Node.js のインストール方法

### 🌐 公式サイトからインストール（初心者推奨）

#### ステップ1: 公式サイトにアクセス

🔗 **[Node.js 公式サイト](https://nodejs.org/)**

#### ステップ2: LTS版をダウンロード

1. **LTS版を選択**
   - 緑色のボタン「LTS」をクリック
   - LTS = Long Term Support（長期サポート版）
   - 安定性重視の推奨版

2. **自動的にOSを判別**
   - サイトが自動的にOS（Mac/Windows）を判別
   - 適切なインストーラーが表示される

#### ステップ3: OS別インストール手順

### 🍎 Mac でのインストール

#### インストーラー（.pkg）を使う方法

1. **ダウンロード**
   - `node-v20.xx.x.pkg` ファイルがダウンロードされる
   - 通常は「ダウンロード」フォルダに保存

2. **インストーラーを起動**
   - ダウンロードした `.pkg` ファイルをダブルクリック

3. **インストール手順**
   ```
   1. 「続ける」をクリック
   2. 使用許諾契約を読んで「続ける」→「同意する」
   3. インストール先（通常は変更不要）→「続ける」
   4. 「インストール」をクリック
   5. Macのパスワードを入力
   6. インストール完了まで待つ（1-2分）
   7. 「閉じる」をクリック
   ```

4. **インストーラーの削除**（オプション）
   - ダウンロードした `.pkg` ファイルは削除してOK

#### Homebrew を使う方法（上級者向け）

1. **Homebrewの確認**
   ```bash
   brew --version
   ```

2. **Node.jsをインストール**
   ```bash
   brew install node
   ```

3. **最新版に更新**
   ```bash
   brew upgrade node
   ```

### 🪟 Windows でのインストール

#### インストーラー（.msi）を使う方法

1. **ダウンロード**
   - `node-v20.xx.x-x64.msi` ファイルがダウンロードされる
   - 64bit版が推奨（ほとんどのPCは64bit）

2. **インストーラーを起動**
   - ダウンロードした `.msi` ファイルをダブルクリック

3. **インストール手順**
   ```
   1. 「Next」をクリック
   2. ライセンス規約 → チェックボックスにチェック → 「Next」
   3. インストール先（通常は変更不要）→「Next」
   4. カスタムセットアップ（変更不要）→「Next」
   5. Tools for Native Modules（オプション）
      - 必要に応じてチェック → 「Next」
   6. 「Install」をクリック
   7. 管理者権限の確認 → 「はい」
   8. インストール完了まで待つ（2-3分）
   9. 「Finish」をクリック
   ```

4. **PowerShellを再起動**
   - インストール後は必ずPowerShellを再起動

#### Chocolatey を使う方法（上級者向け）

1. **管理者権限でPowerShellを起動**

2. **Node.jsをインストール**
   ```powershell
   choco install nodejs
   ```

---

## 🐧 Linux でのインストール

### Ubuntu/Debian

```bash
# パッケージリストを更新
sudo apt update

# Node.js と npm をインストール
sudo apt install nodejs npm

# バージョン確認
node --version
npm --version
```

### CentOS/RHEL/Fedora

```bash
# Node.js と npm をインストール
sudo yum install nodejs npm

# または dnf を使用
sudo dnf install nodejs npm
```

### NodeSource リポジトリを使う（最新版）

```bash
# Ubuntu/Debian
curl -fsSL https://deb.nodesource.com/setup_lts.x | sudo -E bash -
sudo apt-get install -y nodejs

# CentOS/RHEL
curl -fsSL https://rpm.nodesource.com/setup_lts.x | sudo bash -
sudo yum install nodejs
```

---

## ✅ インストール後の確認

### 必須確認項目

1. **ターミナル/PowerShellを再起動**
   - 重要：必ず一度閉じて、再度開く

2. **Node.jsバージョン確認**
   ```bash
   node --version
   ```
   期待される結果: `v18.0.0` 以上

3. **npmバージョン確認**
   ```bash
   npm --version
   ```
   期待される結果: バージョン番号が表示される

4. **動作テスト**
   ```bash
   node -e "console.log('Node.js is working!')"
   ```
   期待される結果: `Node.js is working!` と表示

---

## 🔄 バージョンの更新・管理

### npm を使った更新

```bash
# npm自体を最新版に更新
npm install -g npm@latest

# Node.jsの更新は公式サイトから再インストール
```

### バージョン管理ツール

#### nvm (Node Version Manager) - Mac/Linux

1. **インストール**
   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash
   ```

2. **使い方**
   ```bash
   # 利用可能なバージョンを表示
   nvm list-remote

   # 特定バージョンをインストール
   nvm install 20.11.0

   # バージョンを切り替え
   nvm use 20.11.0

   # デフォルトバージョンを設定
   nvm alias default 20.11.0
   ```

#### nvm-windows - Windows

1. **インストール**
   - [nvm-windows](https://github.com/coreybutler/nvm-windows)からダウンロード

2. **使い方**
   ```powershell
   # バージョン一覧
   nvm list available

   # インストール
   nvm install 20.11.0

   # 切り替え
   nvm use 20.11.0
   ```

---

## 🚨 トラブルシューティング

### 問題1: PATHが通っていない

**症状:** インストール後も `command not found` エラー

**Mac/Linux 解決方法:**
```bash
# PATHを確認
echo $PATH

# .zshrc または .bashrc に追加
echo 'export PATH="/usr/local/bin:$PATH"' >> ~/.zshrc
source ~/.zshrc
```

**Windows 解決方法:**
1. システムのプロパティを開く
2. 「環境変数」をクリック
3. システム環境変数の「Path」を編集
4. Node.jsのパスを追加（通常: `C:\Program Files\nodejs\`）
5. PCを再起動

### 問題2: 権限エラー

**症状:** `EACCES` エラー

**解決方法:**
```bash
# npmのデフォルトディレクトリを変更
mkdir ~/.npm-global
npm config set prefix '~/.npm-global'
echo 'export PATH=~/.npm-global/bin:$PATH' >> ~/.zshrc
source ~/.zshrc
```

### 問題3: 古いバージョンがインストールされている

**解決方法:**
1. 現在のバージョンを確認
2. 公式サイトから最新版をダウンロード
3. 上書きインストール
4. ターミナル/PowerShellを再起動

---

## 📊 バージョン要件の確認

### Gemini CLI の要件

- **最小要件:** Node.js v18.0.0 以上
- **推奨:** Node.js v20.x.x LTS

### バージョン番号の見方

```
v20.11.0
 │  │  │
 │  │  └─ パッチバージョン（バグ修正）
 │  └──── マイナーバージョン（機能追加）
 └─────── メジャーバージョン（大きな変更）
```

### LTS vs Current

- **LTS (Long Term Support)**
  - 長期サポート版
  - 安定性重視
  - 本番環境向け
  - **推奨**

- **Current**
  - 最新機能版
  - 新機能を試したい人向け
  - 開発環境向け

---

## 📚 関連リンク

- [ターミナル・PowerShell起動ガイド](./TERMINAL_POWERSHELL_GUIDE.md)
- [Gemini CLI インストールガイド](./GEMINI_CLI_INSTALLATION_GUIDE.md)
- [Node.js 公式サイト](https://nodejs.org/)
- [npm 公式サイト](https://www.npmjs.com/)

---

## 💡 次のステップ

Node.jsのインストールが完了したら：

1. 📖 [Gemini CLI インストールガイド](./GEMINI_CLI_INSTALLATION_GUIDE.md) に進む
2. ⚡ [Gemini CLI クイックスタート](./GEMINI_CLI_QUICKSTART.md) で素早く始める

---

**作成日**: 2025年8月21日  
**対応バージョン**: Node.js v18.0.0以上