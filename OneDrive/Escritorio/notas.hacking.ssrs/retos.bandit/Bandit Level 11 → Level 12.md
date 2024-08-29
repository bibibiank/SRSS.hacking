## Objetivo 
The password for the next level is stored in the file **data.txt**, where all lowercase (a-z) and uppercase (A-Z) letters have been rotated by 13 positions

## Commands you may need to solve this level

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd
## Datos de acceso al nivel 
user: bandit11
pass: dtR173fZKb0RRsDFSGsg2RWnpNVj3qRr

## Solución  

==FORMA 1== 
`bandit11@bandit:~$ la -la`
`total 24`
`drwxr-xr-x  2 root     root     4096 Jul 17 15:57 .`
`drwxr-xr-x 70 root     root     4096 Jul 17 15:58 ..`
`-rw-r--r--  1 root     root      220 Mar 31 08:41 .bash_logout`
`-rw-r--r--  1 root     root     3771 Mar 31 08:41 .bashrc`
`-rw-r-----  1 bandit12 bandit11   49 Jul 17 15:57 data.txt`
`-rw-r--r--  1 root     root      807 Mar 31 08:41 .profile`
`bandit11@bandit:~$ cat data.txt`
`Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4`
`bandit11@bandit:~$ cat data.txt | tr [a-Za-Z] [n-za-mN-ZA-M]`
`tr: range-endpoints of 'a-Z' are in reverse collating sequence order`
`bandit11@bandit:~$ cat data.txt | tr [a-zA-Z] [n-za-mN-ZA-M]`
`The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4`
`bandit11@bandit:~$`


==FORMA 2== 
`bandit11@bandit:~$ python3`
`Python 3.12.3 (main, Apr 10 2024, 05:33:47) [GCC 13.2.0] on linux`
`Type "help", "copyright", "credits" or "license" for more information.`
>>> `import codecs`
>>> `codecs.decode("Gur cnffjbeq vf 7k16JArUVv5LxVuJfsSVdbbtaHGlw9D4",`
 `"ROT13")`
`'The password is 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4'`
>>>
## Notas Adicionales 
ROT13 -  rota los caracteres 13 posiciones en el alfabeto 


### Referencias

Helpful Reading Material
- [Rot13 on Wikipedia](https://en.wikipedia.org/wiki/ROT13)