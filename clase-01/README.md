# Clase 01 - Git Desarrollo Colaborativo

## Página de Git

<https://git-scm.com/>

## Git con interfaz gráfica

* <https://www.sourcetreeapp.com/>
* <https://www.gitkraken.com/>
* <https://desktop.github.com/download/>

## Configuración inicial
Está configuración se hace una sola vez. Y es para indicarle a git con que nombre y correo se van a firmar los commits creados

```sh
git config --global user.name "Maximiliano Principe"
git config --global user.email mlpeducacionit@gmail.com
```

## Verificar la configuración del usuario

```sh
git config --get-regexp user
```

## Listar configuraciones

```sh
git config --list
```

## Para editar las configuraciones

```sh
git config --global -e
```

## Para crear un repositorio de git

```sh
git init
```

## En el caso de que no haya colocado en la instalación main

```sh
git config --global init-defaultBranch main
```

## Ver los commits generado (Timeline de commits)

```sh
git log # versión larga
git log --oneline # versión corta
```
