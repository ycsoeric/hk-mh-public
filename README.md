# 香港精神健康求助資源

公開靜態網頁：求助熱線與資源簡介，以及危機相關公開新聞整理（日期／時間／類別／來源連結）。**不載個案細節、方式或識別資料。**

站點：https://ycsoeric.github.io/hk-mh-public/

## 內容

| 檔案 | 說明 |
|------|------|
| `index.html` | 首頁 |
| `hotlines.html` | 求助熱線一覽 |
| `news-overview.html` | 危機相關公開新聞整理（載入 feed 列表） |
| `about.html` | 關於本站 |
| `disclaimer.html` | 免責聲明 |
| `styles.css` | 共用樣式（流動版友善） |
| `public-news-feed.json` | 公開新聞來源列表（由數據隊維護） |
| `hotlines-public.json` 等 | 公開資源／統計 JSON |
| `assets/` | 插圖／圖示 |

## 啟用 GitHub Pages

1. 將本目錄**可公開**檔案推送到 repo `ycsoeric/hk-mh-public` 的預設分支（建議放在 repo **根目錄**）。
2. 於 GitHub：Settings → Pages → Source 選 **Deploy from a branch**。
3. Branch 選 `main`（或你的預設分支），資料夾選 `/ (root)`，儲存。
4. 稍候即可於 `https://ycsoeric.github.io/hk-mh-public/` 瀏覽。

無需建置步驟；純 HTML／CSS（新聞列表以輕量前端讀取 JSON）。

## 注意

- 緊急請撥 **999**。
- 熱線號碼以各機構最新公佈為準。
- 發佈前確認公開檔文案只用中性名稱，唔用內部服務品牌。
