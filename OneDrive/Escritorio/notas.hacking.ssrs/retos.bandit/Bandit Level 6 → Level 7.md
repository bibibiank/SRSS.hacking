## Objetivo 
The password for the next level is stored **somewhere on the server** and has all of the following properties:

- owned by user bandit7
- owned by group bandit6
- 33 bytes in size


*Commands you may need to solve this level* 
[ls](https://manpages.ubuntu.com/manpages/noble/man1/ls.1.html) , [cd](https://manpages.ubuntu.com/manpages/noble/man1/cd.1posix.html) , [cat](https://manpages.ubuntu.com/manpages/noble/man1/cat.1.html) , [file](https://manpages.ubuntu.com/manpages/noble/man1/file.1.html) , [du](https://manpages.ubuntu.com/manpages/noble/man1/du.1.html) , [find](https://manpages.ubuntu.com/manpages/noble/man1/find.1.html) , [grep](https://manpages.ubuntu.com/manpages/noble/man1/grep.1.html)


## Datos de acceso al nivel 

user: bandit6
pass: HWasnPhtq9AVKe0dmk45nxy20cvUa6EG

## Solución  

## Notas Adicionales 
find / -user bandit7 -group bandit6 -size 33c 2>/dev/null

    / indica a find que busque desde el directorio raiz

    -user indica a que usuario pertenece el archivo

    -group indica a que grupo pertence el archivo

    - 2>/dev/null manda la salida de error al dispositivo null, es decir, se oculta al usuario

### Referencias

