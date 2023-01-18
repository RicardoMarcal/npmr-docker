# N.P.M.R Docker

> N.P.M.R. é uma sigla para Nginx, PHP, MySQL e Redis. Este repositório

## 💻 Pré-requisitos

Antes de começar, verifique se você atendeu aos seguintes requisitos:

* Este projeto foi clonado em sua máquina;
* Em seu terminal você está na pasta raiz dest projeto;
* Você possui o `Docker` instalado em sua máquina;
* O `Docker` está rodando em sua máquina.

## 🚀 Iniciando o "N.P.M.R Docker"
Desenvolvimento:
```
docker compose -f docker-compose.dev.yaml up --build -d
```

Produção:
```
docker compose up --build -d
```

## 💻 Instalando as dependências de desenvolvimento do PHP
> OBS: você deve estar com o projeto rodando em modo de desenvolvimento.
```
docker exec -it npmr-docker-app-1 sh
```
```
composer install --ignore-platform-reqs
```
```
composer dump-autoload
```
```
exit
```

## ⬇️ Parando o "N.P.M.R Docker"
```
docker compose down
```