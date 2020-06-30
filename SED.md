Add sequencial na frente das linhas:

```sh
sed = file.csv | sed 'N;s/\n/;/' > new_file.csv
```
