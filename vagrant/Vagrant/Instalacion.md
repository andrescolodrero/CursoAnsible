## Prácticas de Ansible
## Prerequisitos: Vagrant o Maquina Virtual UBUNTU en HYperV
#  Desinstalar CodeReadyContainer o DockerDesktop para liberar memoria y espacio.
# Maquina virtual Ubuntu
1. Descargar Ubuntu Server ISO: https://ubuntu.com/download/server
2. Powershell como admin: Get-NetIPInterface | where {$_.InterfaceAlias -eq 'vEthernet (WSL)' -or $_.InterfaceAlias -eq 'vEthernet (K8s-Switch)'} | Set-NetIPInterface -Forwarding Enabled

3. Crear máquina virtual con HyperV
3.1. Seleccionar "New -> Virtual Machine". Requisitos:
- Memory: 2GB
- VirtualSwitch: Default Switch
- Disco: 20gb
- Installation: ISO file (importar el iso descargado previamente)
- Si falla reboot, desmontar el CD de la máquina.

4. Proceder a Instalación básica de una maquina Linux.
NOTA: Usar configuración básica. No hace falta esperar para "snap" updates.
NOTA: recordar usuario.


# Vagrant 
# Habailitar port forwading: (como admin)
Get-NetIPInterface | where {$_.InterfaceAlias -eq 'vEthernet (WSL)' -or $_.InterfaceAlias -eq 'vEthernet (K8s-Switch)'} | Set-NetIPInterface -Forwarding Enable

1. Desinstalar CodeReadyContainer o DockerDesktop para liberar memoria y espacio.
2. Instalar Vagrant: https://www.vagrantup.com/downloads
3. Descargar o ejecutar como admin "choco install vagrant"
4. Crear una carpeta "vagrant": mkdir c:\vagrant
4. Reiniciar ordenador
5. Crear una nueva variable de systema "VAGRANT_HOME" = "c:\vagrant"
6. Probar la instalacion: /sesiones/Ansible/Vagrant

# Instalar Ansible en nuestra maquina.
Ansible solo se ejecuta en linux, asi que tendremos que editar y ejecutar comandos desde WSL2

1. Installar en Visual Studio Code: "Remote -WSL"
2. Reiniciar Visual Studio Code
3. Abrir un Terminal de Ubuntu
4. Apt update
5. apt 

