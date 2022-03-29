# NVDOC 網站開發筆記

整理 nvdoc 網站的相關設定。

## 支援 Google Search

欲透過 Google Search Console（以下簡稱 GSC） 讓 Google 盡快索引我們的網站，必須先通過網站擁有者的驗證。GSC 驗證網站擁有者的作法可參考 Google 官方文件：[Add a website property](https://support.google.com/webmasters/answer/34592?ref_topic=9268559)。NVDOC 沒有自訂網域名稱，所以是採用 URL-prefix property 的方式來驗證，其實就是在網站根目錄底下放置一個由 GSC 產生的 HTML 檔案。

如果要直接驗證網站擁有者，可以[點此連結](https://search.google.com/search-console/welcome?utm_source=wnc_376106&utm_medium=panel&utm_campaign=wnc_376106&utm_content=msg_376106)。

## 值得參考的 Jekyll 布景主題

- [Huxpro](https://github.com/Huxpro/huxpro.github.io)
