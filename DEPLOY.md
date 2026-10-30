# 部署／更新 Runbook｜hk-mh-public

公開站：https://ycsoeric.github.io/hk-mh-public/  
Repo：https://github.com/ycsoeric/hk-mh-public  
本機工作副本：`/workspace/hk-mh-public-site/`（純檔案，無 `.git`）

## 現況（已核實）

- GitHub Pages：**Deploy from a branch** → `main` / `/ (root)`
- 系統 workflow：`pages-build-deployment`（active）
- 內容：純靜態 HTML／CSS；無 build、無表單、無 JS 對外請求
- **安全邊界**：公開端不連內部監察庫（`hk-mh-crisis-monitor`）、不載個案／識別資料
- **對外命名**：站上與 README 用中性名稱「香港精神健康求助資源」；唔用內部服務品牌

## 日常更新（建議流程）

1. 在本機副本改檔：`/workspace/hk-mh-public-site/`（或前端同事交付的同等檔）。
2. **發佈前檢查**
   - 無個案、姓名、地址、新聞事故細節
   - 無連到內部 DB／內部網址／API
   - 熱線號碼以機構最新公佈為準
   - 品牌掃描通過（見下）
3. 將改動推上 `ycsoeric/hk-mh-public` 的 `main` 根目錄（只推可公開檔；勿加敏感／內部備忘）。
4. 等 Pages 建置完成（通常 1–3 分鐘），開公開 URL 抽查首頁／熱線／關於／免責。
5. 本機副本與 remote 用檔案 hash 對齊後才算完成。

### 用 Cursor／助手推送時

- 任何 repo 內容變更經 cloud agent／授權流程；未准唔實作。
- 本機目錄無 git：推送前需暫用授權方式同步到 GitHub（勿把內部監察庫路徑一併提交）。

## 首次／設定核對

Settings → Pages → Source = Deploy from a branch；Branch = `main`；Folder = `/ (root)`。  
自訂 domain 暫無；路徑前綴為 `/hk-mh-public/`（相對連結請保持相對路徑）。

## 回滾

`git revert` 最近 commit 或還原上一版檔案後再推 `main`；Pages 會再部署。

## 唔好做

- 唔好把 `hk-mh-crisis-monitor`、SQLite、個案 CSV／digest 放入本 repo
- 唔好在公開站加會收集個案內容的表單（見免責頁）
- 唔好開需要讀內部庫的 API
- 唔好把 `report-to-manager-*.md` 等內部備忘推上公開 repo

## 發佈前品牌掃描（必做）

推 `main` 前對**將上架**的公開檔確認：title、brand、footer、README、本 runbook 均為中性名稱，**唔出現內部服務品牌字樣**（含粵語全稱同英文 Family Joy 相關字串）。可用本機搜尋再人工確認。

## Repo metadata（推送時一併改）

- Description：`香港精神健康求助資源`
- Homepage：`https://ycsoeric.github.io/hk-mh-public/`
