# HANDOFF — LANG 美語與日語自學系統

## 專案定位

- 單檔 HTML：`index.html`
- 離線可開、無 build step、無 npm
- 主題：美語與日語自學，第一版把「聽力」放在核心，而不是只做文字教材
- 狀態：localStorage

## 檔案

- `index.html`：主程式、課程資料、CSS、JS 全在單檔
- `README.md`：使用說明
- `WIP.md`：目前狀態與下一步
- `HANDOFF.md`：交接資訊

## localStorage keys

- `lang/state`：目前語言、課程、選中短句、設定、完成/收藏/分數/筆記

## 互動模組

- `speechSynthesis`：瀏覽器 TTS，依 `en-US` / `ja-JP` 選 voice
- 聽力實驗室：
  - Play：正常速度
  - Slow：慢速
  - Loop x3：循環三次
  - Dictation：聽寫後比對標準答案與 accepted aliases
  - Shadowing：使用者自評 1-5 分
- Export：複製 Markdown 學習紀錄

## 課程資料結構

`LANG_COURSES` 依語言分組：

```js
{
  id, name, lang, speechLang, tracks: [
    { id, title, goal, phrases: [
      { id, text, display, roman, zh, focus, listenFor, accepted }
    ] }
  ]
}
```

## 注意

- TTS voice 依使用者作業系統/瀏覽器而異，不保證每台都有自然的日語或美語聲音。
- 不要把課程資料拆成外部 JSON，第一版維持單檔可攜。
- 若要加入真人音檔，需決定音檔是否進 git；大量 media 不建議直接進 repo。
