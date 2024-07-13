---
title: "為什麼要學爬蟲？"
date: 2024-07-12T09:30:32+07:00
slug: /python-web-Scraper-intro/
description: 解鎖你的網路力-讓你輕鬆徜徉在網路海中，「截」你所需，「取」你所要
image: images/chris-ried-ieic5Tq8YMk-unsplash.jpg
caption: Photo by Chris Ried on Unsplash
categories:
  - tools
tags:
  - 爬蟲
  - Python
  - feature
draft: false
---

如果想要從網路上取得某個資訊，像是這個月各大書店暢銷書的價格比較，除了開啟好幾個分頁，一本一本比價外，有沒有什麼方式可以一鍵完成呢？  
像這樣重複性高，數量眾多，又與網頁相關的問題，就不得不提到「爬蟲」這件事

## 什麼是爬蟲
簡單來說就是透過程式將網路伺服器回傳給瀏覽器的資料擷取下來，從中取得使用者有興趣的部分
以這個例子來說就是某本書的在某個電商平台上的價錢

![](/images/books_search.gif)


## 要怎麼實作呢？

1. 安裝Python 和 Python package (以Python3為例)
- Python [官網下載](https://www.python.org/downloads/)
- requests
  - 最常使用到的get這個function
  - 可以從r.text得到我們想要的資訊（針對package的內容以HTTP header為基準做初步的解碼）
  ```Python
  import requests
  r = requests.get('https://www.books.com.tw/')
  r.text
  ```
- beautifulsoup
  - 快速解析HTML檔案，是爬蟲中最重要的模組之一

![](/images/packages_install.gif)

2. 分析網頁架構 （以chrome browser為例）
  - 進入網頁後按右鍵或F12可看在檢查這個選項
  - 點選左上角的按鈕後
  - 找到想要書籍的圖片點下去後
  - 就可以對應到相對的HTML內容
  ![](/images/html_inspect.gif)
3. 使用上述安裝的packages

  ```Python
  import requests
  from bs4 import BeautifulSoup
  r = requests.get('https://www.books.com.tw/products/0010984894')
  soup = BeautifulSoup(r.content, "html.parser")
  price = soup.find("ul",class_="price").find(class_="price01").getText()
  ```

  ![](/images/bs4_map.png)
  
  將BeautifulSoup得到的資料加以拆解
  - 我們要得到的金額是包含在\<ul\> 這個tag下class屬性是“price”的這個大框架下
  - 再進一步往下去定位到“price01”這個class
  - 取得最內層的數值，就是我們想要的資訊 

![](/images/bs4_demo.gif)

## To Be Continued ...
乍看之下，我們一開始提出的問題好像已經解決了
但我們要怎麼從電商平台的首頁找到暢銷榜？
和要怎麼從暢銷版連結到每個排名的書籍呢？

這就不得不進一步提到selenium 和webdriver 這兩個工具
請繼續看下去 
