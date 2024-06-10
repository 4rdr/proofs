Vulnerability: GNU SOCIAL 2.0.1-beta0 Stored XSS via broughtby parameter

URL: Any File Upload for posting content

Payload: ```<script>alert(1)</script>```

Action to trigger: Saving the payload in the broughtby field and then visiting any page containing the stored value. for example: https://192.168.124.42/index.php/panel/user

Version: ‎GNU SOCIAL 2.0.1-beta0

Authenticated: Yes

User: Admin

Parameter: broughtby

Vendor Website: https://gnusocial.network/


Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/GNU_SOCIAL_2.0.1-beta0_Stored_XSS_via_broughtby_parameter.gif)
