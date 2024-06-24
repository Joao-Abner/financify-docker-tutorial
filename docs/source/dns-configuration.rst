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
   
   $ORIGIN financify.com.
   $TTL 300;
   @ IN SOA dns {email@domain.com}. (1 30 30 30 30);
   @ IN NS dns
   dns IN A {Virtual Machine IP Address}
   @ IN A {Core Application Container IP Address}
   web IN CNAME
   www IN CNAME @
