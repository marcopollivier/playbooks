# Pacman Cheat Sheet
Lista de comandos úteis para executar quando estiver usando **Pacman**

## Para escolher um "espelho" melhor
Se a atualização dos pacotes estiver lento demais,esse comendo será util
```sh
$ sudo pacman-mirrors -g
```

## Para Atualizar o sistema
```sh
$ sudo pacman -Syu
```

### Para Atualizar a base de dados
```sh
$ sudo pacman -Syy
```

## Instalação
### To install a package (always run pacman -Syu, before installing):
```sh
$ sudo pacman -S package_name
```

### To install a local package, or from a website:
```sh
$ sudo pacman -U /path/to/the/package
```

### To re-install all packages (those from the repo’s), in case of emergency:
```sh
$ sudo pacman -Sy $(pacman -Q | cut -d " " -f1 | grep -v "$(pacman -Qm | cut -d " " -f1)")
```

## Removing Packages

If you want to only remove the package, the following command is sufficient:
```sh
$ sudo pacman -R
```
To remove the package and those of its dependencies that aren’t needed by any other application, do
```sh
$ sudo pacman -Rs
```
Finally, to remove the package, avoid orphaned dependencies and erase its global configuration, type
```sh
$ sudo pacman -Rns package_name
```
which in most cases is the proper command to remove software.

## Searches/Queries

### Info about an installed package:
```sh
$ pacman -Qi package_name
```
### Queries the repo about a package:
```sh
$ pacman -Ss package_name
```
### Queries the repo about a packages, and all that depend on it:
```sh
$ pacman -Sii package_nam
```

## Howto
### List Installed Packages that are not in the Official Repositories:

If you want a list of the packages you build and installed locally or packages that are no longer in the official repositories:
```sh
$ pacman -Qm
```

Make sure to check this regularly, preferably monthly but at least every three months. KaOS repositories are always moving so you don’t want to keep unmaintained and possibly conflicting packages in your install.

### Pacman is completely broken! How do I reinstall it?

In the case that pacman is broken beyond repair, manually download the necessary packages (openssl, libarchive, and pacman) and extract them. The pacman binary will be restored along with its default configuration file. Afterwards, reinstall these packages with pacman to maintain package database integrity. You can use this command to extract them.
```sh
$ sudo tar -xwvpf <i>package_name-version.tar.xz</i> -C / --exclude .PKGINFO --exclude .INSTALL
```
### Lock DB

deletar o arquivo db.lck
```sh
$ sudo rm /var/lib/pacman/db.lck
```
---
More info:
- http://wiki.archlinux.org/index.php/Pacman
- https://kaosx.us/docs/pacman/



