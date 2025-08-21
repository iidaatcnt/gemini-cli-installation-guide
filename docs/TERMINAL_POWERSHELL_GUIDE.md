# 🖥️ ターミナル・PowerShell 起動ガイド

## 📌 このページについて

コマンドラインツール（ターミナル・PowerShell）を初めて使う方のための詳細な起動ガイドです。

---

## 🍎 Mac - ターミナルの起動方法

### 方法1: Spotlight検索を使う（最も簡単）

#### 手順
1. **キーボードショートカットを押す**
   - `Command` キー（⌘）と `Space` キーを**同時に**押す
   - 画面中央に検索ボックスが表示される

2. **「ターミナル」と入力**
   - 日本語で「ターミナル」または英語で「Terminal」と入力
   - 入力中に候補が表示される

3. **Enterキーで起動**
   - ターミナルが候補に表示されたら `Enter` キーを押す
   - 黒い画面（ターミナル）が開く

#### 📸 画面の見方
```
Last login: Mon Aug 21 10:00:00 on ttys000
username@MacBook-Pro ~ % 
```
↑ この表示が出れば成功！

### 方法2: Launchpadを使う

#### 手順
1. **Launchpadを開く**
   - Dockの「Launchpad」アイコンをクリック
   - または、トラックパッドで親指と3本指でピンチ

2. **「その他」フォルダを探す**
   - 「その他」または「Other」というフォルダをクリック

3. **ターミナルをクリック**
   - 黒い四角のアイコン「ターミナル」をクリック

### 方法3: Finderを使う

#### 手順
1. **Finderを開く**
   - Dockの笑顔アイコンをクリック

2. **アプリケーションフォルダへ移動**
   - サイドバーから「アプリケーション」を選択
   - または、メニューバーから「移動」→「アプリケーション」

3. **ユーティリティフォルダを開く**
   - 「ユーティリティ」フォルダをダブルクリック

4. **ターミナルを起動**
   - 「ターミナル.app」をダブルクリック

### 💡 便利な設定

#### Dockに追加する方法
1. ターミナルを起動
2. Dockのターミナルアイコンを右クリック
3. 「オプション」→「Dockに追加」を選択

#### デフォルトシェルの確認
```bash
echo $SHELL
```
- `/bin/zsh` → zsh使用中（macOS Catalina以降のデフォルト）
- `/bin/bash` → bash使用中

---

## 🪟 Windows - PowerShellの起動方法

### 方法1: スタートメニューから（推奨）

#### 手順
1. **スタートメニューを開く**
   - 画面左下のWindowsロゴをクリック
   - または、キーボードの `Windows` キーを押す

2. **「PowerShell」と入力**
   - キーボードで「powershell」と入力
   - 検索結果が自動的に表示される

3. **PowerShellを選択**
   - 「Windows PowerShell」をクリック
   - 青い画面が開く

#### 📸 画面の見方
```
Windows PowerShell
Copyright (C) Microsoft Corporation. All rights reserved.

PS C:\Users\username>
```
↑ この表示が出れば成功！

### 方法2: ファイル名を指定して実行

#### 手順
1. **実行ダイアログを開く**
   - `Windows` + `R` キーを同時に押す

2. **「powershell」と入力**
   - テキストボックスに「powershell」と入力

3. **OKをクリック**
   - `Enter` キーを押すか「OK」をクリック

### 方法3: Windows Terminal を使う（Windows 11）

#### 手順
1. **スタートメニューを開く**
   - Windowsロゴをクリック

2. **「Terminal」と入力**
   - 「Windows Terminal」が表示される

3. **起動**
   - クリックして起動
   - デフォルトでPowerShellが開く

---

## ⚡ 管理者権限で起動する方法

### 🍎 Mac - 管理者権限（sudo）

Macでは通常のターミナルで `sudo` コマンドを使用：

```bash
# 管理者権限でコマンドを実行
sudo npm install -g @google/gemini-cli

# パスワード入力を求められる
Password: [Macのログインパスワードを入力]
```

**注意事項:**
- パスワード入力時、画面に文字は表示されない
- 正しく入力して `Enter` を押す

### 🪟 Windows - 管理者として実行

#### 方法1: スタートメニューから

1. **スタートメニューを開く**
   - Windowsロゴをクリック

2. **「PowerShell」を検索**
   - 「powershell」と入力

3. **右クリックメニューを開く**
   - 「Windows PowerShell」を**右クリック**

4. **「管理者として実行」を選択**
   - クリックすると管理者権限で起動
   - ユーザーアカウント制御（UAC）で「はい」をクリック

#### 方法2: ショートカットキーを使う

1. **検索**
   - `Windows` キーを押して「powershell」と入力

2. **管理者権限で起動**
   - `Ctrl` + `Shift` + `Enter` を同時に押す
   - UACで「はい」をクリック

#### 確認方法
管理者権限で起動できているか確認：
```powershell
# タイトルバーに「管理者」と表示される
# プロンプトが以下のようになる
PS C:\Windows\system32>
```

---

## 🔍 トラブルシューティング

### Mac - ターミナルが見つからない

**解決方法:**
```bash
# Spotlight検索をリセット
sudo mdutil -E /

# 再度検索してみる
```

### Windows - PowerShellが起動しない

**解決方法:**
1. コマンドプロンプト（cmd）を起動
2. 以下を実行：
```cmd
powershell
```

### 文字化けする場合

**Mac:**
```bash
# 文字エンコーディング確認
locale

# UTF-8に設定
export LANG=ja_JP.UTF-8
```

**Windows:**
```powershell
# 文字コード確認
chcp

# UTF-8に変更
chcp 65001
```

---

## 📚 関連リンク

- [Node.js バージョン確認ガイド](./NODEJS_VERSION_CHECK.md)
- [Gemini CLI インストールガイド](./GEMINI_CLI_INSTALLATION_GUIDE.md)
- [Gemini CLI クイックスタート](./GEMINI_CLI_QUICKSTART.md)

---

## 💡 Tips

### ターミナル/PowerShellの基本コマンド

#### 共通コマンド
```bash
# 現在のディレクトリを表示
pwd

# ディレクトリの内容を表示
ls

# ディレクトリを移動
cd フォルダ名

# 一つ上のディレクトリへ
cd ..

# ホームディレクトリへ
cd ~

# 画面をクリア
clear  # Mac
cls    # Windows
```

### コピー＆ペーストのショートカット

**Mac ターミナル:**
- コピー: `Command + C`
- ペースト: `Command + V`

**Windows PowerShell:**
- コピー: `Ctrl + C` または選択して `Enter`
- ペースト: 右クリック または `Ctrl + V`

---

**作成日**: 2025年8月21日  
**対応OS**: macOS, Windows 10/11