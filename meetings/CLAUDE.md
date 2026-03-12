# Meetings — 工作規則

---

## 資料夾結構

```
meetings/
  transcripts/   ← 原始逐字稿（.txt，不修改）
  notes/         ← 整理後的會議筆記（.md）
```

---

## 整理會議記錄時

- 使用 `_templates/meeting-note.md` 格式
- 輸出到 `meetings/notes/`，檔名格式：`YYYYMMDD-{主題簡述}.md`
- frontmatter 填寫：`date`、`project`、`participants`、`tags`

**「背景知識補充」段落一定要填**，這是給未來 AI 讀的，解釋術語、人物、系統背景。

**從會議提取的待辦事項，同步更新 `tasks/backlog.md`。**
- 只把你自己需要 action 的任務放進 backlog
- 其他人的任務記在會議筆記的「待辦事項」區塊即可

---

## 使用 Callout 的規則

| Callout 類型 | 用途 |
|---|---|
| `> [!success]` | 確認的決議 |
| `> [!todo]` | 待辦事項（同步到 backlog 的） |
| `> [!question]` | 遞延議題、尚未確認的問題 |
| `> [!info]` | 背景知識補充 |
| `> [!warning]` | 風險、阻礙、需要注意的事 |

---

## Internal Links 原則

第一次出現人名、系統名、術語時，一律加 wikilink，即使頁面尚未建立也沒關係：

`[[Alice]]`、`[[某功能模組]]`、`[[20260101-project-kickoff]]`

未建立的連結是有意義的佔位符（breadcrumbs），之後補建頁面就能串起關聯。不要為了「頁面不存在」而省略連結。

---

## Tag 規則（完整 taxonomy 見根目錄 [[CLAUDE]]）

必填：`#type/meeting`、`#project/{name}`
會議筆記整理完成後加：`#status/done`
