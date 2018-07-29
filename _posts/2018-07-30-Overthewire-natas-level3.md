---
layout: post
title: Overthewire Natas Level 3
subtitle: ... Write up
tags: [overthewire, natas, level1, overthewire-natas, writeup]
---

## Natas Level 3
* Username: natas3
* Password: sJIJNW6ucpu6HPZ1ZAchaDtwd7oGrD14
* URL:      http://natas3.natas.labs.overthewire.org1

**Step 1:** Let Login to the URL, you will amazingly again see the message as Level 2 did
> There is nothing on this page

**Step 2:** Awesome. Learn from experiences, I check the page source but nothing interesting there.<br>

**Step 3:** Let try to access the _robots.txt_ file. Go to this link _http://natas3.natas.labs.overthewire.org/robots.txt <br>_

**Step 4:** Cool. A Disallow folder named as _s3cr3t_.
```html
User-agent: *
Disallow: /s3cr3t/
```
**Step 5:** Access that folder _http://natas3.natas.labs.overthewire.org/s3cr3t/_. It stores a _users.txt_. Good sign right? Click on it and ...
```html
natas4:Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
```
