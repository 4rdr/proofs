CVE-2025-50975



IPFire 2.29’s web-based firewall interface (firewall.cgi) fails to sanitize several rule parameters—such as PROT, SRC_PORT, TGT_PORT, dnatport, key, ruleremark, src_addr, std_net_tgt, and tgt_addr—allowing an authenticated administrator to inject persistent JavaScript. This stored XSS payload is executed whenever another admin views the firewall rules page, enabling session hijacking, unauthorized actions within the interface, or further internal pivoting. Exploitation requires only high-privilege GUI access, and the complexity of the attack is low.



Stored XSS

```
https://192.168.124.92:444/cgi-bin/firewall.cgi
```

- PROT
- SRC_PORT
- TGT_PORT
- dnatport
- key
- ruleremark
- src_addr
- std_net_tgt
- tgt_addr

!!! There is other XSS for this version of IPFire.  But this is the easiest to demo.

Demo:

![](https://github.com/4rdr/proofs/blob/main/gifs/IPFire-2.29-Stored-XSS-via-Firewall.gif?raw=true)
