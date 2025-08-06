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



