Depois de instalar o MongoDB (pacotes .deb Debian Jessie e Stretch), habilitar
o servico com gerenciador systemctl:

```sh
# systemctl enable mongod.service
```

Para em seguida "subir" o servico:

```sh
# systemctl start mongod.service
```

Insert json in MongoDB:

```sh
$ mongoimport --jsonArray -d DATABASE -c COLECAO --file arquivo.json
```
