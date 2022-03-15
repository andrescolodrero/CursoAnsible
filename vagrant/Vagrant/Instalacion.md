# Prácticas de Ansible
## Prerequisitos: Vagrant o Maquina Virtual UBUNTU en HYperV
# Preinstalación
Para que WSL puede comunicar con maquinas virtuales creadas con Vagrant, todas las maquinas deben de ester ne el mismo virtual siwtch:

powershell: ip config
Ethernet adapter vEthernet (WSL):

   Connection-specific DNS Suffix  . :
   Link-local IPv6 Address . . . . . : fe80::4962:6505:7f4e:9b36%47
   IPv4 Address. . . . . . . . . . . : 192.168.80.1
   Subnet Mask . . . . . . . . . . . : 255.255.240.0
   Default Gateway . . . . . . . . . :

### Copiar "IPv4 Adddress"
Editar el fichero "/vagrant/Vagrantfile

$script = <<-'SCRIPT'
ip address add (ip de la nueva maquina)/20 dev eth0
ip route add default via (ipv4 address de wsl) dev eth0
echo "nameserver 192.168.1.1" > /etc/resolv.conf
SCRIPT


# Vagrant 
1. Desinstalar CodeReadyContainer o DockerDesktop para liberar memoria y espacio.
2. Instalar Vagrant: https://www.vagrantup.com/downloads
3. Descargar ejecutable o ejecutar como admin "choco install vagrant"
4. Crear una carpeta "vagrant": mkdir c:\vagrant
4. Reiniciar ordenador
5. Crear una nueva variable de systema "VAGRANT_HOME" = "c:\vagrant"
6. Probar la instalacion: 
   cd /Vagrant/
   vagrant up -> (como Administrador)
   
 una vex terminada la instalaci´pn, probar con:
 vagrant ssh
 
Test: Desde WSL probar "ping ip"  o "ssh vagrant@ip"

# Instalar Ansible en nuestra maquina.
Ansible solo se ejecuta en linux, asi que tendremos que editar y ejecutar comandos desde WSL2

1. Installar en Visual Studio Code: "Remote -WSL"
2. Reiniciar Visual Studio Code
3. Abrir un Terminal de Ubuntu WSL
4. Apt update
5. apt install ansible

