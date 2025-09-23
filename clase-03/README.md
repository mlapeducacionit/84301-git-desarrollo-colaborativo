# Clase 03 - Git desarrollo colaborativo

## Estado de los archivos

```sh
git status
```

## Agregar a la zona de staging area o index (Área de confirmación)

```sh
git add <nombre-archivo>
git add . # todos los archivos.
```

## Persitir los archivos que coloco en el staging area (Hacer commit)

```sh
git commit -m "Mensaje"
git commit # abre un editor de texto y me permite escribir el mensaje
``` 

## Ver los commits

```sh
git log # forma larga
git log --oneline # forma corta
git log -5 # cantidad de commits que quiero que muestre.
```

## Como veo la diferencia entre lo que tengo en el WD y LR

```sh
git diff
```

## La diferencia entre 2 ramas. La rama main y la rama dev

```sh
git diff <nombre-rama>
# Ejemplo
git switch main
git diff dev
```

## Como arreglo el mensaje de un commit (El último)

```sh
git commit --amend 
```

**IMPORTANTE**: Además de corregir el mensaje puedo agregar archivos que olvidé dentro del commit

```sh
git add <archivo-que-me-olvide>
git commit --amend 
```

## Crear una rama

```sh
git branch <nombre-rama>
```

## Cambiarse de rama

```sh
git switch <nombre-rama>
```

## Funsionar 2 ramas

```sh
git merge <nombre-rama>
# Si me quiero traer los cambios que esta en dev a la rama main
git switch main
git merge dev
```

## Hacer un commit sin cambiar el mensaje pero agregando archivos o línea de código que nos faltar guardar dentro del commit

```sh
git add . # agrego archivos o líneas fueron modificadas
git commit --amend --no-edit # Evito cambiar el mensaje.
```

## Agregar modificaciones de archivos granularmente (Agregar partes del codigo agregado en un archivo)

```sh
git add --patch
```


