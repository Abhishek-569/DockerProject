# DockerProject
This is my first project on Docker which I Integrated with PostgreSQL( RDMS) and Odoo(business management software )running both on different Docker O.S. WISH ME LUCK.:smile:
 
I learned about this Awesome tool Docker on i internet first.Further enquiry led me to LIVE Instrucctor led live training by  [Mr. Vimal Daga Sir](https://www.linkedin.com/in/vimaldaga/) for free under their [IIEC RISE](https://www.facebook.com/IIECRise/) Campaign.It was my first time learning this technology and exploring various fields of same.I am sharing here how I made this Project with you so that fellow aspirants can also benefit from it.

## Description
This project is used to check one's Knowledge on docker and docker compose.For Database management I used [PostgreSQL](https://www.postgresql.org/) which is an  open source and free  Relational Database Management System .For setting up my Web application I used [Odoo](https://www.odoo.com/) an open source ERP and CRM. On Odoo I launched my Web app  for Online Product Delivery system with Payment option also.This System of using Multiple  O.S.  tied together is termed as **Multi-tier architecture** .With use of **Networking**(PAT) and **Persistent Storage** (docker Volumes) which helped in achieving this accomplishment and rest is history.

## Initial Configuration
Some Initial Changes must be made on your base O.S. so  that proper connection can be estabhlished .
### FIREWALL 
For this project firewall must be Disabled .This might affect your security on your O.S. so recommended to do so on a Virtual Machine.

***Step 1:***

```systemctl stop firewalld```

This step Disables the firewall but temporarily and might again come up when base O.S. is booted.

***Step 2:***

```systemctl disable firewalld```

This permanently disables the firewall.

### IPTABLES 
This must be done to allow all Packets in iptables for smooth flow of data.

***Step 1:***

```iptables -F```

To flush all the rules which were already setup.

***Step 2:***

```iptables -nvL```

To Check the validity of first command.

***Step 3:***

```iptables -P FORWARD ACCEPT```

To make changes in iptable and allow all traffic.

***Step 4:***

```iptables -nvL```

To Check the final results.

## Prerequisites
1. **Docker CE** must installed on your BASE O.S. mine was RHEL 8 on Virtual box Oracle 
2. **Docker Compose** must also be Installed .Version 2 and above is recommended because some commands are not supported in below versions. 

## Docker Compose
[Compose](https://docs.docker.com/compose/) is a tool for defining and running multi-container Docker applications. With Compose, you use a YAML file to configure your application’s services. Then, with a single command, you create and start all the services from your configuration. For Installation site [click here](https://docs.docker.com/compose/install/).

After installation Seperate directory must be created on your base O.S. so management of files can be made easy .Directory can be created anywhere 

```mkdir /abhi```

```cd /abhi```

Inside the directory foloowing commands should be typed to create a yml file.

```vim docker-compose.yml```

Inside the vim editor Following Commands must be typed as it is.***WARNING :Spacing should be done using Spacebar and not TAB to avoid errors .*** 
![alt text](http://url/to/img.png)




  
