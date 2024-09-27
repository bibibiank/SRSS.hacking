## Objetivo 

Find the flag being held on this server to get ahead of the competition [http://mercury.picoctf.net:53554/](http://mercury.picoctf.net:53554/)

## Solución  

```java

┌──(kali㉿kali)-[~]
└─$ curl -X HEAD  http://mercury.picoctf.net:53554/index.php
Warning: Setting custom HTTP method to HEAD with -X/--request may not work the 
Warning: way you want. Consider using -I/--head instead.

^C
                                                                               
┌──(kali㉿kali)-[~]
└─$ curl -I HEAD  http://mercury.picoctf.net:53554/index.php
curl: (6) Could not resolve host: HEAD
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}
Content-type: text/html; charset=UTF-8

                                                                               
┌──(kali㉿kali)-[~]
└─$ curl -I HEAD  http://mercury.picoctf.net:53554/index.php
curl: (6) Could not resolve host: HEAD
HTTP/1.1 200 OK
flag: picoCTF{r3j3ct_th3_du4l1ty_2e5ba39f}
Content-type: text/html; charset=UTF-8

```

picoCTF{r3j3ct_th3_du4l1ty_cca66bd3}

## Notas Adicionales 

***curl -X**. 
se utiliza para especificar el método HTTP que deseas usar al hacer una solicitud. Por defecto, `curl` utiliza el método `GET`, pero con la opción `-X` puedes indicar otros métodos, como `POST`, `PUT`, `DELETE`, etc.


***curl -I**. 
se utiliza para realizar una solicitud HTTP y obtener solo los encabezados de la respuesta. La opción `-I` (o `--head`) le dice a `curl` que solicite únicamente los headers, sin descargar el cuerpo del contenido.

### Referencias

https://keepcoding.io/blog/que-es-burp-suite/


