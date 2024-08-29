## Objetivo 
The password for the next level is stored in the only human-readable file in the **inhere** directory. Tip: if your terminal is messed up, try the “reset” command.
## Datos de acceso al nivel 
user: bandit4
password: 2WmrDFRmJIq3IPxneAaMGhap0pFhF3NJ

## Solución  

C:\Users\hoydw>ssh bandit4@bandit.labs.overthewire.org -p 2220
                         _                     _ _ _
                        | |__   __ _ _ __   __| (_) |_
                        | '_ \ / _` | '_ \ / _` | | __|
                        | |_) | (_| | | | | (_| | | |_
                        |_.__/ \__,_|_| |_|\__,_|_|\__|


                      This is an OverTheWire game server.
            More information on http://www.overthewire.org/wargames

bandit4@bandit.labs.overthewire.org's password:

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

bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere
bandit4@bandit:~/inhere$ ls
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
bandit4@bandit:~/inhere$ cd -file00
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ cd -file01
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ cd -file02
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ cd -file03
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ cd -file04
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ cd -file05
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ cd -file06
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ cd -file07
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ cd -file08
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ cd -file09
-bash: cd: -f: invalid option
cd: usage: cd [-L|[-P [-e]] [-@]] [dir]
bandit4@bandit:~/inhere$ ls
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
bandit4@bandit:~/inhere$ ~/inhere$ cat ./-file00
-bash: /home/bandit4/inhere$: No such file or directory
bandit4@bandit:~/inhere$ cat ./-file00
��,��␦����Yq��f�L���j␦�0����x�4Fbandit4@bandit:~/inhere$ cat ./-file01
N�.��bandit4@bandit:~/inhere$ cat ./-file02
��9������F��p������tk���%��bandit4@bandit:~/inhere$ cat ./-file03
�����n�Qy�y͍�{+R�bZ�k�F�*       bandit4@bandit:~/inhere$ cat ./-file04

l�����]�a߯-@gQ�÷�wz�P�ߠy�bandit4@bandit:~/inhere$ cat ./-file05
�pӻT9�F��3ˤ����)
T�՜F�ǭ�bandit4@bandit:~/inhere$ cat ./-file06
�QĹ�M���p4�-�8��=��!#g���bandit4@bandit:~/inhere$ cat ./-file07
4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
## Notas Adicionales 
cat ./*  es un comodin para usar un comando con todos los archivos del directorio

file me dice el tipo de archivo


password to the next level: 4oQYVPkxZOOEOO5pTW81FB8j8lxXGUQw
### Referencias