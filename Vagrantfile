Vagrant.configure(2) do |config|
  config.vm.define :host do |node|
    node.vm.box = "centos7"
    node.vm.network :forwarded_port, guest: 22, host: 2001, id: "ssh"
    node.vm.network :private_network, ip: "192.168.33.11"
  end

  config.vm.define :target do |node|
    node.vm.box = "centos7"
    node.vm.network :forwarded_port, guest: 22, host: 2002, id: "ssh"
    node.vm.network :forwarded_port, guest: 80, host: 8000, id: "http"
    node.vm.network :private_network, ip: "192.168.33.12"
  end
end
