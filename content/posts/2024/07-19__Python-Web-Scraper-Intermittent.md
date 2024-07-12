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


## 動態爬蟲

### Prequisite
python packages
- selenium
- webdriver (取決於使用的瀏覽器)
  - chrome 版本必須和 chromedriver使用一致的版本
- 

- 用webdriver ＋ selenium 模擬實際用瀏覽器開啟網頁的過程
  - 與瀏覽器相關
- 動態開啟網頁後，就回歸到靜態爬蟲

## 破解反爬蟲
[ref](https://medium.com/@kaojia/%E8%B3%87%E6%96%99%E5%88%86%E6%9E%90-python%E7%88%AC%E8%9F%B2%E5%85%A5%E9%96%80%E5%AF%A6%E4%BD%9C-%E4%B8%8B-%E5%8B%95%E6%85%8B%E7%B6%B2%E9%A0%81%E7%88%AC%E8%9F%B2-%E5%8F%8D%E5%8F%8D%E7%88%AC%E8%9F%B2-json-%E6%A0%BC%E5%BC%8F-2170c88b0ec8)

### Prequisite
python packages
- Pytesseract (dependency Tesseract)

[ref](https://medium.com/@kaojia/%E8%B3%87%E6%96%99%E5%88%86%E6%9E%90-python%E7%88%AC%E8%9F%B2%E5%B0%88%E6%A1%88%E5%AF%A6%E4%BD%9C-%E8%BE%A8%E8%AD%98%E5%9C%96%E7%89%87%E6%96%87%E5%AD%97-%E9%A9%97%E8%AD%89%E7%A2%BC-pytesseract%E5%A5%97%E4%BB%B6-43e7adb29316)

## 進階： Facebook 貼文分析

