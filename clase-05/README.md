# Clase 05 - Git Desarrollador Colarativo

## Ayuda de Git Stash

```sh
git stash --help
```

## Alias de GIT
Me permite crear alias de comandos para en vez de estar escribiendo el comando y sus subcomandos hacerlo en forma resumida (corta). A través de una letra o una palabra.

### Creo un alias

```sh
git config --global alias.<alias-elegido> "<comando-de-git-sin-la-palabra-git>"
git config --global alias.l "log --oneline"
git config --global alias.ll "log --oneline --all --graph --decorate"
git config --global alias.s "status --short"
git config --global alias.c "commit -m"
```




