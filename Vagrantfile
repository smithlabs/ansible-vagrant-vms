Vagrant.configure("2") do |config|

  (1..3).each do |i|

  # Disable the new default behavior introduced in Vagrant 1.7, to
  # ensure that all Vagrant machines will use the same SSH key pair.
  # See https://github.com/mitchellh/vagrant/issues/5005
  config.ssh.insert_key = false

    config.vm.define "vm#{i}" do |node|
      node.vm.box = "ubuntu/bionic64"
      node.vm.network "private_network", ip: "192.168.25.10#{i}"
      node.vm.provision "shell", inline: "echo hello from node 10#{i}"
    end
  end
  
end
