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