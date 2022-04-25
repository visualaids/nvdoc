---
title: "讓自己的程式開口說話"
tags:
  - python
---
好不容易學會 python, 要開始動手寫程式。
想讓自己寫的程式與眾不同，
一個可以採用的奇招市讓自己寫的程式會開口說話。
python 可用的 TTS library 還不少，這次介紹的 pyttsx3 具有以下特色：

1. 可離線使用無須網路
2. 使用 Windows 內建語音隱形無須額外安裝
3. 可調整發音的各項參數

請用以下指令安裝 library:

```
pip install pyttsx3
```

接下來用以下程式碼進行測試：

```
import pyttsx3
engine = pyttsx3.init()
engine.say("hello, how are you?") # 說中文馬也通喔
engine.runAndWait()
```

先想想上面的技巧要如何運用在你的程式裡，剩下的我們來日有緣再續
