# DOCKER

## CONFIGS

Driver php/mysql para BBIntegra:
- php5-mysqlnd

+ Execute a imagem run na imagem, pra executar o container.
+ faca alterações nos arquivos e instale programas necessarios.

Parar o container:

```sh
# docker stop containercriado
```

Faça o commit das alterações em uma imagem (mas o container nao pode ser parado):

```sh
# docker commit -a "Your Name <youremail@email.com>" -m "nome of image" CONTAINER_ID nome_criador/nome_imagem:versao

# docker commit CONTAINER_ID NOME_CRIADOR/NOME_IMAGEM:VERSAO
```


Colocar TAG em uma imagem:
```sh
# docker tag NOME_IMAGEM:VERSAO NOME_IMAGEM:latest
```

Remove do sistema qualquer imagem de conteiner docker usado ou nao
```sh
# docker system prune -a
```

Exportar imagem para arquivo:
```sh
# docker save NOME_CRIADOR/NOME_PROJETO:VERSAO > IMAGEM.tar
```

Acessando um container:
```sh
# docker exec -it CONTAINER_ID /bin/bash
```

Executar container:

```sh
$ docker run -d -it --name devtest --mount type=bind,source="$(pwd)"/target,target=/app \
  nginx:latest
```

Gerando imagens com Dockerfile (esteja no dir. do projeto Docker):
```sh
# docker build -t minhaimagem:VERSAO .
```

Carregar imagens Docker:
```sh
# docker load -i imagem
```
