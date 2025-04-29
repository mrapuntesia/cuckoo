Descargar y levantar una maquina virtual con Ubuntu 18.04.6 LTS (Bionic Beaver):
    https://releases.ubuntu.com/18.04.6/ubuntu-18.04.6-desktop-amd64.iso

sudo apt update

sudo apt upgrade

sudo apt-get install python python-pip python-dev libffi-dev libssl-dev -y

sudo apt-get install python-virtualenv python-setuptools -y

sudo apt-get install libjpeg-dev zlib1g-dev swig -y

sudo apt-get install mongodb -y

sudo apt-get install postgresql libpq-dev -y

sudo apt install virtualbox -y

sudo apt-get install tcpdump apparmor-utils -y

sudo adduser --disabled-password --gecos "" cuckoo

sudo groupadd pcap

sudo usermod -a -G pcap cuckoo

sudo chgrp pcap /usr/sbin/tcpdump

sudo setcap cap_net_raw,cap_net_admin=eip /usr/sbin/tcpdump

getcap /usr/sbin/tcpdump

sudo aa-disable /usr/sbin/tcpdump

sudo apt-get install swig

sudo pip2 install m2crypto==0.31.0

sudo usermod -a -G vboxusers cuckoo

cd /opt/

sudo nano cuckoo-setup-virtualenv.sh
    #!/usr/bin/env bash
    
    # NOTES: Run this script as: sudo -u <USERNAME> cuckoo-setup-virtualenv.sh
    
    # install virtualenv
    sudo apt-get update && sudo apt-get -y install virtualenv
    
    # install virtualenvwrapper
    sudo apt-get -y install virtualenvwrapper
    
    echo "source /usr/share/virtualenvwrapper/virtualenvwrapper.sh" >> ~/.bashrc
    
    # install pip for python3
    sudo apt-get -y install python3-pip
    
    # turn on bash auto-complete for pip
    pip3 completion --bash >> ~/.bashrc
    
    # avoid installing with root
    pip3 install --user virtualenvwrapper
    
    echo "export VIRTUALENVWRAPPER_PYTHON=/usr/bin/python3" >> ~/.bashrc
    
    echo "source ~/.local/bin/virtualenvwrapper.sh" >> ~/.bashrc
    
    export WORKON_HOME=~/.virtualenvs
    
    echo "export WORKON_HOME=~/.virtualenvs" >> ~/.bashrc
    
    echo "export PIP_VIRTUALENV_BASE=~/.virtualenvs" >> ~/.bashrc 

sudo chmod +x cuckoo-setup-virtualenv.sh

sudo -u thisjesusalan ./cuckoo-setup-virtualenv.sh

source ~/.bashrc

mkvirtualenv -p python2.7 cuckoo-test

pip install -U pip setuptools

pip install -U cuckoo

sudo wget https://archive.org/download/Win7ProSP1ESP/es_windows_7_professional_with_sp1_x64_dvd_u_676947.iso

sudo mkdir /mnt/win7

sudo chown cuckoo:cuckoo /mnt/win7/

sudo mount -o ro,loop es_windows_7_professional_with_sp1_x64_dvd_u_676947.iso /mnt/win7

sudo apt-get -y install build-essential libssl-dev libffi-dev python-dev genisoimage

sudo apt-get -y install zlib1g-dev libjpeg-dev

sudo apt-get -y install python-pip python-virtualenv python-setuptools swig

pip install -U vmcloak

vmcloak-vboxnet0

sudo wget https://archive.org/download/Win7ProSP1ESP/es_windows_7_professional_with_sp1_x86_dvd_u_677069.iso

sudo su cuckoo





Comando adicionales
-------------------------------------------------------------------
Al iniciar ubuntu:
* Moverme a la caperta opt
* Activar el entorno virtual "cuckoo-test"

cd /opt/
workon cuckoo-test
-------------------------------------------------------------------

-------------------------------------------------------------------
Me habia equivocado de iso, tuve que:
* Desmontar la iso de 32bits
* Borrar la iso de 32bits
* Descargar la iso de 64 bits
* Montar la iso de 64 bits

sudo umount /mnt/win7
sudo rm /opt/es_windows_7_professional_with_sp1_x86_dvd_u_677069.iso
sudo wget https://archive.org/download/Win7ProSP1ESP/es_windows_7_professional_with_sp1_x64_dvd_u_676947.iso
sudo mount -o ro,loop es_windows_7_professional_with_sp1_x64_dvd_u_676947.iso /mnt/win7
-------------------------------------------------------------------

Habilitar virtualización anidada en VirtualBox en Windows 11 "Enable Nested VT-x/AMD-V"
-------------------------------------------------------------------
cd C:\Program Files\Oracle\VirtualBox
VBoxManage modifyvm "Ubuntu_Cucko" --nested-hw-virt on
-------------------------------------------------------------------
