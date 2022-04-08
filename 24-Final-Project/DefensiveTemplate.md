# Blue Team: Summary of Operations

## Table of Contents
- Network Topology
- Description of Targets
- Monitoring the Targets
- Patterns of Traffic & Behavior
- Suggestions for Going Further

### Network Topology

![Topology](IMAGE/Final_Toology101.drawio.png)

The following machines were identified on the network:

- Name of Workstation
  - **Operating System**: Linux
  - **Purpose**: To Attack with pen-testing.
  - **IP Address**: 192.168.1.90
  - Name of VM 1
  - **Operating System**: Linux
  - **Purpose**: Wordpress Target.
  - **IP Address**: 192.168.1.110
  Name of Capstone
  - **Operating System**: Linux
  - **Purpose**: To test alerts.
  - **IP Address**: 192.168.1.105
  Name of ELK
  - **Operating System**: Linux
  - **Purpose**: To monitor alerts via the internet.
  - **IP Address**: 192.168.1.100
  Name of Workstation
  - **Operating System**: Windows
  - **Purpose**: Platform to do this lab.
  - **IP Address**: 192.168.1.100


### Description of Targets

The target of this attack was: `Target 1` (192.168.1.110).

Target 1 is an Apache web server and has SSH enabled, so ports 80 and 22 are possible ports of entry for attackers. As such, the following alerts have been implemented:

We set up rules to look for Excessive HTTP, CPU usage, and HTTP size request.

### Monitoring the Targets

Traffic to these services should be carefully monitored. To this end, we have implemented the alerts below:

#### Name of Alert 1

Excessive HTTP Errors is implemented as follows:
  - **Metric**: Packetbeat
  - **Threshold**: 5 for last 5 minutes
  - **Vulnerability Mitigated**: Block IP addresses, password strength, and closing open ports that do not be open. 
  - **Reliability**: This is a HTTP response so I will rate this as HIGH reliability. 

#### Name of Alert 2
CPU Usage  is implemented as follows:
  - **Metric**: Metricbeat
  - **Threshold**: above 0.5 for last 5 minutes
  - **Vulnerability Mitigated**: By removing CPU usage at given thresholds will mitigate a lot stress on your system.
  - **Reliability**: Because this is CPU usage not all false/positives will spike an alert even if there is no attack.

#### Name of Alert 3
HTTP Size Request is implemented as follows:
  - **Metric**: Packetbeat
  - **Threshold**: request bytes above 3500 for last 1 minute. 
  - **Vulnerability Mitigated**: Blocking and filtering the amount of HTTP traffic will slow down any DDOS attacks.
  - **Reliability**: This type of an attack will not set off alerts for false/positives because they are not reliable.


### Suggestions for Going Further (Optional)
_TODO_: 
- Each alert above pertains to a specific vulnerability/exploit. Recall that alerts only detect malicious behavior, but do not stop it. For each vulnerability/exploit identified by the alerts above, suggest a patch. E.g., implementing a blocklist is an effective tactic against brute-force attacks. It is not necessary to explain _how_ to implement each patch.

The logs and alerts generated during the assessment suggest that this network is susceptible to several active threats, identified by the alerts above. In addition to watching for occurrences of such threats, the network should be hardened against them. The Blue Team suggests that IT implement the fixes below to protect the network:
- Vulnerability 1 - Excessive HTTP Errors
  - **Patch**: TODO: E.g., _install `special-security-package` with `apt-get`_
  - **Why It Works**: TODO: E.g., _`special-security-package` scans the system for viruses every day_
  

- Vulnerability 2 - CPU Usage
  - **Patch**: TODO: E.g., _install `special-security-package` with `apt-get`_
  - **Why It Works**: TODO: E.g., _`special-security-package` scans the system for viruses every day_


- Vulnerability 3 - HTTP Size Request
  - **Patch**: TODO: E.g., _install `special-security-package` with `apt-get`_
  - **Why It Works**: TODO: E.g., _`special-security-package` scans the system for viruses every day_
