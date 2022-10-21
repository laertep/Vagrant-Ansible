Vagrant.configure("2") do |config|
   config.vm.provider "virtualbox" do |v|
      v.name = "desafio2"
   end
 config.vm.box = "hashicorp/bionic64"
 config.vm.network "forwarded_port", guest: 80, host: 8090
 config.vm.network "public_network"
     
end  

