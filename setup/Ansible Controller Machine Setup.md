1. Install VirtualBox and Vagrant on your local machine.
Create a directory in your local machine to setup ansible project
Create a folder "E:\AnsibleDemo in Windows System
In "AnsibleDemo" folder create two more folders called "ansible-controller" and "ansible-hosts"
Navigate to ansible-controller and run the following commands.
```sh
mkdir e:/ansibledemo
cd e:/ansibledemo
mkdir ansible-controller
mkdir ansible-hosts
cd ansible-controller
vagrant init centos/7
```
2. In google type "vagrant box search" and goto website "http://app.vagrantup.com/boxes/search". Search for "centos" and click "vagrant file" and copy command to run it from "ansible-controller" directory.
3. Edit the vagrantfile and add the following lines to the end of the file to provision Ansible on the VM.
4. ```sh
    Vagrant.configure("2") do |config|
   
       config.vm.define "ansible-controller" do |controller|
         controller.vm.hostname = "controller"
       end
       config.vm.box = "centos/7"
       config.vm.provision "shell", inline: <<-SHELL
         sudo yum install epel-release -y
         sudo yum install ansible -y
       SHELL
   
    end
   ```
5. After saving the vagrantfile, validate the syntax with the following command. Alternatively you can use "http://codebeautify.org/ruby-formatter-beautifier/".
6. ```sh
   vagrant validate
   ```
