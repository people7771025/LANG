# WIP — LANG 美語與日語自學系統

最後更新：2026-06-09（台北時間）/ Codex

## 現在狀態

- 新專案 `$HOME/Dev/LANG` 已建立，本機 git repo：`main`，目前尚未設定 remote。
- v1 完整章節版：單檔 `index.html`，離線可開，localStorage 保存進度。
- 內容包含：
  - 美語：8 章、40 個聽力短句、16 題章節測驗。
  - 日語：8 章、40 個聽力短句、16 題章節測驗。
  - 聽力實驗室：播放、慢速、循環 3 次、聽寫檢查、跟讀自評、完成標記、收藏。
  - 章節測驗：答錯會進入錯題複習，答對會自動移出錯題。
  - 每日 20 分鐘聽力計畫：盲聽、慢聽、聽寫、跟讀、錯題/收藏回收。
  - 學習紀錄：完成數、聽寫正確率、跟讀自評、章節錯題、收藏句、Markdown 匯出。

## 驗證

- `node` 抽出 `<script>` 後 `new Function()` parser OK。
- 檢查 `index.html` 包含 `speechSynthesis`、`LANG_COURSES`、`copyMarkdown`、`quizAnswers`、`wrongQuizItems` 等核心功能。
- 內容計數：美語 40 句、日語 40 句。
- 尚未做瀏覽器互動實跑；前一輪環境 Browser policy 擋 localhost，所以本輪先以靜態語法驗證為主。

## 下一步

1. 若要部署：建立 GitHub remote 後推送並啟用 GitHub Pages。
2. 若要強化聽力：加入真人錄音或可下載音檔；目前先用瀏覽器 TTS。
3. 若要做進階版：可加入 spaced repetition、錄音回放、JLPT/TOEIC 題型模擬。

## 卡點

- 無 remote，暫時只能本機 commit，不能 push。
