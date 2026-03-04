\# Experiment 002 — DNS cache behavior



\## Goal



Observe how Windows stores and clears DNS records locally.



\## Test



1\. Display the current DNS cache:



```

ipconfig /displaydns

```



This shows all domain names your system has recently resolved.



2\. Flush the DNS cache:



```

ipconfig /flushdns

```



3\. Visit a website (for example google.com) and check the cache again:



```

ipconfig /displaydns

```



\## Observation



Windows stores DNS responses locally so the system does not need to ask the DNS server every time a site is visited.



This speeds up browsing but can also cause problems if a cached entry becomes outdated or incorrect.



\## Fix



When troubleshooting DNS-related issues, clearing the cache can help:



```

ipconfig /flushdns

```



This forces Windows to request fresh DNS information from the DNS server.



\## Reflection



Understanding DNS caching helped me see why some websites keep failing even after the network seems fixed. The system may still be using outdated cached DNS records.

