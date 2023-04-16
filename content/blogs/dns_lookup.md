---
title: Behind the scenes of DNS lookup.
type: page
# description: Click on me to see the content.
topic: career
author: Noble Varghese
---

We use the internet to search for a lot of content online and visit a lot of those websites everyday. But did we know how it actually takes us to those websites ? 
Well that is where a concept called DNS lookup comes in. 

🔎 What is DNS Lookup?
We access the websites by name (say www.google.com). But computers only understand addresses in the form of numbers called IP addresses. Hence, the browser generally takes some extra steps in order to translate the domain name to the IP address. This is called a DNS Lookup.

👀 How does DNS lookup work?
When a user types in a website name (say www.google.com) and press enter the request gets routed to the DNS resolver. 
- The DNS resolver first searches the local cache in the computer that contains the most recent searches and attempts to map the IP.
- If there is no matching result, then the resolver searches the Internet Service Provider(ISP) and its DNS and tries to locate the IP in its cache.
- If the results are not matching, then the lookup happens on the root servers. The root server is the top level on the DNS hierarchy. The root server will contain the IP address to the website we are looking for, but it contains the route to the Top Level Domain server where the next lookup must happen.
- The TDL routes the request to the authoritative name server that contains the IP address to which the request is to be sent. The authoritative name server contains the information of all the nameservers and all the DNS records. Cloud providers across the world provide this server the ability, and you can use a multitude of them.
- The authoritative name server sends the IP address to the DNS resolver and the DNS resolver stores it in the cache. 
- The DNS resolver then sends it to the web browser and it takes the user to the required website. They  also store the data in the local cache so that it becomes easier to resolve the website next time.

🚀 Once the DNS lookup is done, the browser initiates a TCP connection with the web server. The web server then sends back the content that gets rendered on the browser. This is the entire working of the DNS lookup. 

![](https://noble-varghese.github.io/portfolio/images/dns_lookup.png)