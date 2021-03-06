## Automated ELK Stack Deployment

The files in this repository were used to configure the network depicted below.


![TODO: Update the path with the name of your diagram](IMAGE/network2.drawio3.png) 

These files have been tested and used to generate a live ELK deployment on Azure. They can be used to either recreate the entire deployment pictured above. Alternatively, select portions of the `.yml` file may be used to install only certain pieces of it, such as Filebeat.



        Files have been edited and updated.
            Click On The Links Below.

  [Filebeat-Config](filebeat-configuration.yml)

  [Filebeat-Playbook](filebeat-playbook.yml)

  [Metricbeat-Configurat](metricbeat-configuration.yml)

  [Metricbeat-Playbook](metricbeat-playbook.yml)

  [Install-Elk-Playbook](install-elk.yml)

  [Host](hosts.yml)

  [roulette_dealer_finder_by_time](roulette_dealer_finder_by_time.sh)

  [Dealers_working_durring_losses](Dealers_working_durring_losses.sh)

This document contains the following details:
- Description of the Topology

![Jump-Box](IMAGE/Jump-Box-Topology.png)

![Elk-Network](IMAGE/Elk-Network-Topology.png)

![RedTeam-Network](IMAGE/RedTeamNetwork-Topology.png)


- Access Policies
- ELK Configuration
  - Beats in Use
  - Machines Being Monitored
- How to Use the Ansible Build


### Description of the Topology

The main purpose of this network is to expose a load-balanced and monitored instance of DVWA, the Damn Vulnerable Web Application.

Load balancing ensures that the application will be **`highly accessible`**, in addition to restricting any **`inbound traffic`** to the network.
- _TODO: What aspect of security do load balancers protect? What is the advantage of a jump box?_

      They are closed to inbound traffic unless opened by admins. It also will shift traffic somewhere else.
      ElkStack is used to monitor mega data and proccess this information to let admins monitor the daily logs and machines running. 
      The advantage of the Jump-Box is to manage devices through the Jump-Box in seperate security zones.

Integrating an ELK server allows users to easily monitor the vulnerable VMs for changes to the **`LOGS`** and system **`TRAFFIC`**.
- _TODO: What does Filebeat watch for?_

        Monitors and collects Log files and sends them to elkstack for proccessing or indexing. 

        
![FileBeat](IMAGE/filebeat.png)

- _TODO: What does Metricbeat record?_

        Monitors and collects data from specific service, such as Redis and MySQL and so on. The metricbeat specifies how to connect, how often to collect metrics and which metric to collect. 
        A good example of metricbeats is that it monitors and analyzes system CPU, Memory and Load.In Docker metricbeat can monitor container performance metrics. 

![FileBeat](IMAGE/metricbeat.png)

The configuration details of each machine may be found below.
_Note: Use the [Markdown Table Generator](http://www.tablesgenerator.com/markdown_tables) to add/remove values from the table_.

| Name     | Function          | IP Address  | Operating System |
|----------|-------------------|------------ |------------------|
|Phillip   | Local Host        | 69.8.223.334| MacOs            |
|Jump Box  | Gateway           | 10.0.0.4    | Linux Ubuntu18.4 |
|Web-1     | DVWA Server       | 10.0.0.5    | Linux Ubuntu18.4 |
|Web-2     | DVWA Server       | 10.0.0.7    | Linux Ubuntu18.4 |

### Access Policies

The machines on the internal network are not exposed to the public Internet. 

Only the **`Jump-Box Provisioner`** machine can accept connections from the Internet. Access to this machine is only allowed from the following IP addresses:
- _TODO: Add whitelisted IP addresses_
          
          Jump-Box public IP: 20.106.143.99

Machines within the network can only be accessed by **`Jump-Box Provisioner`**.
- _TODO: Which machine did you allow to access your ELK VM? What was its IP address?_
          
          Jump-box private IP: 10.0.0.4 

A summary of the access policies in place can be found in the table below.

| Name        | Publicly Accessible | Allowed IP Addresses|
|-------------|---------------------|---------------------|
| Jump Box    | Yes | 10.0.0.0/16 - 10.1.0.0/16 |
| Phillip     | Yes | 10.0.0.0/16 - 10.1.0.0/16 |
| Web-1       | No  | 10.0.0.0/16 - 10.2.0.0/16 |
| Web-2       | No  | 10.0.0.0/16 - 10.2.0.0/16 |
| Web-3       | No  | 10.0.0.0/16 - Out of Service |

### Elk Configuration

Ansible was used to automate configuration of the ELK machine. No configuration was performed manually, which is advantageous because...
- _TODO: What is the main advantage of automating configuration with Ansible?_

        Pass te buck$$$ automation is the future and if you can free up admins for other work, moving forward, the furture will look brighter. Automating daily tasks is best practice to elliminate errors also. By using the same playbooks updating and installing web servers to the network will be much faster and easier.

The playbook implements the following tasks:
- _TODO: In 3-5 bullets, explain the steps of the ELK installation play. E.g., install Docker; download image; etc._
- ... Install Docker add containers as needed. **intall docker .io, python3, docker module**
- ... Install Ansible configure playbooks and config files. **configure elk server and memory increase. download elk docker container and configure it.** 

The following screenshot displays the result of running **`docker ps`** after successfully configuring the ELK instance.

![TODO: Update the path with the name of your screenshot of docker ps output](IMAGE/elk_docker_ps.png)

### Target Machines & Beats
This ELK server is configured to monitor the following machines:
- _TODO: List the IP addresses of the machines you are monitoring_

        Web-1 10.0.0.5 and Web-2 10.0.0.7

We have installed the following Beats on these machines:
- _TODO: Specify which Beats you successfully installed_

      Filebeats and metricbeats

These Beats allow us to collect the following information from each machine:
- _TODO: In 1-2 sentences, explain what kind of data each beat collects, and provide 1 example of what you expect to see. E.g., `Winlogbeat` collects Windows logs, which we use to track user logon events, etc._

**`system log and appliction detail which includes web traffic gathered by filebeats.
   CPU, Memory, Disk, Network, specifically gathering with metricbeats.**`




### Using the Playbook
In order to use the playbook, you will need to have an Ansible control node already configured. Assuming you have such a control node provisioned: 

SSH into the control node and follow the steps below:
- Copy the` filebeat-playbook.yml and metricbeat-playbook.yml` file to` a nano filebeat-playbook.yml and metricbeat-playbook.yml in my /etc/ansible/files directory`.
- Update the` filebeat-config.yml and metricbeat-config.yml`file to include...`IP address of Elk server 10.1.0.51 on specific ports`
- Run the playbook, and navigate to` Kibana (http://20.80.180.39:5601/app/kibana)` to check that the installation worked as expected.

![Beats](IMAGE/added_data.png)

<br>

![Beats](IMAGE/Metricbeat_data.png)



_As a **Bonus**, provide the specific commands the user will need to run to download the playbook, update the files, etc._

        cd /etc/ansible/files then run theses below
        ansible-playbook install-elk.yml
        ansible-playbook filebeat-playbook.yml and ansible-playbook metricbeat-playbook.yml
        http://20.80.180.39:5601/app/kibana