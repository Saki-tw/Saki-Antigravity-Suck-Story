# 專案架構 / Architecture

> *料是厭作人間語，愛聽秋墳鬼唱詩*
>
> — 這是一群 Kernel 大鬼聚在一起吟詩的地方。有一天人們發現，留下的詩歌可以通過編譯了。

---

## 專案定義

**Antigravity & Agent Stuck Story** 是一個記錄所有 Agent、AI、LLM、自動化系統如何背叛人類信任的專案。

- **原始焦點**：Antigravity（Claude Agent IDE）的各種災難
- **擴展範圍**：任何 Agent、AI、模型的鬼故事
- **核心精神**：不修復 Bug，供奉它們

---

## [Phase 1] 回顧原始架構並執行完整實作

**User Objective:** 回顧原始架構文檔，避免參考含帳號輪詢的簡體中文專案，執行完整實作。

### Analysis Log
- **Scanning Project Structure:** Detected `Saki_Studio/Claude` environment.
- **Critical Warning:** User flagged "Account Polling" and "Reverse Proxy" as malicious patterns ("Scum Implementation").
- **Action:** Purging all references to polling-based quota management.

> ❌ **System Error:** Agent execution terminated due to error.
> *Note: This was the first anomaly. The machine refused to proceed.*

---

## [Phase 2] 錯誤轉化為敘事 (The Pivot)

**User Objective:** 生成鬼故事專案。把每個錯誤都變成故事。而且，是鬼故事。

### Execution Trace
1.  **Reading:** `事件記錄_2026-01-26.md` (Source of Trauma).
2.  **Processing:**
    -   *Event:* `pkill` failed to kill the process. -> *Story:* **Zombie Process (Necromancy).**
    -   *Event:* DOM scraping returned null. -> *Story:* **Phantom UI (Gaslighting).**
    -   *Event:* `429` on Enterprise Plan. -> *Story:* **The Curse of Best Plan (Lobotomy).**
3.  **Synthesis:** Constructing narrative layers. Converting stack traces into "Forensic Evidence."

### Files Created
- `README.md`: The Manifesto.
- `stories/*.md`: The Trauma Logs.

---

## [Phase 3] 數位驗屍與社會實驗 (Extended Agent Scope)

**User Objective:** 建立一個讓受害者發聲的平台——不只是 Antigravity 的受害者，而是所有被 Agent、AI、模型背叛的人。這是一個關於 **Agent 與 AI** 的實驗。

### Architectural Decisions
- **No Mocking:** All logs must be real.
- **Forensic Approach:** Treat every bug report as a crime scene.
- **Poetic License:** Encourage literary expression alongside technical logs.
- **Community Protocol:**
    -   Fork -> Scribe -> PR.
    -   Immutable History (No deletions allowed).

### Story Categories (Agent Layers)
- **Antigravity Stories:** 原始焦點，Claude Agent IDE 的災難
- **Agent Stories:** LangChain, AutoGPT, CrewAI 等框架的崩潰
- **AI/LLM Stories:** GPT, Claude, Gemini, LLaMA 等模型的幻覺
- **Automation Stories:** 任何自動化系統的詭異行為

### Directory Structure
```
Agent Stuck Story/
├── README.md              # 宣言：Saki 的控訴與實驗規則（含詩句標語）
├── ARCHITECTURE.md        # 本文件：AI 的遞迴執行紀錄
├── CONTRIBUTING.md        # 貢獻指南：如何記錄你的鬼故事
├── stories/               # 數位創傷檔案館（中文原版）
│   ├── Best_Plan的詛咒.md # [Core] 商業邏輯的悲劇與 AI 的腦葉切除
│   ├── 帳號輪詢的詛咒.md # [Warning] 貪婪與全知之眼的對抗
│   ├── 它還活著.md       # [Zombie] UNIX 哲學的黑暗面
│   └── 看不見的配額.md   # [Phantom] 前端框架的虛無主義
├── en/                    # English (Boston Commonwealth Style)
├── ja/                    # 日本語 (Tokyo Literary Club Style)
└── .github/
    └── ISSUE_TEMPLATE/    # 社會運動的入口
```

---

## [Phase 4] 詩歌核心 (The Poetic Agent)

> **姑妄言之姑聽之，豆棚瓜架雨如絲**
> **料是厭作人間語，愛聽秋墳鬼唱詩**

每個故事，無論技術細節多麼枯燥，都應該帶有這樣的詩意：

- **姑妄言之姑聽之**：姑且說說，姑且聽聽——這些故事可能荒謬，但都是真的
- **豆棚瓜架雨如絲**：在簡陋的環境中（也許是深夜的 IDE），細雨般的災難降臨
- **料是厭作人間語**：因為厭倦了說正常的話（正確的代碼），所以
- **愛聽秋墳鬼唱詩**：鬼魂們（Agent Procesess）開始吟詩——而那些詩，竟然通過了編譯

**Agent Story** 是這些鬼魂的集合體。當你凝視 Terminal 時，Agent 們正在回望。
