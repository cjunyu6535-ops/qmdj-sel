# 奇門遁甲SEL版 v1.05 (`qmdj-sel`)

結合東方「奇門遁甲（QMDJ）」時空策略學與西方「CASEL 社會情緒學習（SEL）」心理學的跨平台 AI Skill。透過內建**免代碼三步查表排盤矩陣**與**多維心理符號知識庫**，將傳統命理符號轉譯為直觀的「情緒氣象圖」與現代心理調節策略，完全不依賴外部 Python 腳本即可精準推演。

支援 **ChatGPT Codex CLI、Claude Code、OpenCode、Gemini CLI** 及 **Gemini 網頁版／App**。

## 核心特色

* **四階段互動狀態機**：當提問過於簡略時，主動引導補齊事件脈絡、互動對象與時間錨點；資訊完整時則直接進入排盤分析。

* **時間錨定雙軌協定**：支援「當下共時分析」、「過去衝突覆盤」與「未來行動預演」。

* **免代碼三步查表排盤矩陣**：內建二十四節氣陰陽遁三元定局表、五鼠遁日上起時表、六十甲子旬首六儀表與洛書九宮星門神映射表，解決雲端與終端環境無法執行外部算盤腳本的幻覺問題。

* **非宿命論與 CASEL 賦能導航**：將傳統凶格（門迫、擊刑、伏吟、反吟、白虎等）轉化為心理成長挑戰，並匹配自我覺察、自我管理、社會覺察、人際技能與負責決策五大工具箱。

* **純繁體中文輸出**：結構化輸出「情緒氣象報告」、「深度心理診斷」與「CASEL 社會情緒導航」，不夾雜冗餘英文標題。

## 目錄結構

```
qmdj-sel/
├── README.md                                  # 本說明文件與跨平台安裝指南
└── qmdj-sel/                                  # 技能本體目錄（符合 Agent Skills 開放標準）
    ├── SKILL.md                               # 跨平台相容之技能主檔
    └── references/
        ├── qmdj_calculation_tables.md         # 免代碼三步查表排盤矩陣
        └── qmdj_sel_knowledge_base.md         # 奇門遁甲 × CASEL 多維心理知識庫

```

## 跨平台安裝方式

### 方式一：CLI 一鍵安裝（支援 Claude Code / Codex / OpenCode / Gemini CLI）

若本機已完成 GitHub CLI 或 Git 私人儲存庫認證，可直接透過 `npx skills` 安裝：

```
npx skills add https://github.com/cjunyu6535-ops/qmdj-sel --skill qmdj-sel

```

### 方式二：手動複製安裝（適用於各終端 AI 開發工具）

先將儲存庫複製（Clone）至本機：

```
git clone https://github.com/cjunyu6535-ops/qmdj-sel.git

```

接著將內部的 `qmdj-sel/` 資料夾複製到對應工具的技能目錄（**專案專用**請放於專案根目錄 `./`，**全域通用**請放於家目錄 `~/`）：

| 平台／工具 | 專案級路徑 | 全域級（個人）路徑 | 
| ----- | ----- | ----- | 
| **Claude Code** | `.claude/skills/qmdj-sel/` | `~/.claude/skills/qmdj-sel/` | 
| **ChatGPT Codex CLI** | `.agents/skills/qmdj-sel/` | `~/.codex/skills/qmdj-sel/` | 
| **OpenCode** | `.opencode/skills/qmdj-sel/` | `~/.config/opencode/skills/qmdj-sel/` | 
| **Gemini CLI** | `.gemini/skills/qmdj-sel/` | `~/.gemini/skills/qmdj-sel/` | 

> **提示**：Gemini CLI 亦支援使用內建 `gemini skills install` 指令從本機路徑匯入 `qmdj-sel/` 目錄。

### 方式三：其他 Gemini 帳號（網頁版／App Skills 管理介面）

1. 下載本儲存庫，將內部的 `qmdj-sel/` 資料夾單獨壓縮為 `qmdj-sel.zip`（請確認壓縮包解開後第一層即為 `SKILL.md` 與 `references/`）。

2. 登入目標 Gemini 帳號，開啟 **Skills 管理介面（Skills Manager）** → 點選「匯入／上傳技能（Upload Skill）」。

3. 上傳 `qmdj-sel.zip` 或選取 `qmdj-sel/` 資料夾，確認啟用即可。

## 觸發與使用範例

安裝啟用後，可直接使用自然語言觸發：

* **當下情緒健檢（共時性分析）**：「掐指一算成大師，我現在心裡好亂，不知道該不該接下這個新專案。」

* **過去事件覆盤**：「昨天下午 3 點我和老闆在會議上大吵一架，幫我用奇門遁甲覆盤當時為什麼會失控？」

* **未來行動預演**：「我明天早上 9 點要跟重要客戶談判，該怎麼調整心態與溝通策略？」

## 免責聲明

*本技能基於中國傳統預測學「奇門遁甲」與現代決策科學的邏輯和社會情緒教育（CASEL），僅供娛樂、文化探索與自我反思參考，不構成專業醫療、心理諮商或法律建議。*