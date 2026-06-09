# LANG 美語與日語自學系統

一份離線可開、單檔 HTML 的語言自學工具，聚焦 **美語 + 日語**。現在定位是「考試通關學習系統」：英文目標對準 GEPT 高級、TOEFL iBT、IELTS Academic；日文目標至少通過 JLPT N2，並保留 N1 銜接。

## 怎麼用

1. 直接打開 `index.html`
2. 選擇美語或日語
3. 先走「考試通關路線」，逐章完成診斷、輸入、輸出、模考與補弱
4. 用「聽力實驗室」播放、慢速播放、循環聽、聽寫、跟讀自評
5. 做章節測驗；答錯會進入錯題複習
6. 進度、錯題與收藏難句存在瀏覽器 localStorage

## 完整章節範圍

- 英文考試路線：48 章
  - 目標：GEPT 高級 C1、TOEFL iBT 5.0+（2026 後官方 1-6 制；0-120 為過渡參考）、IELTS Academic 7.0+ 且單科不低於 6.5
  - 流程：診斷、C1 基礎、聽力、閱讀、寫作、口說、整合任務、考試別策略、模考補弱
- 美語：8 章、40 個聽力短句、16 題章節測驗
  - Daily small talk
  - Clarifying and repair
  - Cafe and restaurants
  - Travel and transport
  - Work and meetings
  - Connected speech
  - American sound focus
  - Short news and stories
- 日文考試路線：48 章
  - 目標：至少 JLPT N2 通過，並銜接 N1
  - 流程：N4/N3 補洞、N2 語彙漢字、N2 文法、N2 讀解、N2 聽解、綜合速度、N2 模考、N1 銜接
- 日語：8 章、40 個聽力短句、16 題章節測驗
  - 問候與自我介紹
  - 請求與確認
  - 店家與餐廳
  - 交通與方向
  - 時間與約定
  - 助詞與句型聽力
  - 長音、促音、拗音
  - 日常短對話
- 聽力：瀏覽器 Web Speech API 播放，支援正常/慢速/循環
- 練習：聽寫檢查、跟讀自評、完成標記、錯句收藏、章節錯題
- 每日流程：20 分鐘聽力計畫，包含盲聽、慢聽、聽寫、跟讀、回收
- 匯出：可複製 Markdown 學習紀錄，含完成句、錯題、收藏難句

## 注意

- 語音播放依賴瀏覽器內建語音。Chrome/Edge 通常可用；可用聲音會因電腦而異。
- 考試格式可能調整，正式報考前仍應查看官方最新資訊。
- 本系統是學習工具，不取代真人老師或正式語言測驗教材。
- 單檔 HTML，無 build step、無套件安裝。

## 官方依據

- GEPT Advanced: https://www.gept.org.tw/Eng/advanced.html
- TOEFL iBT Test Content: https://www.ets.org/toefl/test-takers/ibt/about/content.html
- IELTS Scoring: https://ielts.org/take-a-test/your-results/ielts-scoring-in-detail
- JLPT Test Sections: https://www.jlpt.jp/e/guideline/testsections.html
