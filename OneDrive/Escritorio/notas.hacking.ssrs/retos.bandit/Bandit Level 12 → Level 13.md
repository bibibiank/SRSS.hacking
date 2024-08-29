## Objetivo 

The password for the next level is stored in the file **data.txt**, which is a hexdump of a file that has been repeatedly compressed. For this level it may be useful to create a directory under /tmp in which you can work. Use mkdir with a hard to guess directory name. Or better, use the command “mktemp -d”. Then copy the datafile using cp, and rename it using mv (read the manpages!)

## *Commands you may need to solve this level*

grep, sort, uniq, strings, base64, tr, tar, gzip, bzip2, xxd, mkdir, cp, mv, file


## Datos de acceso al nivel 
user: bandit12
pass: 7x16WNeHIi5YkIhWsfFIqoognUTyj9Q4
## Solución  

`bandit12@bandit:~$ ls`
`data.txt`
`bandit12@bandit:~$ xxd -r data.txt | file -`
`/dev/stdin: gzip compressed data, was "data2.bin", last modified: Wed Jul 17 15:57:06 2024, max compression, from Unix`
`bandit12@bandit:~$ xxd -r data.txt | zcat | file -`
`/dev/stdin: bzip2 compressed data, block size = 900k`
`bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | file -`
`/dev/stdin: gzip compressed data, was "data4.bin", last modified: Wed Jul 17 15:57:06 2024, max compression, from Unix`
`bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | file -`
`/dev/stdin: POSIX tar archive (GNU)
`bandit12@bandit:~$ xxd -r data.txt | zcat | bzcat | zcat | tar xO | tar xO | bzcat | tar xO | zcat`
`The password is FO5dwFsc0cbaIiH0h8J2eUks2vdTDwAn
`bandit12@bandit:~$`

`



## Notas Adicionales 
 xxd .profile- 
 
### Referencias

