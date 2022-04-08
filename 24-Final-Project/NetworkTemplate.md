# Network Forensic Analysis Report

## Time Thieves 

1. What is the domain name of the users' custom site? 

            Frank-n-Ted-DC.frank-n-ted.com

###### We ran this curl command and found the ip address of Frank and Ted. The curl was a way to put the pcap file into wireshark.

###### The command we ran: curl -L -o pcap.pcap http://tinyurl.com/yaajh8o8

![wiresahrk](IMAGE/wireshark-curl.png)

###### To get to find Frank and Ted we ran ip.src == 10.6.12.0/24

        After running this we realized that Frank and Ted were using IP 10.6.12.12 to gain access to the internet. 

![wiresahrk](IMAGE/domain-name.png)



2. What is the IP address of the Domain Controller (DC) of the AD network?

            IP address: 10.6.12.12

3. What is the name of the malware downloaded to the 10.6.12.203 machine?

            We found a suspicious GET HTTP file called june11.dll After finding this we exported it using export objects and saved the HTTP info and then uploaded it to Virustotal.com to find the Ad-Ware virus Trojan.Mint.Zamg.O 


   ##### Once we found the IP address and the TimeStamp we clicked on the line and then went to file tab and selected export objects then selected HTTP. Once that was done we were able to filter using the word june and then saved the file and ran it virustotal.com to find the malware Trojan.Mint.Zamg.O

   ![wiresahrk](IMAGE/june11.png)

   


4. Upload the file to [VirusTotal.com](https://www.virustotal.com/gui/). 


5. What kind of malware is this classified as?

            Trojan name: Trojan.Mint.Zamg.O


###### Here we find the malware virus Trojan.Mint.Zamg.O classified as Ad-Ware

   ![wiresahrk](IMAGE/trojan.png)

---

## Vulnerable Windows Machine

1. Find the following information about the infected Windows machine:
    - Host name

            ROTTENRDAM-PC.mind-hammer.net we found this by running ip.addr == 172.16.4.0/24 and http

    - IP address

            172.16.4.205

    - MAC address

            00:59:07:b0:63:a4


![rotten dam pc](IMAGE/rottendam-pc.png)
    
2. What is the username of the Windows user whose computer is infected? We found a lot of information on this website here. 

Click to go to: [Paloalto](https://unit42.paloaltonetworks.com/using-wireshark-identifying-hosts-and-users/ )



        matthijs.devries To find this we used ip.addr == 172.16.4.205 && kerberos.CNameString


![CName](IMAGE/CName.png)


3. What are the IP addresses used in the actual infection traffic? We used the same path (ip.addr == 172.16.4.205 && kerberos.CNameString) to find the packets, we went into Statistics and then conversations. The tricky part was to arrow up on the Packets tab to get the higher packet volume to the top.

###   *Traffic from 185.243.115.84 infected 172.16.4.205*

        We found 4 IP addresses that look to be infected because of the high volume of packets. 
        185.243.115.84 and 172.16.4.205 and 64.187.66.143 and 23.43.62.169

![Packets](IMAGE/packets.png)


4. As a bonus, retrieve the desktop background of the Windows host.

        We went to the same path as above (ip.addr == 172.16.4.205 && kerberos.CNameString) and then went to export objects and saved file to desk top and wambam. see pics below. 

![img file](IMAGE/img-file.png)

![bird](IMAGE/bird-shot.png)

---

## Illegal Downloads

1. Find the following information about the machine with IP address `10.0.0.201`:
    - MAC address

            00:16:17:18:66:c8  We ran this code to find this ip.addr == 10.0.0201 && dhcp

![MAC addr](IMAGE/MAC-addr.png) 

    - Windows username

            We used ip.src == 10.0.0201 && Kerberos.CNameString finding elmer.blanco

![Elmer Fudd](IMAGE/elmer.png)


    - OS version

            We ran this code to find the OS version. ip,src == 10.0.0.201 && http.request to get the Windows NT 10.0 version. 


![os-version](IMAGE/os-version.png)

2. Which torrent file did the user download?

        We ran this code to find the Torrent file. ip.src == 10.0.0.201 && http.request.method.uri contains ".torrent"  and as you can see in the high-lighted section we found the Torrent file Betty Boo.


![Torrent-1](IMAGE/torrent-1.png)

        Then we put this information into a export file and saved it the desktop. After saving it to the desktop we can open it and see the betty boo picture show. The movie Betty Boo Show was downloaded on the Reservation.avi
        See pictures below to verify conclusion. 

![public-1](IMAGE/public-1.png)

![public-2](IMAGE/public-2.png)

![export](IMAGE/export-objects.png)

![saved](IMAGE/saved-file.png)

![betty boo](IMAGE/betty-boo.png)

