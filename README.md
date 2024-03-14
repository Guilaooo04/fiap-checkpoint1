# Checkpoint 1

Aplicação Java com container para exemplo

## Pré-requisitos

- Java 17+
- Docker
- Acesso a internet
- Acesso ao Docker Hub

## Instalação

#### Clone

```
git clone https://github.com/Guilaooo04/fiap-checkpoint1.git
```

## Execução


#### Docker

* Criar imagem

```
docker build -t ping .
```

* Executar container

Para o perfil de desenvolvimento:

```
docker run -d -p 8080:8080 -e PROFILE=dev ping
```

Para o perfil de staging:

```
docker run -d -p 8080:8080 -e PROFILE=stg ping
```


Para o perfil de produção:

```
docker run -d -p 8080:8080 -e PROFILE=prd ping
```

## Container Registry


#### Docker Hub

* Login

```
docker login -u Guilaooo04
```

* Criar imagem pronta para upload (método 1 - criando nova imagem)


```
docker build -t Guilaooo04/ping .
```


* Criar imagem pronta para upload (método 2 - renomeando imagem existente)


```
docker tag ping Guilaooo04/ping
```


* Upload de imagem para o Docker Hub


```
docker push Guilaooo04/ping 
```



#### Navegação

- Base

http://localhost:8080

- Endpoint que retorna string "Pong"

http://localhost:8080/ping


## Features (Funcionalidades)

- Múltiplos profiles

## Contatos

- Desenvolvedor 1 - guigatome05@outlook.com

