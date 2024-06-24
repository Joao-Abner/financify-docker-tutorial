=================
DNS Configuration
=================

This section delves into the additional configurations required for the application beyond basic setup. While these configurations are not strictly necessary for local development, they play a crucial role in enhancing the application's accessibility and security, particularly when deployed in a production environment. Specifically, we'll cover DNS configuration and SSL certificate management.

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