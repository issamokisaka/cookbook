Para executar jobs YARN/MAPREDUCE, adicione o users (que executara os jobs) em todos os nos do cluster Hadoop:

Adicionar user ao grupo big
# usermod -a -G yarn big

Remover user de um grupo
# gpasswd -d <user> <group>
