# HANDOFF — LANG 美語與日語自學系統

## 專案定位

- 單檔 HTML：`index.html`
- 離線可開、無 build step、無 npm
- 主題：美語與日語自學，v2 考試通關版把「考試路線 + 聽力實驗室」放在核心
- 英文目標：GEPT 高級 C1、TOEFL iBT、IELTS Academic 7.0+
- 日文目標：至少 JLPT N2 通過，並銜接 N1
- 狀態：localStorage

## 檔案

- `index.html`：主程式、課程資料、CSS、JS 全在單檔
- `README.md`：使用說明
- `WIP.md`：目前狀態與下一步
- `HANDOFF.md`：交接資訊

## localStorage keys

- `lang/state`：目前語言、課程、選中短句、設定、完成/收藏/分數/測驗/錯題/考試章節/筆記

## 互動模組

- `speechSynthesis`：瀏覽器 TTS，依 `en-US` / `ja-JP` 選 voice
- 聽力實驗室：
  - Play：正常速度
  - Slow：慢速
  - Loop x3：循環三次
  - Dictation：聽寫後比對標準答案與 accepted aliases
  - Shadowing：使用者自評 1-5 分
- 章節測驗：
  - 每章 2 題
  - `quizAnswers` 記錄作答結果
  - `quizReview` 保存錯題，答對後移出錯題
- 考試通關路線：
  - `EXAM_PATHS` 依語言分組
  - 英文 48 章：診斷、C1 基礎、聽力、閱讀、寫作、口說、整合任務、考試策略、模考補弱
  - 日文 48 章：N4/N3 補洞、N2 語彙漢字、文法、讀解、聽解、綜合速度、模考、N1 銜接
  - `examCompleted` 記錄考試章節完成狀態
- 每日 20 分鐘計畫：
  - 盲聽
  - 慢聽
  - 聽寫
  - 跟讀
  - 錯題/收藏回收
- Export：複製 Markdown 學習紀錄

## 課程規模

- 美語：8 章、40 句、16 題測驗
- 日語：8 章、40 句、16 題測驗
- 英文考試路線：48 章
- 日文考試路線：48 章

## 課程資料結構

`LANG_COURSES` 依語言分組：

```js
{
  id, name, lang, speechLang, tracks: [
    { id, title, level, goal, phrases: [
      { id, text, display, roman, zh, focus, listenFor, accepted }
    ], quiz: [
      { question, choices, answer, why }
    ] }
  ]
}
```

`EXAM_PATHS` 依語言分組：

```js
{
  title, desc, goals, gates, sources, phases: [
    { title, weeks, goal, chapters: [
      { id, title, outcome, practice, gate }
    ] }
  ]
}
```

## 注意

- TTS voice 依使用者作業系統/瀏覽器而異，不保證每台都有自然的日語或美語聲音。
- TOEFL 2026 後官方資訊已顯示 1-6 分制並於過渡期提供 0-120 對照；若考試格式再改，需更新 `EXAM_PATHS.en.goals` 與考試策略章。
- JLPT、GEPT、IELTS 正式報考前仍要檢查官方最新頁面。
- 不要把課程資料拆成外部 JSON，第一版維持單檔可攜。
- 若要加入真人音檔，需決定音檔是否進 git；大量 media 不建議直接進 repo。
