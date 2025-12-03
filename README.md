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
- 在 GitHub Pages 設定中選擇「Deploy from a branch」，並指定打包後的 `dist` 目錄（可透過 CI 或手動上傳）。
- 本專案不包含打包輸出或二進位資源，直接推送程式碼即可。

## 重要檔案
- `src/components/*`: Joy UI 組件與訊息列表邏輯。
- `src/data.ts`: 範例使用者與訊息內容（使用線上頭像連結，避免提交二進位檔）。
- `vite.config.ts`: GitHub Pages 相容的 `base` 設定。
