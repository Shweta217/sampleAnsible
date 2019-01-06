# -*- mode: ruby -*-
 
# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|
  config.vm.provision :shell, inline: "sudo echo nameserver 208.67.222.222 > /etc/resolv.conf"
  config.vm.define "acs" do |acs|
    acs.vm.box = "ubuntu/trusty64"
	acs.vm.network "private_network", ip: "192.168.57.2"
	acs.vm.provider "virtualbox" do |vb|
	  vb.gui = true
	end
  config.vm.provision "file", source: "C:/Users/VINITA/Desktop/cf/ansible/jdaaj1_v3.yml", destination: "~/sampleAnsible/templates/stack.yml"
  config.vm.provision "file", source: "C:/Users/VINITA/Desktop/cf/ansible/all.yml", destination: "~/sampleAnsible/group_vars/all.yml"
  config.vm.provision "file", source: "C:/Users/VINITA/Desktop/cf/ansible/site.yml", destination: "~/sampleAnsible/site.yml"
  config.vm.provision "file", source: "C:/Users/VINITA/Desktop/cf/ansible/create_stack.yml", destination: "~/sampleAnsible/tasks/create_stack.yml"
  #config.vm.provision "file", source: "C:/Users/VINITA/Desktop/cf/ansible/secrets.yml", destination: "~/sampleAnsible/secrets.yml"
  #config.vm.provision "file", source: "C:/Users/VINITA/Desktop/cf/ansible/secrets1.txt", destination: "~/.aws/credentials"
  

  
	
  end

 
 # config.vm.provision "ansible" do |ansible|
  #  ansible.verbose = "v"
	#ansible.playbook = "site.yml"
  #end
  
  
end
