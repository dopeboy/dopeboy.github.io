---
layout: post
title: Scanning with the Brother HL-2280DW on Linux
image: bot.png
---

When scanning on Linux using the Brother HL-2280DW, I've relied on reformedmusing's [invaluable guide](https://reformedmusings.wordpress.com/2013/01/26/setting-up-a-brother-hl-2280dw-in-ubuntu-12-10/) many times. In the guide, you must know the IP of the Brother machine in order to setup the scanner. If you're in a shared office setting like me where you don't have access to the router, this can be difficult. Here's a quick tip:

1.  Find the subnet you're on by finding your internal IP: <br/><br/> 
```ip route get 8.8.8.8 | awk '{print $NF; exit}'```<br/><br/>Say you get 192.168.1.8. Probably a safe assumption the printer is on 192.168.1.* <br/><br/>
2.  Use `nmap` to find all the hosts on your subnet. `nmap` will also spit out nodenames. Per Brother's [documentation](https://www.brother-usa.com/VirData/Content/en-US%5CLabelPrinters%5CConsumer%5CNetworkUsersManual%5CNUG_QL710W_720NW_EN.pdf):

>The node name appears in the current BRAdmin Light window. The default node name of the print server
in the printer is “BRNxxxxxxxxxxxx” or “BRWxxxxxxxxxxxx”. (“xxxxxxxxxxxx” is based on your printer’s
MAC Address / Ethernet Address.)

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;So run:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;```nmap -sP 192.168.1.0-255 | grep "BR\(W\|N\)" | awk '{print $NF; exit}' | tr -d '()'```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;That will return the IP that you can feed into the brsaneconfig4 command. 

Happy scanning.
