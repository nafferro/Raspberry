# New Raspbian Setup
---
## Basic

     sudo raspi-config
        Advanced Options
              A1 Expand Filesystem 
     sudo rpi-update
     sudo apt-get update
     sudo apt-get dist-upgrade
---
## Static IP
    sudo nano /boot/cmdline.txt
        add ip=192.168.1.20 to the end of the line
---
### Create new user
    sudo adduser nafferro
### Add user to the sudo group
    sudo adduser nafferro sudo
### Delete pi user
    sudo deluser pi
    sudo rm -rf /home/pi
---
## VNC Server
    sudo apt-get install realvnc-vnc-server realvnc-vnc-viewer
    sudo raspi-config
        Interfacing Options
        VNC > Yes

## Reconfigure locale in raspberry-pi
    sudo nano /etc/locale.gen
        uncomment the line with en_US.UTF-8
    sudo locale-gen en_US.UTF-8
    sudo update-locale en_US.UTF-8