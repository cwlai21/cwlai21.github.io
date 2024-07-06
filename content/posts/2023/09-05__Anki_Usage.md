---
title: "Anki 使用心得 - 擴充法文單字量"
date: 2023-09-05T14:15:05+07:00
slug: /Anki-Usage/
description: 學習第二外語好幫手
image: images/anki.png
caption: Photo by Anki App
categories:
  - tools
tags:
  - anki
  - vocabulary
  - self-learned
  - French
draft: false
---

在學習第二外語的路上，不免俗地總是會拿來與第一外語的學習歷程做比較，然而這個下意識的行為反而很容易在初學後段到中級的階段打退堂鼓。而我就是在這樣反覆不斷的提起興致到因為忙碌而又荒廢的循環中，接觸到了anki 這個提升記憶的工具

初期花了些時間摸索，建立自己的單字庫。但隨著每天將一些零碎的時間運用在anki的使用上，單字量的確有顯著的提升，語言能力的提升也是蠻有感的

## Anki 是什麼 ?

Keyword: Forgetting Curve Short-Term Memory Long-Term Memory

基於艾賓浩斯的遺忘曲線，統計上來說我們在學習後的一個小時後，僅僅只剩下不到一半的記憶量，若將時間拉長到一個月左右，剩下的記憶量僅僅只有20%。在這樣的理論基礎下，我們可以透過適當時間的複習來將短期記憶盡可能地轉化成中長期記憶，在心理學上稱為間隔重複理論，通常以flashcard 的方式達成。而Anki，就是透過使用者在複習時選擇每張字卡的難易程度以及複習次數決定卡片出現的頻率。換句話說，當我們一開始接觸一個新的知識點或新的單字，我們處在最容易忘記的時候，所以這張卡片會出現的比較頻繁來不斷加深我們的印象。隨著我們對這個知識點或單字越來越熟悉後，這張卡片出現的頻率就會降低，除非我們覺得有必要加強記憶強度

![](/images/4a24d4b397761.jpg)

## Why Anki ?

Keyword: Cross-Platform Synchronization Proactive Learning  Hit the ground running

Anki 最大的優勢是跨平台的雲端同步功能，字卡以及學習進度都可以一鍵同步到所有平台的同一個帳號

但缺點是新手不友善，需要花一些時間去找到或是設計符合自己預期的模板和建立卡片模組



## How to Use Anki ?

Keyword: Add-on Azure TTS
1. 註冊一個帳號
  - 網頁版 [連結](https://apps.ankiweb.net/)
  - Windows/Mac/Linux [官網下載](https://apps.ankiweb.net/)
  - Android (Google Play 免費下載)
  - iOS (須付費下載)

2. 建立筆記

Anki 卡片使用的語法是HTML 和 CSS，也可以透過簡單的script code去讀取特定欄位的值讓卡片有對應的變化

  - Anki 官方有提供一些簡易的模板教學 [官網](https://docs.ankiweb.net/templates/intro.html)
  - 網路社群交流: [GitHub](https://github.com/topics/anki-template)， [Reddit](https://www.reddit.com/r/Anki/search/?q=anki+template&cId=11f75043-74fa-4c4c-91c5-d4f60cd6da4f&type=link&sort=new)

雖然上述的資源除了模板的分享外也有相當多單字牌組的共享，但我還是選擇從每日學習的內容中將不懂的單字，句型以及片語製作成字卡。主要還是這樣的方式比較貼近學習歷程，單字也會是我比較常用到的相關領域

而我選擇的是將[鳳梨小姐的德文模板](https://serioustravel.co/anki-german-words-cards-deck/)加以修改成為我想要的模式:  
一來，德文跟法文的單字脈絡較為接近，都有陰陽性及動詞的多種變化  
二來，也可以同時加強相關的聽力訓練

  - Reading：法 ➞ 英/法（看到法文➞必須答出法文或英文解釋） 
  - Listening：音檔 ➞ 法＋英/法（聽到音檔➞必須答出法文或英文）  
    + 名詞會因為陰陽性不同而顯示不同顏色  
    +  動詞加上conjugasion，加深印象  
    +  透過chatGPT 增加例句的豐富性，尤其是片語和句型  


3. Add-on for Anki
***只有Desktop Anki可以安裝add-on， 但可以透過同步的方式讓手機application 有同樣的功能***

如何新增Anki Add-on？
  1. 點進網址後，網頁在download部分，會有「一串數字」
  2. 打開你的Anki，選擇選單Tools ➞ Add-ons
  3. 進入Add-ons畫面 ➞ 右上第一個按鈕 Get Add-ons
  4. 輸入Code(剛剛那一串數字)


## Useful Add-on

1.  [AwesomeTTS](https://ankiweb.net/shared/info/1436550454) (Microsoft Azure for français): 將語音加入字卡中

  - Create Microsoft Azure account and login
  - Create a Subscription (skip if you already have one)
  - Create a Resource Group based on the Subscription just created
  - Create a Speech Service based on the Resource Group and Subscription
  - Create Key and Endpoint
  - Fill the API key in the corresponding field of AwesomeTTS

2. [Review HeatMa](https://ankiweb.net/shared/info/1771074083): 在anki 主頁顯示視覺化的學習歷程
  ![](/images/anki_record_desktop.jpg)
3. [Image Occlusion Enhanced](https://ankiweb.net/shared/info/1374772155): 將圖片中想要記憶的部分遮擋起來，並一次創造出多張卡片

