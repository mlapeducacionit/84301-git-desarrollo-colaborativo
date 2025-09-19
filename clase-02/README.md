# Clase 02 - Git Desarrollo Colaborativo

## .gitkeep
Es un archivo que me permite hacer un commit para guardar una carpeta que no es detectada por git cuando esta vacía.

## .gitignore
Es un archivo que me permite ignorar archivos o carpetas completas, que no quiero que guarden dentro del repositorio. Dentro del archivo menciono los archivo que quiero que git ignore y no guarde dentro del repositorio.

## Repaso comandos básicos

### Marcar archivos que quiero que sean parte del próximo commit
O sea marcar archivos que están en el working directory terminado y quiero llevarlos al area de confirmación para que sean parte del próximo commit.

```sh
git add <nombre-archivo1> <nombre-archivo2>
git add <nombre-archivo>
git add README.md
```

### Ver el contenido de un commit hecho

```sh
git show <hash>
git show 332ad9c
```

### Guardar los cambios en el repositorio

```sh
git commit -m "Mensaje"
git commit # Se abre el editor para escribir el mensaje
git commit -a # Se hace un add de los archivos modificados, no se hace un add de los archivos untracked y se abre el editor para escribir el mensaje
git commit -am "Mensaje" # Se agregan los archivos modificados y no se abre el editor para escribir el mensaje
```

**NOTA**: Los mensajes idealmente pueden tener máximo 80 caracteres.

### Ver los commits dentro del repositorio

```sh
git log # largo con detalle
git log --oneline # corto solo el mensaje
git log -2 # Me muestra 2 commits del listado, los últimos 2
git log --oneline -2 # corto solo el mensaje y solo 2 commits los últimos
```

### Ver la diferencia entre el working directory y el local repo

```sh
git diff
```

## Empezando con ramas


### Lista las ramas locales

```sh
git branch 
```

### Listar ramas remotas y locales

```sh
git branch -av
```

### Crear un rama

```sh
git branch <nombre-rama>
git branch feature/ramas
```

### Cambiarme a la rama

```sh
git switch <nombre-rama>
git switch feature/ramas
```

### Crear una rama y moverse a la rama creada

```sh
git switch -c <nombre-rama>
git switch -c feature/ramas
```