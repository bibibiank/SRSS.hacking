
## Objetivo 
There are 2 files in the homedirectory: **passwords.old and passwords.new**. The password for the next level is in **passwords.new** and is the only line that has been changed between **passwords.old and passwords.new**

**NOTE: if you have solved this level and see ‘Byebye!’ when trying to log into bandit18, this is related to the next level, bandit19**

## Commands you may need to solve this level

cat, grep, ls, diff
## Datos de acceso al nivel 
usewr: bandit17
pass: EReVavePLFHtFlFsjn3hyzMlvSuSAcRD

## Solución  
`bandit17@bandit:~$ cat /etc/bandit_pass/bandit17`

`EReVavePLFHtFlFsjn3hyzMlvSuSAcRD`

`bandit17@bandit:~$ ls`

`passwords.new  passwords.old`

`bandit17@bandit:~$ wc -l passwords.`

`passwords.new  passwords.old`

`bandit17@bandit:~$ wc -l passwords.`

`passwords.new  passwords.old`

`bandit17@bandit:~$ wc -l passwords.`

`passwords.new  passwords.old`

`bandit17@bandit:~$ diff passwords.old passwords.new`

`42c42`

`< bSrACvJvvBSxEM2SGsV5sn09vc3xgqyp`

`---`

> `x2gLTTjFwMOhQ8oWNbMN362QKxfRqGlO`

`bandit17@bandit:~$`

`Pass BANDIT 17 : EReVavePLFHtFlFsjn3hyzMlvSuSAcRD`


## Notas Adicionales 

### Referencias
