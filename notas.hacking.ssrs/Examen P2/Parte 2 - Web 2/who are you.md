## Objetivo 

Let me in. Let me iiiiiiinnnnnnnnnnnnnnnnnnnn [http://mercury.picoctf.net:34588/](http://mercury.picoctf.net:34588/)

## Solución  

usamos Burp Suite para enviar la página a Repeater. Como no se puede acceder sin PicoBrowser, modificamos el Request cambiando el User-Agent a PicoBrowser para poder ingresar al sitio.
```java 
User-Agent: PicoBrowser

```
nos muestra un mensaje de que no confía en los que la visitan desde otro sitio por lo que agregamos un punto **referer** para que la pagina vea que no hemos entrado desde otro sitio

```java 
Referer: mercury.picoctf.net:34588
```
nos muestra un mensaje de que este sitio solo funciona en 2018, añadimos un encabezado de fecha

```java
Date: Wed, 21 Oct 2018 07:28:00 GMT
```

nos muestra un mensaje de que no confía en los usuarios que pueden ser rastreados por lo que le añadimos el encabezado de solicitud DNT

```java
DNT: 1
```
nos dice que la pagina es para personas de Suecia, así que trabajamos con otro encabezado

```java
X-Forwarded-For: 102.177.146.1
```

dice que no hablamos sueco, cambiamos el encabezado de idioma a sueco

```java 
Accept-Language: sv-sv,sv;q=0.5
```

nos dio la bandera
```java
picoCTF{http_h34d3rs_v3ry_c0Ol_much_w0w_79e451a7}
```
## Notas Adicionales 

### Referencias
