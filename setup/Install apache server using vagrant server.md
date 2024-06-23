# Install apache server using vagrant server

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
          >vagrant ssh
      <br>
8. To add another virtual box like ubuntu<br>
          >vagrant box add ubuntu/bionic4
<br>

9. Add following lines in vagrantfile <br>
	```sh    
	  config.vm.box = "centos/7"
	  config.vm.provision "shell", inline: <<-SHELL
		sudo yum update -y 
		sudo yum install -y httpd
	  SHELL
	  >vagrant reload
	```

10. create new file provision1.sh in windows E:\vagrantprojects folder and write the following commands
    ```sh
	#!/usr/bin/env bash

	#install apache web server
	sudo yum update -y
	sudo yum install -y httpd
	
	#start apache and set it to run at boot
	sudo systemctl start httpd
	sudo systemctl enable httpd
	
	#create a sample index.html file
	sudo echo "<html><body><h1>Hello, world!</h1></body></html>"
	> /var/www/html/index.html
	
	#restart apache to serve the new index.html file 
	sudo systemctl restart httpd
    ```

 11. Add the following line at the end of vagrantfile
     <br>
	```sh
	config.vm.provision :shell, path: "provision1.sh"
	```
  13. Run > vagrant reload --provision
  14. Go to browser and type the command to see the website in action
      ```sh
      http://localhost:8080
      ```
       
