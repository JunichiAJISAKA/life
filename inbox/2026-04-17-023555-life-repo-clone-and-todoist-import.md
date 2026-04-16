---
source: slack
session_id: 20260417_023554_88665aaa
type: conversation-log
saved_at: 2026-04-17 02:52:42 JST
---

# life リポジトリ準備と Todoist life ラベル取り込み

- 保存日時: 2026-04-17 02:52:42 JST
- 出典: Jun との Slack スレッド
- セッションID: `20260417_023554_88665aaa`
- 種別: 実行ログ / 運用メモ
- 関連対象:
  - `git@github.com:JunichiAJISAKA/life.git`
  - `~/git/life`
  - Todoist `life` ラベル
- キーワード: [life, todoist, inbox, git, github, import]

## 要点
`life` リポジトリを `~/git/life` に clone し、Jun が「ライフ」と言ったときの参照先として記録。その後、Todoist の `life` ラベル付きタスクを `life/inbox` に保存し、Todoist から削除、GitHub へ commit/push まで実施した。

## 依頼内容
1. `life` リポジトリを clone
2. 「ライフ」がこのリポジトリを指すと記録
3. Todoist `life` ラベルの内容を `life/inbox` に保存し、Todoist から削除
4. `life` リポジトリは自動コミット・プッシュ
5. 追加分が出たため再実行

## 実施内容
- `git@github.com:JunichiAJISAKA/life.git` を `~/git/life` に clone。
- リポジトリは初回時点で empty repository だった。
- 「ライフ」＝ `git@github.com:JunichiAJISAKA/life.git` / `~/git/life` として扱う前提を記録。
- Todoist `life` ラベル付きタスクを `life/inbox` に保存。
- 保存済みタスクを Todoist から削除。
- Git commit / push を実施。
- 再実行時に新規 2 件を追加で保存し、同様に削除・push まで完了。

## 保存ファイル
- `~/git/life/inbox/2026-04-17-024141-todo-github.md` ほか 11 件
- `~/git/life/inbox/2026-04-17-025209-hermes.md` ほか 1 件
- 旧集約ファイル 2 件は廃止し、現在は各 Todo を 1 ファイルずつ保存

## 実行結果
- 初回保存件数: 12 件
- 再実行保存件数: 2 件
- 最終確認時点の Todoist `life` ラベル: 0 件
- commit: `26649b0` / `2998209`

## 今回追加で保存された 2 件
1. `Hermesのインターフェースで、より良いものがないかを検討`
2. `ok googleのようなハードがhermesにはないか？`

## 実務上の意味
- `life` を個人運用の受け皿として使う基盤ができた。
- Todoist から `life/inbox` への移送運用が成立した。
- 自動 commit/push 前提のため、収集内容がそのまま GitHub 側でも追跡できる。

## 現時点の結論
`life` リポジトリの初期セットアップと Todoist `life` ラベルの inbox 取り込み運用が開始された。
