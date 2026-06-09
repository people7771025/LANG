# WIP — LANG 美語與日語自學系統

最後更新：2026-06-09（台北時間）/ Codex

## 現在狀態

- 新專案 `$HOME/Dev/LANG` 已建立，本機 git repo：`main`，目前尚未設定 remote。
- 第一版 MVP：單檔 `index.html`，離線可開，localStorage 保存進度。
- 內容包含：
  - 美語：3 個課程、9 個短句，重點含生活會話、點餐、旅行與美式連音。
  - 日語：3 個課程、9 個短句，重點含問候、自我介紹、請求確認、店家交通。
  - 聽力實驗室：播放、慢速、循環 3 次、聽寫檢查、跟讀自評、完成標記、收藏。
  - 學習紀錄：完成數、聽寫正確率、跟讀自評、收藏句、Markdown 匯出。

## 驗證

- `node` 抽出 `<script>` 後 `new Function()` parser OK。
- 檢查 `index.html` 包含 `speechSynthesis`、`LANG_COURSES`、`copyMarkdown` 等核心功能。
- 尚未做瀏覽器互動實跑；前一輪環境 Browser policy 擋 localhost，所以本輪先以靜態語法驗證為主。

## 下一步

1. 增加更多課程：美語發音最小對比、日語長音/促音/拗音、每日 20 分鐘訓練路線。
2. 若要部署：建立 GitHub remote 後推送並啟用 GitHub Pages。
3. 若要強化聽力：加入真人錄音或可下載音檔；目前先用瀏覽器 TTS。

## 卡點

- 無 remote，暫時只能本機 commit，不能 push。
