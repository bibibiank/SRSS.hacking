## Objetivo 

My dog-sitter's brother made this website but I can't get in; can you help? [login.mars.picoctf.net](https://login.mars.picoctf.net)
## Solución  

entramos al código fuente de la pagina, luego entramos al archivo de js que ejecuta:
```java 
<script src="index.js"></script>
```
El archivo JavaScript verifica tanto el nombre de usuario como la contraseña, codificando esta última en base64 para poder compararla con los criterios de acceso. Con CyberChef, tomamos el valor usado para comparar la contraseña y aplicamos la operación "From Base64" para decodificar el texto de la contraseña, que resulta ser la bandera.

```java
picoCTF{53rv3r_53rv3r_53rv3r_53rv3r_53rv3r}
```
## Notas Adicionales 

### Referencias
