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
- [Contributing](#contributing)


## Prerequisites
1. python 3.5 or later (python ≥ 3.6 is recommended) and pip are installed
2. python-Passlib and python-Bcrypt


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




