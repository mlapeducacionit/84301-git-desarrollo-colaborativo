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

## Recuperar el stash

```sh
git stash pop # Recuperar el último stash realizado y si no hay conflicto lo borra.
```

## Aplicar un stash en particular

```sh
git stash apply # Aplica el stash de arriba de todo
git stash apply 1 # stash@{1}
git stash apply 2 # stash@{1}
```

## Eliminar un stash en particular

```sh
git stash drop # Borra el stash de arriba de todo
git stash drop 1 # stash@{1}
git stash drop 2 # stash@{2}
```

# Git resets
Me permite deshacer commits. Hay 3 tipos

## GIT RESET SOFT
Me permite deshacer uno o varios commits y los cambios lo arroja al staging area (SA)

```sh
git reset --soft <hash>
```

## GIT RESET MIXED (default)
Me permite deshacer uno o varios commits y los cambios los arroja al working directory (WD)

```sh
git reset <hash>
git reset --mixed <hash>
```

## GIT RESET HARD
Me permite deshacer uno o varios commits y los cambios los descarta (CUIDADO PIERDO LOS CAMBIOS SOBRE LOS ARCHIVOS)

```sh
git reset --hard <hash>
```

## Trabajar colaborativamente con personas que no conozco (Fork y Pull Request)

Me permite trabajar colaborativamente en proyectos donde no conozco a las personas o no tengo la suficiente confianza para darle permisos al repositorio de trabajo. 

Normalmente cuando trabajo con Fork y Pull Request lo hago en proyectos Open Source.

* Fork es una copia del respositorio remoto de alguien a mi cuenta de GitHub.
* Pull Request. Solicitud  a los dueños originales del repositorio para proponerles un cambio. Es una propuesta de cambio a alguien que no conozco pero quiero ayudar.

1. Hacer un fork del proyecto. Del proyecto del cual quiero contribuir (Me voy copiar en mi cuenta el repo del proyecto original)
2. Me clono el fork desde mi cuenta github
3. Trabajo normalmente. Subo los cambios (A repo propio)
4. Me voy al proyecto original en el apartado Pull Request. Creo un nuevo Pull Request. Algunas veces aparece en mi repo la posibilidad Pull Request.
---
5. Si el repo original sufrió más modificaciones. (Commits). Voy a tener que actualizar mi fork.
6. Voy a la cuenta del proyecto original y me copio la url del repositorio
7. Y agrego en mi repositorio local, la url (el remoto) del proyecto original.

    git remote add upstream <URL-repositorio-original>

8. Me traigo los cambios del repositorio original a mi repo local

    git pull upstream <rama-que-quiero-actualizar>

9. Subo a mi repositorio remoto (Fork) las actualizaciones del repo local

    git push origin <rama-a-actualizar>

# Git TAGS

## 2 tipos de punteros (referencias). Punteros (referencias) estáticos y los punteros dinamicos

# Estáticos

> Tags

# Dinámicos

> HEAD, Ramas

## Crear un tags

```sh
git targ v1.0
git tag  -a v0.8 -m "Versión no final" <hash>
# Ejemplo de tag en un commit en especifico
git tag  -a v0.8 -m "Versión no final" c616c7d
# Ejemplo de tag en último commit
git tag -a v1.0 -m "Versión actual de la documentación"
```

## Listar tags creados

```sh
git tag --list
```