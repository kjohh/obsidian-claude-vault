---
date: 2026-02-15
type: interview
product: flowly
interviewee: Sarah
role: Operations Manager
company: Mid-size logistics company（匿名）
themes: [search-ux, navigation, daily-workflow]
tags: [product/flowly, type/interview, status/synthesized]
status: synthesized
---

# 20260215 — Flowly 使用者訪談：Sarah

**受訪者**：Operations Manager @ 物流公司（100-200 人規模）（匿名代稱：Sarah）
**訪談時長**：45 分鐘
**原始逐字稿**：[[meetings/transcripts/20260215-user-sarah.txt]]
**主要主題**：search-ux、navigation

---

## 受訪者背景

Sarah 是一家中型物流公司的運營主管，團隊約 15 人。使用 Flowly 約一年，主要用來管理跨部門的 SOP workflow。每天使用頻率高，早上會先看 dashboard，下午會重複搜尋特定 workflow 確認各部門進度。

---

## 主要發現

### 搜尋行為

Sarah 平均每天搜尋 8-10 次，但成功率不高。她說自己養成了一個習慣：每個重要 workflow 都會把連結存在 Notion 頁面，因為「用 Flowly 搜很難找到」。

> [!quote] 代表性 Quote
> "我知道那個 workflow 叫什麼，但我就是打了第一個字之後什麼都找不到。然後我就直接去問同事。這很浪費時間。"

### 結果混亂問題

她說搜尋結果同時出現 workflow、template、同事名字，讓她不知道要點哪個。特別是她不知道 Template 和 Workflow 的差別（在她的認知裡是同一件事）。

> [!quote] 代表性 Quote
> "為什麼搜尋一個流程，會跑出一堆人名？我根本不是要找人。"

---

## Pain Points

> [!warning] 痛點清單
> - **搜尋容錯率低**：打錯一個字母就找不到，必須記住完整名稱
> - **結果沒有分類**：不同類型的結果混在一起，認知負擔重
> - **沒有搜尋歷史**：每次都要重新輸入，重複搜尋效率很低

---

## 正面回饋

- 喜歡 workflow 的執行介面，說「跑起來很順」
- Dashboard 的今日概覽對她很有用，每天必看

---

## Feature Requests / 期望

- 希望可以用 `Cmd+K` 全域搜尋，不用先點搜尋框
- 希望搜尋結果可以只看 workflow，不要混其他類型

---

## 設計啟發

> [!tip] 對設計的影響
> - 模糊搜尋是最高優先，Sarah 的痛點完全在這
> - 結果分類是第二優先，且要讓使用者能快速切換只看某個類型
> - `Cmd+K` 全域搜尋的需求真實存在，值得評估要不要提前做
> - **Template vs Workflow 的命名混淆**是另一個問題，可能需要單獨的 research

---

## 待追蹤

> [!todo] 後續行動
> - [x] 更新 [[research/_example-product/_synthesis]] — search-ux 主題
> - [ ] 把 Template/Workflow 命名混淆的問題記錄到 open questions
