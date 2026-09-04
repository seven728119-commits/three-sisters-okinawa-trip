沖繩慢慢排 PWA｜使用與部署

一、直接使用
1. 建議用本機伺服器或已部署的 HTTPS 網址開啟，不要只雙擊 index.html。
2. 時間軸：切換 Day 1～Day 5，直接修改開始時間，↑↓ 可每次移動 30 分鐘。
3. 找靈感：可用「景點／美食、地區、情境、搜尋」縮小 115 個選項。
4. 加入行程：選日期、時間、停留時間與重要程度後，右側會更新順路建議。
5. 換照片：每張卡和首頁封面都支援圖片網址或本機照片；照片只存在目前瀏覽器。
6. 自選名單：可新增自己的景點或美食，再加入時間軸。

二、通用 JSON
1. 點頁首、旅程設定區或手機底部的「匯出」。
2. 下載的 JSON 使用 schemaVersion 1，可直接給「沖繩通用動態行程PWA」讀取。
3. 本資料夾已附 okinawa-family-trip.json；另一份已放進「沖繩通用動態行程PWA」資料夾。
4. 若要讀回其他行程，請在旅程設定區點「讀取 JSON」。

三、部署
將下列檔案與資料夾一起上傳到同一個網站根目錄：
  index.html
  styles.css
  places.js
  app.js
  okinawa-family-trip.json
  manifest.webmanifest
  service-worker.js
  icons/
  assets/

部署到 HTTPS 網址後，iPhone 可用 Safari「分享 → 加入主畫面」，Android 可用 Chrome「安裝應用程式」。

四、離線快取更新
若更新後仍看到舊版，請先重新整理並關閉再開。部署內容有變動時，也可再調高 service-worker.js 的 CACHE_NAME 版本。

五、備份
重整前的原始單檔版本保留為 index.legacy-20260823.html，可隨時參考或還原。
