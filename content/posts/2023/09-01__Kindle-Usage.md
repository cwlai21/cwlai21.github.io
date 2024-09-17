---
title: "Kindle 使用心得"
date: 2023-09-01T14:15:05+07:00
slug: /Kindle-Usage/
description: 初心者也能快速上手
image: images/kindle.jpg
caption: Photo by Kindle App
categories:
  - tools
tags:
  - kindle
  - eBooks
  - eReader
  - feature
  - self-growth
draft: false
---

一向偏好紙本書籍閱讀的我，在因緣際會下，在八月入手了Kindle Oasis 閱讀器後，一腳踏進入電子書的新大門。截至目前，在kindle unlimited 第一個月免費試用和不小心續訂了第二個月的強大誘因下，體驗了英法書籍，法文BD (Bande Desinée) 以及中文漫畫的閱讀，整體的使用者體驗相當不錯。

一來，長時間使用下不會造成眼睛過度的疲勞及乾澀，二來，機器本身相當輕巧，耗電量也不高，隨身攜帶的負擔不會太過沉重，但又可以隨時沉靜在書海中。考量家中不斷減少的閒置書櫃空間和各種推陳出新的有趣新書，這個剁手行為還是相當划算。

## 中文電子書

Keyword: Pubu Kobo

透過[PuBu](www.pubu.com.tw/)以及[樂天Kobo](www.kobo.com/tw/zh)電子書城補足Amazon ebook 中文書籍稀缺的缺口

前置動作 (one-time job)

-  下載Adobe DRM (官網下載) -  > 建立Adobe ID - >  授權電腦

-  下載 pdf epub drm removal，免費版有移除上限，可自行搜尋破解版

-  下載 Calibre 搭配 DeDRM Plugins (較推薦)

-  設定  Approved Personal Document Email List (許可的個人文件電子郵件清單)，可以透過 email 夾帶附件的方式將檔案send to kindle

    Manage Your Content & Devices (管理您的內容和裝置) > **Preferences (偏好) > Personal Document Settings (個人文件設定)  > 新增許可的電子郵件地址**

PuBu採用DRM free的方式將電子書檔案提供給使用者，然而樂天Kobo的檔案則是受到DRM 保護，需要額外移除DRM後才能傳輸到任意電子閱讀器

在書城購買任一本書後

1. 在書庫中下載 .ascm檔

2. 將檔案丟進 Adobe DRM 獲得 .epub 檔案

    詳細內容可參考 Pubu 的官方文章[買書更有保障，我們支援 Adobe DRM 了](https://support.pubu.tw/hc/zh-tw/articles/360050221451-%E8%B2%B7%E6%9B%B8%E6%9B%B4%E6%9C%89%E4%BF%9D%E9%9A%9C-%E6%88%91%E5%80%91%E6%94%AF%E6%8F%B4-Adobe-DRM-%E4%BA%86)

3. (Kobo/files with DRM only) 將.epub 檔案丟進軟體中，即可獲得DRM free 的 .epub 檔案

4. 將電子書轉換成直排閱讀閱讀 (optional)

     -  中文書的閱讀習慣是從右至左的直式排列，反觀外文書則是左到右的橫式排列

     -  透過[Sigil(官網下載)] (sigil-ebook.com/sigil/download/)這個開源的電子書編輯軟體修改電子書的CSS 架構和翻頁模式

     -  修改kindle 字型， 將思源黑體 Noto Sans(官網下載)下載並用usb 傳輸至kindle fonts 資料夾 (one-time job)

5. 透過[send to kindle](www.amazon.com/-/zh_TW/sendtokindle) 將 .epub 檔案傳輸至裝置

     - Supported File Types: PDF, DOC, DOCX, TXT, RTF, HTM, HTML, PNG, GIF, JPG, JPEG, BMP, EPUB

     - 直接在網頁上傳檔案或是透過email 附件

![](/images/library.jpg)

## 閱讀器選擇 - 電子書閱讀器 vs 平板/手機

Keyword: Tablet eReader eInk

電子書閱讀器採用的是電子墨水/電子紙的技術，其兩大特點為「雙穩態」以及「反射式」，分別對應到節電和護眼這兩個最主要優勢。

目前市面上常見的電子書閱讀器以「黑白雙色電子墨水」為主，是由數百萬個「微膠囊」（Micropcapsules）組成，每個微膠囊大約只有頭髮的直徑那麼大，而其中又含有許多的黑白兩色電泳粒子懸浮在微膠囊的液體之中，白色帶有負電荷，黑色則是正電荷。通電時，會因為正負相吸而移動，所以使用者就可以看到白色或者是黑色。在沒電的時候，畫面會靜止不動不會消失，而因為只有畫面在變動的時候需要電力，所以電子書閱讀器十分省電

另外一個技術特點就做「反射式」，意思是指電子紙本身不會發光也不需傳統螢幕的背光源。環境光源照射在電子紙上會再折射光線到人眼中，就跟閱讀紙本書一樣，不僅在陽光下清晰可見，也少了藍光等，閱讀起來眼睛更舒適。反觀手機及平板，不論是LCD 或是OLED，都是採用元件主動式的發光方式作為螢幕顯示的方式，其所造成的炫光反射所造成的視覺疲勞都是顯而易見的

## 閱讀器選擇 - 開放式 vs 封閉式

Keyword: OS Comparison 

開放式系統 (HyRead, )不受限電子書的來源，在Android 的作業系統下可以安裝各家電子書的app來閱讀，即便是網路小說甚至網路漫畫也都涵蓋在內。但相對的，各家app 使用者體驗不盡相同，閱讀器本身的硬體規格也不足以像手機或平板支援流暢的同時執行多個應用程式

相對封閉式系統(Kindle, Kobo, MooInk)則是閱讀器廠商綁定自家的電子書城，統一規格的好處即是效能和使用的流暢度會好蠻多的

## 萬用的客服

Keyword: Custom Service

透過[Amazon customer service](www.amazon.com/hz/contact-us/foresight/hubgateway)，請對方協助將廣告版的廣告免費移除
每個人的第一台機器理論上都可以獲得此福利，之後的設備則須支付原價20-25美金的費用

![](/images/kindle_customer.jpg)

移除後，all setting - > Device options - >  switch on Display Cover

即可在待機畫面時顯示當下閱讀書籍的封面

