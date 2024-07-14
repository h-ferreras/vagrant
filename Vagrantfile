Vagrant.configure("2") do |config|

  # Configuración de la primera máquina virtual
  config.vm.define "web1" do |web1|
    web1.vm.box = "ubuntu/bionic64"
    web1.vm.network "private_network", type: "dhcp"
    web1.vm.hostname = "web1"

    # Provisión para instalar Apache y compartir la carpeta
    web1.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y apache2
      sudo rm -rf /var/www/html
      sudo ln -fs /vagrant/html /var/www/html
    SHELL
  end

  # Configuración de la segunda máquina virtual
  config.vm.define "web2" do |web2|
    web2.vm.box = "ubuntu/bionic64"
    web2.vm.network "private_network", type: "dhcp"
    web2.vm.hostname = "web2"

    # Provisión para instalar Apache y compartir la carpeta
    web2.vm.provision "shell", inline: <<-SHELL
      sudo apt-get update
      sudo apt-get install -y apache2
      sudo rm -rf /var/www/html
      sudo ln -fs /vagrant/html /var/www/html
    SHELL
  end

end
