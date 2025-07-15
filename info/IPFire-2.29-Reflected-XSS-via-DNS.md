CVE-2025-50976



IPFire 2.29’s DNS management interface (dns.cgi) fails to properly sanitize user-supplied input in the NAMESERVER, REMARK, and TLS_HOSTNAME query parameters, resulting in a reflected cross-site scripting (XSS) vulnerability.





```
https://192.168.124.92:444/cgi-bin/dns.cgi
```
- NAMESERVER
- REMARK
- TLS_HOSTNAME

!!! There is other XSS for this version of IPFire. But this is the easiest to demo.

Demo:

![](https://github.com/4rdr/proofs/blob/main/gifs/IPFire-2.29-Reflected-XSS-via-DNS.gif?raw=true)
