\# Experiment 001 — IP works but domain fails



\## Goal



Understand the difference between network connectivity and DNS resolution.



\## Test



1\. Ping an IP address:



```

ping 8.8.8.8

```



Result: success



2\. Ping a domain name:



```

ping google.com

```



Result: fails



\## Explanation



If the IP ping works but the domain ping fails, the machine has network connectivity but cannot resolve domain names.



This usually indicates a DNS configuration problem.



\## Fixes to test



Check DNS configuration.



Flush the DNS cache:



```

ipconfig /flushdns

```



Restart the network adapter if necessary.



\## Reflection



This experiment helped me understand why users often say "the internet is broken" even when the network connection itself is actually working. The issue can simply be DNS resolution failing.

