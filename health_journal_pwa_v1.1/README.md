# ❤️ 健康日誌 PWA v1.1

這是一套無伺服器的個人健康紀錄 App。資料使用 `localStorage` 保存在當前裝置、當前網站來源的瀏覽器空間。沒有雲端同步、分析腳本或第三方資源。

## GitHub Pages 部署

1. 在 GitHub 建立 **Public** repository，例如 `health-journal`（不要放入個人醫療紀錄、CSV、JSON 備份）。
2. 上傳本資料夾內的 `index.html`、`manifest.webmanifest`、`sw.js`、`icon-192.png`、`icon-512.png` 到 repository 根目錄。
3. Repository → Settings → Pages → Build and deployment → Deploy from a branch → `main` → `/(root)` → Save。
4. 等 GitHub 顯示已發佈，手機 Chrome 開啟 Pages 網址，選單 → **安裝應用程式** 或 **新增至主畫面**。

網站原始碼及網址是公開的，但資料不會自動上傳到 GitHub。若清除網站資料或解除安裝，紀錄可能會消失。**每週匯出 JSON 備份。**

## 測試

PWA 安裝與 service worker 須透過 HTTPS 或 localhost 運作；直接開 `file://` 可看頁面，但無法安裝成完整 PWA。發布後請先試存一筆測試資料，再測試 CSV、JSON 匯出與 JSON 還原。
