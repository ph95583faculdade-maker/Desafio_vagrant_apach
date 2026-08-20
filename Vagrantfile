Vagrant.configure("2") do |config|G
  # 1. Define a imagem base do sistema (Ubuntu)
  config.vm.box = "ubuntu/focal64"

    # 2. Define um nome limpo para a máquina na rede
  config.vm.hostname = "pedrinho-gameplays"
  
  # 3. Faz o mapeamento da porta para você conseguir testar no navegador do PC físico
  config.vm.network "forwarded_port", guest: 80, host: 8080

  # 4. O Provisionamento via Shell Script exigido pelo professor para instalar o Apache
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update
    sudo apt-get install -y apache2
  SHELL
end