# method-1
#run this command as root user and substitute username with actual user to be included in wheel group.
<br>
#Users in the wheel group can use sudo command.
<br>
usermod -aG wheel username

# method-2
#Adding User to the sudoers File
<br>
#The users’ and groups’ sudo privileges are configured in the /etc/sudoers file of /etc/sudoers.d directory
