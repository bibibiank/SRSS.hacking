## Objetivo 

Unzip this archive and find the file named 'uber-secret.txt'

## Solución  

```bash
┌──(kali㉿kali)-[~]
└─$ cd Downloads      
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ ls    
 big-zip-files.zip  'challenge(1).zip'  'challenge(2).zip'  'challenge(3).zip'   challenge.zip   files   files.zip
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ find files 
files
files/satisfactory_books
files/satisfactory_books/16021.txt.utf-8
files/satisfactory_books/more_books
files/satisfactory_books/more_books/37121.txt.utf-8
files/satisfactory_books/23765.txt.utf-8
files/adequate_books
files/adequate_books/more_books
files/adequate_books/more_books/1023.txt.utf-8
files/adequate_books/more_books/.secret
files/adequate_books/more_books/.secret/deeper_secrets
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
files/adequate_books/46804-0.txt
files/adequate_books/44578.txt.utf-8
files/14789.txt.utf-8
files/acceptable_books
files/acceptable_books/more_books
files/acceptable_books/more_books/40723.txt.utf-8
files/acceptable_books/17880.txt.utf-8
files/acceptable_books/17879.txt.utf-8
files/13771.txt.utf-8
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ find files |grep uber-secret.txt
files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ cat files/adequate_books/more_books/.secret/deeper_secrets/deepest_secrets/uber-secret.txt
picoCTF{f1nd_15_f457_ab443fd1}

```

## Notas Adicionales 



### Referencias
