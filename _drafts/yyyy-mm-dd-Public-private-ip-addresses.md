---
layout: default
title: Public and Private IP Addressing
permalink: /blog/
---

{: style="text-align:center"}
![Network Diagram](/images/Network_diagram.png)

-----

### IP Addressing 

In networking, public and private IP addresses are used for computers and routers to interface and communicate over the internet. A public IP address differs from a private IP address in that the public IP address can be accessed over the internet. A private IP address is typically assigned to connected devices behind a router and not exposed to the internet. Typically, in a home network, all connected devices, such as cell phones, tablets, Raspberry Pis, or even smart devices, like Nest thermostats, get assigned a private IP address by the router via the Dynamic Host Configuration Protocol (DHCP). These connections to the router can certainly be wired or wireless, but serve as "address points" that the router uses to direct incoming or outgoing network traffic. 

A public IP address is an assigned address provisioned by an Internet Service Provider (ISPs), such as Comcast, to routers and modems. By providing a public IP address to a router, any network traffic coming from a connected device on a home network can traverse the home network and pass through the router using the router's public IP address.

Typically private IP addresses are assigned from the Class C address block ranging from 192.168.0.0; therefore, 192.168.0.4 and 192.168.0.24 could be examples of connected devices on someone's home network. Public IP addresses for Google's DNS servers are 8.8.8.8 and 8.8.8.4. These two services are servers that are likely resolving the majority of the internet user base URL queries.
