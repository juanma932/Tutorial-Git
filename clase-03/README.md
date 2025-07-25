# Clase 03 - Git Desarrollo Colaborativo

## Como subir un repositorio local al repositorio remoto.

1. Crear el repositorio en GitHub

2. Agregar la ruta del repositorio remoto en el local

```sh
git remote add <alias> <url>
git remote add origin https://github.com/mlapeducacionit/git-78016.git
```

3. Hacen la subida del repositorio local al remoto

```sh
git push -u <remoto> <rama>
git push -u origin main
```

## Para configurar su entorno y la cuenta de GitHub para SSH

<https://kinsta.com/es/blog/generar-claves-ssh/>


## Para clonar un repositorio
Traerse al local no solo los archivos sino también la carpeta .git (Una copia exacta del repositorio)

```sh
git clone <url>
git clone https://github.com/mlapeducacionit/git-78016.git # crear una carpeta con el nombre del repo y dentro clona
git clone https://github.com/mlapeducacionit/git-78016.git ./ # ./ ---> Le indica a clone que no cree la carpeta y clone todo en el directorio actual
```

## Branches (Ramas)

### Proyectos complejos
![ramas](_ref/image-1.png)

### Proyectos sencillos
![ramas](_ref/image-2.png)

## Crear una rama

```sh
git branch <nombre-rama>
git branch feature/ramas # crea la rama pero no cambia a esa rama
git switch -c <nombre-rama>
git switch -c dev
```

