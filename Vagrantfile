Vagrant.configure("2") do |config|

	config.vm.box = "ubuntu/ubuntu-14.04-64"
	config.vm.box_url = "https://cloud-images.ubuntu.com/vagrant/trusty/current/trusty-server-cloudimg-amd64-vagrant-disk1.box"
	config.vm.hostname = "nodebase"
	config.vm.network "private_network", ip: "192.168.24.102"

	config.vm.provision :shell, :path => "vagrant_ansible_bootstrap"

	config.vm.provider "virtualbox" do |v|
		v.name = "nodebase"
		v.memory = 1024
	end


end
