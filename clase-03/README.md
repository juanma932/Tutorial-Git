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


