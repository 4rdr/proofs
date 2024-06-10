Vulnerability: GNU SOCIAL 2.0.1-beta0 Stored XSS via name parameter

URL: https://192.168.124.42/index.php/panel/site

Payload: ```<script>alert(1)</script>```

Action to trigger: Saving the payload in the name field and then visiting any page containing the stored value. For example: https://192.168.124.42/index.php/main/login

Version: ‎GNU SOCIAL 2.0.1-beta0

Authenticated: Yes

User: Admin

Parameter: name

Vendor Website: https://gnusocial.network/


Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/GNU_SOCIAL_2.0.1-beta0_Stored_XSS_via_name_parameter.gif)
