# Red Team: Summary of Operations

## Table of Contents
- Exposed Services
- Critical Vulnerabilities
- Exploitation

### Exposed Services

Nmap scan results for each machine reveal the below services and OS details:

```bash
$ nmap -sC -sV 192.168.1.110

```

![nmap Target 1](IMAGE/nmaptarget-1.png)

This scan identifies the services below as potential points of entry:
- Target 1
  - Port 22/SSH
  - Port 80/HTTP
  - Port 111/rpcbind

_TODO: Fill out the list below. Include severity, and CVE numbers, if possible._

The following vulnerabilities were identified on each target:
- Target 1
  - List of
  - Critical
  - Vulnerabilities

_TODO: Include vulnerability scan results to prove the identified vulnerabilities._

### Exploitation

The Red Team was able to penetrate `Target-1` and retrieve the following confidential data:

We ran a enumeration scan on wordpress site. Our results are below.

![enumeration](IMAGE/wpscan-1.png)

![enumeration](IMAGE/wpscan-2.png)

After finding the user names we ran these thru hydra to find passwords. 

      The Command used for Hydra:
      hydra -t 1 -l michael -P 
      /usr/share/john/password.lst 
      -vV 192.168.1.110 ftp



![hydra 1](IMAGE/hydra-1.png)

![hydra 2](IMAGE/hydra-2.png)


### As we went through these vulnerabilities we found several ways to find the issues on hand. Some were done through the command line and others were done through the browser as you can see here with flag-2.

![Flag](IMAGE/flag-2.png)

### The next flag we found there were two different ways to finding this issue one was through the browser and the other we ran through the command line and found the footer with the flag-1 in it.

![Flag](IMAGE/flag-1.png)

![Flag](IMAGE/flag-1.1.png)

### After finding those flags we started looking for some more. We found the hash keys for Michael and Steven. We dumped them into a shell and ran John to find Stevens pass word of pink84. Using this information we were able to get into target one and take privilege as Steven. 

##### Here are the hashes we found:

![Flag](IMAGE/wp-hashes.png)

##### Then we dumped them into here to find secret password for Steven:

##### Using command: mysql -u root -p wordpress we were able to find databases and tables with access to flags 3 and 4.

![Flag](IMAGE/DB-dump-3.png)

##### We used code: show databases; to view list of databases. Then we choose: use wordpress database. then to view tables we ran: show tables; Then from there we wanted to view tables for insight and ran: select * from wp_posts and found flags 3 and 4. We ran a few other tables to see if other flags were there. 

![Flag](IMAGE/DB-dump-2.png)

![Flag](IMAGE/DB-dump-1.png)

##### This is where we found the password. We ran: nano wp-config.php to open this file.

![Flag](IMAGE/DB-password.png)

##### This is how we gained access to root for Steven.
##### Command ran to gain access: sudo python -c 'import pty;pty.spawn("/bin/bash");'
##### This string of code is to Spawn a shell script, the hardest thing on the system because it uses so much CPU if not monitored could crash system.

![Flag](IMAGE/privalage-steven.png)

##### After running John and finding the password below is a shot of this.
##### Putting the hashes into a text file: touch wp_hashes.txt we were able to run John: john wp_hashes.txt seeing that it found one password we ran: john -show wp_hashes.txt to find pink84

![Flag](IMAGE/john-hash.png)

##### We were then able to gain access of privileged use of Target-1.
##### Command used: ssh steven@192.168.1.110 then entered password found pink84.

![Flag](IMAGE/in-as-steven.png)
