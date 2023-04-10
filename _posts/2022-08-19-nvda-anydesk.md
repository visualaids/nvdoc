---
title: "使用 NVDA 來操作 AnyDesk 的常見問題與技巧"
categories:
  - 軟體應用
tags:
  - NVDA
  - AnyDesk
---

這篇文章要分享一些 NVDA 與遠端遙控軟體 AnyDesk 搭配運用時常見的問題與解決方法。

作者：蔡煥麟

本文提及之相關軟體與版本如下：

* NVDA 2022.2
* AnyDesk 7.0.14

### 簡介

我平日經常使用遠端遙控軟體來處理遠端電腦上的各項工作，有時候也替別人解決電腦操作上的問題，省時省力，非常方便。目前市面上有許多同類型的軟體工具，像是微軟 Windows 內建的遠端桌面、TeamViewer、AnyDesk、JumpDesk 等等。我目前最常用的是 AnyDesk 和 JumpDesk，而且這兩套軟體都有提供行動裝置 app，亦即可以在平板或手機上面直接操控遠端的 Windows 電腦。

[AnyDesk](https://anydesk.com/) 雖然好用，但是與 NVDA 搭配起來不太好操作，容易碰到一些問題。因此，我在這篇文章裡面整理了幾個常見問題和使用技巧，包括：

1. 如何查看本機電腦的 AnyDesk 連線地址（即 AnyDesk ID）。
2. 如何接受遠端電腦的連入請求。
3. 連線到遠端電腦之後，如何用鍵盤切回本機電腦操作。

前兩項技巧都與被控端有關，第三項技巧則和主控端有關。也就是說，如果你需要讓別人遠端連入你的電腦，那麼你會需要閱讀第 1 項和第 2 項技巧。如果你是主控端，也就是連線到其他電腦的那一方，則需要學會第 3 項技巧。

接著依序說明。

備註：如果你還沒有用過 AnyDesk，可以[點此連結下載 Windows 版 AnyDesk](https://anydesk.com/zht/downloads/thank-you?dv=win_exe)。下載之後無須安裝，直接執行就可以使用。就像 NVDA 有隨身版與安裝版兩種使用模式，AnyDesk 也可以安裝在你的 Windows 電腦上，以便隨時提供遠端連線。

### 查看本機電腦的連線地址

每一台有安裝 AnyDesk 的 Windows 電腦都會有一個專屬的 AnyDesk 連線地址，這個連線地址又稱為 AnyDesk ID，是一串九位數的數字。當別人欲透過 AnyDesk 遠端連線至你的電腦時，對方會需要你的電腦的 AnyDesk 連線地址。

對於有視覺的人來說，查看本機的 AnyDesk 連線地址毫無困難，可是對於使用 NVDA 報讀軟體的視障者來說，就沒那麼容易了。底下是操作步驟：

1. 先確保鍵盤的 NumLock 為關閉的狀態，而且 AnyDesk 主視窗是作用中視窗。
2. 按 NVDA+九宮格數字 2 來移動至子物件，此時 NVDA 會唸出「索引標籤控制項」。
3. 按 NVDA+九宮格數字 6 來移動至下一個物件，此時 NVDA 應該會唸出「新建連接 Invite 此工作台」，然後接著一串九位數的數字，這串數字就是此電腦的連線地址。

查到自己電腦的 AnyDesk 連線地址後，便可將此地址提供給想要連線至你電腦的人。理論上，這組連線地址是全球唯一的，不會跟別人重複，而且也不會變動（除非你重新安裝 Windows），故建議你把自己電腦的 AnyDesk 連線地址保存在筆記裡，方便日後需要的時候可以隨時找到。

當別人嘗試連線到你的電腦時，AnyDesk 會彈出一個對話窗，你必須在此對話窗中點一下「接受」按鈕，對方才能夠連線。接著說明如何使用 NVDA 來找到此對話窗裡面的「接受」按鈕，以便接受遠端電腦的連入請求。

備註：AnyDesk 也有提供「無人值守」的連線方式，也就是不需要有人在電腦前面點「接受」按鈕，隨時都允許別台電腦連線的模式。將來也許會再寫一篇進階文章來介紹此功能。

### 接受遠端電腦的連入請求

每當別人嘗試透過 AnyDesk 連入你的電腦時，AnyDesk 會彈出一個對話窗，而你必須在此對話窗中點一下「接受」按鈕，對方才能夠連線。然而，在 AnyDesk 的接受連線對話窗中，我們根本無法靠 Tab 鍵或方向鍵來找按鈕，這是 AnyDesk 本身設計上的一個缺點。幸運的是，NVDA 的物件導覽模式能夠解決這個問題。

首先，有一件事非常重要：你必須先確定你的 NVDA 是「安裝版」，才能順利執行稍後的操作步驟。如果你用的 NVDA 是隨身版（可攜式版本），便會因為[隨身版本身的限制](https://innoobj.blogspot.com/2022/08/nvda.html)而導致無法順利完成相關操作。

接下來，假設有人正要嘗試連線到你的電腦，此時 AnyDesk 應該會開啟一個請求連線的對話窗，讓你決定是要接受連線，還是拒絕連線。請按以下步驟操作：

1. 你必須把 Windows 的作用中視窗切換至 AnyDesk 的請求連線對話窗。你可以連續按 Alt+Tab 鍵來尋找視窗，直到 NVDA 報讀視窗標題為「AnyDesk」或「AnyDesk 視窗」時，便有可能是 AnyDesk 的連線對話窗。
2. 按 NVDA+九宮格 2，如果聽到 NVDA 報讀「不明」，便可繼續下一個步驟。但是如果你聽到的是「索引標籤控制項」，則表示目前作用中的視窗可能是 AnyDesk 主視窗，而不是連線對話窗，此時請回到上一個步驟來尋找連線對話窗。
3. 按 NVDA+九宮格 6，此時應該會聽到 NVDA 報讀「接受」，這就是「接受」按鈕了。此時請接著按 NVDA+九宮格的除號（即 /），以便將滑鼠定位至此按鈕，然後接著按九宮格的除號，便可模擬滑鼠點擊該按鈕，也就是按下了「接受」，於是對方便可以成功連入你的電腦。

另外要提醒的是，隨著 AnyDesk 的版本更新，連線對話窗的操作方式也可能有所改變。如果你發現上述操作步驟無論反覆做幾次都無法順利找到「接受」按鈕，你可以試試看各種不同順序的 NVDA+九宮格 2、4 和 6，或許就能找到。

### 用鍵盤切回本機電腦操作

本節所介紹的技巧，只跟遠端連線的控制端有關，而與接收端無關。也就是說，如果你並沒有需要遠端連線到另一台電腦，便可跳過本節。

當你用 AnyDesk 連接到遠端電腦，此時所有的按鍵都會先送入遠端電腦的 AnyDesk 視窗，所以如果要切換至本機操作，用滑鼠很簡單，可是用鍵盤卻會有問題，因為在連線至遠端電腦的情況下，AnyDesk 會優先把所有按鍵傳送至遠端電腦，比如說，按 Win 鍵時並不會開啟本機 Windows 的程式集，而會開啟遠端電腦的程式集。

如果在遠端連線時想要切回本機電腦操作，可使用 AnyDesk 提供的一組熱鍵：Ctrl+Alt+Shift+I。當你在 AnyDesk 遠端電腦視窗中按下這組熱鍵，就會關閉遠端電腦的任何輸入，包括鍵盤和滑鼠。換句話說，此時的任何滑鼠和鍵盤按鍵，都只會作用在你的本機電腦，而不會傳送至遠端電腦。

等到你在本機操作完畢，想要改切回去遠端電腦時，可用 Alt+Tab 來把作用中視窗切換至 AnyDesk 遠端電腦的視窗，然後再按一次 Ctrl+Alt+Shift+I 來讓遠端電腦恢復接收鍵盤輸入。

如果想知道 AnyDesk 還有提供哪些熱鍵來協助操作，可接著閱讀下一節。

### AnyDesk 常用熱鍵

* Ctrl+Alt+Shift+C：開啟交談選單。
* Ctrl+Alt+Shift+I：切換遠端電腦的輸入狀態（開啟或關閉）。
* Ctrl+Alt+Shift+P：螢幕截圖。
* Ctrl+Alt+Shift+S：切換遠端電腦的聲音傳輸功能（開啟或關閉）。
* Ctrl+Alt+Shift+Del：傳送 Ctrl+Alt+Del 至遠端電腦。
* Ctrl+Alt+Shift+F11：切換全螢幕模式或視窗模式。

如需完整的熱鍵說明，請參考官方文件：[Keyboard & Hotkeys](https://support.anydesk.com/knowledge/keyboard-and-hotkeys)。

### 延伸閱讀

* [NVDA 隨身版（免安裝版）的功能限制](https://innoobj.blogspot.com/2022/08/nvda.html)
* [AnyDesk 熱鍵](https://support.anydesk.com/knowledge/keyboard-and-hotkeys)
* [如何使用 Anydesk 的遠端桌面程式分享屏幕畫面](https://blog.anydesk.com/zh-hant/%e5%a6%82%e4%bd%95%e5%88%86%e4%ba%ab%e6%a1%8c%e9%9d%a2%e5%b1%8f%e5%b9%95%e7%95%ab%e9%9d%a2/)