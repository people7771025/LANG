# WIP — LANG 美語與日語自學系統

最後更新：2026-06-09（台北時間）/ Codex

## 現在狀態

- 專案 `$HOME/Dev/LANG` 已建立，本機 git repo：`main`，remote：`https://github.com/people7771025/LANG.git`。
- GitHub Pages 已啟用：<https://people7771025.github.io/LANG/>
- v2 考試通關版：單檔 `index.html`，離線可開，localStorage 保存進度。
- 內容包含：
  - 英文考試路線：48 章，對準 GEPT 高級 C1、TOEFL iBT、IELTS Academic 7.0+。
  - 美語：8 章、40 個聽力短句、16 題章節測驗。
  - 日文考試路線：48 章，對準 JLPT N2 通過並銜接 N1。
  - 日語：8 章、40 個聽力短句、16 題章節測驗。
  - 考試通關路線：每章有成果、練習、通過門檻，可標記完成並匯出。
  - 聽力實驗室：播放、慢速、循環 3 次、聽寫檢查、跟讀自評、完成標記、收藏。
  - 章節測驗：答錯會進入錯題複習，答對會自動移出錯題。
  - 每日 20 分鐘聽力計畫：盲聽、慢聽、聽寫、跟讀、錯題/收藏回收。
  - 學習紀錄：完成數、聽寫正確率、跟讀自評、章節錯題、收藏句、Markdown 匯出。

## 驗證

- `node` 抽出 `<script>` 後 `new Function()` parser OK。
- 檢查 `index.html` 包含 `speechSynthesis`、`LANG_COURSES`、`EXAM_PATHS`、`copyMarkdown`、`quizAnswers`、`wrongQuizItems`、`examCompleted` 等核心功能。
- 內容計數：美語 40 句、日語 40 句；英文考試路線 48 章、日文考試路線 48 章。
- 已用 Playwright 透過臨時本地 server 驗證：
  - 英文考試路線：8 階段、48 章、4 目標、4 gate 正常渲染。
  - 日文考試路線：8 階段、48 章、4 目標、4 gate 正常渲染。
  - 考試章節完成按鈕可寫入 localStorage 並更新進度。

## 下一步

1. 若要強化聽力：加入真人錄音或可下載音檔；目前先用瀏覽器 TTS。
2. 若要做進階版：可加入 spaced repetition、錄音回放、正式模考題庫與作文/口說評分 rubric。
3. 若要整合入口：透過 LEARN <https://people7771025.github.io/LEARN/> 導覽。

## 卡點

- 無卡點。
