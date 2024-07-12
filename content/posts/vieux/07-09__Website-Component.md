---
title: "網站是怎麼構成的？"
date: 2024-07-09T09:30:32+07:00
slug: /website-component/
description: Show how sebsite is constructed and the interaction between each components.
image: images/greg-rakozy-vw3Ahg4x1tY-unsplash.jpg
caption: Photo by Greg Rakozy on Unsplash
categories:
  - website
tags:
  - HTML
  - 伺服器
  - 瀏覽器
draft: false
---

最基本的元素是HTML，可以視作一棟房子的設計圖，從首頁（index.html）出發，透過指定不同的url通往其他的頁面
在每個html檔案都會有以下的基本架構，由tag和content構成，組出這個房間該有的空間規劃

```HTML
<!doctype html>
<html lang="zh-Hant-TW">

<head>
	<meta charset="utf-8">
	<title>網頁標題/出現於瀏覽器頁籤</title>
	<meta name="viewport" content="width=device-width, initial-scale=1.0">
	<meta name="description" content="提供搜尋引擎關於網頁頁面內的重要資訊">
	<link rel="stylesheet" href="style.css">
</head>

<body>
	<header>
		<nav>
			<span class="nav-title">My Website</span>
			<ul class="nav-link">
				<li><a href="#">Who am I</a></li>
				<li><a href="#">My Work</a></li>
				<li><a href="#">Contact me</a></li>
			</ul>
		</nav>
	</header>
	<main>
	</main>
	<footer>
	</footer>
</body>
</html>
```
單純的html文檔是如此的蒼白無力
![](/images/only_html_demo.png)

若加上了如同房間裝潢的CSS，自然多了點生機

```CSS
a {
  color: #ffffff;
  font-size: 20px;
  text-decoration: none;
  margin: 0 10px;
  border: 2px solid white;
  border-radius: 8px;
  padding: 5px 20px;
}

main {
	background-color: #b4b8ab;
	height: 200px;
}
footer {
	height: 60px;
	background-color: #d8c2fc;
}
```
![](/images/html_css_demo.png)

似乎還少了一點使用者與網頁之間的互動
- 為\<a\> tag加上個專屬的id，方可識別使用者的操作，做出對應的動作
```html
  <nav>
    <ul class="nav-link">
			<li><a href="#" id="who-am-i-link">Who am I</a></li>
			<li><a href="#">My Work</a></li>
			<li><a href="#">Contact me</a></li>
		</ul>
	</nav>
```
- 加上對應的javasciprt code 鑲嵌進原本的html 
  
```HTML
		<script>
			document.getElementById('who-am-i-link').addEventListener('click', function(event) {
				event.preventDefault(); // Prevent the default link behavior
				alert('Hello World!!!!'); // Show a pop-up message
			});
		</script>
```
  - 亦可放在另外的.js檔案中，只需要在htm中註明
```html
<!-- Link to the external JavaScript file -->
<script src="index.js"></script>

</body>
</html>
```
- 點下 “Who am I” 這個link後，我們就會看到一個視窗彈出

![](/images/action_html.png)



