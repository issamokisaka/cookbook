Para todas as instâncias
```sh
docker stop $(docker ps -a -q)
```

Remove todas as instâncias
```sh
docker rm $(docker ps -a -q)
```

Para todas as imagens
```sh
docker image rm $(docker image ls -a -q)
```

Para todos os volumes
```sh
docker volume prune
```
