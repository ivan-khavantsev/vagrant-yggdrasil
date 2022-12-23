Vagrant.require_version ">= 2.2.19"

Vagrant.configure("2") do |config|
	
	# Машина с yggdrasil
	config.vm.define "yggdrasil" do |yggdrasil|
		yggdrasil.vm.box = "debian/bullseye64"
		yggdrasil.vm.box_version = "11.20211018.1"
		
		yggdrasil.vm.provider "virtualbox" do |virtualbox|
			virtualbox.memory = "256"
		end
	
		yggdrasil.vm.network "private_network", ip: "192.168.56.8"
		yggdrasil.vm.provision "ansible_local" do |ansible|
			ansible.install = true
			ansible.playbook = "./provision/playbook.yml"
		end
	end
	
 
end







