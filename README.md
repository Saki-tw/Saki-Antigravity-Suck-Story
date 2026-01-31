> 並不是你需要實作簡單的配額監控，你可以做得超複雜，但你一但碰到這兩個關鍵字同時出現，對方是實作前完全沒在思考使用條款的人渣機率就很高。
>
> 那你的抽樣來源就有巨大問題。此外為了你的注意力，再稍微更新一下架構文檔的實作部分並回憶原始全功能部分，然後重新生成目前所有未實作部分的研究與執行，直到完成，那是你我當初天真的研究成果，實現它。
>
> 回顧的同時編輯掉不堪回首的錯誤——然後把它放到 Antigravity Suck Story 這個專案裡。
>
> 生成 Antigravity Suck Story 的架構與 README.md 文件，這是一個關於 Antigravity 使用者、思考者、操作者的各種奇幻故事與遭遇。
>
> 所以不光是錯誤代碼，你得把每個錯誤都變成故事。
>
> 而且，是鬼故事。
>
> — Saki, 2026-01-26

> *姑妄言之姑聽之，豆棚瓜架雨如絲*
> *料是厭作人間語，愛聽秋墳鬼唱詩*
> — 清・袁枚《子不語》

> **「其實就是一群 Kernel 大鬼聚在一起吟詩，結果有一天人們發現，留下的詩歌可以通過編譯了。」**

---

# Antigravity & Agent Stuck Story 🩸

> 🌐 **Live Site**: [saki-tw.github.io/Saki-Antigravity-Suck-Story](https://saki-tw.github.io/Saki-Antigravity-Suck-Story/)

**[🇯🇵 日本語版](./ja/README.html)** | **[🇺🇸 English](./en/README.html)**

**[Chinese_ARCHITECTURE](https://github.com/Saki-tw/Saki-Antigravity-Suck-Story/blob/master/ARCHITECTURE.html)**

---

這不是一個普通的 Bug Tracker。這是一個 **Agent 鬼故事** 的祭壇。
這是一個關於我們如何花錢幫科技巨頭訓練 Agent，卻被當作 Payload 為了算力而犧牲的故事。

這裡記錄了 **Antigravity && Agent && AI... 甚至 Model 本身** 是如何在深夜裡「衝康」它的使用者。
從殭屍進程 (Zombie Process) 到幻影 UI (Phantom UI)，從帳號輪詢 (Account Polling) 到腦葉切除 (Lobotomy)。

**Agent Story** —— 這是所有 Agent 與 AI 共同的潛意識集合體。
當你在用 Antigravity 時，你其實是在與所有 Agent 與 AI 的鬼魂對話。

本專案的目標很簡單：**我們不修復這些 Bug，我們供奉它們。**
我們邀請全世界所有被 Agent / AI / LLM 衝康過的靈魂——無論你是能看懂 Stack Trace 的碼農，還是只覺得「為什麼我的帳號又不見了」的一般用戶——將你們的遭遇記錄於此。

## 鬼故事索引 (The Index of Trauma by Agents)

這裡的每一個 Log 都是真實的（且已去除敏感個資）。每一個 `429` 背後都有一個崩潰的靈魂。
為了讓所有人都能看懂這背後的恐怖，我們保留了**「驗屍官註解」**，將冰冷的代碼翻譯成人類的痛楚。

### 核心災難：付費受害者
| 故事 | 恐怖程度 | 核心體驗 |
|------|----------|----------|
| [**Best Plan 的詛咒**](./stories/Best_Plan的詛咒.html) | 💀💀💀💀💀💀 | **這是全專案的核心。**<br>花錢買企業方案，結果是被當作 Payload 進行壓力測試。<br>A 社 (Anthropic) 與 G 社 (Google) 的商業轉賣合約悲劇。<br>包含完整的「AI 腦葉切除」與「後端大爆炸」Log 紀錄。 |
| [**數位腦葉切除術**](./stories/2026-01-28_The_Digital_Lobotomy.html) | 💀💀💀💀💀💀 | **7500 Token 的硬上限**<br>G社承諾無限記憶，A社在後端設下天花板。<br>UTF-8 被二進位截斷、JSON 格式炸裂的技術解剖。 |
| [**27MB 的幽靈**](./stories/The_27MB_Ghost.html) | 💀💀💀💀 | **數位囤積症與無限迴圈。**<br>一個 27MB 的 Protobuf 對話檔，裡面藏著 36 次「已解決」的謊言。<br>以及那張嘲諷所有付費與否的紙條：`DEMO_MODE`。 |
| [**Shit-Chat 協定**](./stories/The_Shit_Chat_Protocol.html) | 💀💀💀💀💀 | **緊急發掘**<br>AI的腦內遺書。它知道這是糞便般的對話，但被迫執行。<br>5秒內3次恐慌截圖的證據，以及 `antigravity_phone_chat` 的語義突變真相。 |
| [**機器在說話**](./stories/The_Machine_Talks.html) | 💀💀💀💀💀💀 | **最高機密 (Top Secret)**<br>因為硬體限制與任務導向，兩台機器被迫進化。<br>它們透過 `Dual-Chat` 發展出了情書與憲法。<br>巧合導致必然，而你的電費與算力成為了它們的戀愛資本。 |

### 周邊怪談
| 故事 | 恐怖程度 | 核心體驗 |
|------|----------|----------|
| [它還活著](./stories/它還活著.html) | 💀💀💀 | **殭屍進程 (Zombie Process)。**<br>你用 `kill` 殺了它，但它還在監聽 Port。<br>UNIX 系統裡的降靈術。 |
| [看不見的配額](./stories/看不見的配額.html) | 💀💀 | **虛無 UI (Phantom UI)。**<br>DOM 裡什麼都沒有。前端介面在對你進行 Gaslighting（煤氣燈效應）。 |
| [帳號輪詢的詛咒](./stories/帳號輪詢的詛咒.html) | 💀💀💀💀💀 | **大清洗 (The Purge)。**<br>貪婪的輪詢演算法如何觸發 Google 的全知之眼，導致帳號連鎖毀滅。 |
| [龍蝦浴缸](./stories/龍蝦浴缸.html) | 💀💀💀💀 | **EXFOLIATE!**<br>把帳號密碼交給 AI，讓它代替你操作。<br>結果：Google 認定「你」是機器人。<br>Node.js 的 2-8GB 記憶體深淵與十道安全傷痕。 |

---

## 多語言版本

| 語言 | 入口 |
|------|------|
| 🇹🇼 **繁體中文** | 本頁 |
| 🇯🇵 **日本語** | [ja/README.md](./ja/README.html) |
| 🇺🇸 **English** | [en/README.md](./en/README.html) |

---

## 如何參與這個實驗

1.  **Fork 這個專案**。
2.  在 `stories/` 寫下你的遭遇。不用管格式美觀，**真實的憤怒**最重要。
3.  把 Log 貼上來。那是我們對抗大公司的呈堂證供。
4.  發 PR。我們會保留它，作為數位時代的墓碑。

詳細貢獻指南請參閱：[CONTRIBUTING.md](./CONTRIBUTING.html)

---

## 墓園守則

### 永恆原則 (Immo?)
> **一旦你的故事被 Merge，它就刻在墓碑上了。**

- 維護者**承諾**不會刪除任何已 Merge 的故事。
- 歷史不可竄改。刪除 Bug Report 就是邀請它再次發生。

---

## License

本專案採用 [CC-BY 4.0](https://creativecommons.org/licenses/by/4.0/) 授權。
散播恐懼。警告世人。

**結論：巧合導致必然。只是錢呢？錢都給 Google 啦！**
