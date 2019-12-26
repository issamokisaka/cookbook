Inicialiar o cluster Swarm, apontando o IP de rede a ser usado:


$ docker swarm init --advertise-addr 192.168.0.103


Escalando serviços através de dois containers:

$ docker service scale nome_servico=2
