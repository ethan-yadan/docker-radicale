![Don't Panic](ParanoidAndroidMarvin.jpg)

# Radicale Docker task 

Installing Radicale on Docker. 
Radicale is a small but powerful CalDAV (calendars, to-do lists) and CardDAV (contacts) server, that:

	* Shares calendars and contact lists through CalDAV, CardDAV and HTTP.
	* Supports events, todos, journal entries and business cards.
	* Works out-of-the-box, no complicated setup or configuration required.
	* Can limit access by authentication.
	* Can secure connections with TLS.
	* Works with many CalDAV and CardDAV clients.
	* Stores all data on the file system in a simple folder structure.
	* Can be extended with plugins.
	* Is GPLv3-licensed free software.

## Table of Contents

- [Prerequisites](#prerequisites)
- [Installation](#installation)
- [Usage](#usage)
- [Setup](#setup)
- [Contributing](#contributing)


## Prerequisites
1. Linux Debian distribution 
2. python 3.5 or later (python ≥ 3.6 is recommended) and pip are installed
3. python-Passlib and python-Bcrypt


## Installation 

1. Installing prequisites: 
''' bash 
sudo apt install python3-pip python3-passlib
sudo pip3 install bcrypt
'''

2. Clone the repository: 
'''bash 
git clone https://github.com/ethan-yadan/docker-radicale.git
'''

Radicale is really easy to install and works out-of-the-box.

| # Run the following command as root or
| # add the --user argument to only install for the current user
| python3 -m pip install --upgrade radicale
| python3 -m radicale --storage-filesystem-folder=~/.var/lib/radicale/collections

When the server is launched, open http://localhost:5232 in your browser! You can login with any username and password.


## Usage

I've worked with a linux mint VM. 
bcrypt is a password-hashing function, which takes an input string and other random values, to compute a 192-bit hash.
Each user will have his personal hash, configured in the Radicale users file, authanticating users using Radicale.   


## Setup

### Updating, upgarding and installing in linux debian: 

1. ''' sudo apt update '''
2. ''' sudo apt-get upgrade '''
3. ''' sudo apt install python3-pip '''
4. ''' sudo apt install python3-passlib '''
5. ''' sudo apt install python3-bcrypt '''

### Creating folders and files for docker and radicale installation: 

6. ''' mkdir -p docker/radicale/data '''
* created the folder for the task * 
   
7. ''' nano users ''' 
* edited the file to contain two users: eitan and alex, each with its bcrypt hash created in bcrypt generator * 
* passwords to enter the radicale server are: eitan1234, alex1234 *
	   
8. ''' nano docker-compose.yml ''' 
* created docker-compose file to pull docker image for radicale (file was created in docker/radicale) * 

9. ''' sudo apt install docker-compose ''' 
	
10. ''' docker-compose up -d && docker-compose logs -f '''
* creating and uploading docker container *

11. ''' docker ps '''
* checking that the container created in up and running *

12. ''' ip -br a '''
* checking my localhost ip in my virtual machine *

13. ''' sudo apt install radicale '''
14. ''' sudo systemctl start radicale '''

### Uploading radicale in web browser:

15. accessing Radicale on web browser at 10.0.2.15:5232 (localhost_ip:5232) 
16. using eitan or alex user and password to enter radicale CALDEV 
