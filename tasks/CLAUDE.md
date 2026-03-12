# Tasks — 工作規則

---

## 重要前提：backlog 是你的個人待辦

**只放你自己需要 action 的事項。**
協作者的具體執行任務不放這裡，記在對應 `projects/{專案}/brief.md` 的「進度紀錄」或「下一步建議」。
你在 delegate 出去的任務上要做的事（例如 review、給 feedback），才放進 backlog。

---

## 整理 Backlog 時

**任務格式：**
```
- [ ] 任務描述 — due 日期 — [[來源連結]]
```

**Waiting / Blocked 標記：**
任務卡在等別人時，在該 section 的說明 blockquote 加上：
```
> ⏳ Waiting: 等誰做什麼
```

**Section 標頭格式：**
```
## {Project 名稱} — Priority: urgent / high / middle / low
```
- 可加補充說明，例如：`> @Alice 主要負責；你的角色 = Review`
- 不屬於特定專案的零散任務一律放在 `## Others`

**Sequential 任務（連環步驟）：**
只放「當前可執行的 next action」在 backlog；後續需要等前一步完成才能做的步驟，放到 `projects/{專案}/brief.md`。backlog 是「現在可以做的清單」，不是完整計畫。

**完成任務：**
- 移到 `## 完成` 區塊，加上完成日期：`— ✓ YYYY-MM-DD`
- 不要直接刪除任何任務

**若有連接 Slack：**
- 掃描過去 3 天的 DM，讀完整對話，不只看 from:me
- 對方最後一則有未回答的問題或請求 → action
- 你的最後一則含行動語意（「我去試試」「再確認」「朝這個方向做」等）→ action
- 雙方都已收尾（「好」「謝謝」「沒問題」）且無未完成承諾 → 不需 action

---

## 準備每日待辦時

1. 若有連接 Google Calendar，先查看當天行程，了解今天的空檔與會議負擔
2. 讀取 `tasks/backlog.md`，依 **Project Priority + 截止日期** 排序，找出：
   - 🔴 今天到期或已逾期的任務
   - 🟡 未來 3 天內到期的任務
   - 🟢 其他進行中但無緊迫截止的任務
3. 結合行事曆空檔，評估今天實際可執行的任務
4. **只在對話裡輸出**，不存檔，格式簡潔，不超過 10 項

---

## 準備週會更新時

- 讀取 `tasks/backlog.md` 的 `## 完成` 區塊，篩選上週日期的項目作為 Last Week
- 讀取各 project 的待辦，整理本週計畫作為 This Week
- 輸出到 `tasks/weekly-log.md`，最新一週置頂
- 格式依 Project 分類，對應週會投影片的 Last Week / This Week 兩欄
