---
layout: post
title: Overthewire Natas Level 0
subtitle: ... Write up
tags: [overthewire, natas, level0, overthewire-natas, writeup]
---
## Natas Level 0
* Username: natas0
* Password: natas0
* URL:      http://natas0.natas.labs.overthewire.org

**Step 1:** Access the URL above, enter username and password to login
**Step 2:** We will see a message _"You can find the password for the next level on this page."_. Let check the page source by right click on your browser and choose _View Page Sourse_.
**Step 3:** Hooray! Easy right? The password is obviously in the comment of html file
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
<script>var wechallinfo = { "level": "natas0", "pass": "natas0" };</script></head>
<body>
<h1>natas0</h1>
<div id="content">
You can find the password for the next level on this page.
<!--The password for natas1 is gtVrDuiDfck831PqWsLEZy5gyDz1clto -->
</div>
</body>
</html>
```
