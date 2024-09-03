
## Objetivo 
## Datos de acceso al nivel 

user: bandit20
Pass: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO
## Solución  
`bandit20@bandit:~$ ls`

`suconnect`

`bandit20@bandit:~$ ls -la`

`total 36`

`drwxr-xr-x  2 root     root      4096 Jul 17 15:57 .`

`drwxr-xr-x 70 root     root      4096 Jul 17 15:58 ..`

`-rw-r--r--  1 root     root       220 Mar 31 08:41 .bash_logout`

`-rw-r--r--  1 root     root      3771 Mar 31 08:41 .bashrc`

`-rw-r--r--  1 root     root       807 Mar 31 08:41 .profile`

`-rwsr-x---  1 bandit21 bandit20 15604 Jul 17 15:57 suconnect`

`bandit20@bandit:~$ ./suconnect 3030`

`Could not connect`

`bandit20@bandit:~$ nc -lnvp 5050`

`Listening on 0.0.0.0 5050`

`^C`

`bandit20@bandit:~$ nc localhost 5050`

`bandit20@bandit:~$ nc localhost 5050`

`hola quien eres`

`^C`

`bandit20@bandit:~$ nc -lnvp 1618 <<<0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO &`

`[1] 3139816`

`bandit20@bandit:~$ Listening on 0.0.0.0 1618`

`^C`

`bandit20@bandit:~$ ls -la`

`total 36`

`drwxr-xr-x  2 root     root      4096 Jul 17 15:57 .`

`drwxr-xr-x 70 root     root      4096 Jul 17 15:58 ..`

`-rw-r--r--  1 root     root       220 Mar 31 08:41 .bash_logout`

`-rw-r--r--  1 root     root      3771 Mar 31 08:41 .bashrc`

`-rw-r--r--  1 root     root       807 Mar 31 08:41 .profile`

`-rwsr-x---  1 bandit21 bandit20 15604 Jul 17 15:57 suconnect`

`bandit20@bandit:~$ ./suconnect`

`Usage: ./suconnect <portnumber>`

`This program will connect to the given port on localhost using TCP. If it receives the correct password from the other side, the next password is transmitted back.`

`bandit20@bandit:~$ ./suconnect  1618`

`Connection received on 127.0.0.1 40244`

`Read: 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO`

`Password matches, sending next password`

`EeoULMCra2q0dSkYj561DX7s1CpBuOBt`

`[1]+  Done                    nc -lnvp 1618 <<< 0qXahG8ZjOVMN9Ghs7iOWsCfZyXOUbYO`

`bandit20@bandit:~$`
## Notas Adicionales 

& si agregamos este simbolo al final de un comando lo estamos enviando al segundo plano (background)

Jobs me muestra que comanndos estan en el segundo plano

### Referencias
