Depois de instalar o MongoDB (pacotes .deb Debian Jessie e Stretch), habilitar
o servico com gerenciador systemctl:

# systemctl enable mongod.service


Para em seguida "subir" o servico:

# systemctl start mongod.service


Insert json in MongoDB:

mongoimport --jsonArray -d DATABASE -c COLECAO --file arquivo.json
