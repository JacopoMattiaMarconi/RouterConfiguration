# Configurazione Router Cisco :computer:

[HOSTNAME](#HOSTNAME)<br>
[PROTEZIONE USER EXEC](#PROTEZIONE-USER-EXEC)<br>
[PROTEZIONE PRIVILEGED EXEC](#PROTEZIONE-PRIVILEGED-EXEC)<br>
[PROTEZIONE ACCESSO TELNET SSH](#PROTEZIONE-ACCESSO-TELNET-SSH)<br>
[PROTEZIONE PASSWORD](#PROTEZIONE-PASSWORD)<br>
[AVVISO LEGALE](#AVVISO-LEGALE)<br>
[CONFIGURAZIONE INTERFACCIA](#CONFIGURAZIONE-INTERFACCIA)<br>
[SALVARE CONFIGURAZIONE](#SALVARE-CONFIGURAZIONE)<br>
[CONFIGURAZIONE INTERFACCE](#CONFIGURAZIONE-INTERFACCE)<br>
[VERIFICA CONFIGURAZIONE INTERFACCE](#VERIFICA-CONFIGURAZIONE-INTERFACCE)<br>

## HOSTNAME<br>
>Router(config)# hostname R1


## PROTEZIONE USER EXEC<br>
>R1(config)# line console 0
>
>R1(config-line)# password "password"
>
>R1(config-line)# login
>
>R1(config-line)# exit

## PROTEZIONE PRIVILEGED EXEC<br>
>R1(config)# enable secret "password"


## PROTEZIONE ACCESSO TELNET SSH<br>
>R1(config-line)# line vty 0 15
>
>R1(config-line)# password "password"
>
>R1(config-line)# login
>
>R1(config-line)# exit


## PROTEZIONE PASSWORD<br>
>R1(config)# service password-encryption


## AVVISO LEGALE<br>
>R1(config)# banner motd #No access allowed#


## CONFIGURAZIONE INTERFACCIA<br>
>R1(config)# interface vlan1
>
>R1(config)# ip address "ip-subnetmask"
>
>R1(config)# ip default-gateway "ip"
>
>R1(config)# no shutdown


## SALVARE CONFIGURAZIONE<br>
>R1(config)# copy running-config startup-config


## CONFIGURAZIONE INTERFACCE<br>
>R1(config)# interface gigabitethernet 0/0
>
>R1(config-if)# ip address "ip" "subnetmask"
>
>R1(config-if)# description Link to LAN-10
>
>R1(config-if)# no shutdown


## VERIFICA CONFIGURAZIONE INTERFACCE<br>
>R1# show ip interface brief
>
>R1# ping "ip"
>
>R1# show ip route

