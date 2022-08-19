---
title: "NVDA 隨身版（可攜式版本）的限制"
categories:
  - NVDA
tags:
  - NVDA
---

NVDA 隨身版（可攜式版本）有一些限制，使得某些使用情境下無法順利使用 NVDA 來執行特定操作。這篇文章會說明隨身版有哪些限制。

NVDA 使用者手冊有列出[隨身版的限制](https://www.nvaccess.org/files/nvda/documentation/userGuide.html#PortableAndTemporaryCopyRestrictions)，整理如下：

* 無法在 Windows 登入畫面中使用。這是理所當然的，因為都還沒進入 Windows 作業環境，當然也就不可能執行隨身版 NVDA 了。
* 除非 NVDA 隨身版在啟動的時候是以管理員的身分執行，否則無法操作具有管理員權限的應用程式。我們不建議以管理員身分來執行 NVDA。
* 以系統管理員身分來啟動某個應用程式時，NVDA 隨身版無法報讀使用者帳戶控制（UAC）畫面的內容。
* Windows 8 與後續版本：不支援觸摸式螢幕。
* Windows 8 與後續版本：在 Windows 商店的 app 中，有些功能會無法使用，例如瀏覽模式以及報讀輸入的字元。
* Windows 8 與後續版本：不支援音量自動調整（audio ducking）。
 
> 註：audio ducking 也有人翻譯為「聲音迴避」，其作用是當 NVDA 發出聲音時，會自動降低其他應用程式的音量。

舉個實際的例子，是我自己親身碰到的問題：當別人透過 AnyDesk 嘗試遠端連線至我的電腦，AnyDesk 會彈出一個對話窗，此時必須點「接受」按鈕，對方才能連線。然而，NVDA 隨身版會完全無法在這個接受連線的對話窗裡面執行任何操作。如果改用安裝版的 NVDA，則沒有這樣的狀況。