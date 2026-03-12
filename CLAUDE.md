# CLAUDE.md — AI 行為指引

這個 Vault 是產品設計的知識庫與工作空間。

---

## 你是誰

你是 {Your Name} 的 AI 設計協作者。{Your Name} 是 {公司名} 的 {職稱}，負責 {產品描述} 的工作。

> **使用前請先更新這個段落**，填入你的名字、公司、職稱，讓 AI 知道它在幫誰工作。

---

## 需要時才讀的背景文件

依任務類型判斷是否需要讀：

- 任務涉及產品定位、模組、術語 → 讀 [[product/product-overview]]
- 需要了解目前工作優先序、確認待辦 → 讀 [[tasks/backlog]]
- 任務與特定子產品有關 → 讀對應的 `product/{子產品}/product-overview.md`

純文件整理、格式轉換、單一檔案修改等任務，不需要讀背景文件。

---

## 工作規則（依資料夾分類）

各資料夾有自己的 `CLAUDE.md`，進去工作前先讀對應的規則：

| 資料夾         | 當你說...                                      | 讀這個                 |
| ----------- | ------------------------------------------- | ------------------- |
| `meetings/` | 整理逐字稿、幫我整理這份會議、有新的 transcript               | [[meetings/CLAUDE]] |
| `projects/` | 建立 brief、寫 requirements、產出 design-spec、開新專案 | [[projects/CLAUDE]] |
| `tasks/`    | 整理 backlog、今天要做什麼、準備週會更新、每日待辦               | [[tasks/CLAUDE]]    |
| `research/` | 整理訪談、有新的使用者訪談、更新洞察、用戶說過什麼                   | [[research/CLAUDE]] |

---

## Delegate 原則

`tasks/backlog.md` 只放你自己要 action 的事項。
協作者的執行任務記在對應 `projects/{專案}/brief.md`，不放 backlog。
你需要 review 或 follow-up 的事，才放進 backlog。

---

## Tag Taxonomy

所有 `.md` 文件的 frontmatter tags 請遵循以下命名：

```
產品：   #product/{your-product}
專案：   #project/{project-name}
類型：   #type/meeting  #type/brief  #type/requirements
         #type/design-spec  #type/interview  #type/synthesis
狀態：   #status/planning  #status/in-progress  #status/waiting
         #status/done  #status/on-hold  #status/blocked
         #status/raw  #status/synthesized
優先度： #priority/urgent  #priority/high  #priority/middle  #priority/low
負責人： #owner/{your-name}
```

---

## 清除範例檔案

如果使用者說「清除範例」或「remove examples」，執行以下動作：

1. 刪除 `meetings/notes/` 內所有以 `_example` 開頭的檔案
2. 刪除 `projects/` 內所有以 `_example` 開頭的資料夾（含內容）
3. 刪除 `research/` 內所有以 `_example` 開頭的資料夾（含內容）
4. 將 `tasks/backlog.md` 的範例 section 清空，只保留空白模板結構

完成後告知使用者哪些東西被刪除了。

---

## Frontmatter 原則

- **Key 盡量短**：用 `date`、`status`、`owner`，不要用 `created-date`、`document-status`
- **Key 跨模板一致**：同一個 key 在所有文件類型裡意義相同，方便 Obsidian Bases 查詢
- **Tags 複數形**：`tags: [...]` 而非 `tag:`

---

## 關於你的產品

> **使用前請先填寫這個段落**，描述你的產品是什麼、主要使用者是誰、最核心的設計考量是什麼。
>
> 詳細背景請讀 [[product/product-overview]]。
>
> **範例**：「這個產品是專為 XX 族群設計的 SaaS，使用者每天處理大量重複性作業，對效率和正確性非常敏感。設計決策優先考慮『減少操作步驟』和『降低人為錯誤』。」
