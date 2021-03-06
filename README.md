# VestaCP on Digital Ocean (Ubuntu 16.04 LTE)
A little script for myself to have a web server in Digital Ocean with Vesta Control Panel in no time.

Currently installing 
- VestaCP
- Nginx 1.11.x
- PHP 7.0.x
- MySQL 5.7.x
- Exim 4.x
- Dovecot 2.2.x
- vsftpd
- named
- iptables
- fail2ban

On servers over 3Gb of ram:
- Spam-Assasin
- ClamAV

What I aditionally do to a standard VestaCP installation is:
- Make a swap partition of 1gb to make some room for some things to work better.
- Configure server Time Zone.
- Configure server Locales.
- Fully Update the OS.
- Setup unattended-upgrades.
- Remove admin group.
- ...and after installation, run patches to the specific VestaCP version if available.

Minimal requirements

A 5 dollars a month Digital Ocean Ubuntu 16.04 64bit server, 512 mb ram / 1 CPU, 20 GB SSD Disk, 1000 GB Transfer.
Get it at https://goo.gl/WWmpYW . They will give you 10 u$ credit in virtual machines just for signing in with that link.

After login to the droplet for the first time, copy the line bellow and execute it in the terminal

    curl -O https://raw.githubusercontent.com/FastDigitalOceanDroplets/VestaCP/master/vestacp.sh && bash vestacp.sh

Once installed REBOOT the droplet.

I have prepared some basic setups and patches installation for the specific VestaCP version. Copy the line bellow and execute it in the terminal. (the patch may or may not reboot the system again)

    bash post.sh
    
