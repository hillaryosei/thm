## What is DNS?
* Domain Name Sysem (DNS): simple way to communicate with devices on the internet without remembering IP addresses

## Domain Hierarchy
* Top-Level Domain (TLD): most righthand part of a domain name (ex: the TLD for google.com is .com) 
* Types of TLD are gTLD (Generic Top Level) and ccTLD (Country Code Top Level Domain)
   * gTLD: tells use what the domain name's purpose is (ex: .com is for commercial purposes, .org for an organization, .edu for education, .gov for government)
   * ccTLD: used for geographical purposes (ex: .ca for sites based in Canada)
* Due to high demand, there's an influx of new gTLDS like .online, .club, .tech, etc
* In URLs like facebook.com, facebook is the second level domain
* The second-level domain is limited to 63 characters + the TLD & can only use a-z, 0-9, and hyphens (can't start or end with hyphens or have consecutive hyphens)
* The subdomain sits on the left hand side of the second-level domain using a period to separate it (ex: in admin.tryhackme.com, the admin part is part of the subdomain)
* Subdomain has same restrictions as second-levle domain
* There can be multiple subdomains spit with periods (ex: jupiter.servers.tryhackme.com), but the length must be 253 characters or less

## DNS Record Types
* A Record: resolve to IPv4 addresses
* AAAA Record: resolves to IPv6 addresses
* CNAME Record: resolve to another domain name
* MX Record: resolve to address of servers that handle the email for the domain you're querying
* TXT Record: free text firelds where any text-based data ccan be stored. Used to list servers that have the authority to send an email on behalf of the domain, verify ownerships of the domain name when signing up for third-party services

# Making A Request
* Here's what happens when you make a DNS request:
  * When the domain name is requested, the device checks its local cache to see if the address has been looked up recently. If it hasn't a request to the Recursive DNS server is made
  * The Recursive DNS server has a local cache of recently searched domain names. If there's a result found, it's sent back to the device. If not, request is redirected to the Root DNS server
  * The root server redirects user to the correct top-level domain server
  * The TLD server rholds records for where to find the authoritative (aka nameserver) server to answer the DNS request
  * An authoritative DNS server is responsible for storing DNS records for a particular domain name and where any updates to a domain name DNS records are made. Depending on record type, DNS record is sent back to Recursive DNS server where a local copy is cached for future requests and relayed back to the original client who made the request. DNS records have TTL (Time to Live value), which records in seconds how long a DNS record should be cached for 
