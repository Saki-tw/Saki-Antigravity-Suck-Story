# 獻祭指南 (Contributing Guide) 👻

## 歡迎來到數位創傷檔案館

> *「每一個 Bug 背後都有一個鬼故事。*
> *每一個故事都值得被記住，否則歷史將在下一個 Sprint 輪迴重演。」*

---

## 🎯 我們在收集什麼

我們收集**真實的經歷**，並希望你用帶有**都市傳說**或**賽博恐怖**風格的筆觸來記錄。我們在尋找那些機器表現得彷彿帶有**私人恩怨**的時刻。

| 分類 | 描述 | 關鍵字 |
|------|------|--------|
| **不死者 (The Undead)** 💀 | `kill -9` 也殺不死的 Process。作業系統裡的地縛靈。 | `defunct`, `zombie`, `orphan process`, `不死身` |
| **幻影 (The Phantom)** 👻 | 畫面上有，資料裡無。前端給你的集體幻覺。 | Null Pointer, 配額幻覺, 幽靈流量, Hydration Error |
| **水蛭 (The Leech)** 🧛 | 在你睡覺時偷偷吸乾資源（錢、Token、記憶體）的系統。 | Memory Leak, 帳單爆炸, 遞迴計費, 遺忘的 EC2 |
| **海妖 (The Siren)** 😈 | 用優雅的架構誘惑你觸礁沈船。「Clean Code」導致的生產環境癱瘓。 | 過度設計, 優化陷阱, Best Practice 的反噬 |
| **迷宮 (The Labyrinth)** 🌀 | 讓執行指標 (Pointer) 陷入無限迴圈的邏輯黑洞。Call Stack 的事件視界。 | 無限遞迴, Deadlock, Callback Hell, 循環依賴 |
| **詛咒 (The Curse)** 🔮 | 接上 Debugger 就會消失的 Bug。薛丁格的貓。只在週二發生的怪談。 | Race Condition, 量子 Bug, Production Only |

---

## 📝 故事格式

請使用這種結合**技術嚴謹性**與**克蘇魯式絕望感**的敘事結構：

```markdown
# [故事標題]

> *「一句話摘要，要讓人背脊發涼的那種。」*

## 暴風雨前的寧靜 (The Setting)
描述當時的環境。機房的低頻嗡嗡聲。剛通過 CI 的虛假安全感。

## 異象初現 (The Anomaly)
第一個徵兆是什麼？閃爍的 Log？奇怪的延遲？數字對不上？

## 墜入深淵 (The Descent)
詳細描述 Debug 的過程。發現標準工具完全失效時的絕望。感覺被代碼注視著。

## 恐怖降臨 (The Horror)
根本原因是什麼？是 Race Condition？還是...更邪門的東西？
*請附上 Stack Trace、代碼片段或 Log 作為靈異照片（證據）。*

## 倖存者的傷痕 (The Survivor's Scar)
你學到了什麼？為了防止黑暗再次降臨，你現在會執行什麼儀式（測試）？

---
*記錄時間：YYYY-MM-DD*
*恐怖程度：💀💀💀💀💀 (1-6 顆骷髏)*
*標籤：殭屍/幻影/水蛭/海妖/迷宮/詛咒*
```

---

## 🚀 獻祭儀式

### 1. 繼承詛咒 (Fork)
Fork 這個 Repository。現在這也是你的業障了。

### 2. 撰寫惡夢 (Scribe)
在 `stories/` 目錄下建立你的故事檔案。檔名最好能暗示內容的恐怖。
`stories/the_silent_killer.md`

### 3. 更新名冊 (Update Index)
在 `README.md` 中加入你的故事連結。加入倖存者的行列。

### 4. 發送請求 (Pull Request)
發送 PR。我們會審查——不是審查代碼品質，而是審查**恐懼的品質**。

---

## ⚠️ 墓園守則

### 永恆原則 (The Principle of Permanence)
> **一旦你的故事被 Merge，它就刻在墓碑上了。**

- 維護者**承諾**不會刪除任何已 Merge 的故事。
- 歷史不可竄改。刪除 Bug Report 就是邀請它再次發生。
- 你可以提交「續集」或「勘誤」，但原始的恐懼將被保留。

### 會被驅魔的內容 (Rejected)
- 明顯的惡意或仇恨言論。
- 私鑰或個資 (PII)（我們要的是鬼故事，不是傳票）。
- 沒有技術靈魂的純虛構小說。

---

## 🏆 倖存者名單
所有貢獻者都會被記錄。在黑暗中，你並不孤單。

---

## 📜 授權
[CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/).
散播恐懼。警告世人。