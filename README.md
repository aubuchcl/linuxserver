
#  Sign up for Amazon Lightsail
	1.[Amazon] (https://amazonlightsail.com/)
	1.Download the key that is generated when you start your instance
	1.log into your instance from the command line
		1. ssh ~/.ssh/yourpemfile.pem ubuntu@yourdomain -p your port

#  make a grader user
	1.create a new user `$ sudo adduser newuser`
	1.give user sudo powers `$ sudo usermod -a -G sudo newuser`

#  change the port to 2200
	1. open the config file `$vim /etc/ssh/sshd_config`
	1. change the port to 2200
	1. in the lightsail gui add 2200, 123, and 80 to be safe

#  change password auth to no

#  use ssh-keygen to get the public key
	1.`ssh-keygen -y`
	1.path to private key
	1.copy the public key returned
	1.add to authorized_keys file

#  set up ufw to accept ports
	1. `$ sudo ufw allow 2200/tcp`
	1. `$ sudo ufw allow 80/tcp`
	1. `$ sudo ufw allow 123/udp`


#  set timezone  [timezone](https://forums.aws.amazon.com/thread.jspa?threadID=244253)
	1.`$timedatectl list-timezones`
	1. `$ sudo timedatectl set-timezone UTC`

#  install required packages
	1. `$ sudo apt-get install apache2`
	1. replace apache2 with libapache2-mod-wsgi


#  install project dependencies
	1.`$ sudo apt-get install python-pip`
	1.`$ sudo pip install dependencies`

#  install postgres
	1. `$ sudo apt-get install postgresql`

#  go to your developer console in google
	1. add redirect and javascript origins links
	1. download new client secrets file
	1. modify the client secrets . json file


------ before changes------
#  *IP and SSH port <br>
	*52.42.124.225
<br>*ssh port is 2200 as requested
<br>
#  *url
<br>	*http://ec2-52-42-124-225.us-west-2.compute.amazonaws.com/
<br>*summary
<br>	*all software used for actual program is in requirements.txt (/var/www/catalog/catalog/requirements.txt)
<br>	*apache2
<br>	*wsgi
<br>	*git
<br>	*postgres
<br>third party resources
<br>	*stackoverflow
<br>	*aws docs
<br>	*digital ocean
<br>	*github
<br>	*ubuntu forums
<br>	*askubuntu
<br>	*apache docs