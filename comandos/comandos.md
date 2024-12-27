>> Inicializando a boxe
-> vagrant init ubuntu/trusty64 --box-version 20191107.0.0

>> Configuração
Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_version = "20191107.0.0"
end

>> Inicialização 
-> vagrant up

>> Destruir
-> vagrant destroy

>> Acesso a boxe
-> vagrant ssh

>> Recarregar 
-> vagrant reload

>> Provision
-> vagrant provision