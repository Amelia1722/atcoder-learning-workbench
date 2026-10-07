# AtCoder Learning Workbench

**「次に何を学習すればよいか」で迷わないための、AtCoder学習ロードマップ兼ワークスペースです。**

自分のAtCoder IDのAC・WA履歴を使った推薦と、ロードマップ、メモ・タイマー、知識ガイドをまとめたローカルアプリです。次に取り組む問題を選び、分からない知識を確認し、振り返りを残せます。IDなしのゲストでも使い始められます。

## できること

- **学ぶ順番を見つける**：ロードマップと関連知識から、次の学習内容を探す
- **理由を見て問題を選ぶ**：本人IDの未AC・WA履歴・未経験タグなどを基に候補を表示する。ゲストは公開Difficultyが低い順に表示する
- **ヒントの後に理解を確かめる**：ヒント使用後のACをReviewに残し、確認済みの同技法・近いDifficultyの別問題を提案する。条件に合う候補がなければ理由を示す
- **学習を続ける**：問題ごとのメモ・タイマーとKnowledge Atlasを行き来し、Pythonの実行で確認する

## 実画面

### IDなしで始める

![ゲストのDashboard](01-guest-dashboard.png)

ゲストは履歴0件から開始します。Rating・解答確率を推測で埋めず、一般的な候補を表示します。

### 自分の履歴から次の問題を選ぶ

![本人IDのDashboard](02-personal-dashboard.png)

本人提供の画面です。公開提出履歴の集計と推薦理由を確認できます。画像はDashboardの記録で、全機能・全問題の動作保証ではありません。

## ダウンロードして試す

1. **[最新版ZIPをダウンロード](https://github.com/Amelia1722/atcoder-learning-workbench/raw/refs/heads/main/AtCoder-Learning-Workbench-Source-20261007.zip)** し、新しいフォルダーに展開する
2. **launch-review.cmd** をダブルクリックする
3. 準備完了後、**http://127.0.0.1:5173** を開く
4. Learning Lab → **ABC081_A（8件）を開く** → **コードを入力して実行** から、同梱テストを試す

必要環境：**Windows / Python 3.14（py launcher付き）/ Node.js 24（npmを含む）**。初回は固定依存を取得するため通信が必要です。既存の個人DBがあるフォルダーへ上書きしないでください。

詳しい起動・ヒントの操作・保存先（ZIP内 README_JA.md） · テストの再現手順（ZIP内）

## 技術構成

- React / TypeScript / Vite：画面と状態管理
- FastAPI / SQLite：ローカルAPI、ID別の学習記録・キャッシュ
- Web Worker / Pyodide：ブラウザー内の学習用Python実行
- ゲストのメモ・タイマー：ブラウザー内に保存

設計・推薦ルール・担当範囲の説明（ZIP内）

AtCoderの公式サービスではありません。プロジェクト全体へのMIT等の一括ライセンスは付与していません。依存物と上流コンテンツの権利はそれぞれの権利者に帰属します。
