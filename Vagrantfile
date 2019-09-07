VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos/7"
  config.vm.box_version = "1804.02"
  config.ssh.forward_agent = true
  config.vm.box_check_update = true
  config.ssh.insert_key = false
  config.vm.host_name = "appserver"
  config.ssh.username = 'vagrant'
  config.vm.synced_folder ".", "/vagrant", :owner => "vagrant"
  config.vm.network :private_network, ip: "192.168.33.10"
  config.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--memory", 3092, "--cpus", 2, "--name", "ansible-lab"]
  end
end
