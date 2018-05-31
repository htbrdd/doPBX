Find the YouTube Video here: https://youtu.be/A6mxdvIMLEc

## Pre-requisites
- SELinux is Disabled (it is in DigitalOcean by default)
- A CentOS 7 droplet (of any size)

## Step 1: Get/Clone (if you have git) the script found in my GitHub Repository
- wget https://raw.githubusercontent.com/cameronbackus/doPBX/master/install_freepbx.sh

## Step 2: Run the Script
- sh install_freepbx.sh

The Script will run for a bit more, you then will be able to choose if you would like any more Asterisk modules to be installed.

The script will then finish and you can browse to the FreePBX WebGUI using the droplet IP address.



worth noting 2 things you don't go over here (which may be the result of changes on digitalocean's end) 1) wget does not come installed anymore so you need to do "yum install wget" to get started and 2)this script fails if selinux is enabled in centos 7.4 so youll need to modify /etc/selinux/config and change the config from SELINUX=enforcing to SELINUX=disabled then reboot. THEN your ready to start. Not a huge deal but worth noting to save some other users some time.﻿
