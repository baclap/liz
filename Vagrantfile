Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip: "192.168.33.10"
  config.vm.synced_folder ".", "/liz" #, owner: "vagrant", group: "www-data", mount_options: ["dmode=775,fmode=664"]
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "py-playbook.yml"
  end
  config.vm.provision "ansible" do |ansible|
    ansible.verbose = "v"
    ansible.playbook = "main-playbook.yml"
  end
end
