## Projeto - Vagrant & Ansible

$ Criação da maquina VM no Virtualbox
* Instalação da VirtualBox e Vagrant na máquina local
* Instalação da ferramenta Ansible na máquina guest;
* Instalação da ferramenta sshpass;
* Copia da pasta ansible local para VM guest;
* Sincronismo da pasta ansible (arquivos de configuração) com a VM na pasta tmp/ansible;
* Copia da pasta tmp/ansible para home/vagrant

$ Criação do arquivo playbook / arquivo de configuração servidor
* Pasta ansible/playbook.yml - arquivo responsável pela execução das roles configuraras;
* Pasta ansible/servidor - arquivo responsável pela localização do servidor e os acessos via ssh pelo usuário vagrant com permissionamento; 
* Execução do comando ansible no arquivo principal vagrantfile - ansible-playbook -i servidor playbook.yml 

$ Criação das roles common e nginx:
* Role common - subpasta tasks - responsável pela instalação dos pacotes de atualização seguido da criação do nome da máquina e um usuário;
* Role nginx - subpasta tasks - responsável para instalar o paconte do nginx e alterar a pagina index no servidor (/var/www/html);
* Role nginx - subpasta handlers - responsável para iniciar o serviço nginx;
* Role nginx - subpasta templates - responsável pelo contéudo da página html

![image](https://user-images.githubusercontent.com/44216245/201559866-9baf289b-4a55-4ff0-bee8-544126218c99.png)
