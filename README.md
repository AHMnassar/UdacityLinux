# Server IP:
 18.130.161.54

# My private key is:
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDpA9bpKkiYm0p7XleDSzQRbml8i9fnE7QUPR/ewPoTvOmTi9qkpZCp+Uccan2YVRJP1qkXfxxsmTBtqbHwhTUx7BAzZLOU4GMswJcb+CDeevxUF0RMDXH2/KfVZlD9jr7rYck05w8Nx6+KOVQep0P7X02CKNUnqrqAyBQK2WWPN+dhLu1q5RiWxsaSPJK3sXPXOfQAvDVwOmWTRejH9WWAzv+JMJyfDKGUxagF33U8cxq05pXZPF8Gy7KR+HvhhTvGYN6dgBB3R45qWt9ZjPB7fd6god0O4Us+K92XP4CvmLuQxM5nwddl2p2yTABjWZmJuqvULcZ1r3IfFL1xELYp imported-openssh-key


# SSH private key for grader user
-----BEGIN RSA PRIVATE KEY-----
MIIEpAIBAAKCAQEAu/bYCdetGKRh19K+7zHbTkPXzHjlfoyOFR2lmEM2bXEa23v0
RDCCbA0FAv8MyJhWT07hxKFU/zp2kJSaWHOmlujKzqDivYv1EhFs5EOMWt1SP9ow
5u9+JN/D9Zp8X/T51SPU9uP3gJGi66InrQvK5DFKALTgWTqpffZAwhTMajmruVjX
4Ru2jr1TPlvwQQWoO2fDdpcY7Wkrza8rvsEISs7HD3oAVcpOWa4ELcAQffgKreCH
UuQi1SXTelt5jtJrf/05Gx2xpHJv2/cdpUu13yoptLxEIQUnEyU+Chz6gTY2qviC
VdkyGRQZ5uZC8+tepzP7ezGBShNzF/W1vCNvGwIDAQABAoIBAQCIKsHFF5aRVHyB
Mm4ZsD+UijdqLGbs73v6thiBnqduT1LKkBib0ZyaFDB+RDCJnTphh96saMe/giXk
hZLu4xFbH9fUKt83u41VgoQlNP4X0V/FXBazJep3Yhd+9GSHy1u12ZhtJybk4Bxr
oXQmu3VHLKHUszQX0BR7aQruzsxrYo6re+jNDOCeuTbi+XD5BfD/WgtCG7wg3oAK
rUTTRRZ5BtKP1/tDXWXvMtXSrR9Z1J6tIFLFxnjeCo+bWpGpaiFQg/4Tn9SXYpWk
HyFca1CSmiN24HeupAtFflWFWrQ0AI4IDOvYoSo8qM6CwhJ58qVv+PWaTpu6QPIw
X3WW6KIJAoGBAPJLvFkOs5fnHLg6MoE5PuQsrpCOLtHzsNjKSWPIs2EWGjlXQNuR
M77+dIPzPOCrPNyScz1vhEetKcCPOYq4O9eu5iZQuQJRHTMRvYcO/oV7298VAaQr
qklw5USmiZR6L6KwMpt/kGjm0fBp4lfTjAAD1tckN67IFGb/pqyonzxdAoGBAMaY
bT4200MiZ/E1LJPcd7khrokRMA1+GmP98yzOcCr84SM3iygaj7R9CMMAWo1KMWYZ
k9ItkBRUwhsBz4q1EnZGgwv0m8IqD51egMyECk+f7NnMxPrickX0+jYYQKYLOjkm
7Hdpe5dC3EW2feWdmmDqaGXED97O0a5mfvBeIuHXAoGBALk3b+lcNalfADNMOaNS
0WK3TVIvflb8RCnUqLlgiM8kiDNhIbE2lCnidcsQO287NzEdun4yKxpnos0SL1h9
cTF0/3Y2qta8juelHg6KRcJgZjln43NN9cRiSsBp1i3sIVHqAyWfJBMsrztqlZ2x
lwnD5Y1coDw5sm7x6sV9uQv5AoGAPz61s5V0LDId1gQwIRqaChw+4CnYGsPpFaT/
N2q68AW+kR+UMn5a+4jCLI/FRq+1EaXdnJakBsWDV2R5Otw1d/M2sq0AmZIZjO1W
qUr3man9nNMIfDl3WO4ObQHGPNrgfOj3b4PpNx+01IKsj15klq6v9pC82SEWR6se
i9/+zdsCgYBSalBMjMZbI8Kms74xc1WOQDkH8F+TCllzE1Dbcfwd4DbFVga0BQOr
ISyPa9OTh88VwIuVSAa1/Thf5L+9t3TWanh5ZX98i5/6d1fw9U9aq95F6d9OMqYF
RtThAn5pBW+EXVpXKl0+uKjEQDVLx3BsEysj4yvdr0zg/eGaMr3DlA==
-----END RSA PRIVATE KEY-----

 
# Password for grader user is GRADER0000grade
# SSH port: 2200
# The SSH key for grader user is located at: /home/ubuntu/.ssh/graderkeys




##Configurations:

# Update all currently installed packages

`apt-get update` 

`apt-get upgrade`

