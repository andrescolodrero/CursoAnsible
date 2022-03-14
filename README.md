## CursoAnsible
Código para el curso de Ansible

# Prerequisitos

Instalar Vagrant y Ansible. Instrucciones en /vagrant/instalacion.

# Post-install
1. Crear un usuario "vagrant", "pass:" vagrant en vuestra máquina "WSL" (este usuario se usará para conectarse a la máquina creada con Vagrant)

2. Anotar IP de vuestra máquina de vagrant (la hemos creado con IP estática en el fichero /vagrant/vagranfile)

3. Desde WSL probar: 
    ping 172.23.240.10 

4. Desde WSL:
    su vagrant
    ssh 172.23.240.10
    o con sudo: ssh vagrant@172.23.240.10

Si los test 3 y 4 funcionan, podemos proceder a Ansible