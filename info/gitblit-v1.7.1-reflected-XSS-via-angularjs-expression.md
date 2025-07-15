CVE-2025-50977


Vulnerability: Angular Template Injection/Reflected XSS


A template injection vulnerability leading to reflected cross-site scripting (XSS) has been identified in version 1.7.1, requiring authenticated admin access for exploitation. The vulnerability exists in the 'r' parameter and allows attackers to inject malicious Angular expressions that execute JavaScript code in the context of the application. The flaw can be exploited through GET requests to the summary endpoint as well as POST requests to specific Wicket interface endpoints, though the GET method provides easier weaponization.


Version: ```v1.7.1```


Authenticated: Yes

User: Admin

Vulnerable Parameter:
```r```

Payload:
```http://172.18.0.34/summary/?r=%7b%7bconstructor%2econstructor('alert(document.domain)')()%7d%7d```

Other locations are vulnerable as well, the POST request
```http://172.18.0.34/?wicket:interface=:101:searchForm::IFormSubmitListener::```

Will work as well but is not as easily weaponized

Tested on

```v1.7.1```

but unless that parameter is fixed it may just take a newer angular version payload to work

See demo

![](https://github.com/4rdr/proofs/blob/main/gifs/gitblit-v1.7.1-reflected-XSS-via-angularjs-expression.gif?raw=true)
