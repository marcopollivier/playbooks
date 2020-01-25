# Git Cheat Sheet 

## Configurações Iniciais 

```sh
$ git config --global user.name "Fulano da Silva"
$ git config --global user.email fulanodasilva.git@gmail.com
```

## Criação

### Iniciando um repositório
```sh
$ git init
```

### Clonando um repositório remoto

```sh
$ git clone https://github.com/fulanodasilva/citacoes.git
```

## Verifica o estado dos arquivos em um repositório Git

```sh
$ git status
```

## Adiciona o arquivo na staging area 

```sh
$ git add filmes.txt # Arquivo especifico
$ git add .          #Todos os arquivos
```

## Commita o arquivo 

```sh
git commit -m "Arquivo inicial de citacoes"
```

## Verifica as alterações realizadas 

```sh
$ git log
```

## Aponta o repositório local para um repositório remoto 

```sh
$ git remote add origin https://github.com/fulanodasilva/citacoes.git
```

## Envia as alterações para o servidor remoto 

```sh
$ git push origin master
```

