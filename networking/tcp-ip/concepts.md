### Name Servers
DNS is client-server system
Servers are also called as name servers
Client are called resolvers, and they query name servers

Resolver ==query==> Name Server


### Resolver
Resolvers are client half of DNS' client-server system.
Resolvers are part of Operating system such as Windows, Linux, Mac

Resolvers take request from application and translate them to DNS queries.
And passes the response from DNS to application

### Resolution
Resolution is the process by which resolver and name server cooperate to locate data stored in DNS

### Message Format
Queries and Message use UDP portocol with below syntax

### A Records
 The A originally stood for address. And it's tempting to call A records address records.

###  AAAA Record
 The IPv6 equivalent to the A record is the Quad A record, which has the type mnemonic AAAA. It has four A's because a 128-bit IPv6 address is four times as long as the 32-bit IPv4 address in an A record.

### NSLookup Record
nslookup is standard dns query tool.