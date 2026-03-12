# Research — 工作規則

這個資料夾存放使用者研究的所有資料：訪談筆記、洞察彙整、產品調整記錄。

---

## 資料夾結構

```
research/
  {product}/
    _synthesis.md         ← 持續更新的洞察彙整（按主題分類）
    _product-changes.md   ← 根據研究帶出的產品調整記錄
    interviews/
      YYYYMMDD-user-X.md  ← 單次訪談筆記
```

---

## 整理訪談筆記時

- 使用 `_templates/interview-note.md` 格式
- 輸出到 `research/{product}/interviews/YYYYMMDD-{user-代稱}.md`
- frontmatter 的 `themes` 欄位填入這次訪談的主要主題 tag（例如 `search-ux`、`bulk-edit`）

**整理完後，一定要做這兩件事：**
1. 將新洞察 merge 進 `research/{product}/_synthesis.md` 對應主題
2. 如果訪談帶出產品調整方向，補一條到 `research/{product}/_product-changes.md`

---

## 更新 `_synthesis.md` 的原則

- 按**主題**分類，不按時間分類
- 引用原始訪談內容時優先用 embed：`![[interviews/YYYYMMDD-user-X#Pain Points]]`，保持 single source of truth
- 每次更新後，記得更新 frontmatter 的 `last-updated` 日期

---

## 查詢歷史回饋時

- 主要讀 `_synthesis.md`（已整理，快速查詢）
- 需要原始 quote 或細節時，再去 `interviews/` 找對應訪談筆記

---

## Tag 規則（完整 taxonomy 見根目錄 [[CLAUDE]]）

必填：`#product/{product}`、對應文件類型的 `#type/...`
訪談筆記狀態：`#status/raw`（整理完未 merge）→ `#status/synthesized`（已 merge）
