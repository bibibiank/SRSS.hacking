## Objetivo 

The password for the next level is stored in **/etc/bandit_pass/bandit14 and can only be read by user bandit14**. For this level, you don’t get the next password, but you get a private SSH key that can be used to log into the next level. **Note:** **localhost** is a hostname that refers to the machine you are working on

## Commands you may need to solve this level

ssh, telnet, nc, openssl, s_client, nmap
## Datos de acceso al nivel 

user: bandit13
pass: FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
## Solución
```bash 
ssh -i sshkey.private bandit14@localhost -p 2220
The authenticity of host '[localhost]:2220 ([127.0.0.1]:2220)' can't be established.
ED25519 key fingerprint is SHA256:C2ihUBV7ihnV1wUXRb4RrEcLfXC5CXlhmAAM/urerLY

bandit14@bandit:~$ whoami
bandit14
bandit14@bandit:~$ ls -la
total 24
drwxr-xr-x  3 root root 4096 Jul 17 15:57 .
drwxr-xr-x 70 root root 4096 Jul 17 15:58 ..
-rw-r--r--  1 root root  220 Mar 31 08:41 .bash_logout
-rw-r--r--  1 root root 3771 Mar 31 08:41 .bashrc
-rw-r--r--  1 root root  807 Mar 31 08:41 .profile
drwxr-xr-x  2 root root 4096 Jul 17 15:57 .ssh
bandit14@bandit:~$ pwd
/home/bandit14
bandit14@bandit:~$ cat /etc/bandit_pass/bandit14
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
bandit14@bandit:~$
```
MU4VWeTyJk8ROof1qqmcBPaLh7lDCPvS
## Notas Adicionales 
*ssh-private-key*: una llave privada permite al usuario ingresar al servidor ssh sin ingresar el password 

*ssh -i sshkey.private bandit14@localhost -p 2220*
llave para pasarle la llave al ssh, se usa el parámetro 




### Referencias

