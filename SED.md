
# Add sequencial na frente das linhas:

sed = file.csv | sed 'N;s/\n/;/' > new_file.csv
