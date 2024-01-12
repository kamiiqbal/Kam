1.	Create your own username (use your first name), grant yourself administrator rights then switch to that user to complete the exercise.
adduser Kamran
pass = Kamran
usermod -aG sudo kamran    #( administrator rights)  DONE..
2.	What is current the time zone? Correct it to the local time zone and correct time.
timedatectl
Time zone: Australia/Sydney (AEDT, +1100)
3.	What OS and version is the VM running?
lsb_release -a
Distributor ID: Ubuntu
Description:    Ubuntu 22.04.3 LTS
Release:        22.04
Codename:       jammy
4.	What are the current mirrors on the VM?   Mirrors are package repositories.
cat  /etc/apt/sources.list

deb http://mirrors.digitalocean.com/ubuntu/ jammy main restricted
deb http://mirrors.digitalocean.com/ubuntu/ jammy-updates main restricted
deb http://mirrors.digitalocean.com/ubuntu/ jammy universe
deb http://mirrors.digitalocean.com/ubuntu/ jammy-updates universe
deb http://mirrors.digitalocean.com/ubuntu/ jammy multiverse
deb http://mirrors.digitalocean.com/ubuntu/ jammy-updates multiverse
deb http://mirrors.digitalocean.com/ubuntu/ jammy-backports main restricted universe multiverse
deb http://security.ubuntu.com/ubuntu jammy-security main restricted
deb http://security.ubuntu.com/ubuntu jammy-security universe
deb http://security.ubuntu.com/ubuntu jammy-security multiverse

5.	What are the MAC addresses on the VM?

ip addr show

Mac address = 9a:87:d0:84:17:c8
2: eth0: <BROADCAST,MULTICAST,UP,LOWER_UP> mtu 1500 qdisc fq_codel state UP group default qlen 1000
    link/ether 9a:87:d0:84:17:c8 brd ff:ff:ff:ff:ff:ff
    altname enp0s3
    altname ens3
    inet 159.65.52.247/20 brd 159.65.63.255 scope global eth0
       valid_lft forever preferred_lft forever
    inet 10.16.0.6/16 brd 10.16.255.255 scope global eth0
       valid_lft forever preferred_lft forever
    inet6 fe80::9887:d0ff:fe84:17c8/64 scope link
       valid_lft forever preferred_lft forever

6.	Rename VM to Lab_complete
sudo hostnamectl set-hostname Lab_complete
