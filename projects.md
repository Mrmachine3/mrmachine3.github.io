---
layout: page
#title: Projects
permalink: /projects/
---

![banner](/images/banner.png)

----

##### [Raspberry Pi (RPi) - Security Camera](https://github.com/Mrmachine3/RPiSec_Cam/blob/master/README.md)
This github repository contains project files related to building and deploying a Raspberyy Pi for use as a security camera with the Raspbian opewith the Raspbian. The Raspberry Pi will host a Flask webserver that will serve the live video frames and also help control the pan-tilt server mechanism to remotely control the angle of the camera.
***

##### [4RPi Cluster - ELK Stack](https://github.com/Mrmachine3/4RPi_ELKstack/blob/master/README.md)
This github repository contains project files related to building a four node Raspberry Pi cluster and automating the configuration of the cluster to host an Elasticsearch, Logstash, Kibana stack, commonly referred to as an ELK stack. The purpose of this is to monitor web traffic on my local area network (LAN) by analyzing packet captures and event logs from endpoint devices, such as routers, firewalls, and connected devices such as a ***[RPiZ security camera] [1]***.

***
#### Other Projects
##### [RPi Kali Box](https://mrmachine3.github.io/404.html)
<!--##### [RPi Kali Box](https://github.com/mrmachine3)-->
*Project concept taken from* __*[Official Kali Website] [3]*__

This project is intended to create a standalone, headless device that users can access remotely via secure shell (SSH) protocol to execute remote commands on the terminal. Example use cases could be to deploy the RPi within your own personal local area network and run packet analysis tools, like wireshark, netcat, kismet, or even custom python scripts.

##### [Jupyter Droplet](https://mrmachine3.github.io/404.html)
*Project concept taken from* __*[Digital Ocean Tutorials] [4]*__

This project is intended to host an open source jupyter notebook web application on the cloud using Ditigal Ocean droplets. Example use cases could be to programmatically cleanse or transform network capture data or infrastructure event logs for data visualization or machine learning models.

[1]: https://github.com/mrmachine3
[2]: https://www.kerberos.io
[3]: https://www.kali.org/tutorials/secure-kali-pi-2018/
[4]: https://www.digitalocean.com/community/tutorials/how-to-set-up-jupyter-notebook-for-python-3
