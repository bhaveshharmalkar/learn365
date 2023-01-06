<h2> Day 4 : Recon 12 - Recon 16 exercise on Pentester Lab </h2>

</br>

#### 1. Check if the load balancer has been configured.
```
Serving requests for a single application can be done by multiple backends. It can pay off to send the same request multiple times 
to check if any load balancers are set up.
```

#### 2. DNS records
```
You must check any information in the DNS records when performing pentesting. There are multiple types DNS records such as A, 
AAAA, CNAME, MX, NS, TXT, PTR, SOA
> nslookup -type=any example.com 8.8.8.8  
> dig -t any example.com
```

#### 3. DNS Zone Transfer
```
Zone transfer means whenever there is a change in the zone data on the primary DNS, then the changes have to be shared with the 
secondary DNS of the zone. It has two types 'Asynchronous Transfer Full Range(AXFR)' and 'Incremental Zone Transfer(IXFR)'
However, occasionally it has weaknesses because to improper configuration.

Check if DNS zone tranfer happened
> dig axfr @ns_server domain_name
> host -t axfr domain_name ns_server
```

#### 4. Check for DNS BIND version
```
Check for BIND versions to see if any outdated versions are running on it or if there are any known vulnerabilities.
> dig -c ch -t any @ns_server version.bind
```
