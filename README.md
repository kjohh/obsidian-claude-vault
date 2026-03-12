# Obsidian × Claude Vault Template

一個讓 AI（Claude）真正能幫你工作的 Obsidian Vault 結構。

---

## 這是什麼

這個 repo 是一個 **Obsidian Vault 模板**，專為搭配 Claude（或其他 AI）做產品設計工作而設計。

核心概念很簡單：**用 `CLAUDE.md` 告訴 AI 在這個 Vault 裡應該怎麼工作**。每個資料夾有自己的規則，AI 進去之前會先讀，知道要做什麼、怎麼做、輸出到哪裡。

---

## 資料夾結構

```
vault/
  CLAUDE.md              ← AI 的全域行為指引（必讀）
  README.md

  meetings/
    CLAUDE.md            ← 整理會議記錄的規則
    notes/               ← 整理後的會議筆記
    transcripts/         ← 原始逐字稿（不修改）

  projects/
    CLAUDE.md            ← 建立專案文件的規則
    {project-name}/
      brief.md
      requirements.md
      design-spec.md

  research/
    CLAUDE.md            ← 整理使用者研究的規則
    {product}/
      _synthesis.md      ← 持續更新的洞察彙整
      _product-changes.md
      interviews/        ← 單次訪談筆記

  tasks/
    CLAUDE.md            ← 管理 backlog 的規則
    backlog.md
    weekly-log.md

  product/
    product-overview.md  ← 產品背景（給 AI 讀的）

  _templates/            ← 所有文件模板
```

---

## 核心設計原則

**1. CLAUDE.md 是 AI 的操作手冊**
每個資料夾放一個 `CLAUDE.md`，說明這個資料夾的用途、輸出規則、格式規範。AI 每次進來工作前先讀，不需要每次重複說明。

**2. 背景知識補充段落**
每份文件都有「給未來 AI 讀的」段落，記錄術語、人物、系統背景。讓不同時間點進來的 AI 都能快速上手，不需要重新解釋脈絡。

**3. Internal Links 作為 breadcrumbs**
第一次出現的人名、術語、系統名一律加 `[[wikilink]]`，即使頁面尚未建立也沒關係。未來補建頁面後，關聯自然串起。

**4. Single Source of Truth**
`_synthesis.md` 用 embed（`![[]]`）引用原始訪談內容，不複製貼上。更新原始資料，彙整自動同步。

**5. Backlog 只記錄「現在可以做的事」**
不是完整計畫，是可執行的 next action。Sequential 步驟的後段放在 `brief.md`，等前一步完成再搬出來。

---

## 如何使用

1. Clone 或 Download 這個 repo
2. 用 Obsidian 開啟資料夾（Open folder as vault）
3. 編輯根目錄的 `CLAUDE.md`，填入你的角色、產品、工作情境
4. 編輯 `product/product-overview.md`，填入你的產品背景
5. 把 `_templates/` 裡的模板設定為 Obsidian Templates 來源
6. 開始用 Claude Code（或任何支援讀取本地文件的 AI）在 vault 裡工作

---

## 工具建議

- **Obsidian**：主要編輯介面
- **Claude Code**（CLI）：在 terminal 裡直接操作 vault，讀文件、寫筆記、整理 backlog
- **Obsidian Bases**：用 frontmatter 做跨文件查詢（依 project、status、owner 篩選）

---

## Obsidian Plugins

這個工作流實際使用的 plugin 只有兩個，保持輕量：

- **[Git](https://github.com/Vinzent03/obsidian-git)**：自動備份 vault 到 GitHub，不需要手動 commit
- **[Tasks](https://github.com/obsidian-tasks-group/obsidian-tasks)**：在 Obsidian 裡查詢跨文件的 checkbox 任務（配合 backlog.md 使用）

**Claude 整合：**

- **[obsidian-markdown](https://github.com/anthropics/claude-code)**（Claude Code 官方）：讓 Claude 能直接讀取 vault 裡的 `.md` 文件。裝好後，Claude 的 AI Skills 也能在 Obsidian 裡直接使用。

---

## 參考與靈感

這個 vault 結構的設計參考了 Obsidian 創辦人 Steph Ango 的文章：

**[Vault — Steph Ango](https://stephango.com/vault)**

幾個共同的核心理念：

- **File-first**：一切都是普通的 `.md` 檔案，不依賴任何平台或工具的私有格式
- **Internal links 作為 breadcrumbs**：未建立的連結也有意義，是未來知識串聯的佔位符
- **一致的個人規則**：固定的 tag taxonomy、frontmatter 格式，減少每次決策的摩擦
- **模板驅動**：用模板統一文件結構，方便 AI 讀取和查詢

主要差異在於這個模板**以 AI 協作為核心設計目標**——`CLAUDE.md` 是這套系統的靈魂，讓 AI 能理解你的工作脈絡、按你的規則輸出文件。

---

## License

MIT — 自由使用、修改、分享。
