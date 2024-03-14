---
tags:
  - ca0305
  - code
  - professor
  - git
type: code
---
# Comandos básicos de Git

Luego de la instalación y descarga de Git, es indispensable la practica de algunos comandos básicos y recurrentes en la manipulación de Git.

## Configuraciones `ris:Tools`

1. Cambio de usuario. Nombre a salir en la versión de cambios colaborativo
```shell
git config --global user.name "Nombre de usuario"
```

2. Correo electrónico. Debe ser el asociado a la cuenta de GitHub o  GitLab.
```shell
git config --global user.email "correo_personal@gmail.com"
```

Luego de la configuración se puede abrir *Git CMD* o *Git Bash* para posicionarse en la carpeta que se desea realizar el control de versiones en git. Se pueden usar los comandos:

* *dir*: para ver los archivos en los directorios
* *cd nombre_carpeta*: para ingresar a una carpeta deseada
* *cd..*: regresar al directorio anterior
* *mkdir nombre_carpeta*: crear una carpera o directorio

Luego de posicionarse en la carpeta deseada, creamos el la carpeta de respaldo **.git** ejecutando:
```shell
git init
```

Para verificar,  puede irse de manera manual a la carpeta creada y verificar que haya una carpeta `ris:FolderOpen` **.git**

Para añadir un archivo de la carpeta a *git* se puede ejecutar:

```shell
git add nombre_archivo
```

Luego de agregar el archivo, es necesario realizar el primer **commit** (comentario):

```shell
git commit -m "docs: se agrega docuemento de pueba"
```

### Renombrar ramas

En git podemos trabajar multiples ramas de desarrollo. Para nombrar la rama que se trabaja actualmente se puede ejecutar:
```shell
git branch -M main 
```

* Para crear una nueva rama
```shell
git branch prueba
```

* Cambio de rama
```shell
git creckout prueba
```

En esta rama de prueba se puede realizar varios cambios los cuales es necesario guardar y asegurarse de hacer *commits* antes de tratar de cambiar de rama.

*  Unir ramas 
Antes de unificar las ramas debe tomar en cuenta que es lo que se desea:
![[Merge_vs_rebase.jpg|300]]

Además, debe posicionarse en la rama principal (la que desea mantener) para luego unir la rama secundaria:
```shell
git merge rama_unir_main
```

* Eliminar ramas

```shell
git branch -d prueba
```



## Conexión con GitHub o GitLab
```shell
git remote add origin https://github.com/PotoyJuarez/CA0305_I24.git
```


