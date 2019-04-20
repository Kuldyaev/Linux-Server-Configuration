# Linux-Server-Configuration








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
    
7.Create new user

    sudo adduser grader

8.Check the SODOERS directory

    sudo ls /etc/sudoers.d
    
9.Create file 'grader' in /etc/sudoers.d directory

    sudo nano /etc/sudoers.d/grader
    
10.Add text in file 'grader'
    
    grader ALL=(ALL) NOPASSWD:ALL
    
11.Create pair of keys on local machine and copy public key

    $ ssh-keygen
    
12.Login as 'grader' user

    sudo login grader
    
13.Create directory .ssh and authorized_keys file. Copy public key in 'authorized_keys' file

    mkdir .ssh
    touch .ssh/authorized_keys
    
14.
