# Create ansible-hosts virtual machines
1.  Go to windows ansibledemo folder. Create ansible-hosts folder and navigate to that folder. Run the following command.
   ```sh
    vagrant init centos/7
   ```
2. Add the following content to the vagrantfile and save.
   ```sh
   Vagrant.configure("2") do |config|
     config.vm.box = "centos/7"
  
     config.vm.define "web" do |web|
         web.vm.hostname = "web"
         web.vm.network "private_network", ip: "192.168.33.10"
     end
  
     config.vm.define "db" do |db|
         web.vm.hostname = "db"
         web.vm.network "private_network", ip: "192.168.33.11"
     end
   
      config.vm.network "forwarded_port", guest: 80, host: 8080, auto_correct: true
      config.vm.usable_port_range = (8000..9000)
  
   end
   ```
