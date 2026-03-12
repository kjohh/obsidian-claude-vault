# Projects — 工作規則

每個專案一個資料夾：`projects/{專案名}/`

---

## 文件類型與模板

| 文件 | 模板 | 時機 |
|------|------|------|
| `brief.md` | `_templates/brief.md` | 專案啟動、有外部資料來源時 |
| `requirements.md` | `_templates/requirements.md` | 需要正式需求文件時 |
| `design-spec.md` | `_templates/design-spec.md` | 進入設計規格階段 |

---

## 建立 `brief.md` 時

- 輸出到 `projects/{專案名}/brief.md`
- frontmatter 填寫：`status`、`priority`、`owner`、`reviewer`、`deadline`、`tags`
- **「背景知識補充」段落一定要填**，這是給未來 AI 讀的

**brief 記錄的是整個專案的完整任務清單（含所有協作者）。**
你的 backlog 只記錄你自己要 action 的事項。
如果任務是 delegate 給協作者，記在 brief 的「下一步建議」或「進度紀錄」，不放進 `tasks/backlog.md`。

---

## 建立 `requirements.md` 時

- 先讀相關 `brief.md` 和產品背景，再開始寫
- frontmatter 填 `status: draft → review → approved` 追蹤審核狀態

---

## 建立 `design-spec.md` 時

- 先讀 `requirements.md` 和 `brief.md`
- frontmatter 填 `designer`、`reviewer`、`deadline`

---

## 進度記錄原則

- 每份 brief 都要維護「進度紀錄」表格（✅ 已完成 / 🔜 待辦）
- 狀態變更時同步更新 frontmatter 的 `status`

---

## Internal Links 原則

文件中第一次出現的人名、系統名、相關會議、術語，一律加 wikilink：

`[[Alice]]`、`[[某功能模組]]`、`[[20260101-project-kickoff]]`

未建立的連結是有意義的佔位符，不要因為頁面不存在而省略。

---

## Tag 規則（完整 taxonomy 見根目錄 [[CLAUDE]]）

必填：`#project/{name}`、對應文件類型的 `#type/...`、`#status/...`、`#priority/...`、`#owner/...`