`sudo apt install unattended-upgrades`

 edit /etc/apt/apt.conf.d/50unattended-upgrades
 Unattended-Upgrade::Allowed-Origins {
        "${distro_id}:${distro_codename}";
        "${distro_id}:${distro_codename}-security";
//      "${distro_id}:${distro_codename}-updates";
//      "${distro_id}:${distro_codename}-proposed";
//      "${distro_id}:${distro_codename}-backports";
};

To enable automatic updates, edit /etc/apt/apt.conf.d/20auto-upgrades
APT::Periodic::Update-Package-Lists "1";
APT::Periodic::Download-Upgradeable-Packages "1";
APT::Periodic::AutocleanInterval "7";
APT::Periodic::Unattended-Upgrade "1";


# Add user grader
command: `sudo adduser grader`

# Add sudo to grader user
command ```sudo nano /etc/sudoers.d/grader```
and add:

`grader ALL=(ALL) ALL`


# Generating and installing public keys for grader user

on your local machine perform the following command: `ssh-keygen`
and specify a file for the key as: /home/ubuntu/.ssh/graderkeys

Then command:
`cat /home/ubuntu/.ssh/graderkeys.pub`
copy the key.
Now, log in as grader: ssh grader@18.130.161.54 -p 2200
Then:
```
mkdir .ssh
touch .ssh/authorized_keys 
nano .ssh/authorized_keys 
```
paste key from graderkeys.pub
```
sudo chmod 700 .ssh
sudo chmod 644 .ssh/authorized_keys
```
Now you can login as grader with the public key as followed:
Can now login as the `grader` user using the command:

`ssh grader@18.130.161.54 -p 2200 -i ~/.ssh/graderkeys`



# Disable root login

Change Port number to 2200:
`port 2200`

Change PermitRootLogin to no:
```
PermitRootLogin no
```

Change PasswordAuthentication to no sshd_config file `sudo nano /etc/ssh/sshd_config`:
```
PasswordAuthentication no
```

Then
` sudo service ssh restart`


# Change timezone to UTC

`sudo timedatectl set-timezone UTC`




# Configuration Uncomplicated Firewall (UFW)

`sudo ufw default deny incoming`

`sudo ufw default allow outgoing`

`sudo ufw allow 2200/tcp`

`sudo ufw allow www`

`sudo ufw allow ntp`

`sudo ufw show added`

`sudo ufw enable`


# Install Apache and mod_wsgi 

`sudo apt-get install apache2`

`sudo apt-get install libapache2-mod-wsgi`


# Install and configure the PostgreSQL
 
```
 sudo apt-get update
 sudo apt-get install postgresql postgresql-contrib
```
 
```
sudo -u postgres
CREATEUSER catalog;
CREATEDATABASE catalog;
psql catalog
ALTER DATABASE catalog OWNER TO catalog;
ALTER USER catalog WITH PASSWORD 'catalogpassword';
\q
exit
```

# Install Flask
```
sudo apt-get install python-psycopg2 python-flask
```
# Install Sqlalchemy

```
sudo apt-get install python-sqlalchemy python-pip
```
# Install oauth2client

```
sudo pip install oauth2client
```
# Install requests

```
sudo pip install requests
```
# Install httplib2

```
sudo pip install httplib2
```
# Install flask-seasurf

```
sudo pip install flask-seasurf
```


# Install Git version control software
```
sudo apt-get install git
```

# Clone Catalog Project app

```
cd /var/www
sudo mkdir project
sudo chown -R grader:grader project
cd project
sudo git clone https://github.com/AHMnassar/CatalogProject.git project
```

# Configure PostgreSQL
In Both Files:
__init__.py And python__DB_setup.py  

Change the DATABASE_URI 'postgresql://catalog:catalogpassword@localhost/catalog'


# Configure Apache.
 
```
sudo nano /var/www/project/app.wsgi
```

And Add:

#!/usr/bin/python
import sys 
import logging
logging.basicConfig(stream=sys.stderr)
sys.path.insert(0,"/var/www/project/")
from project import app as application
application.secret_key = 'super_secret_key'


Update the Apache configuration file

```
sudo nano /etc/apache2/sites-enabled/000-default.conf
```
And Add:

	 ServerName 18.130.161.54
	ServerAdmin mido.legend48@yahoo.com
	WSGIScriptAlias / /var/www/project/app.wsgi
	<Directory /var/www/project/project>
		Order allow,deny
		Allow from all
	</Directory>
	Alias /static /var/www//project/project/static
	<Directory /var/www/project/project/static/>
		Order allow,deny
		Allow from all
	</Directory>
	ErrorLog ${APACHE_LOG_DIR}/error.log
	LogLevel warn
	CustomLog ${APACHE_LOG_DIR}/access.log combined 



Restart Apache.

```
sudo apache2ctl restart
```


# References:

- [How To Install and Use PostgreSQL on Ubuntu 14.04](https://www.digitalocean.com/community/tutorials/how-to-install-and-use-postgresql-on-ubuntu-14-04)
- StackOverflow Posts.
- [How to Deploy a Flask Application on Ubuntu] (https://www.digitalocean.com/community/tutorials/how-to-deploy-a-flask-application-on-an-ubuntu-vps)
