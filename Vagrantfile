HOST_INTERFACE = "wlp0s20f3"
IP_ADDRESS = "192.168.1.70"
NETWORK_MASK = "255.255.255.0"

Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/focal64"
    # config.vm.provision "shell", inline: <<-SHELL
    #     apt install -y curl=7.65.0-1ubuntu2.18
    # SHELL

    config.vm.define "ansible-target" do |server|
        server.vm.hostname = "ansible-target"
        server.vm.network :public_network, bridge: HOST_INTERFACE, ip: IP_ADDRESS, :netmask => NETWORK_MASK
    end
    
    config.vm.provider "virtualbox" do |v|
       v.memory = 4096
       v.cpus = 2
  
  end
end
