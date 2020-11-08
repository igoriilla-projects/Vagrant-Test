Vagrant.configure("2") do |config|

  config.vm.box = "generic/ubuntu1804"
  config.ssh.insert_key = false
  
  config.vm.define "web" do |web|
	web.vm.hostname = 'web-01'
	web.vm.network "public_network", ip: "192.168.2.107"
		
	web.vm.provider :virtualbox do |vb|
	  vb.customize ["modifyvm", :id, "--memory", 1024]
	  vb.customize ["modifyvm", :id, "--name", "web-01"]
	end
  end
  
  config.vm.define "db" do |db|
	db.vm.hostname = 'db-01'
	db.vm.network "public_network", ip: "192.168.2.199"
		
	db.vm.provider :virtualbox do |vb|
	  vb.customize ["modifyvm", :id, "--memory", 1024]
	  vb.customize ["modifyvm", :id, "--name", "db-01"]
	end
  end
  
    config.vm.provision "ansible" do |ansible|
    ansible.playbook = "main.yml"
  end
end
