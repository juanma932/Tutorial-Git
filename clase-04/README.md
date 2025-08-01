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

## .gitignore
Me permite ignorar archivos que no quiero que formen parte del repo

## .gitkeep
Me permite guardar una carpeta vacía en un repo de git.

## Continuando con ramas (merge)
Tengo que estar en la rama que quiero traerme los cambios.
Cuando quise traerme los cambios que estaban en feature/ramas tuve que moverme a la rama main porque ahí quería los cambios de la rama feature/ramas

```sh
git switch main
git merge <nombre-rama-que-quiero-traerme>
git merge feature/ramas
```

* fast-forward -> Automatico -> Nos encanta. Es la manera automatica que tiene git de resolver una fusión.
* triple-via -> Automatico (tiene diferentes algoritmos para resolver la fusión) -> Nos gusta. Crea un commit intermedio.
* conflicto -> Manual -> No sabe que hacer con las líneas de código que queremos fusionar. Tenemos que trabajar para solucionar el conflictos. 

## Herramientas con interfaz gráfica para trabajar con GIT

* Github Desktop <https://desktop.github.com/download/>
* GitKraken <https://www.gitkraken.com/>
* Sourcetree <https://www.sourcetreeapp.com/>

## GIT STASH
No se puede subir al remoto. Me permite almacenar trabajo que no están terminado. Para poder seguir trabajando en otra funcionalidad o problema que haya surgido.

### Listar stashes que tengo.

```sh
git stash list
```

### Crear un stash

```sh
git stash 
git stash -m "mensaje descriptivo de lo que guardo"
```

### Para recuperar un stash (último)
El pop lo que hace es recuperar lo que está dentro del stash y borrarlo. Si hay conflicto. No borra el stash.

```sh
git stash pop 
```

### Para ver el contenido de un stash

```sh
git show stash@{0}
```