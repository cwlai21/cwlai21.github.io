---
title: "什麼是URL ?"
date: 2024-07-10T09:30:32+07:00
slug: /url-definition/
description: Show the mechanism of URL with DNS server and web server
image: images/remotar-jobs-s5kTY-Ve1c0-unsplash.jpg
caption: Photo by Remotar Jobs Unsplash
categories:
  - website
tags:
  - 伺服器
  - 瀏覽器
draft: false
---


我們所說的網址，專業的說法是URL (Uniform Resource Locator)，用來告知瀏覽器該用什麼方式和去哪一個位置取得網頁內容  
但究竟是怎麼辦到的呢？  

### 拆解URL  
https://www.google.com/search?q=weather+of+taipei  
**\[Protocol\]:\/\/\[Domain Name\]\/\[Path\]**

- Protocol \[https\]
	- http or https: s代表著secure，會以加密的方式進行網頁傳輸
	- ftps: 檔案傳輸協定
	- mailto: 電子郵件傳輸
	- smb: 在資料夾開啟共享後，可在windows 和 mac電腦之間進行資料的傳輸
- Domain name \[www.google.com\]
	- 如果網址列上不是IP 的話，需要透過詢問 DNS (Domain Name System) server 取得網頁伺服器的 IP 位址
	- Domain Name 是為了讓人更容易記得的網站名稱，與IP位址為唯一對應關係
- Path \[search?q=weather+of+taipei \]
	- 指定特定的路徑
	- 透過指定參數找到特定的頁面
		- ***search?q=*** 進行搜尋
		- 'weather of taipei' 為搜尋的內容
		- 如果有多項參數會以 ***'&'*** 串連

{{< mermaid >}}
sequenceDiagram
    Web Browser->>DNS Server: Request IP address of this domain name
    DNS Server-->>Web Browser: Request granted!
    DNS Server-)Web Browser: Voilà, here is the IP address!
{{< /mermaid >}}
  
