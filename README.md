
#Udacity full stack nano degree: Linux server project

##IP Address:

##URL:

##Port: 2200

# Create a new ubuntu linux server using amazong lightsail
- Create an AWS account
- Create an ubuntu instance choosing the cheapest plan
-Name your instance and create

#ssh into your server
- Download the private key on lightsail
- Use the key to ssh into your instance using some sort of terminal.
- Example command: ssh -i ~/.ssh/lightsail_key.rsa ubuntu@xx.xxx.xx.xxx

#Set all of the ufw ports
- Allow port 2200, 123, and 80
- Deny port 22
- Go into the sshd_config and change the prot from 22 to 2200
-Restart your service for these changes to take affect

#Update all of your packages
- use apt-get to update and upgrade all of the packages

#Create a grader user
- Create a new user named grader
- Give sudo access to that grader user

#Create ssh for grader
- Use ssh keygen to make a key for the grader user
- As the grader user add the public key to the authorized keys
- Change the password authentication to no so that the user needs the key
- The password for the grader is "grader"

#Change the time zone
- change the timezone to utc

#Install apache
- Install apache2

#Install what you need for python
- Install the mod_wsgi package
- Enable and wegi and restart apache
- Check if python is installed, if not install python

#Install postgresql
- Install postgresql
- Create a new postgresql user
- Connect to postgresql
- Create a catalog user with the ability to create tables and databases
- Exit psql

#Create a new linux user
- Create a new linux user named catalog
- Give this user sudo access
- Create database catalog
- Go back to grader user

#Install git
- Install git
- make a directory for your catalog project
- clone your catalog project
- change your application.py name to __init__.py
- Change app.run line to just say app.run()

#Edit the client secrets
- Add the new paths to your client secret on the google console developer page
- Copy the new client secrets to your machine

#Install pip
- Install pip for whichever version of python that you are using for your program
- Use pip to install the necessary packages

#Enable virtual host
- create a file called catalog.conf
- Add the virtual host tag along with the required information

#Make the wsgi file
- create a catalog.wsgi file
- Add the required information to that file and save and exit
- Restart apache for it to take affect

#Edit the db path
- in your __init__.py change the engine to the new engine needed

#Disable the defailt apache page
- Run the command to disable the default apache site
- Reload apache2

#Set up db schema
- Run your database setup python file
- Restart your apache
- go to the link provided above to see if the application is running correctly

#Sources
- [Lightsail](https://lightsail.aws.amazon.com/ls/webapp/home/instances?#)
- [Udacity](https://classroom.udacity.com/nanodegrees/nd004/parts/ab002e9a-b26c-43a4-8460-dc4c4b11c379/modules/357367901175462/lessons/3573679011239847/project)
- [Google API console](https://console.cloud.google.com/home/dashboard?project=cool-archery-236915)
