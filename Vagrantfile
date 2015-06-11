Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"

  config.vm.network "public_network"
  config.vm.network :forwarded_port, guest: 8080, host: 8080

  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 1
  end

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "provisioning/playbook.yml"
    ansible.host_key_checking = false
  end
end

#  config.vm.network :forwarded_port, guest: 3000, host: 3000
#  config.vm.network :forwarded_port, guest: 8083, host: 8083
#  config.vm.network :forwarded_port, guest: 8086, host: 8086
