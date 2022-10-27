Vagrant.configure("2") do |config|
   config.vm.provider "virtualbox" do |v|
      v.name = "desafio2"
   end
 config.vm.box = "hashicorp/bionic64"
 config.vm.network "forwarded_port", guest: 80, host: 8090
 config.vm.network "public_network"
 config.vm.synced_folder "./ansible/","/tmp/ansible"
 config.vm.provision "shell",inline:<<-SHELL
  sudo apt update
  sudo apt -y install ansible
  sudo apt -y install sshpass
  sudo cp -Rf /tmp/ansible/. /home/vagrant/
  sudo cp /tmp/ansible/ansible.cfg /etc/ansible/
  sudo ansible-playbook /tmp/ansible/playbook.yml
  sudo ansible-playbook -i servidor playbook.yml
  SHELL
 
end  

