# Clase 06 - Git Desarrollo Colaborativo.

## Operadores ^ y ~
Se utilizan para referirse a commits anteriores a partir del HEAD

### ^ (padre directo)
Se usa para acceder a los padres de un commit. Por defecto ^ equivale a ^1

### ~ (n ancestros atrás en la primera línea) -> ALT + 126
Se usa para retroceder n commits siguiendo siempre el primer padre. Es un equivalente a utilizar ^^^.

## Git Tag
Me permite marcar ciertos commits y darles un indentificador especial. Lo que es marcas ciertos commits con una etiqueta


### Crear un tag

```sh
git tag v1.0 # Si no le indico commit al cual quiero agregarle un tag, me lo coloca en el último.
git tag -a v0.5 HEAD~3 -m "Versión BETA"
git tag -a v0.1 e1a79a3 -m "Empiezo a desarrollar"
```

### Listar tags

```sh
git tag
```

### Ver información sobre un tag

```sh
git show <nombre-tag>
git show v0.1
git show v1.0
```

### Borro un tag

```sh
git tag -d <nombre-tag>
git tag -d v0.1
```

### ¿Subimos todos los tags?
No es recomendable subir todos los tags

```sh
git push origin --tags # SUBE TODOS LOS TAGS (NO USAR)
```

> Subir tags en especifico

```sh
git push origin v1.0
git push origin v0.1
git push origin v0.5
```

> Borrar tags subidos a GitHub

```sh
git push origin --delete v0.5
```

# Trabajar con GIT en forma colaborativa con personas que conozco
Lo que tengo que hacer es crear un repositorio en GitHub y agregar a mis colaboradores.

* Voy a la cuenta de GitHub 
* Creo el repositorio
* Agrego a mis colaboradores -> Settings -> Collaborators

## Git Blame
Me va a permitir ver línea por línea quien fue el último que modificó esa línea y en que commit se hizo el cambio.

```sh
git blame <nombre-archivo>
git blame <nombre-archivo> -L # rango de líneas
git blame <nombre-archivo> -e o -s # correo o nombre del que hizo el commit
```

```sh
git blame --help
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

