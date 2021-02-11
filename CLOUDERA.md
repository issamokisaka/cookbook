``
CLOUDERA
``

Copia, edição e remoção de arquivo em HDFS, sem o user HDFS criado nos nodes do cluster HADOOP:

```sh
# sudo -u hdfs hdfs dfs -ls /tmp
```

Atualizar lista de grupos e suas permissoes no HDFS:

```sh
$ hdfs dfsadmin -refreshUserToGroupsMappings
```
