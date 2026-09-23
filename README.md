# AllinPay BR 智能預填 Demo

[開啟客戶測試 Demo](https://notdesign.github.io/allinpay-br-demo/)

支援香港商業登記證的文字 PDF、掃描 PDF、JPG 和 PNG，並提供歪斜校正、原件對照、人工核對及表單預填。每檔最多 10 MB，PDF 最多 5 頁。建議使用桌面 Chrome。

文件與辨識結果只在瀏覽器記憶體處理，不傳送至 GitHub 或 OCR 服務，也不儲存到瀏覽器資料庫。網站及約 68 MB 的辨識資源由 GitHub Pages 提供，因此 GitHub 仍會收到一般網站資源請求。重新整理或清除後，本頁資料消失。

這是功能驗證 Demo，未連接正式申請系統。低畫質、遮蔽或歧義欄位可能留空或需人工修正。90% 的真實文件欄位正確率目標尚未完成驗收。附帶範例全部為虛構測試資料。

## 原始碼與部署

`source.zip` 是本次版本的完整執行原始碼與合成範例，沒有真實客戶文件。解壓後執行：

```sh
npm ci --ignore-scripts
npm run setup
npm start
```

開啟 http://127.0.0.1:8765/。`npm run build` 產生可放在子目錄的 `dist/`。GitHub Actions 只發佈此目錄。PDF.js、Tesseract.js 與其依賴的授權隨 `/vendor/` 一併提供。
