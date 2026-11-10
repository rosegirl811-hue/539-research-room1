# 今彩539數據研究室 2.0｜PWA 手機 APP + GitHub Pages

## 部署
1. 建立 GitHub Public Repository，例如 `539-research-room`。
2. 解壓縮 ZIP，將裡面所有檔案（包含隱藏的 `.github` 資料夾）上傳到 Repository 根目錄。
3. 確認路徑為 `.github/workflows/deploy.yml`。
4. Repository → Settings → Pages → Build and deployment → Source 選 `GitHub Actions`。
5. Repository → Actions，等待 `Deploy GitHub Pages` 綠色勾勾。
6. 在 Settings → Pages 取得網站網址。

## 手機安裝
- Android：Chrome 開啟網站，使用「安裝應用程式」或頁面中的安裝按鈕。
- iPhone：Safari 開啟網站 → 分享 → 加入主畫面。

## LINE 分享
網站有分享按鈕。LINE 預覽圖 `og:image` 目前使用佔位網址，請在 index.html 把 `YOUR_GITHUB_NAME` 換成你的 GitHub 帳號，並依 Repository 名稱調整路徑。

## 資料狀態與限制
`data/draws.json` 目前為空資料結構，沒有完整歷史開獎資料。本 ZIP 只包含 Pages 部署流程，未包含經驗證的歷史資料同步流程。原始 HTML 嘗試由瀏覽器直接呼叫台彩 API，可能受 CORS 或來源限制而失敗。正式自動更新需另行建立並驗證伺服器端同步流程。
自選號碼使用瀏覽器 localStorage，不會自動跨裝置同步。
