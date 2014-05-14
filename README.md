toolbox
=======

La caja de herramientas del Escuadrón de Datos


## Dependencias

* [Vagrant](http://www.vagrantup.com/) con [Virtualbox](https://www.virtualbox.org/wiki/Downloads) (recomendado) o [VMware](http://www.vmware.com/)
* [Ansible](http://www.ansible.com)


## Cómo utilizarlo
Una vez instaladas las dependencias, [clonar el repositorio](http://git-scm.com/book/es/Fundamentos-de-Git-Obteniendo-un-repositorio-Git#Clonando-un-repositorio-existente), y ejecutar desde línea de comandos:

```shell
vagrant up
```
ésto puede tardar unos minutos.

Una vez descargada la imagen
```shell
vagrant provision
```

Para entrar al sistema:
```shell
vagrant ssh
```
donde se encontrará el directorio **_dockerfiles_** con varios directorios que contienen las herramientas.

Para construir el contenedor con una herramienta:
```shell
cd NombreDeLaHerramienta
sudo docker.io build .
```

Más detalles en el [wiki](https://github.com/mxabierto/toolbox/wiki)
