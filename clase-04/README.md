# Clase 04 - Git desarrollo colaborativo

## Git Stash

* Existe dentro de git
* No se puede subir al remoto
* Trabaja con una estructura de pila

![fifo-lifo](_ref/image.png)

## Listar los stashes

```sh
git stash list
```

## Crear un stash

```sh
git stash -m "Mensaje descriptivo"
```

## Ver contenido del stash

```sh
git stash show <identificador del stash>
git stash show 0
git stash show stash{0}
```