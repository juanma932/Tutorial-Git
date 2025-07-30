# Clase 04 - Git Desarrollo Colaborativo

## Listar ramas disponibles en el repositorio

```sh
git branch
```

## Cambiarse de ramas

```sh
git switch <nombre-rama>
git switch dev
git switch main
git switch - # me permite cambiar entre la rama actual y la última en la que estuve
```

## Crear un rama

> Crea la rama y no me mueve a la rama creada

```sh
git branch <nombre-rama>
```

> Crea la rama y me mueve a la rama creada
```sh
git switch -c <nombre-rama>
```

## Borramos un rama

```sh
git branch -d <nombre-rama>
git branch -d feature/borrar-rama
```

## Forzar el borrado
Esto se va a necesitar hacer cuando la rama que quiero borrar no este fusionada con otras. O sea que hay cambios que en la rama que borrar no se encuentran en las demás.

```sh
git branch -D <nombre-rama>
git branch -D feature/borrar-rama # Borro de manera forzada la rama
```

## Contar la cantidad de commit local

```sh
git rev-list --count HEAD
```

## Para revisar si hay cambios en el remoto (Sin traerlos)
Solo traigo la metada data. (Actualizo la carpeta .git local)

```sh
git fetch
```

## Me traigo los cambios

```sh
git pull # git fetch y luego git pull
```
