## Objetivo 

The password for the next level can be retrieved by submitting the password of the current level to **port 30000 on localhost**.

## Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap
## Datos de acceso al nivel 

bandit14

MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
## Solución  
bandit14@bandit:~$ ls
bandit14@bandit:~$ which nc
/usr/bin/nc
bandit14@bandit:~$ nc localhost 3030
hola
quien eres
ola
exit
bandit14@bandit:~$ nc localhost 6666
hola desde el infierno
exit
bandit14@bandit:~$ nc localhost 30000
exit
Wrong! Please enter the correct current password.
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
bandit14@bandit:~$ nc localhost 300000
nc: port number too large: 300000
bandit14@bandit:~$ nc localhost 30000
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
Correct!
8xCjnmgoKbGLhHFAZlGE5Tmu4M2tKJQo


## Notas Adicionales 
netcat (nc) es una herrramienta que permite conectarse a un host remoto, tambien podemos abrir un puerto 

localhost 30000
localhost - es el host o la maquina 


### Referencias

