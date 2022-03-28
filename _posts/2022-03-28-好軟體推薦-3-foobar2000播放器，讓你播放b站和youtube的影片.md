---
  : "好軟體推薦-3 foobar2000播放器，讓你播放b站和youtube的影片"
categories:
  - 好軟體推薦
tags: 
  - 軟體使用
date: 2022-03-28
---

作者:小羔羊


### 好軟體推薦-3 foobar2000播放器，讓你播放b站和youtube的影片

hi各位，最近我投稿了一篇文章，內容是分享一個可以讓foobar播放幾乎所有多媒體格式的差件，
這個插件會調用一個編解碼器(ffmpeg)來將指定的格式轉檔成foobar認識的格式，達到萬用播放的效果，
而這次我要分享的也跟這個foobar插件有關，不過還搭配了之前介紹過的youtube for foobar插件，有興趣可以參考這篇→
[教你用foobar2000開心看youtube](https://www.nvda.org.tw/teaching/article/ui=2004160143tm=1937079283)
在研究過程中，我意外的發現foobar的youtube插件調用的youtube-dl還能解析B站，也就是哔哩哔哩平台的影片，因此搭配了最近介紹的邊解碼器插件完成了播放B站影片的壯舉，
想必有看過B站的都有些經驗，要在網頁上播放B站的影片、快進、快退並不是那麼方便，因此有了這個foobar，將給你帶來更多的便利，
設定不難，只要在foobar的參數選項設定youtube for foobar，在第三方二進位程式中將youtube設為系統，並且指定編解碼的差件要轉碼.flv的格式就能完成設定，
詳細的設定步驟會在之後在介紹，成品可以直接在下方下載。

---


### 下載

如果點選下方連結無法彈出存檔的視窗，請在下載連結上按快顯鍵找另存，之後按ctrl+j到下載管理葉面選擇保留方可下載
[點我從小羔羊服務器下載foobar2000 可以播放b站和youtube的播放器.rar](https://file.lamb.tw/f/abd6ee6f81714568b1f7/?dl=1)

---


### 使用說明

確定目前電腦有聯網，解壓並已系統管理員全縣直行
安裝巧克力和ffmpeg以及youtube-dl.cmd
這個cmd只有三行，會安裝名為巧克力的軟體管理器，以及ffmpeg邊解碼器和youtube-dl並自動建立環境變數，
之後打開資料夾內的foobar2000.exe，你也可以將其發送捷徑到桌面上，再來可以按下面介紹的快捷鍵來操作foobar:

#### 全局快速鍵

下面這些快速鍵是在任何地方都有效，不需要特別打開foobar視窗

* ctrl+win+alt+上或下 調整音量
* ctrl+win+alt+左或右 快進快退
* alt+p 播放或暫停
* ctrl+alt+反影號(大鍵盤1左邊的鍵) 可以強制關閉foobar，當foobar卡住或你想關閉他的時候很好用


#### 一般快速鍵

下面這些快速鍵只有在foobar視窗裡按才有效


* ctrl+u 會打開一個編輯框，在此貼上要用foobar看的網址，例如b站或youtube的連結，之後按enter，tab在播放列表找到影片名稱按enter即可播放
* ctrl+c 在播放清單裡的某個影片名稱上按此鍵可以複製影片連結到剪貼版
* enter 在播放列表內的影片、檔案名稱上按的話可以播放
* ctrl+y 打開youtube搜尋面板，這裡可以直接搜尋並瀏覽搜尋的結果
* ctrl+p 參數選項


---

另外，如果你是用nvda的話→

* ctrl+shift+e 查看播放了多少時間
* ctrl+shift+r 查看剩餘時間


---

如果想閱讀我的更多原創文章，可以到我的網站→[小羔羊分享站](https://lamb.tw/)