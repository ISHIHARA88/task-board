# task-board

Vite + Reactで構築したタスクボードアプリ。タスクの追加・完了切り替え・削除ができる。

## 技術スタック

- **React 19** — UIコンポーネント、`useState` / `useEffect` によるstate管理
- **Vite 8** — ビルドツール・開発サーバー
- **Vanilla CSS** — CSSフレームワークなし、`App.css` に直接記述
- **localStorage** — タスクデータの永続化（ページリロード後も保持）

## ファイル構成

- `index.html` — エントリーポイント
- `src/main.jsx` — Reactのマウント処理
- `src/App.jsx` — アプリ全体のコンポーネントとロジック
- `src/App.css` — タスクボード用スタイル
- `src/index.css` — ベーススタイル（body・リセット）
- `vite.config.js` — Vite設定（`base: '/task-board/'` を指定）

## コンポーネント命名規約

- コンポーネントファイル名・関数名は **PascalCase**（例: `App`, `TaskItem`）
- イベントハンドラは **`handle` プレフィックス**（例: `handleKeyDown`, `handleSubmit`）
- state更新関数は **動詞 + 対象**（例: `addTask`, `toggleTask`, `deleteTask`）
- CSSクラス名は **kebab-case**（例: `task-list`, `input-row`, `delete-btn`）

## デプロイ先

https://ishihara88.github.io/task-board/

- ブランチ: `gh-pages`（`npm run deploy` で自動生成・更新）

## Git運用ルール

- コードを変更するたびに必ずコミットし、GitHubにプッシュすること
- リモートリポジトリ: https://github.com/ISHIHARA88/task-board.git
- ブランチ: `main`

### デプロイ手順

```bash
npm run deploy
```

`predeploy` で自動的に `npm run build` が実行され、`dist/` を `gh-pages` ブランチへプッシュする。

### コミット手順

```bash
git add <変更ファイル>
git commit -m "変更内容の説明"
git push
```
