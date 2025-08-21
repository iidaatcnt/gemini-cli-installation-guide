# 🎯 Gemini CLI 基本コマンド集

## 📚 学習・教育

### プログラミング学習
```bash
# 基本概念の説明
gemini "オブジェクト指向プログラミングとは何か、初心者向けに説明して"

# 言語比較
gemini "PythonとJavaScriptの違いを教えて"

# アルゴリズム学習
gemini "バブルソートのアルゴリズムをPythonで実装して"
```

### 技術用語解説
```bash
# Web技術
gemini "RESTとGraphQLの違いを表形式で比較して"

# インフラ
gemini "DockerとKubernetesの関係を分かりやすく説明して"

# データベース
gemini "SQLとNoSQLの使い分けを教えて"
```

## 🔧 コード生成・修正

### 関数・クラス生成
```bash
# ユーティリティ関数
gemini "JavaScriptで配列から重複を除去する関数を作って"

# クラス設計
gemini "Pythonでユーザー管理クラスを作って"

# React コンポーネント
gemini "ボタンコンポーネントをReactで作って、props対応で"
```

### バグ修正・デバッグ
```bash
# エラー解決
gemini "TypeError: Cannot read property 'map' of undefined の原因と解決方法"

# コードレビュー
gemini "このコードの問題点を指摘して" --file buggy-code.js

# パフォーマンス改善
gemini "このコードを最適化して" --file slow-function.py
```

## 📝 ドキュメント作成

### プロジェクトドキュメント
```bash
# README生成
gemini "Node.jsプロジェクト用のREADMEテンプレートを作って"

# API仕様書
gemini "ユーザー管理APIの仕様書をMarkdownで作成して"

# コメント生成
gemini "この関数にJSDocコメントを追加して" --file function.js
```

### 設定ファイル
```bash
# 設定ファイル生成
gemini "TypeScriptプロジェクト用のtsconfig.jsonを作って"

# .gitignore生成
gemini "React プロジェクト用の.gitignoreを作って"

# package.json のスクリプト
gemini "開発用のnpm scriptsを提案して"
```

## 🎨 フロントエンド開発

### HTML/CSS
```bash
# レスポンシブデザイン
gemini "モバイルファーストのNavbarをHTML/CSSで作って"

# CSS Grid レイアウト
gemini "3カラムレイアウトをCSS Gridで実装して"

# アニメーション
gemini "ローディングスピナーをCSSアニメーションで作って"
```

### JavaScript/TypeScript
```bash
# 非同期処理
gemini "fetch APIを使ってデータを取得する関数を作って"

# イベント処理
gemini "フォームバリデーションをJavaScriptで実装して"

# 型定義
gemini "ユーザーデータのTypeScript型定義を作って"
```

## 🗄️ バックエンド開発

### API開発
```bash
# Express.js
gemini "Express.jsでCRUD APIを作って"

# データベース操作
gemini "MongoDBでユーザー検索機能を実装して"

# 認証機能
gemini "JWT認証をNode.jsで実装して"
```

### SQL
```bash
# テーブル設計
gemini "ECサイト用のデータベーステーブルを設計して"

# 複雑なクエリ
gemini "売上上位の商品を取得するSQLクエリを書いて"

# インデックス最適化
gemini "このクエリのパフォーマンスを改善して"
```

## 🧪 テスト・デバッグ

### テストコード
```bash
# ユニットテスト
gemini "この関数のJestテストを書いて" --file utils.js

# E2Eテスト
gemini "ログイン機能のE2Eテストシナリオを作って"

# モック作成
gemini "API呼び出しのモックをJestで作って"
```

### デバッグ
```bash
# ログ出力
gemini "デバッグ用のログ出力を追加して" --file app.js

# エラーハンドリング
gemini "try-catch文を適切に追加して" --file api-call.js
```

## 🚀 DevOps・インフラ

### Docker
```bash
# Dockerfile作成
gemini "Node.jsアプリ用のDockerfileを作って"

# docker-compose
gemini "WebアプリとDB用のdocker-compose.ymlを作って"
```

### CI/CD
```bash
# GitHub Actions
gemini "Node.jsプロジェクト用のCI/CDワークフローを作って"

# デプロイスクリプト
gemini "Vercelデプロイ用のスクリプトを作って"
```

## 💡 プロのテクニック

### ファイル操作との組み合わせ
```bash
# ファイル内容を分析
gemini "このコードの複雑度を評価して" --file complex-code.js

# 複数ファイルの比較
gemini "2つのファイルの違いを説明して" --file old.js --file new.js

# 設定ファイルの説明
gemini "この設定ファイルの各項目を説明して" --file webpack.config.js
```

### 出力の活用
```bash
# ファイルに保存
gemini "React Hooksの使い方ガイド" > react-hooks-guide.md

# クリップボードにコピー（Mac）
gemini "gitコマンドのチートシート" | pbcopy

# パイプでの連携
gemini "TODOリストアプリの要件定義" | grep -i "機能"
```

### 継続的な会話
```bash
# 前回の続き
gemini --continue "さっきのコードを改良して"

# 履歴クリア
gemini --clear-history

# 特定のトピックでフォーカス
gemini --context="React開発" "コンポーネントの最適化方法は？"
```

---

## 📝 コマンド使用のコツ

1. **具体的に質問する**: 「ボタンを作って」より「ホバーエフェクト付きのボタンコンポーネントを作って」
2. **コンテキストを提供**: プロジェクトの情報や使用技術を伝える
3. **段階的に深掘り**: 基本から始めて、徐々に詳細な質問をする
4. **エラーは全文コピー**: エラーメッセージは省略せずに全て貼り付ける

## 🔍 さらなる活用方法

- [公式ドキュメント](https://github.com/google-gemini/gemini-cli)
- [詳細ガイド](../docs/GEMINI_CLI_INSTALLATION_GUIDE.md)
- [クイックスタート](../docs/GEMINI_CLI_QUICKSTART.md)