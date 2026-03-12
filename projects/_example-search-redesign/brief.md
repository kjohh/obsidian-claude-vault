---
title: Search Redesign
type: brief
project: search-redesign
status: in-progress
priority: high
owner: amy
reviewer: ben
deadline: 2026-03-15
tags: [project/search-redesign, type/brief, status/in-progress, priority/high, owner/amy]
---

# Search Redesign — 專案簡報

**資料來源**：
- [[meetings/notes/_example-20260210-search-redesign-kickoff]]
- [[research/_example-product/_synthesis]]

**下一個里程碑**：2026-02-28 — 完成 wireframe，準備 design review

---

## 一句話說清楚

> 讓 Flowly 使用者能快速找到他們需要的 workflow，不再因為搜尋失敗而卡住工作。

---

## 背景與動機

使用者訪談和客服資料都顯示，「找不到東西」是 Flowly 排名第二的使用者痛點（第一是「設定太複雜」）。
目前的搜尋只做完整字串匹配，使用者需要記住確切名稱才能搜到；加上結果沒有分類，搜一個字可能同時出現 workflow、template、team member，很難判斷。

競品 Notion、Linear 的搜尋體驗都明顯比我們好，已經有使用者在 review 上提到這個差距。

---

## 使用者情境

Sarah 是一位運營主管，每天要在 Flowly 裡找不同部門的 workflow 來確認進度。她通常記得 workflow 的大概名字，但不一定記得完整名稱。現在她每次搜尋都要試好幾次，找不到就直接叫同事傳連結。

---

## 功能範圍

**In Scope（Phase 1）：**
- 模糊搜尋（fuzzy match，容許拼字誤差）
- 搜尋結果依類型分組（Workflows / Templates / People）
- 搜尋歷史（最近 10 筆）

**Out of Scope（Phase 2）：**
- 進階篩選（by status、by owner、by date）
- Operator 語法（`status:active`）
- 跨欄位搜尋（搜尋 workflow 內的 task 名稱）

---

## 設計含義（Design Implications）

- 搜尋框的觸發方式：目前是點 icon，要不要改成 `Cmd+K` 全域呼叫？
- 結果分組後的視覺層級怎麼處理？不能讓三個群組看起來同等重要
- 搜尋歷史的隱私問題：多人共用帳號時，歷史要不要分 user？

---

## 進度紀錄

| 日期 | 狀態 | 說明 |
|------|------|------|
| 2026-02-10 | ✅ 完成 | Kickoff 會議 |
| 2026-02-17 | ✅ 完成 | 競品分析完成 |
| 2026-02-20 | 🔜 待辦 | 使用者訪談（3 人） |
| 2026-02-28 | 🔜 待辦 | Wireframe + Design Review |

---

## 開放問題（Open Questions）

> [!question] 待確認
> - [ ] `Cmd+K` 全域搜尋是否在 Phase 1 一起做？還是維持原有入口？
> - [ ] 搜尋歷史是 per-user 還是 per-browser？需要工程確認技術方案

---

## 背景知識補充

> [!info] 給未來 AI 讀的
> - **Flowly**：幫運營團隊管理工作流程的 SaaS
> - **Workflow**：Flowly 的核心物件，類似一個可執行的標準作業流程
> - **Template**：workflow 的預設版本，使用者可以 clone 後修改
> - **Amy**：負責這個專案的 Designer；**Ben**：PM；**Claire**：前端工程師
> - Phase 1 = 最小可用版本，預計 2026-03-15 上線
