# Projeto Cluster Local, Vagrant-VirtualBox-Docker

Demonstração e exercício para curso Docker Fundamentos, DIO

## Ambiente
Host local: Sistema operacional Ubuntu 22.04, 8Gb RAM, Intel Core i5

### Instalação VirtualBox
```bash
wget -O- https://www.virtualbox.org/download/oracle_vbox_2016.asc | sudo gpg --yes --output /usr/share/keyrings/oracle-virtualbox-2016.gpg --dearmor
sudo apt update
sudo apt-get install virtualbox-7.1
```
Obs: Vagrant não suporta versão 7.2 do VirtualBox.

### Instalação Vagrant
```bash
wget -O - https://apt.releases.hashicorp.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/hashicorp-archive-keyring.gpg
echo "deb [arch=$(dpkg --print-architecture) signed-by=/usr/share/keyrings/hashicorp-archive-keyring.gpg] https://apt.releases.hashicorp.com $(grep -oP '(?<=UBUNTU_CODENAME=).*' /etc/os-release || lsb_release -cs) main" | sudo tee /etc/apt/sources.list.d/hashicorp.list
sudo apt update && sudo apt install vagrant
```
O arquivo worker.sh é preenchido durante a execução e está com conteúdo somente para efeitos de demonstração.

### Imagem utilizada: Ubuntu Jammy 22.04 LTS
Vagrant Image TAG bento/ubuntu-22.04
https://portal.cloud.hashicorp.com/vagrant/discover/bento/ubuntu-22.04

### Imagem com testes em andamento e mais leve
Vagrant Image TAG bento/fedora-42
https://portal.cloud.hashicorp.com/vagrant/discover/bento/fedora-42

<img width="959" height="660" alt="VirtualBox com hosts em execução" src="https://github.com/user-attachments/assets/156213e7-6c6e-4465-a465-1bee1eb76e12" />

<img width="1868" height="1023" alt="Hosts em cluster com apache e load da máquina hospedeira" src="https://github.com/user-attachments/assets/b6dda4be-44ee-443c-babf-a66dead49551" />
