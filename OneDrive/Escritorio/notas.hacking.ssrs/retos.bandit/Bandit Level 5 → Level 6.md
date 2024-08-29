## Objetivo 
The password for the next level is stored in a file somewhere under the **inhere** directory and has all of the following properties:

- human-readable
- 1033 bytes in size
- not executable
## Datos de acceso al nivel 

user: bandit5
pass:4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw

## Solución  
C:\Users\hoydw>ssh bandit5@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit5@bandit.labs.overthewire.org's password:

      ,----..            ,----,          .---.
     /   /   \         ,/   .`|         /. ./|
    /   .     :      ,`   .'  :     .--'.  ' ;
   .   /   ;.  \   ;    ;     /    /__./ \ : |
  .   ;   /  ` ; .'___,/    ,' .--'.  '   \' .
  ;   |  ; \ ; | |    :     | /___/ \ |    ' '
  |   :  | ; | ' ;    |.';  ; ;   \  \;      :
  .   |  ' ' ' : `----'  |  |  \   ;  `      |
  '   ;  \; /  |     '   :  ;   .   \    .\  ;
   \   \  ',  /      |   |  '    \   \   ' \ |
    ;   :    /       '   :  |     :   '  |--"
     \   \ .'        ;   |.'       \   \ ;
  www. `---` ver     '---' he       '---" ire.org


Welcome to OverTheWire!

If you find any problems, please report them to the #wargames channel on
discord or IRC.

--[ Playing the games ]--

  This machine might hold several wargames.
  If you are playing "somegame", then:

    * USERNAMES are somegame0, somegame1, ...
    * Most LEVELS are stored in /somegame/.
    * PASSWORDS for each level are stored in /etc/somegame_pass/.

  Write-access to homedirectories is disabled. It is advised to create a
  working directory with a hard-to-guess name in /tmp/.  You can use the
  command "mktemp -d" in order to generate a random and hard to guess
  directory in /tmp/.  Read-access to both /tmp/ is disabled and to /proc
  restricted so that users cannot snoop on eachother. Files and directories
  with easily guessable or short names will be periodically deleted! The /tmp
  directory is regularly wiped.
  Please play nice:

    * don't leave orphan processes running
    * don't leave exploit-files laying around
    * don't annoy other players
    * don't post passwords or spoilers
    * again, DONT POST SPOILERS!
      This includes writeups of your solution on your blog or website!

--[ Tips ]--

  This machine has a 64bit processor and many security-features enabled
  by default, although ASLR has been switched off.  The following
  compiler flags might be interesting:

    -m32                    compile for 32bit
    -fno-stack-protector    disable ProPolice
    -Wl,-z,norelro          disable relro

  In addition, the execstack tool can be used to flag the stack as
  executable on ELF binaries.

  Finally, network-access is limited for most levels by a local
  firewall.

