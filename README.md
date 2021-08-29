# VMs

Estos apuntes están dirigidos a usuarios de Windows10. Las máquinas virtuales disponibles están configuradas para disponer de 2 cores y 2 GB de memoria RAM, pero usted puede cambiar esta configuración desde VirtualBox.

## Antes de empezar

* Debe tener por lo menos 20 GB de espacio libre en su disco duro.
* Instalar el [paquete](https://drive.google.com/file/d/14INu8uW38vVVi1LEN8iZlwWvrf0QWgmz/view?usp=sharing) de extensiones de VirtualBox.
* La ruta donde se encuentra VirtualBox, sus dependencias y utilidades deben estar en la variable de entorno "Path".
* Debe tener instalado Visual Studio Code con la extensión Remote-SSH

## Imágenes disponibles

1. Nuevas:
 
No tienen nada de lo que se va a usar en el curso instalado y se sugiere su uso para aprender a instalar paquetes desde línea de comandos, matar procesos y, en general, para familiarizarse con Ubuntu.

  * [Ubuntu-18.04](https://drive.google.com/file/d/17eUGPDmPD8C9plIF1EdrqPL8qmOOJ9tw/view?usp=sharing)
  * [Ubuntu-20.04](https://drive.google.com/file/d/1m_NJOja1VXeqs6pnyCVahivZhBzPhw9D/view?usp=sharing)

2. Preparadas:

Los paquetes principales que se usarán en el curso ya están instalados.

  * [Ubuntu-18.04](https://drive.google.com/file/d/1lQXXdfGuLRHf5ktGbrCcM_zRyaTSoOsS/view?usp=sharing)
  * [Ubuntu-20.04](https://drive.google.com/file/d/1JZSAU2ndzrxba75M1qq1KP1MB4PROga5/view?usp=sharing)

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

## Para el archivo `config`

Para abrir el archivo `config` hace click en el ícono azul ubicado en la esquina inferior izquierda y selecciona la opción "Open SSH Configuration File ..."

![vscode-config-file](https://github.com/Stefano1511/imagen_ubuntu/blob/main/imgs/vscode-config-file.png)

Luego seleccionar la primera opción

![vscode-config-file-2](https://github.com/Stefano1511/imagen_ubuntu/blob/main/imgs/vscode-config-file-2.png)

En el archivo que se abra coloque lo siguiente

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

## Comandos

Primero, debe abrir un terminal desde Visual Studio Code. Para esto, va a la pestaña "Terminal" y elige "Nuevo terminal"

![vscode-terminal](https://github.com/Stefano1511/imagen_ubuntu/blob/main/imgs/vscode-terminal.png)

Debería observar una sección similar a la siguiente, y se ubica en ella para poder ejecutar los comandos.

![vscode-terminal-2](https://github.com/Stefano1511/imagen_ubuntu/blob/main/imgs/vscode-terminal-2.png)

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
