---
layout: default
title: "Gemini CLI Installation Guide"
description: "Google Gemini CLI の日本語インストールガイド・完全ドキュメント"
---

# 🤖 Gemini CLI Installation Guide

> Google Gemini CLI の日本語インストールガイド・完全ドキュメント

[![Gemini CLI](https://img.shields.io/badge/Gemini_CLI-Official-4285F4?style=flat-square&logo=google)](https://github.com/google-gemini/gemini-cli)
[![Language](https://img.shields.io/badge/Language-Japanese-red?style=flat-square)](README.md)
[![License](https://img.shields.io/badge/License-MIT-green?style=flat-square)](LICENSE)
[![GitHub Pages](https://img.shields.io/badge/GitHub_Pages-Live-brightgreen?style=flat-square)](https://iidaatcnt.github.io/gemini-cli-installation-guide/)

## 📚 ドキュメント一覧

### 📖 インストールガイド

<div class="guide-cards">
  <div class="card">
    <h3>📘 完全インストールガイド</h3>
    <p>初心者向けの詳細な手順書・トラブルシューティング付き</p>
    <a href="docs/GEMINI_CLI_INSTALLATION_GUIDE" class="btn">詳細ガイドを見る</a>
  </div>

  <div class="card">
    <h3>⚡ クイックスタートガイド</h3>
    <p>5分で始められる最速ガイド</p>
    <a href="docs/GEMINI_CLI_QUICKSTART" class="btn">クイックスタート</a>
  </div>
</div>

### 🎯 特徴

- ✅ **完全日本語対応** - 初心者にも分かりやすい説明
- ✅ **OS別対応** - Mac・Windows・Linux すべてカバー
- ✅ **実践的** - すぐに使えるコマンド例が豊富
- ✅ **トラブル対応** - よくある問題と解決方法を網羅
- ✅ **最新版対応** - 2024-2025年版に対応

## 🚀 クイックスタート

### 前提条件
- Node.js 18+ がインストール済み
- Googleアカウントを持っている

### 3ステップインストール
```bash
# 1. Gemini CLI をインストール
npm install -g @google/gemini-cli

# 2. 起動
gemini

# 3. ブラウザでGoogleアカウントに認証
# → 完了！
```

### 最初のコマンド
```bash
gemini "こんにちは！自己紹介をして"
```

## 📋 詳細ガイド

### 🔰 初心者の方
1. [📘 完全インストールガイド](docs/GEMINI_CLI_INSTALLATION_GUIDE) から始めてください
2. Node.jsのインストールから丁寧に説明しています

### ⚡ 経験者の方
1. [⚡ クイックスタートガイド](docs/GEMINI_CLI_QUICKSTART) をご覧ください
2. 5分で始められます

## 🎯 Gemini CLI でできること

### 🔧 プログラミング支援
```bash
# コード生成
gemini "Pythonで素数判定する関数を作って"

# バグ修正
gemini "このエラーを修正して" --file debug.py

# コードレビュー
gemini "このコードの改善点は？" --file mycode.js
```

### 📝 ドキュメント作成
```bash
# README作成
gemini "このプロジェクト用のREADMEを作って"

# API仕様書
gemini "RESTfulなAPI仕様書を作成して"
```

### 🎓 学習サポート
```bash
# 概念説明
gemini "Dockerとは何か初心者向けに説明して"

# ベストプラクティス
gemini "Reactのベストプラクティスを教えて"
```

## 💡 Tips & Tricks

### エイリアス設定
```bash
# ショートカット設定
alias g="gemini"
alias gcode="gemini 'このコードを説明して' --file"

# 使用例
g "Hello World"
gcode index.js
```

### よく使うコマンドパターン
```bash
# ファイル操作
gemini "このファイルの内容を要約して" --file README.md

# 出力をファイルに保存
gemini "gitignoreテンプレートを作って" > .gitignore

# Web検索含む質問
gemini "2024年最新のJavaScriptトレンドは？"
```

## 📚 さらに詳しく

### 🎯 コマンド例集
[基本コマンド例](examples/basic-commands) で実践的な使い方を学べます。

### 🤝 コントリビュート
このプロジェクトをより良くするために、皆様の貢献を歓迎します！  
詳細は [コントリビューションガイド](CONTRIBUTING) をご覧ください。

## 🌟 コントリビュート

このプロジェクトをより良くするために、皆様の貢献を歓迎します！

### 📝 貢献方法
1. このリポジトリをフォーク
2. 新しいブランチを作成 (`git checkout -b feature/amazing-feature`)
3. 変更をコミット (`git commit -m 'Add amazing feature'`)
4. ブランチにプッシュ (`git push origin feature/amazing-feature`)
5. プルリクエストを作成

### 🐛 バグ報告・機能要望
- [Issues](https://github.com/iidaatcnt/gemini-cli-installation-guide/issues) でお知らせください
- 日本語での報告を歓迎します

## 📞 サポート

### 🔗 関連リンク
- [Gemini CLI 公式リポジトリ](https://github.com/google-gemini/gemini-cli)
- [Google AI Developer](https://ai.google.dev/)
- [Gemini API ドキュメント](https://ai.google.dev/gemini-api)

### ❓ よくある質問
詳細は各ガイドの「トラブルシューティング」セクションをご覧ください。

## 📄 ライセンス

このプロジェクトは [MIT License](LICENSE) のもとで公開されています。

## 🏷️ タグ

`gemini-cli` `google-ai` `ai-assistant` `command-line` `japanese` `tutorial` `guide` `installation` `beginner-friendly`

---

## ⭐ このプロジェクトが役に立ったら

ぜひ **Star** ⭐ をお願いします！また、SNSでのシェアも大歓迎です。

**最終更新**: 2025年8月21日  
**作成者**: [@iidaatcnt](https://github.com/iidaatcnt)  
**GitHub Pages**: [https://iidaatcnt.github.io/gemini-cli-installation-guide/](https://iidaatcnt.github.io/gemini-cli-installation-guide/)

<style>
.guide-cards {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
  gap: 2rem;
  margin: 2rem 0;
}

.card {
  background: #f8f9fa;
  border: 1px solid #e9ecef;
  border-radius: 8px;
  padding: 1.5rem;
  box-shadow: 0 2px 4px rgba(0,0,0,0.1);
}

.card h3 {
  margin-bottom: 1rem;
  color: #333;
}

.card p {
  color: #666;
  margin-bottom: 1rem;
}

.btn {
  display: inline-block;
  background: #007bff;
  color: white;
  padding: 0.5rem 1rem;
  text-decoration: none;
  border-radius: 4px;
  transition: background-color 0.3s;
}

.btn:hover {
  background: #0056b3;
  color: white;
  text-decoration: none;
}
</style>