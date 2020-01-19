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


