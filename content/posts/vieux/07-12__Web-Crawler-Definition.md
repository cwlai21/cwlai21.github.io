---
title: "什麼是網路爬蟲"
date: 2024-07-01T09:30:32+07:00
slug: /web-scrawler-definition/
description: Study note of using Python to execute web scrawler in static and dynamci approaches.
image: images/chris-ried-ieic5Tq8YMk-unsplash.jpg
caption: Photo by Chris Ried on Unsplash
categories:
  - tools
tags:
  - 爬蟲
  - 伺服器
  - 瀏覽器
draft: true
---

## 網頁運作原理簡介  
[ref](https://jimmyswebnote.com/principle-of-website/)
Web browser 透過URL 向 DNS Server請求 IP， 詳情可參考 [連結](../../vieux/url-definition)  
Web browser 透過該IP 向 Web Server 請求特定的網站內容
Wev Server 回傳Web browser [網站資料](../../vieux/website-component) 
在網路回傳的路上，我們透過爬蟲程式，獲取那份封包資料，這就是所謂的[爬蟲](../../vieux/web-scrawler-definition)


[ref1](https://hackmd.io/@NCHUIT/1101223)

## Scraper vs. Crawler

|        | Web Crawling  | Web Scraping |
|  ----  | ----  | ----  |
| Goal  | understand the content of a website | convert specific website content into a structured format, such as tables, JSON, databases, and XML representations|
| Process  | Gather URL(s), retrieve and analyze the URL(s), save the indexed and store in database   | Determine the target website, extract the necessary date, download data in the intended format  |       
| Illustration   | [Ref](https://www.baeldung.com/cs/web-crawling-vs-web-scraping)![](/images/web_crawling.png) | [Ref](https://www.baeldung.com/cs/web-crawling-vs-web-scraping)![](/images/web_scraping.png)
| Scale | Mostly in large scale | in any scale |
| Application | Search engines like Google, Yahoo, or Bing | stock market analysis utilizes to download financial information from online resources  |



