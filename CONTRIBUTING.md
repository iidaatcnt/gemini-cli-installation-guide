# 🤝 コントリビューションガイド

Gemini CLI Installation Guide プロジェクトへのご協力、ありがとうございます！

## 📋 貢献の種類

### 📝 ドキュメントの改善
- 誤字脱字の修正
- 説明の明確化
- 新しいセクションの追加
- 翻訳の改善

### 💡 新しいコンテンツ
- コマンド例の追加
- ユースケースの追加
- トラブルシューティング情報
- ベストプラクティス

### 🐛 バグ報告
- リンク切れの報告
- 手順の不備
- 動作しないコマンド例

## 🚀 コントリビューション手順

### 1. リポジトリのフォーク
```bash
# GitHubでこのリポジトリをフォーク
# あなたのアカウントにコピーが作成されます
```

### 2. ローカルにクローン
```bash
git clone https://github.com/あなたのユーザー名/gemini-cli-installation-guide.git
cd gemini-cli-installation-guide
```

### 3. 新しいブランチを作成
```bash
# 機能追加の場合
git checkout -b feature/add-new-examples

# バグ修正の場合
git checkout -b fix/broken-link

# ドキュメント改善の場合
git checkout -b docs/improve-installation-guide
```

### 4. 変更を加える
- ファイルを編集
- 新しいファイルを追加
- 既存の内容を改善

### 5. 変更をコミット
```bash
git add .
git commit -m "feat: Add advanced command examples for AI development"

# コミットメッセージの例：
# feat: 新機能追加
# fix: バグ修正
# docs: ドキュメント更新
# style: フォーマット修正
# refactor: リファクタリング
```

### 6. プッシュ
```bash
git push origin feature/add-new-examples
```

### 7. プルリクエスト作成
1. GitHubでプルリクエストを作成
2. 変更内容を詳しく説明
3. レビューを待つ

## 📝 ファイル構成

```
gemini-cli-installation-guide/
├── README.md                 # メインページ
├── docs/                     # ドキュメント
│   ├── GEMINI_CLI_INSTALLATION_GUIDE.md
│   └── GEMINI_CLI_QUICKSTART.md
├── examples/                 # 例とサンプル
│   └── basic-commands.md
├── CONTRIBUTING.md           # このファイル
├── LICENSE                   # ライセンス
└── .gitignore               # Git除外設定
```

## 📖 コンテンツガイドライン

### 📚 ドキュメント作成時のポイント

#### 1. 読みやすさを重視
- 見出しを適切に使用
- コードブロックには言語指定
- 絵文字で視覚的に分かりやすく

#### 2. 初心者目線
- 専門用語には説明を付ける
- ステップバイステップで説明
- スクリーンショットや図解があると良い

#### 3. 実用性
- 実際に動くコマンド例
- よくある使用場面を想定
- トラブルシューティング情報

### ✅ 良い例
```bash
# ✅ 良い例：具体的で実用的
gemini "React Hooksを使った状態管理のベストプラクティスを教えて"

# 出力例：
# React Hooksを使った効果的な状態管理には以下のパターンがあります...
```

### ❌ 避けるべき例
```bash
# ❌ 避ける例：曖昧で実用性が低い
gemini "プログラミングについて教えて"
```

## 🎯 プルリクエストガイドライン

### タイトル
- 簡潔で分かりやすく
- 変更内容が一目で分かる

### 説明
- **何を**変更したか
- **なぜ**変更したか
- **どのように**変更したか

### 例
```markdown
## 変更内容
AI開発関連のコマンド例を examples/ai-development.md に追加

## 変更理由
AI/ML開発でGemini CLIを活用したいユーザーが増えているため

## 変更詳細
- 機械学習のコード生成例を追加
- データ分析用のコマンドを追加
- AI倫理に関する質問例を追加
```

## 🔍 レビュープロセス

### 確認項目
- [ ] 内容が正確である
- [ ] リンクが正しく動作する
- [ ] コマンド例が実際に動作する
- [ ] 日本語が自然である
- [ ] ファイル構成が適切である

### レビュー時間
- 通常1-3日以内
- 大きな変更の場合は1週間程度

## 💬 コミュニケーション

### 質問・相談
- [Issues](../../issues) で気軽に質問
- 日本語でのコミュニケーション歓迎
- Discord/Slackなどのリアルタイムチャットは現在なし

### 提案・アイデア
- [Issues](../../issues) で「enhancement」ラベルを使用
- 新しい機能やコンテンツのアイデア
- 構成の改善提案

## 🏷️ Issue/PRラベル

### Issues
- `bug`: バグ報告
- `documentation`: ドキュメント関連
- `enhancement`: 新機能・改善提案
- `good first issue`: 初心者におすすめ
- `help wanted`: ヘルプ募集中

### Pull Requests
- `feat`: 新機能
- `fix`: バグ修正
- `docs`: ドキュメント更新
- `style`: スタイル修正
- `refactor`: リファクタリング

## 🙏 謝辞

すべてのコントリビューターに心から感謝します！

### コントリビューター一覧
<!-- コントリビューターは自動的に追加されます -->

---

## 📞 連絡先

- GitHub Issues: [Issues](../../issues)
- メンテナー: [@iidaatcnt](https://github.com/iidaatcnt)

皆様のご協力により、より良いリソースを作ることができます。どんな小さな貢献でも大歓迎です！