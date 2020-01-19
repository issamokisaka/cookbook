Para ediçoes de config do Grub, retire "rhgb noquiet" para Debug total inicialização no arquivo:

Grub centos 6:

/boot/grub/grub.conf


Grub Centos 7:

/etc/default/grub

E ao final regere o Grub2 com:

grub2-mkconfig -o /boot/grub2/grub.cfg




How to install kernel headers in 7. To install Linux addionals for VBox:

# yum install kernel-devel

but install: packages gcc make perl


Config rede centos 7

Edite o arquivo:

/etc/sysconfig/network-scripts/ifcfg-enp0s3

Adicionando as linhas abaixo
               IPADDR=192.168.1.70
               NETMASK=255.255.255.0
               GATEWAY=192.168.1.1
               DNS1=192.168.1.1
               DNS2=8.8.8.8
               DOMAIN=rheltest.lan

