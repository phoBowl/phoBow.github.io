---
layout: post
title: Overthewire Natas Level 1
subtitle: ... Write up
tags: [overthewire, natas, level1, overthewire-natas, writeup]
---

## Natas Level 1
* Username: natas1
* Password: gtVrDuiDfck831PqWsLEZy5gyDz1clto
* URL:      http://natas1.natas.labs.overthewire.org1

**Step 1:** Login to URL, you will see the message
>You can find the password for the next level on this page, but rightclicking has been blocked!


**Step 2:** Cool. They blocked us to access the page source. Let try another way to access the page source. F12 on windows is a shortcut. Give it a try. Expand the ```html <div id="content">``` and Yay! Again password still in the comment of the page source
```html
    <!--The password for natas2 is ZluruAthQk7Q2MqmDeTiUij2ZvWy2mBi -->
```
