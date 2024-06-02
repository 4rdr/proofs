
Vulnerability: Reflected XSS via data parameter

URL: http://192.168.124.128/textileParser?data=test<script>alert(1)</script>

Payload: test<script>alert(1)</script>

Action to trigger: None

Version: ‎v7.54 Pro

Authenticated: Yes

User: Admin (possibly others)

Vulnerable Parameter: data

Vulnerability Location:

Vendor Website: https://www.icescrum.com/


Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/icescrum__v7.54_Reflected_XSS_via_data_parameter.gif)
