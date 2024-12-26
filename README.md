# AWS Lambda Phone Verification Service

## 簡介
這是一個基於 AWS Lambda 的電話號碼驗證服務，旨在幫助檢查員工電話號碼的有效性及填寫問卷的資格。透過檢查所輸入的台灣手機號碼，並確認該號碼是否為公司員工，使用者可以輕鬆進行驗證。

## 功能
- 驗證輸入的手機號碼格式是否符合台灣的手機號碼規範。
- 檢查該手機號碼是否為公司員工的聯絡號碼。
- 確保填寫問卷的時間間隔不低於60秒。
- 返回相應的狀態碼及訊息給用戶，告知驗證結果。

## 安裝與使用方式
1. 請確保您的環境中已安裝 Node.js 並具備 AWS 的相關帳號及許可。
2. 將此專案下載到本地端並進入專案資料夾。
3. 在 `AWS.config.update` 中填入您的 AWS `accessKeyId`、`secretAccessKey`，及所使用的 S3 Buckets 的相關設定。
4. 將函數上傳至 AWS Lambda，並配置相應的 API Gateway 以便啟用 HTTP 請求。
5. 透過發送 POST 請求至 API Gateway，提供有效的 JSON 格式請求体，例如：
   ```json
   {
       "value": "0912345678"
   }
   ```

## 必要的依賴模組清單
- `aws-sdk`: 用於與 AWS 服務的交互，進行 S3 資料存取的操作。

## 授權條款
本專案使用 MIT 授權條款，詳情請參閱 [LICENSE](LICENSE) 檔案。

```
將此 markdown 文檔存為 `README.md` 檔案可方便開發者了解此專案的基本資訊及使用方式。