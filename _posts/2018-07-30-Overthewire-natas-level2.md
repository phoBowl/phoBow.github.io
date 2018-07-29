---
layout: post
title: Overthewire Natas Level 2
subtitle: ... Write up
tags: [overthewire, natas, level2, overthewire-natas, writeup]
---

## Natas Level 2
* Username: natas2
* Password: ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi
* URL:      http://natas2.natas.labs.overthewire.org1

**Step 1:** Let Login to the URL, you will see the message
> There is nothing on this page

And it is true, there is nothing here

**Step 2:** Let check the page source. (F12 on Windows or right click > view Page Source). Uh oh sadly nothing there :(
```html
<html>
<head>
<!-- This stuff in the header has nothing to do with the level -->
<link rel="stylesheet" type="text/css" href="http://natas.labs.overthewire.org/css/level.css">
<link rel="stylesheet" href="http://natas.labs.overthewire.org/css/jquery-ui.css" />
<link rel="stylesheet" href="http://natas.labs.overthewire.org/css/wechall.css" />
<script src="http://natas.labs.overthewire.org/js/jquery-1.9.1.js"></script>
<script src="http://natas.labs.overthewire.org/js/jquery-ui.js"></script>
<script src=http://natas.labs.overthewire.org/js/wechall-data.js></script><script src="http://natas.labs.overthewire.org/js/wechall.js"></script>
<script>var wechallinfo = { "level": "natas2", "pass": "ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi" };</script></head>
<body>
<h1>natas2</h1>
<div id="content">
There is nothing on this page
<img src="files/pixel.png">
</div>
</body></html>
```

**Step 3:** Hey wait! Look at the ```html <img src="files/pixel.png">```. That's make sense right? Basic html syntax to load an image to the page. However, naughty hacker love the folder _files/_ that stores that image. Let check it out. Access _http://natas2.natas.labs.overthewire.org/files/_

**Step 4:** It somehow stores _pixel.png_ as we knew before and a _users.txt_ file. Awesome! Open the _txt_ file and Oops -- easy game.
```text
# username:password
alice:BYNdCesZqW
bob:jw2ueICLvT
charlie:G5vCxkVV3m
natas3:sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
eve:zo4mJWyNj2
mallory:9urtcpzBmH
```
