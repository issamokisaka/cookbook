Add sequencial na frente das linhas:

```sh
sed = file.csv | sed 'N;s/\n/;/' > new_file.csv
```


Script para retirar acentos:

```sh
sed 'y/áÁàÀãÃâÂéÉêÊíÍóÓõÕôÔúÚçÇ/aAaAaAaAeEeEiIoOoOoOuUcC/' < input.txt > output.txt
sed 'y/áÁàÀãÃâÂéÉêÊíÍóÓõÕôÔúÚçÇ/aAaAaAaAeEeEiIoOoOoOuUcC/' -i file.txt
```


Substituindo a 5a ocorrencia do caracter "/" por expressao qualquer, como 'A='

```sh
/fdsafdas/fdsa/fdsa/fdsa/teste

sed 's/\// A=/5' teste.txt

/fdsafdas/fdsa/fdsa/fdsa A=teste
```


DELETAR TAGS HTML
```sh
sed 's/<[^>]*>//g' saida1.txt
```

REMOVER Linhas em branco:
```sh
sed '/^$/d' saida.txt
```

CTRL+V CTRL+M aparece o caracter ^M:
```sh
sed 's/^M//g' file_input.txt                                                                                            
```


REMOVER LINHAS QUE COMEÇAM COM DETERMINADA STRING "+---":
```sh
sed -i 's/^+---.*$//'  arquivo.csv
```

Remover linhas em branco:
```sh
sed -i '/^$/d'  arquivo.csv
```

Retirar pipe do inicio da linha:
```sh
sed -i 's/^|//'  arquivo.csv
```

Retirar pipe  do final da linha:
```sh
sed -i 's/|$//'  arquivo.csv   
```

OBS:> Em sed, pesquisa não pode conter "&", "/" , "'", "!" , """ e ","
