# Linux Cheat Sheet
Comandos Linux bons de serem lembrados

## Criação de Links simbólicos
> Os comandos precisam ser executados como `sudo`
```sh
$ ln -s [alvo] [link]

$ ln -s /opt/apps/apache-maven-3.0.5 /usr/local/maven
$ ldconfig (para atualizar)
```

## Descompactação

```sh
$ gzip -d [nome.tar.gz]

$ tar -tvf [nome.tar] (lista a estrutura de pastas e arquivos dentro do compactado)
$ tar -xvf [nome.tar]

$ unzip [nome.zip]
```

## Instalação
Como instalar pacotes em distros Linux

### Via RPM
```sh
$ rpm -i [pacote]
```

### Execução e descompactação

```sh
$ chmod u+x SenchaCmd-3.1.2.342-linux-x64.run 
```
> Sepois basta executar como um bash normal
> Também vale para .bin

## Habilitar ROOT
```sh
$ sudo passwd root
$ su root
$ sudo su -
```

## Alteração de permissões ###
```sh
$ chown -R [usuario]]:[grupodeusuarios] [pasta]

$ chmod -R  o+rx android-sdk-linux/
$ chmod -R 755 android-sdk-linux/
```

```
0 == --- == no access
1 == --x == execute
2 == -w- == write
3 == -wx == write / execute
4 == r-- == read
5 == r-x == read / execute
6 == rw- == read / write
7 == rwx == read / write / execute

-R == alterar também para arquivos e subpastas
```

## Informações sobre os processos
```sh
$ ps -ef | grep [expressão]
$ top
$ sa - Mostra informações sobre os processos que estão sendo executados pelos usuários.

$ kill -9 [numero do processo]
$ killall [nome do processo]
```

## Transferência na rede
```sh
$ scp -rp Maven/ eclipse-jee-juno-SR1-linux-gtk-x86_64.tar root@10.5.114.37:/tmp
```

## Samba e Rede Windows
### Acesso a rede Windows
```sh
$ smb://[endereco da rede]
```

### Reiniciar Samba
```sh
$ invoke-rc.d samba restart
```