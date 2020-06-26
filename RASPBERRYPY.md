/etc/network/interfaces:

```sh
allow-hotplug eth0
iface eth0 inet dhcp
        #address 192.168.15.254
        #netmask 255.255.255.0
        #gateway 192.168.15.1
        wpa-driver wired
        wpa-conf /etc/wpa_supplicant/wpa_supplicant.conf
```


/etc/wpa_supplicant/wpa_supplicant.conf:

```sh
network={
        key_mgmt=IEEE8021X
        eap=PEAP
        phase2="auth=MSCHAPV2"
        identity="server"
        password="pass"
}
```

Queimar imagens Raspbian:

```sh
# dd bs=4M if=2019-09-26-raspbian-buster.img of=/dev/sdX conv=fsync
```
