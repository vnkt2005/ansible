# My ansible journey

1. Install ubuntu 22.04 on windows 10
2. install ansible on ubuntu terminal
3. install vagrant for windows on windows 10
4. Install VirtualBox(Oracle) on windows 10
5. Open new folder in windows E:\vagrantprojects<br>
       >windows prompt<br>
       >vagrant init<br>
       >this command creates Vagrantfile in e:\vagrantprojects folder<br>
6. Goto app.vagrantup.com/boxes/search ---> discover vagrant boxes<br>
          Search for centos<br>
          Click virtualbox and copy the following line<br>
          config.vm.box = "centos/7"
          open vagrantfile, paste above line at the end and save the file<br>
7.        >vagrant up
          >vagrant box list
       
