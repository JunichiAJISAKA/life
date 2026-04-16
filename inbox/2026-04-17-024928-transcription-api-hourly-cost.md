---
source: slack
session_id: 20260417_024928_6b9c76ac
type: conversation-log
saved_at: 2026-04-17 02:52:42 JST
---

# 音声文字起こしAPIの1時間あたりコスト試算

- 保存日時: 2026-04-17 02:52:42 JST
- 出典: Jun との Slack スレッド
- セッションID: `20260417_024928_6b9c76ac`
- 種別: コスト試算メモ
- 関連対象:
  - OpenAI Whisper / transcription API
  - 為替換算
- キーワード: [speech-to-text, whisper, pricing, cost, yen]

## 要点
OpenAI の文字起こし API を前提に、1 時間あたりの費用を円換算した結果、約 57 円 / 時間という試算になった。

## 前提
- 料金: `$0.006 / 分`
- 1 時間: `60 分`
- 為替: `1 USD = 158.98 JPY`（Frankfurter, 2026-04-16）

## 計算
- `$0.006 × 60 = $0.36 / 時間`
- `$0.36 × 158.98 = 約57.23円 / 時間`

## 結果
- 約 `57円 / 時間`
- 参考: `10時間 = 約572円`

## 補足
- OpenAI 公式価格ページは取得時にブロックされたため、検索経由で OpenAI Developer Community 上の `Whisper is $0.006/minute` 記述を確認して計算した。
- 別 API（Google / Deepgram / AssemblyAI など）を前提にする場合は再計算が必要。

## 現時点の結論
音声文字起こしを低コストに試す観点では、Whisper 系 API は 1 時間あたり約 57 円という感覚値で見積もれる。