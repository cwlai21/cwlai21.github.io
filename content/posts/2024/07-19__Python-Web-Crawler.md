---
title: "Python Web Crawler Learning Note"
date: 2024-07-01T09:30:32+07:00
slug: /python-web-scrawler/
description: Study note of using Python to execute web scrawler in static and dynamci approaches.
image: images/chris-ried-ieic5Tq8YMk-unsplash.jpg
caption: Photo by Chris Ried on Unsplash
categories:
  - tools
tags:
  - 爬蟲
  - python
  - beautifulSoup
  - selenium
draft: true
---


## 什麼是爬蟲？

## 靜態爬蟲


- 分析網頁架構
  - 找到要取得的資訊的標籤名稱作為搜尋的定位點
- request
  - 獲得伺服器上回傳的response
- BeautifulSoup
  - 得到需要的標籤內容

## 動態爬蟲

- 用webdriver ＋ selenium 模擬實際用瀏覽器開啟網頁的過程
  - 與瀏覽器相關
- 動態開啟網頁後，就回歸到靜態爬蟲

## 進階： Facebook 貼文分析

