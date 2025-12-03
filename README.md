# Joy UI Messages 模板 (Vite + React + TypeScript)

這個專案將 [MUI Joy UI Messages 範例](https://github.com/mui/material-ui/tree/master/docs/data/joy/getting-started/templates/messages)
重新整理成可直接部署到 GitHub Pages 的 Vite 應用程式。版面、互動與配色均使用 Joy UI 元件實作，並移除所有二進位檔案。

## 開發與預覽
1. 安裝相依套件：
   ```bash
   npm install
   ```
2. 啟動開發伺服器：
   ```bash
   npm run dev
   ```
3. 打包正式版 (輸出到 `dist/`)：
   ```bash
   npm run build
   ```

## GitHub Pages 部署提示
- `vite.config.ts` 的 `base` 已設定為 `/MUI/`，適用於以此儲存庫名稱部署到 GitHub Pages (`https://<USERNAME>.github.io/MUI/`).
- 在本機確認頁面：執行 `npm install && npm run build` 後可用 `npm run preview` 檢視 `dist/`，畫面會與 Pages 相同。
- `.github/workflows/deploy.yml` 會在 `work` 分支推送或手動觸發時自動：
  1. 設定 Pages 環境
  2. 執行 `npm ci && npm run build`
  3. 上傳 `dist/` 為 Pages artifact 並發布到 GitHub Pages
- 本專案不包含打包輸出或二進位資源，直接推送程式碼即可。

## 重要檔案
- `src/components/*`: Joy UI 組件與訊息列表邏輯。
- `src/data.ts`: 範例使用者與訊息內容（使用線上頭像連結，避免提交二進位檔）。
- `vite.config.ts`: GitHub Pages 相容的 `base` 設定。
