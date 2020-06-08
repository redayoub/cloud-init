Vagrant.configure("2") do |config|
    config.vm.provision :cloud_init,
      wait: true,
      user_data: "./cloud-ini/user-data.yml",
      meta_data: "./cloud-ini/meta-data.yml"
    
    config.vm.define "server1" do |server1|
      server1.vm.box = "debian/buster64"
      server1.vm.hostname = "server1"
      server1.vm.network "private_network", ip: "192.168.10.100"
      server1.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
      end
    end
end