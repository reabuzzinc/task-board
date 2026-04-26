# CLAUDE.md — タスクボード プロジェクト

## プロジェクト概要

Vite + React で構築したタスクボードアプリケーション。

**機能:**
- テキスト入力でタスクを追加（Enter キーまたはボタン）
- チェックボックスで完了／未完了を切り替え
- タスクを削除
- 完了済みタスクはグレー＋打ち消し線で表示
- タスクはローカルストレージに保存（リロードしても消えない）

**技術スタック:** React 19, Vite, CSS（UIライブラリなし）

**公開URL:** https://reabuzzinc.github.io/task-board/

---

## Git 運用ルール

### コードを変更するたびに GitHub へプッシュする

**コードを変更したら、必ずコミットして GitHub にプッシュすること。**

毎回のワークフロー:

```bash
git add <変更したファイル>
git commit -m "<変更内容を簡潔に説明するメッセージ>"
git push origin <現在のブランチ名>
```

ルール:
- `git add` はファイル名を指定する。`git add -A` や `git add .` は機密ファイルやバイナリを誤って含めるリスクがあるため使わない。
- コミットメッセージは命令形で書く（例: `Add login page`, `Fix task deletion bug`）。過去形（`Added`, `Fixed`）は使わない。
- `main`／`master` への force-push は**いかなる場合も禁止**。
- pre-commit フックのスキップ（`--no-verify`）は**禁止**。

### ブランチ戦略

- `main` — 本番リリース済みのコードのみ。
- 機能開発は短命のブランチで行う: `feature/<トピック名>`。
- `main` へのマージは Pull Request 経由。明示的に指示された場合を除き直接プッシュしない。

### コミットメッセージの形式

```
<type>: <概要>  （50文字以内）

<本文 — 任意、72文字で折り返す>
```

type の種類: `feat`（機能追加）, `fix`（バグ修正）, `refactor`（リファクタ）, `style`（スタイル）, `test`（テスト）, `docs`（ドキュメント）, `chore`（雑務）

---

## 開発ガイドライン

- 新規ファイルの作成より既存ファイルの編集を優先する。
- タスクの要件を超えたエラーハンドリングや抽象化を追加しない。
- コメントは「なぜそうするのか」が自明でない場合のみ書く。
- コミット前に `npm run dev` で UI の動作を確認する。

### GitHub Pages へのデプロイ

```bash
npm run deploy
```

ビルドと `gh-pages` ブランチへのプッシュが自動で実行される。

---

## 環境

- プラットフォーム: Windows 11
- シェル: bash（コマンドは Unix 構文で記述）
- 作業ディレクトリ: `c:\claudeAI\task-board`
- リモートリポジトリ: https://github.com/reabuzzinc/task-board.git
