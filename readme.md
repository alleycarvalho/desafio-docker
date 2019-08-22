# Desafio Docker 1

Aplicação Laravel dentro de uma imagem com Docker.

## Imagem do Projeto

https://hub.docker.com/r/alleycarvalho/desafio-docker

## Utilização

Clonar o repositório:

```
git clone git@github.com:alleycarvalho/desafio-docker.git
```

Acessar o diretório do projeto:

```
cd desafio-docker/
```

Executar o docker-compose:

```
docker-compose up -d
```

Verificar log da aplicação:

```
docker logs app -f
```

Pressionar `CTRL+C` para sair do log.

Acessar a url `http://localhost:8000` para visualizar a aplicação.

# Desafio Docker 2

Imagem Docker menor que 2MB - Golang

## Imagem do Projeto

https://hub.docker.com/r/alleycarvalho/codeeducation

## Utilização

Executar a imagem com docker:

```
docker run alleycarvalho/codeeducation
```

* Se você visualizar a mensagem `Code.education Rocks!`, significa que a aplicação executou com sucesso.
