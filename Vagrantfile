Vagrant.configure("2") do |config|

# Configurando a VM
    config.vm.define:magnoUbuntu do |teste_config|
        teste_config.vm.box = "ubuntu/focal64"
        teste_config.vm.network "public_network", ip: "192.168.10.58"
        teste_config.vm.synced_folder "./data", "/vagrant_data"
        #teste_config.vm.vm.synced_folder "../ansible/", "/tmp/ansible"
    config.vm.hostname = "ubuntu-magno"
    config.vm.provision "shell", inline: <<-SHELL
      sudo apt update
      sudo apt -y install vim curl telnet unzip wget net-tools htop nmap
      sudo useradd magno
      sudo apt -y install nginx
      SHELL
    end
end