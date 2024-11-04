
## Objetivo 
This vault uses some complicated arrays! I hope you can make sense of it, special agent. The source code for this vault is here: [VaultDoor1.java](https://jupiter.challenges.picoctf.org/static/87e103a8db01087de9ccf5a7a022ddf8/VaultDoor1.java)

## Solución  

```java 

kali㉿kali)-[~/Downloads/vault-door-1]
└─$ cat VaultDoor1.java                                                      
    
                       password.charAt(0)  == 'd' &&
               password.charAt(29) == '3' &&
               password.charAt(4)  == 'r' &&
               password.charAt(2)  == '5' &&
               password.charAt(23) == 'r' &&
               password.charAt(3)  == 'c' &&
               password.charAt(17) == '4' &&
               password.charAt(1)  == '3' &&
               password.charAt(7)  == 'b' &&
               password.charAt(10) == '_' &&
               password.charAt(5)  == '4' &&
               password.charAt(9)  == '3' &&
               password.charAt(11) == 't' &&
               password.charAt(15) == 'c' &&
               password.charAt(8)  == 'l' &&
               password.charAt(12) == 'H' &&
               password.charAt(20) == 'c' &&
               password.charAt(14) == '_' &&
               password.charAt(6)  == 'm' &&
               password.charAt(24) == '5' &&
               password.charAt(18) == 'r' &&
               password.charAt(13) == '3' &&
               password.charAt(19) == '4' &&
               password.charAt(21) == 'T' &&
               password.charAt(16) == 'H' &&
               password.charAt(27) == 'f' &&
               password.charAt(30) == 'b' &&
               password.charAt(25) == '_' &&
               password.charAt(22) == '3' &&
               password.charAt(28) == '6' &&
               password.charAt(26) == 'f' &&
               password.charAt(31) == '0'
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/vault-door-1]
└─$ cat flag | sort | awk '{print($3)}' | tr -d "'" | tr -d "\n" 

d_tH33_cH4r4cT3r55_ff63b0cr4mbl3 


```

se supone que la bandera es  `picoCTF{d_tH33_cH4r4cT3r55_ff63b0cr4mbl3}` pero no me deja avanzar

![[Pasted image 20241104132153.png]]
## Notas Adicionales 

### Referencias
