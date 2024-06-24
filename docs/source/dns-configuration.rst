=================
DNS Configuration
=================

DNS configuration is crucial for CRUD projects, ensuring smooth internet connectivity and optimal performance by translating domain names into IP addresses, enhancing website accessibility and speed.

**DNS (Domain Name System)**

The Domain Name System (DNS) acts as an internet directory, translating human-readable domain names into IP addresses that computers understand. This translation is essential for browsers to locate websites based on the URLs entered by users.

For the purpose of this project, we utilized a virtual machine equipped with a Bind9 server to simulate a local DNS environment. Bind9 is a widely-used DNS software that allows us to define custom DNS records for our application domains.

Here's an overview of how we configured Bind9 to resolve the application's domain names to the core application container's IP address:


=======================
Bind9 Configuration
=======================

We configured Bind9 to give the browser the core app container IP whenever it searched for the application domains (see Installation). It looks like this:

.. code-block:: none

   $TTL 300;
   @ IN SOA dns {email@domain.com}. (1 30 30 30 30);
   @ IN NS dns
   dns IN A {Virtual Machine IP Address}
   @ IN A {Core Application Container IP Address}
   web IN CNAME @
   www IN CNAME @

- `$TTL 300;`: Specifies the default time-to-live (TTL) for DNS records, in seconds. This value determines how often the DNS resolver should refresh its cache for this zone.

- `SOA (Start of Authority)` record: Provides authoritative information about the DNS zone, including the primary name server (`dns`), email of the administrator (`{email@domain.com}`), and several timers related to zone transfers and refresh intervals.

- `NS (Name Server)` record: Declares the authoritative name server for the domain.

- `A (Address)` records: Map the domain names (`@`, `dns`, `web`, `www`) to their corresponding IP addresses. The `@` symbol represents the root domain, while `dns`, `web`, and `www` are subdomains pointing to the root domain.

- `CNAME (Canonical Name)` records: Alias one name to another. Here, both `web` and `www` are aliases for the root domain (`@`).

By configuring Bind9 in this manner, we ensured that any attempt to access the application's domain names would correctly resolve to the IP address of the core application container, facilitating seamless access to the application.
