前面的代碼是在前端即時生成 iCalendar (.ics) 文件，並提供下載功能。在 Safari 瀏覽器中，它會生成並下載 .ics 文件；在其他瀏覽器或 Google App 中，它會提供跳轉到 Google 日曆活動添加頁面的功能。

代碼說明
瀏覽器檢測：

使用 navigator.userAgent.toLowerCase() 檢測用戶是否在使用 Safari 瀏覽器。
使用 navigator.platform 檢測設備是否為 iOS。
檢測 User-Agent 是否包含 gsa（表示 Google App）。
確保 User-Agent 中包含 Safari 並且不包含 CriOS、FxiOS 和 Chrome，且不包含 gsa。
按鈕邏輯：

如果是 Safari 瀏覽器，下載按鈕將會觸發下載 iCalendar 文件的邏輯。
如果不是 Safari 瀏覽器或是在 Google App 中，下載按鈕將會跳轉到 Google 日曆活動添加頁面。
生成 iCalendar 文件：

使用 JavaScript 在前端即時生成 iCalendar 文件內容。
使用 Blob 物件創建 iCalendar 文件，並生成一個臨時下載鏈接。
觸發文件下載，並在完成後清理臨時鏈接。
