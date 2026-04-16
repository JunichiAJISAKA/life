---
source: slack
session_id: 20260417_020200_389ff66c
type: conversation-log
saved_at: 2026-04-17 02:52:42 JST
---

# Hermes Tools に夜間バグ探索設定を追加

- 保存日時: 2026-04-17 02:52:42 JST
- 出典: Jun との Slack スレッド
- セッションID: `20260417_020200_389ff66c`
- 種別: 実装ログ / 運用メモ
- 関連対象:
  - `hermes tools`
  - `dogfood` スキル
  - cron job
- キーワード: [hermes, tools, dogfood, cron, qa, nightly]

## 要点
`hermes tools` に「Set up nightly bug hunt automation」を追加し、夜間に自動で不具合探索を行う cron job を作成できるようにした。

## 依頼内容
- 夜間に不具合を探す設定を Tools に追加する。

## 実施内容
- `hermes tools` に専用メニュー項目を追加。
- 選択時に `dogfood` スキル付きの夜間バグ探索 cron job を作成するよう実装。
- 入力項目を Job name / Target URL / Scope / Schedule に整理。
- 出力先を `~/.hermes/cron/bug-hunts/<job-name>/` に設定。
- URL は `http/https` のみ受け付けるようにバリデーション追加。
- cron job 作成失敗時に不要ディレクトリを先に作らないよう調整。

## 変更ファイル
- `hermes_cli/tools_config.py`
- `tests/hermes_cli/test_tools_config.py`
- `website/docs/user-guide/features/tools.md`

## 検証
- `pytest tests/hermes_cli/test_tools_config.py -q` → 28 passed
- `python -m py_compile hermes_cli/tools_config.py` → OK

## 実務上の意味
- 夜間の探索的 QA を定型化できる。
- 手動の設定作業を減らし、低コスト運用で継続観測しやすくなる。
- バグ探索結果の保存先が明確になり、後続のログ確認・改善に繋げやすい。

## 現時点の結論
夜間バグ探索を Hermes の Tools から直接セットアップできる状態になった。