---
title: "Cap"
date: 2021-08-31T12:10:00+02:00
draft: false
tags: [htb]

cover:
    image: /learning_paths/ctf/htb/cap/images/cap.png# image path/url
    relative: false # when using page bundles set this to true
---
# Recon 

## Ping
First of all what I'm going to do is use **ping** to know if the machine is up. 
![ping](images/ping.png)


In this case, I don't need to know the operating system of the machine because HTB already gives us that information.
Nevertheless, A cool tip about ping is that it allows you to know more or less the **operating system** used by the 
machine base on the **ttl** (I will leave a link to a page to know more about this in the reference). So like the 
ttl is 64 I asume that the machine uses **linux**.

## Nmap
### PortScan
After use ping, I usually use **nmap** to search for open ports using the following options:
- **-p-** With this flag I'm specifying that the scan will be performed on all ports
- **--open** Using this flag I'm specifying that I only want to show open ports
- **-T5** With this flag I'm specifying that the scan be as fast as possible( The faster the louder the scan)
- **-v** With this flag I'm indicating that the results are shown on the screen as the are found
- **-n** With this flat I'm indicating that I dont't want DNS resolution
- **-oN portscan** To export the result to the portscan file in the nmap format
![portscan](images/nmap.png)

### Port services found
After knowing which ports are open, I will find out what services they are using.

- **-sC** To use basic enumeration scripts
- **-sV** To display the services found on the specified ports 
- **-p21,22,80** To specifying ports
![services](images/nmapServices.png)


# References
[https://subinsb.com/default-device-ttl-values/](https://subinsb.com/default-device-ttl-values/)