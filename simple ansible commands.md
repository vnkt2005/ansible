# Simple Ansible and Shell commands
$ansible --version
$ansible -m ping all

#check memory usage
$ansible -m shell -a 'free -m' host1 

#check ip address, deprecated
$ifconfig 

# How to install ifconfig in centos7
#ifconfig installation 
```sh
$sudo yum update
$sudo yum install net-tools -y
```


#check ip address, new command
$ip a

#How to configure a static IP address on CentOS 7 / RHEL 7
#Create a file named /etc/sysconfig/network-scripts/ifcfg-enp0s3 as follows:
DEVICE=enp0s3.
BOOTPROTO=none.
ONBOOT=yes.
PREFIX=24.
IPADDR=192.168.2.203.
Restart network service: systemctl restart NetworkManager
ip a
nmcli device connect enp0s3
ip a

#Check yaml syntax online
www.yamllint.com
