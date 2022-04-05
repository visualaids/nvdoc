---  
title: "NVDA 多國語言文件語音報讀方案概覽"
author: "coscell"
categories: 
  - NVDA
tags: 
  - NVDA
  - 語音
date: 2022-04-05
---  

摘要：本文整理了 NVDA 多國語音報讀的幾個方案。

作者：coscell 
初稿日期：2020-05-26  
更新日期：2022-04-05

自從 NVDA 2019.3 從 python 2 換成 3 以來，使用者一片哀號聲，我才知道原來大陸駭客製作的星光雙語附加元件在國內如此受到歡迎。

他是利用美國 Nuance 公司的多國語音引擎 Vocalizer，然後自己撰寫程式來驅動。最早提供附加元件的是 https://vocalizer-nvda.com，語音免費，驅動程式的價格不菲。既然需求這麼大，我就來整理一下我所知道的其他免費方案。

## Tony's Enhancements

首先，如果選用微軟的 OneCore 語音，並將 NVDA 的「自動切換語言」打開，它就會按照文件的 lang 屬性自動選用該語言的語音來報讀，當然您必須先裝好該語言套件。缺點是只有少數情況才能獲取文件的 lang 屬性。

欲解決這個問題，我推薦附加元件 [Tony's enhancements](https://github.com/mltony/nvda-tonys-enhancements/releases/latest/download/tonysEnhancements.nvda-addon)。只要打開該支援設定在平常的操作就有效果，缺點是不能針對個別語言指定特定語音角色和個別調整速度。

## Dual Voice

另外，NVDA 官方社群有提供 [Dual Voice 附加元件](https://addons.nvda-project.org/addons/dualvoice.en.html)，可以同時選用一個拉丁語系和一個非拉丁語系的語音來報讀兩種不同的語言。缺點是只支援 SAPI 5 語音，一個聊勝於無的彌補辦法是執行下面這個程式把 OneCore 語音整合到 SAPI 5 來增加語音角色的選擇：

[SAPI Unifier](https://github.com/Mahmood-Taghavi/SAPI_Unifier/releases/download/v1.1/SAPI_Unifier_requires_dot_NET_4.exe)

## HKBU-2020

最後，香港失明人協進會開發了一個 HKBU-2020 附加元件，
除了提供科大訊飛語音 AiSound 外，還包含一個雙語音合成器，提供科大訊飛的語音合成器朗讀中文。此外，亦可搭配其他合成器朗讀英文，不論是「eSpeak」、「Microsoft Speech API version 5」還是「Windows OneCore 語音」皆可。

這個附加元件可以在此下載：[NVDA 讀屏軟件(官方版) 及 HKBU 附加組件2020.03.2 (只支援NVDA 2019.3或較新版本)](https://www.hkbu.org.hk/tc/service/technology/sub-page?page_id=nvda_modules_2020_03)
