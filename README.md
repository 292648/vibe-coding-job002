# 嘉訊知識圖譜 v2

115年1–9月內容，共整理為 **67 篇文章 JSON**。

## 主要功能
- 每篇文章各自一個 `articles/*.json`
- MiniSearch 全文搜尋（標題、作者、主題、全文）
- Cytoscape.js 互動知識圖譜
- 文章全文閱讀模式（舒適字級、行距、米白紙張背景）
- 每篇文章可產生獨立網址：`?article=文章ID`
- 每篇可直接開啟原始 PDF 對應頁面
- GitHub Pages 純靜態網站，不需資料庫

## GitHub Pages 部署
1. **先解壓縮 ZIP**
2. 將解壓縮後的所有內容（`index.html`、`11501-09.pdf`、`articles/`、`data/`）上傳到 GitHub Repository 根目錄。
3. Repository → Settings → Pages
4. Source 選 `Deploy from a branch`
5. Branch 選 `main`，資料夾選 `/ (root)`，Save。
6. 等待 GitHub Pages 完成部署。

> ZIP 只是方便把整個網站專案一次下載與搬運，GitHub Pages 本身不會直接執行 ZIP。

## 目錄
```
/
├─ index.html
├─ 11501-09.pdf
├─ data/
│  └─ manifest.json
└─ articles/
   ├─ p01-01.json
   ├─ p01-02.json
   └─ ...
```

## 新增文章
新增 `articles/*.json` 後，也要同步在 `data/manifest.json` 加一筆 metadata，MiniSearch 才會自動納入搜尋。
