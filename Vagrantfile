Vagrant.configure("2") do |config|
    config.vm.box = "centos/7"
    config.vm.synced_folder ".", "/vagrant", type: 'virtualbox'
    config.vm.network "forwarded_port", guest: 5000, host: 5001
    config.vm.provision "ansible_local" do |ansible|
        ansible.playbook = "ansible/playbook.yml"
        
        ansible.verbose = true
    end
        # Provider for VirtualBox
    config.vm.provider :virtualbox do |vb|
      vb.memory = "4096"
      vb.cpus = 4
    end
  end