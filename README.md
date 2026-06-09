# LANG 美語與日語自學系統

一份離線可開、單檔 HTML 的語言自學工具，聚焦 **美語 + 日語**，並把聽力放在核心流程。

## 怎麼用

1. 直接打開 `index.html`
2. 選擇美語或日語課程
3. 用「聽力實驗室」播放、慢速播放、循環聽、聽寫、跟讀自評
4. 做章節測驗；答錯會進入錯題複習
5. 進度、錯題與收藏難句存在瀏覽器 localStorage

## 完整章節範圍

- 美語：8 章、40 個聽力短句、16 題章節測驗
  - Daily small talk
  - Clarifying and repair
  - Cafe and restaurants
  - Travel and transport
  - Work and meetings
  - Connected speech
  - American sound focus
  - Short news and stories
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
- 本系統是學習工具，不取代真人老師或正式語言測驗教材。
- 單檔 HTML，無 build step、無套件安裝。
