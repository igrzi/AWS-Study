# DNS

## What it is?

The ***Domain Name System*** converts readable domain names to **IP addresses**!

## DNS Searches

### Direct Lookup
- Converts a hostname to an IP Address

### Reverse Lookup
- Converts a IP Address to a hostname

## DNS Response

### Authoritative

This response comes directly from a DNS Server, with this type of response you can trust the accuracy of the information provided to you.

### Non-Authoritative

This response comes from a DNS server that has cached the DNS information, but isn't the source for the domain. This may have accurate information, but it may not be the most recent information.

## DNS Register Types

### SOA (Start of Authority)
- It's the first register in a DNS Zone

- Has information about the domain, like primary/secondary server, TTL, zone file, and others

### NS (Name Server)
- Defines which DNS server has permission to answer the lookup

### MX (Mail eXchange)
- Defines the email servers and their respective priority

### A (Host)
- Maps the hostnames to IP Addresses

### CNAME (Alias - Canonical Name)
- Defines an alias to other hostnames to the same domain

### PTR (Pointer - Reverse)
- Defines the reverse function of type A register (maps an IP to a hostname)