--[ Tools ]--

 For your convenience we have installed a few useful tools which you can find
 in the following locations:

    * gef (https://github.com/hugsy/gef) in /opt/gef/
    * pwndbg (https://github.com/pwndbg/pwndbg) in /opt/pwndbg/
    * peda (https://github.com/longld/peda.git) in /opt/peda/
    * gdbinit (https://github.com/gdbinit/Gdbinit) in /opt/gdbinit/
    * pwntools (https://github.com/Gallopsled/pwntools)
    * radare2 (http://www.radare.org/)

--[ More information ]--

  For more information regarding individual wargames, visit
  http://www.overthewire.org/wargames/

  For support, questions or comments, contact us on discord or IRC.

  Enjoy your stay!

bandit5@bandit:~$ ls -l
total 4
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 inhere
bandit5@bandit:~$ ls -la
total 24
drwxr-xr-x  3 root root    4096 Jul 17 15:57 .
drwxr-xr-x 70 root root    4096 Jul 17 15:58 ..
-rw-r--r--  1 root root     220 Mar 31 08:41 .bash_logout
-rw-r--r--  1 root root    3771 Mar 31 08:41 .bashrc
drwxr-x--- 22 root bandit5 4096 Jul 17 15:57 inhere
-rw-r--r--  1 root root     807 Mar 31 08:41 .profile
bandit5@bandit:~$ cd inhere
bandit5@bandit:~/inhere$ ls
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
bandit5@bandit:~/inhere$ ls -R
.:
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
maybehere03  maybehere07  maybehere11  maybehere15  maybehere19

./maybehere00:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere01:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere02:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere03:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere04:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere05:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere06:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere07:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere08:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere09:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere10:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere11:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere12:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere13:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere14:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere15:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere16:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere17:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere18:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3

./maybehere19:
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3
bandit5@bandit:~/inhere$ ./maybehere00
-bash: ./maybehere00: Is a directory
bandit5@bandit:~/inhere$ ./maybehere01
-bash: ./maybehere01: Is a directory
bandit5@bandit:~/inhere$ cd maybehere01
bandit5@bandit:~/inhere/maybehere01$ ls
-file1  -file2  -file3  spaces file1  spaces file2  spaces file3
bandit5@bandit:~/inhere/maybehere01$ cd maybehere02
-bash: cd: maybehere02: No such file or directory
bandit5@bandit:~/inhere/maybehere01$ cd ..
bandit5@bandit:~/inhere$ find . /type f /size 1033
.
./maybehere07
./maybehere07/-file3
./maybehere07/spaces file2
./maybehere07/-file2
./maybehere07/spaces file1
./maybehere07/-file1
./maybehere07/.file3
./maybehere07/.file2
./maybehere07/.file1
./maybehere07/spaces file3
./maybehere05
./maybehere05/-file3
./maybehere05/spaces file2
./maybehere05/-file2
./maybehere05/spaces file1
./maybehere05/-file1
./maybehere05/.file3
./maybehere05/.file2
./maybehere05/.file1
./maybehere05/spaces file3
./maybehere04
./maybehere04/-file3
./maybehere04/spaces file2
./maybehere04/-file2
./maybehere04/spaces file1
./maybehere04/-file1
./maybehere04/.file3
./maybehere04/.file2
./maybehere04/.file1
./maybehere04/spaces file3
./maybehere08
./maybehere08/-file3
./maybehere08/spaces file2
./maybehere08/-file2
./maybehere08/spaces file1
./maybehere08/-file1
./maybehere08/.file3
./maybehere08/.file2
./maybehere08/.file1
./maybehere08/spaces file3
./maybehere19
./maybehere19/-file3
./maybehere19/spaces file2
./maybehere19/-file2
./maybehere19/spaces file1
./maybehere19/-file1
./maybehere19/.file3
./maybehere19/.file2
./maybehere19/.file1
./maybehere19/spaces file3
./maybehere10
./maybehere10/-file3
./maybehere10/spaces file2
./maybehere10/-file2
./maybehere10/spaces file1
./maybehere10/-file1
./maybehere10/.file3
./maybehere10/.file2
./maybehere10/.file1
./maybehere10/spaces file3
./maybehere15
./maybehere15/-file3
./maybehere15/spaces file2
./maybehere15/-file2
./maybehere15/spaces file1
./maybehere15/-file1
./maybehere15/.file3
./maybehere15/.file2
./maybehere15/.file1
./maybehere15/spaces file3
./maybehere17
./maybehere17/-file3
./maybehere17/spaces file2
./maybehere17/-file2
./maybehere17/spaces file1
./maybehere17/-file1
./maybehere17/.file3
./maybehere17/.file2
./maybehere17/.file1
./maybehere17/spaces file3
./maybehere09
./maybehere09/-file3
./maybehere09/spaces file2
./maybehere09/-file2
./maybehere09/spaces file1
./maybehere09/-file1
./maybehere09/.file3
./maybehere09/.file2
./maybehere09/.file1
./maybehere09/spaces file3
./maybehere11
./maybehere11/-file3
./maybehere11/spaces file2
./maybehere11/-file2
./maybehere11/spaces file1
./maybehere11/-file1
./maybehere11/.file3
./maybehere11/.file2
./maybehere11/.file1
./maybehere11/spaces file3
./maybehere13
./maybehere13/-file3
./maybehere13/spaces file2
./maybehere13/-file2
./maybehere13/spaces file1
./maybehere13/-file1
./maybehere13/.file3
./maybehere13/.file2
./maybehere13/.file1
./maybehere13/spaces file3
./maybehere01
./maybehere01/-file3
./maybehere01/spaces file2
./maybehere01/-file2
./maybehere01/spaces file1
./maybehere01/-file1
./maybehere01/.file3
./maybehere01/.file2
./maybehere01/.file1
./maybehere01/spaces file3
./maybehere02
./maybehere02/-file3
./maybehere02/spaces file2
./maybehere02/-file2
./maybehere02/spaces file1
./maybehere02/-file1
./maybehere02/.file3
./maybehere02/.file2
./maybehere02/.file1
./maybehere02/spaces file3
./maybehere00
./maybehere00/-file3
./maybehere00/spaces file2
./maybehere00/-file2
./maybehere00/spaces file1
./maybehere00/-file1
./maybehere00/.file3
./maybehere00/.file2
./maybehere00/.file1
./maybehere00/spaces file3
./maybehere03
./maybehere03/-file3
./maybehere03/spaces file2
./maybehere03/-file2
./maybehere03/spaces file1
./maybehere03/-file1
./maybehere03/.file3
./maybehere03/.file2
./maybehere03/.file1
./maybehere03/spaces file3
./maybehere18
./maybehere18/-file3
./maybehere18/spaces file2
./maybehere18/-file2
./maybehere18/spaces file1
./maybehere18/-file1
./maybehere18/.file3
./maybehere18/.file2
./maybehere18/.file1
./maybehere18/spaces file3
./maybehere14
./maybehere14/-file3
./maybehere14/spaces file2
./maybehere14/-file2
./maybehere14/spaces file1
./maybehere14/-file1
./maybehere14/.file3
./maybehere14/.file2
./maybehere14/.file1
./maybehere14/spaces file3
./maybehere16
./maybehere16/-file3
./maybehere16/spaces file2
./maybehere16/-file2
./maybehere16/spaces file1
./maybehere16/-file1
./maybehere16/.file3
./maybehere16/.file2
./maybehere16/.file1
./maybehere16/spaces file3
./maybehere06
./maybehere06/-file3
./maybehere06/spaces file2
./maybehere06/-file2
./maybehere06/spaces file1
./maybehere06/-file1
./maybehere06/.file3
./maybehere06/.file2
./maybehere06/.file1
./maybehere06/spaces file3
./maybehere12
./maybehere12/-file3
./maybehere12/spaces file2
./maybehere12/-file2
./maybehere12/spaces file1
./maybehere12/-file1
./maybehere12/.file3
./maybehere12/.file2
./maybehere12/.file1
./maybehere12/spaces file3
find: ‘/type’: No such file or directory
find: ‘f’: No such file or directory
find: ‘/size’: No such file or directory
find: ‘1033’: No such file or directory
bandit5@bandit:~/inhere$ ./maybehere07/.file2
-bash: ./maybehere07/.file2: Permission denied
bandit5@bandit:~/inhere$ ./maybehere07
-bash: ./maybehere07: Is a directory
bandit5@bandit:~/inhere$ cat ./maybehere07
cat: ./maybehere07: Is a directory
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
HWasnPhtq9AVKe0dmk45nxy20cvUa6EG



## Notas Adicionales 

ls -R  - lista archivos de forma recursiva, es decir, las carpetas con subcarpetas

find . -type f -size 1033c
. significa que busca aqui hacia abajo

  -type especifica que busque un archivo del tipo regular

  size 1044c especifica el tamaño de archivo de 1033c




### Referencias