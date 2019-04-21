# Linux-Server-Configuration

IP.54.164.52.239
name: grader
pass: udacity







log

1.Create Amazon Web Services Account  on https://portal.aws.amazon.com/billing/signup#/start

2.Create Viirtual Mashine with Ubuntu 16


![demo](https://github.com/Kuldyaev/Linux-Server-Configuration/blob/master/images/ubuntussh.JPG) 

3.Update package sourse list

    sudo apt-get update

4.Update the software

    sudo apt-get upgrade
    
5.Install Finger application

    sudo apt-get install finger
    
6.Install GIT

    sudo apt-get install git-core
    
7.Change settings Amazon Lightsail firewall. Open ports 2200 and 127.
![demo](https://github.com/Kuldyaev/Linux-Server-Configuration/blob/master/images/AmazFirewall.JPG)

8.Configure ufw firewall on server

    sudo ufw status
    sudo ufw default deny incoming
    sudo ufw default allow outgoing
    sudo ufw allow ssh
    sudo ufw allow www
    sudo utw allow ntp
    sudo ufw allow 2200/tcp
    sudo ufw allow 123/tcp
    sudo ufw enable
    sudo ufw status

9.Create new user

    sudo adduser grader

10.Check the SODOERS directory

    sudo ls /etc/sudoers.d
    
11.Create file 'grader' in /etc/sudoers.d directory

    sudo nano /etc/sudoers.d/grader
    
12.Add text in file 'grader'
    
    grader ALL=(ALL) NOPASSWD:ALL
    
13.Create pair of keys on local machine and copy public key

    $ ssh-keygen
    
14.Login as 'grader' user

    sudo login grader
    
15.Create directory .ssh and authorized_keys file. Copy public key in 'authorized_keys' file

    mkdir .ssh
    touch .ssh/authorized_keys
    
16.Upload programs for web-catalog

    sudo apt install python3-pip
    sudo apt-get install python-sqlalchemy
    sudo pip install Flask
    
17.Clone WWW-Catalog from GitHub

    git clone https://github.com/Kuldyaev/CatalogWWW
    
18.Start web server
    
    

