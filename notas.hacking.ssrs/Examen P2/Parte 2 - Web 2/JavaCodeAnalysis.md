## Objetivo 
BookShelf Pico, my premium online book-reading service. I believe that my website is super secure. I challenge you to prove me wrong by reading the 'Flag' book!

Additional details will be available after launching your challenge instance.

- Username: "user"
- Password: "user"

Source code can be downloaded [here](https://artifacts.picoctf.net/c/478/bookshelf-pico.zip). Website can be accessed [here!](http://saturn.picoctf.net:49406/).
## Solución  

nos metemos a la pagina que nos da el reto, inspeccionamos e ingresamos al local storage, copiamos el auth token y lo pegamos en https://jwt.io/

--nos dio lo sig:

```java 
{
  "typ": "JWT",
  "alg": "HS256"
}

{
  "role": "Free",
  "iss": "bookshelf",
  "exp": 1730614805,
  "iat": 1730010005,
  "userId": 1,
  "email": "user"
}

HMACSHA256(
  base64UrlEncode(header) + "." +
  base64UrlEncode(payload),
  
) secret base64 encoded
```


## Notas Adicionales 


### Referencias
https://jwt.io/