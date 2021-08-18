1.	I copied the IP’s to a text file and ran them in this fping < fping.txt and got the results below.

sysadmin@UbuntuDesktop:~/Desktop$ fping < fping.txt 
<br>
167.172.144.11 is alive
<br>
15.199.151.91 is unreachable
<br>
15.199.158.91 is unreachable
15.199.141.91 is unreachable
15.199.131.91 is unreachable
15.199.121.91 is unreachable
15.199.111.91 is unreachable
15.199.100.91 is unreachable
15.199.99.91 is unreachable
15.199.98.91 is unreachable
15.199.97.91 is unreachable
15.199.96.91 is unreachable
15.199.95.91 is unreachable
15.199.94.91 is unreachable
11.199.158.91 is unreachable
11.199.141.91 is unreachable
11.199.131.91 is unreachable
11.199.121.91 is unreachable
11.199.111.91 is unreachable
11.199.100.91 is unreachable
11.199.99.91 is unreachable
11.199.98.91 is unreachable

I believe that Layer 3 the network layer would be at risk. This is where the IP and routing lives.

![fping](IMAGE/fping.png)

<br>

2.  Port 22/TCP is open. This would be done on layer 4 transport. First part of a 3 way hand shake to establish connection. Putting a firewall to protect this port would be nice. 



![port](IMAGE/nmap.png)


3.	sysadmin@UbuntuDesktop:~$ nslookup 98.137.246.8
8.246.137.98.in-addr.arpa	name = unknown.yahoo.com.

Authoritative answers can be found from:

I would put this on layer 7 as an application. 

![root](IMAGE/inasroot.png)

![root](IMAGE/yahoo.png)

![root](IMAGE/etc.png)

![root](IMAGE/Foundfile.png)

![root](IMAGE/nanohosts.png)

![root](IMAGE/nanopacketinfo.png)

![root](IMAGE/wireshark.png)


<br>

I will say that this one is on layer 7. 

<br>

My final result I do have the blues Mr. Hacker lol.......

![root](IMAGE/mrhacker.png)

<br>

ARP result using arp filter to find mac address of rollingstone.com IP address. 

<br>

![root](IMAGE/arp.png)







This is link I found 
https://drive.google.com/file/d/1ic-CFFGrbruloYrWaw3PvT71elTkh3eF/view?usp=sharing

