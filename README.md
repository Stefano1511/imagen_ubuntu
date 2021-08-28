# VMs

Las máquinas virtuales disponibles están configuradas para disponidor de 2 cores y 2 GB de memoria RAM, pero usted puede cambiar esta configuración desde VirtualBox.

## Imágenes disponibles

* [Ubuntu-18.04](https://drive.google.com/file/d/1az_z5qO1UpoqoB-XD-b2EVzUN09vU1Ud/view?usp=sharing)
* [Ubuntu-20.04](https://drive.google.com/file/d/1m_NJOja1VXeqs6pnyCVahivZhBzPhw9D/view?usp=sharing)

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
