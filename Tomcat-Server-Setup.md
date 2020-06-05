# Tomcat Server Setup

This tutorial is written specifically for OSX and Tomcat 8.0.xx but can be adapted for other versions.

1. Goto http://tomcat.apache.org ⇒ Download ⇒ Tomcat 8.0 ⇒ 8.0.{xx} (where {xx} denotes the latest release) ⇒ Binary 1. 1. distribution ⇒ Core. Download the "tar.gz" package (e.g., "apache-tomcat-8.0.{xx}.tar.gz").
2. Open Terminal
3. `cd ~/Downloads`
4. `tar xvf apache-tomcat-8.0.{xx}.tar.gz`
5. `Sudo mv apache-tomcat-8.0.{xx} ~/Applications`
6. ` cd ~/Applications/apache-tomcat-8.0.{xx}/bin`
7. `chmod 777 *`
8. `./catalina.sh run`


The default port is 8080
http://localhost:8080/ to check to see it is up and running

Setup is now complete.

## Regular Use
To start and stop the server from now on you'll just need to cd into the folder you placed the tomcat folder in and run these commands.

1. `cd apache-tomcat-8.0.{xx}/bin`
2. `./catalina.sh run` This will start the server
3. `./shutdown.sh` This will shutdown the server

## Deploy a .war file
Now that things are up and running we can deploy a .war file. 
Go to https://tomcat.apache.org/tomcat-7.0-doc/appdev/sample/ and click the download link. Make sure the file extension is a .war file.
All you have to do is copy this file into the webapps folder inside the apache-tomcat-8.0.{xx} folder. 
Check to see it worked by going to http://localhost:8080/sample/ 


## Change Configuration Files (Optional) 
### Adding an admin user
You’ll need to do this if you need access to the Server Status, Manager App or Host Manager.
Inside the apache-tomcat-8.0.{xx} navigate to the conf folder. Open tomcat-users.xml in a text editor of your choice. Add the following code inside. You may change the username and password to whatever you would like. Save the file and restart the server. 


`<role rolename="admin"/>
<role rolename="admin-gui"/>
<role rolename="manager-gui"/>
<user username="admin" password="password" roles="admin,admin-gui,manager-gui"/>`


### Changing the port number
To change the port number open server.xml and find where the port number equals 8080. You can choose any number between 1024 and 65535, as long as it is not used by an existing application. Save and restart the server. 


### Additional Configurations 
https://www.ntu.edu.sg/home/ehchua/programming/howto/Tomcat_HowTo.html#configure


This tutotial was adapted from https://www.ntu.edu.sg/home/ehchua/programming/howto/MacUsers_HowTo.html

