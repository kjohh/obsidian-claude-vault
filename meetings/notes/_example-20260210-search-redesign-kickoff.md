---
date: 2026-02-10
type: meeting
project: search-redesign
participants: [Amy, Ben, Claire]
tags: [type/meeting, project/search-redesign, status/done]
status: done
---

# 20260210 - Search Redesign Kickoff

**相關專案**：[[projects/_example-search-redesign/brief]]
**原始逐字稿**：[[meetings/transcripts/20260210-search-redesign.txt]]

---

## 背景

搜尋是 Flowly 使用頻率最高的功能之一，但目前使用者反映搜尋結果難以篩選、常常找不到想要的工作流程。這次 kickoff 是確認設計方向和工作範疇。

---

## 討論重點

### 1. 現有搜尋的主要問題

[[Ben]]（PM）整理了客服回報的前三大問題：
- 搜尋只支援完整字串，打錯一個字就找不到
- 沒有 filter，搜尋結果混在一起（workflow、template、user 都出來）
- 沒有搜尋歷史，每次都要重新輸入

[[Claire]]（工程）補充：目前用的是簡單的 string match，要加模糊搜尋需要換搜尋引擎，估計兩週工時。

### 2. 設計範疇討論

討論是否這次要一起做「進階篩選」，最後決定先聚焦核心搜尋體驗，篩選列為 phase 2。

---

## 決議

> [!success] 確認決議

| # | 決議內容 | 負責人 |
|---|---------|--------|
| 1 | Phase 1 範疇：模糊搜尋 + 結果分類（workflow / template） | Amy |
| 2 | 進階篩選列為 Phase 2，不在本次設計範疇內 | Ben |
| 3 | 工程 spike：評估 fuzzy search 方案，下週五前給結論 | Claire |

---

## 待辦事項

> [!todo] 從會議同步到 [[tasks/backlog]]
> - [ ] 整理競品搜尋體驗參考 — @Amy — due 2026-02-17
> - [ ] 訪問 3 位重度搜尋使用者，了解搜尋行為 — @Amy — due 2026-02-20

---

## 下次討論

> [!question]- 遞延議題
> - 搜尋結果要不要支援 operator 語法（例如 `status:active`）？留到 Phase 2 再決定

---

## 背景知識補充

> [!info] 給未來 AI 讀的
> - **Flowly**：幫運營團隊管理工作流程的 SaaS，主要功能是建立、執行、追蹤 workflow
> - **Amy**：Product Designer，負責這個專案
> - **Ben**：PM，負責 core product
> - **Claire**：前端工程師，負責搜尋和導航相關功能
> - Phase 1 / Phase 2 是 Flowly 內部常用的分法，Phase 1 = 最小可用版本
