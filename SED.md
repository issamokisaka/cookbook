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
