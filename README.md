# Samba-Study

# What it is

Enables Linux and Unix-based systems to seamlessly integrate with Windows-based networks and devices.
It provides a way to share files, printers, and other resources between Linux and Windows systems.

## Functionalities

## How it Works

**1 - Install Samba on **Ubuntu Server****
  - Update the packages on Ubuntu
  -     sudo apt update && sudo apt upgrade -y
  - Install Samba
  -     sudo apt install samba -y

**2 - Create a Directory to the folder sharing**

  - Create the Folder
  -     sudo mkdir -p /srv/samba/compartilhado
  - Adjust the permission of the folder

  - General Access
  -     sudo chmod -R 777 /srv/samba/compartilhado
  - An access just to a specific user
  -     sudo chown -R nobody:nogroup /srv/samba/compartilhado
        sudo chmod -R 770 /srv/samba/compartilhado
**3 - Configure Samba**

   - Open the configuration samba file
   -     sudo nano /etc/samba/smb.conf
   - add the commands to the specific file you created
     -     [compartilhado]
              path = /srv/samba/compartilhado
              browseable = yes
              read only = no
              guest ok = yes
              force user = nobody





  

## Example using a Virtual Machine - Ubuntu Server and Windows



### links

- http://www.linuxfocus.org/English/May2002/article247.shtml
- https://e-tinet.com/linux/servidor-samba-linux-o-que-como-instalar/
