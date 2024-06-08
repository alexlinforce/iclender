# 說明：生成和下載 iCalendar 文件的 HTML 和 JavaScript 代碼

這段代碼提供了一個網頁，當用戶在 Safari 瀏覽器中訪問時，允許下載一個 iCalendar (.ics) 文件；在其他瀏覽器或 Google App 中訪問時，提供將事件添加到 Google 日曆的選項。

## 代碼說明

### HTML 結構：

- 包含一個標題和一個按鈕。
- 按鈕用來觸發下載或跳轉到 Google 日曆。

### CSS：

- `#browserWarning` 用於顯示非 Safari 瀏覽器的提示信息，默認隱藏。

### JavaScript：

- `detectBrowser()` 函數檢測用戶是否使用 Safari 瀏覽器。
- 當頁面加載完成後，檢測瀏覽器並根據結果設置按鈕的行為。
  - 如果是 Safari 瀏覽器，按鈕會觸發 iCalendar 文件的下載。
  - 如果不是 Safari 瀏覽器，按鈕會跳轉到 Google 日曆活動添加頁面。

### 生成 iCalendar 文件：

- 定義事件資訊（主題、開始時間、結束時間、描述、地點）。
- 生成 iCalendar 文件內容並創建 Blob 物件。
- 創建臨時下載鏈接並觸發文件下載。
- 清理臨時鏈接。

### 生成 Google 日曆 URL：

- 使用 `createGoogleCalendarUrl` 函數生成跳轉到 Google 日曆活動添加頁面的 URL。

## 使用方法

1. 將上述代碼保存為 `index.html` 文件。
2. 上傳 `index.html` 文件到 GitHub 儲存庫並啟用 GitHub Pages。
3. 使用不同的瀏覽器和 iPhone 上的 Google App 訪問生成的 GitHub Pages URL。
   - 在 Safari 瀏覽器中，應顯示可用的下載按鈕。
   - 在其他瀏覽器或 Google App 中，應顯示提示信息並將按鈕功能替換為跳轉到 Google 日曆活動添加頁面。

## 測試步驟

1. 使用不同的瀏覽器和設備訪問生成的 GitHub Pages URL。
2. 確認在 Safari 瀏覽器中按鈕行為正確，能夠下載 iCalendar 文件。
3. 確認在其他瀏覽器或 Google App 中按鈕行為正確，能夠跳轉到 Google 日曆活動添加頁面。

這樣可以確保用戶知道該網頁最好在 Safari 中打開，並且在非 Safari 瀏覽器或 Google App 中按鈕會提供跳轉到 Google 日曆活動添加頁面的選項。
