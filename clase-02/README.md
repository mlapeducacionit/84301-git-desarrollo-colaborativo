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