Para executar jobs YARN/MAPREDUCE, adicione o users (que executara os jobs) em todos os nos do cluster Hadoop:

Adicionar user ao grupo big
```sh
# usermod -a -G yarn big
```

Remover user de um grupo
```sh
# gpasswd -d <user> <group>
```
