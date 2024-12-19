<div align="center">

# 🎯 GitHub Kanban MCP Server

<img src="https://raw.githubusercontent.com/Sunwood-ai-labs/github-kanban-mcp-server/main/assets/header.svg" alt="GitHub Kanban MCP Server" width="100%" />

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![TypeScript](https://img.shields.io/badge/TypeScript-4.9.5-blue.svg)](https://www.typescriptlang.org/)
[![Node.js](https://img.shields.io/badge/Node.js-18.x-green.svg)](https://nodejs.org/)
[![npm](https://img.shields.io/badge/npm-9.x-red.svg)](https://www.npmjs.com/)

</div>

## 📋 概要

GitHub Kanban MCP Serverは、GitHubのissueをカンバンボード形式で管理し、LLMのタスク管理を効率化するためのModel Context Protocol（MCP）サーバーです。

## 🚀 特徴

- 🔄 GitHubのissueをカンバン形式で管理
- 🤖 LLMによる自動タスク管理
- 📊 プロジェクトの進捗可視化
- 🔗 GitHubとの完全な統合

## 🛠️ インストール

```bash
npm install @sunwood-ai-labs/github-kanban-mcp-server
```

## ⚙️ 設定

1. 環境変数の設定:
```bash
GITHUB_TOKEN=your_github_token
GITHUB_OWNER=your_github_username
GITHUB_REPO=your_repository_name
```

2. MCPの設定ファイルに追加:
```json
{
  "mcpServers": {
    "github-kanban": {
      "command": "github-kanban-mcp-server",
      "env": {
        "GITHUB_TOKEN": "your_github_token",
        "GITHUB_OWNER": "your_github_username",
        "GITHUB_REPO": "your_repository_name"
      }
    }
  }
}
```

## 🔧 使用可能なツール

### 1. list_issues
カンバンボードのissue一覧を取得します。

**入力パラメータ:**
- `state`: issueの状態（'open', 'closed', 'all'）
- `labels`: フィルタリングするラベルの配列

### 2. create_issue
新しいissueを作成します。

**入力パラメータ:**
- `title`: issueのタイトル（必須）
- `body`: issueの本文
- `labels`: ラベルの配列
- `assignees`: アサインするユーザーの配列

### 3. update_issue
既存のissueを更新します。

**入力パラメータ:**
- `issue_number`: issue番号（必須）
- `title`: 新しいタイトル
- `body`: 新しい本文
- `state`: 新しい状態（'open', 'closed'）
- `labels`: 新しいラベルの配列
- `assignees`: 新しいアサインの配列

## 📝 ライセンス

MIT License - [LICENSE](LICENSE)ファイルを参照してください。

## 🤝 コントリビューション

1. このリポジトリをフォーク
2. 機能ブランチを作成 (`git checkout -b feature/amazing-feature`)
3. 変更をコミット (`git commit -m '✨ feat: 素晴らしい機能を追加'`)
4. ブランチにプッシュ (`git push origin feature/amazing-feature`)
5. プルリクエストを作成

## 📮 フィードバック

問題や提案がありましたら、[Issueを作成](https://github.com/sunwood-ai-labs/github-kanban-mcp-server/issues)してください。
