# DockerProject
This is my first project on Docker which I Integrated with PostgreSQL( RDMS) and Odoo(business management software )running both on different Docker O.S. to create a online portal to sell goods and services . WISH ME LUCK.:smile:
 
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

Inside the vim editor Following Commands must be typed as it is.***WARNING :Spacing should be done carefully using Spacebar and not TAB to avoid any errors .***

![6](https://user-images.githubusercontent.com/64806938/81288793-f80d7080-9082-11ea-9766-4c4b52a4314e.png)

## LIGHT IT UP!:fire::fire:
Now After typing the commands ***SAVE THE FILE***  Write the below code in commmand line in same Directory .

```docker--compose up```

![7](https://user-images.githubusercontent.com/64806938/81288796-f93e9d80-9082-11ea-99f0-2b7dce5b35d3.png)

![1](https://user-images.githubusercontent.com/64806938/81288777-f2b02600-9082-11ea-91ef-12138bf476a4.png)

## FINAL OUTCOME
You can check the validity of above command if done right or not by using the following command in another window terminal .

```docker ps ```

The above will show two containers up and running and also that port no. 8080  also have been diverted.

Now, find your systems ***IPADDRESS*** by using the below command

```ifconfig```

Under your network card name your 32bit size IPADDRESS can be found.In this case we have choosen ***PORT NUMBER :8080*** default for
access but it can be changed only prior that it's free.The port has been diverted to **:8069** because it's default for Odoo and can also be changed.  

Enter Your **IPADDRESS** followed by **PORT NO.** in your browser of any other computer but make sure both are connected to same SWITCH(Router) only. 

You may find this screen welcoming you .

![8](https://user-images.githubusercontent.com/64806938/81288797-f9d73400-9082-11ea-9fa2-ab68f4950ee6.png)

Fill all your details, this is your **Administator's Account**
By clicking on create database next screen is following:

![9](https://user-images.githubusercontent.com/64806938/81288799-fa6fca80-9082-11ea-8b7e-14c2706b5362.png)

***INSTALL THE E-COMMERCE TO SETUP YOUR PLATFORM***

![12](https://user-images.githubusercontent.com/64806938/81288813-fcd22480-9082-11ea-9c94-6a392dfea669.png)

![11](https://user-images.githubusercontent.com/64806938/81288809-fc398e00-9082-11ea-96f1-80f958320d6d.png)

***CHOOSE A THEME FOR YOUR WEBSITE***

![10](https://user-images.githubusercontent.com/64806938/81288804-fb086100-9082-11ea-8184-a851da3f7678.png)

After I published some products(Imaginary :grin:) and edited my home page.

***WELCOME TO MY HOMEPAGE***

![13](https://user-images.githubusercontent.com/64806938/81288820-fd6abb00-9082-11ea-80c0-e9e9064fd716.png)

***THE FOLLOWING ARE THE PRODUCTS I CREATED***

![18](https://user-images.githubusercontent.com/64806938/81288834-0065ab80-9083-11ea-9a24-0e9fd2420509.png)

***SELECT AND ADD THEM TO YOUR CART***

![19](https://user-images.githubusercontent.com/64806938/81288836-00fe4200-9083-11ea-9031-4a3eb69c9120.png)

***AFTER SELECTING YOU  WILL BE REDIRECTED TO FOLLOWING PAGE***

![20](https://user-images.githubusercontent.com/64806938/81288838-0196d880-9083-11ea-9677-0fd9bd1e91fe.png)

***AFTER FILLING YOUR DETAILS YOU CAN MAKE THE PAYMENT BY WIRE (CAN ALSO BE MADE TO SUPPORT OTHER MODE OF PAYMENTS ALSO) AND YOU HAVE SUCCESSFULLY MADE THE PURCHASE***

![21](https://user-images.githubusercontent.com/64806938/81288841-0196d880-9083-11ea-8a1d-e729efb9dfc1.png)

![22](https://user-images.githubusercontent.com/64806938/81288844-022f6f00-9083-11ea-9d87-41320cc11fea.png)

***EVERY PROCESS IS AUTOMATED FROM PLACING A ORDER TO MAKING A PAYMENT SUPPORTED BY ODOO***

## Acknowledgement
I would like to thank  [Mr. Vimal Daga Sir](https://www.linkedin.com/in/vimaldaga/) without his guidance it would have been impossible to achieve this.I would also like to thank his whole team for support also.

***THANK YOU FOR READING THIS AND FOR THE APPRECIATION , [CONNECT](https://www.linkedin.com/in/abhishek-kumar-286151197) ME ON LINKED FOR ANY PROJECT RELATED QUERY***
