# VMs

Las máquinas virtuales disponibles están configuradas para disponidor de 2 cores y 2 GB de memoria RAM, pero usted puede cambiar esta configuración desde VirtualBox.

## Antes de empezar

* Debe tener por lo menos 20 GB de espacio libre en su disco duro.
* Instalar el [paquete](https://drive.google.com/file/d/14INu8uW38vVVi1LEN8iZlwWvrf0QWgmz/view?usp=sharing) de extensiones de VirtualBox.

## Imágenes disponibles

* [Ubuntu-18.04](https://drive.google.com/file/d/1az_z5qO1UpoqoB-XD-b2EVzUN09vU1Ud/view?usp=sharing)
* [Ubuntu-20.04](https://drive.google.com/file/d/1m_NJOja1VXeqs6pnyCVahivZhBzPhw9D/view?usp=sharing)

## Importar VM

* Desde la GUI de VirtualBox ir a la opción Archivo, luego seleccionar "Importar servicio virtualizado"

![primer-paso](https://github.com/Stefano1511/imagen_ubuntu/blob/main/imgs/importar-vm.png)

* Debería observar una ventana de diálogo como la siguiente, haga click en el ícono del directorio

![segundo-paso](https://github.com/Stefano1511/imagen_ubuntu/blob/main/imgs/importar-vm-dialogo-1.png)

* Se debe ubicar en el directorio donde está alguna de las VMs que ha descargado y hacer click en "Abrir"

![tercer-paso](https://github.com/Stefano1511/imagen_ubuntu/blob/main/imgs/importar-vm-dialogo-2.png)

* Debería observar una ventana de diálogo como la siguiente, haga click en "Next"

![cuarto-paso](https://github.com/Stefano1511/imagen_ubuntu/blob/main/imgs/importar-vm-dialogo-3.png)

* Por último, hace click en "Importar" y espera a que el servicio termine de ser importado

![quinto-paso](https://github.com/Stefano1511/imagen_ubuntu/blob/main/imgs/importar-vm-dialogo-4.png)

## Comandos

* Para ver las máquinas virtuales disponibles

```shell
VBoxManage.exe list vms
```

* Para poner en funcionamiento una máquina virtual sin GUI:

```shell
VBoxManage.exe startvm "ubuntu18" --type headless
```

Note que se está usando "ubuntu18" como ejemplo.

* Para apagar la máquina virtual:

```shell
sudo shutdown -P now
```

## Para el archivo `config`

```shell
Host ubuntu18
  HostName 127.0.0.1
  User ubuntu18
  Port 2225

Host ubuntu20
  HostName 127.0.0.1
  User ubuntu20
  Port 2226
```
