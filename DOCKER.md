Para todas as instâncias
```sh
docker stop $(docker ps -a -q)
```

Remove todas as instâncias
```sh
docker rm $(docker ps -a -q)
```

Apaga todas as imagens
```sh
docker image rm $(docker image ls -a -q)
```

Apaga todos os volumes
```sh
docker volume prune
```
