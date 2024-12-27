Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.box_version = "20191107.0.0"
  config.vm.network "forwarded_port", guest: 80, host: 8090
  config.vm.network "public_network"
  config.vm.provision "shell", path: "script.sh"
    ## inline: "apt update && apt -y install nginx && service nginx start"
  config.vm.synced_folder "site/", "/var/www/html"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end
end