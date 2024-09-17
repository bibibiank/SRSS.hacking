## Objetivo 

Using tabcomplete in the Terminal will add years to your life, esp. when dealing with long rambling directory structures and filenames: [Addadshashanammu.zip](https://mercury.picoctf.net/static/fe16c756149cfa85f23e73cd9dbd6a25/Addadshashanammu.zip)


## Solución  
```bash 
┌──(kali㉿kali)-[~/Downloads]
└─$ unzip Addadshashanammu.zip 
Archive:  Addadshashanammu.zip
   creating: Addadshashanammu/
   creating: Addadshashanammu/Almurbalarammi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/
   creating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/
  inflating: Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku/fang-of-haynekhtnamet  
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ ls          
 Addadshashanammu      'challenge(2).zip'   codebook.txt   enc_flag    fixme2.py             level2.py
 Addadshashanammu.zip  'challenge(3).zip'   code.py        files       level1.flag.txt.enc   runme.py
 big-zip-files.zip     'challenge(4).zip'   convertme.py   files.zip   level1.py
'challenge(1).zip'      challenge.zip       drop-in        fixme1.py   level2.flag.txt.enc
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads]
└─$ cd Addadshashanammu 
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/Addadshashanammu]
└─$ ls
Almurbalarammi
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/Addadshashanammu]
└─$ cat Almurbalarammi 
cat: Almurbalarammi: Is a directory
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/Addadshashanammu]
└─$ cd Almurbalarammi  
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/Addadshashanammu/Almurbalarammi]
└─$ ls
Ashalmimilkala
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/Addadshashanammu/Almurbalarammi]
└─$ cd Ashalmimilkala  
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala]
└─$ ls
Assurnabitashpi
                                                                                                                   
┌──(kali㉿kali)-[~/Downloads/Addadshashanammu/Almurbalarammi/Ashalmimilkala]
└─$ cd Assurnabitashpi 
                                                                                                                   
┌──(kali㉿kali)-[~/…/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi]
└─$ ls
Maelkashishi
                                                                                                                   
┌──(kali㉿kali)-[~/…/Addadshashanammu/Almurbalarammi/Ashalmimilkala/Assurnabitashpi]
└─$ cd Maelkashishi   
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi]
└─$ ls
Onnissiralis
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Almurbalarammi/Ashalmimilkala/Assurnabitashpi/Maelkashishi]
└─$ cd Onnissiralis 
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis]
└─$ ls
Ularradallaku
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Ashalmimilkala/Assurnabitashpi/Maelkashishi/Onnissiralis]
└─$ cd Ularradallaku 
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls
fang-of-haynekhtnamet
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ cat fang-of-haynekhtnamet                                                                 
 HH/lib64/ld-linux-x86-64.so.2GNUGNU_���
'�
  ���Ϲ��n= 
 � � � � � � H�H��bc.so.6puts__cxa_finalize__libc_start_mainGLIBC_2.2.5_ITM_deregisterTMCloneTable__gmon_start___ITM_registerTMCloneTableu▒i    1�
 H��t��H���5�
 �%�
 @�%�
 h������%�
H�=�����^H��H���PTL��H�
 �DH�=�
 UH��
8#TT 1tt$D���o�N
�� ��0)@▒f.�H�=i(;▒�                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ls -la                   
total 20
drwxr-xr-x 2 kali kali 4096 Mar 15  2021 .
drwxr-xr-x 3 kali kali 4096 Mar 15  2021 ..
-rwxr-xr-x 1 kali kali 8320 Mar 15  2021 fang-of-haynekhtnamet
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ git log 
fatal: not a git repository (or any of the parent directories): .git
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ nano fang-of-haynekhtnamet 
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ cat fang-of-haynekhtnamet 
 HH/lib64/ld-linux-x86-64.so.2GNUGNU_���
'�
  ���Ϲ��n= 
           Y h "libc.so.6puts__cxa_finalize__libc_start_mainGLIBC_2.2.5_ITM_deregisterTMClone � � � � � � H�H��__ITM_registerTMCloneTableu▒i 1�
 H��t��H���5�
 �%�
 @�%�
 h������%�
H�=�����^H��H���PTL��H�
 �DH�=�
 UH��
 H9�H��tH�Z
]��f.�]�@f.�H�=i
 H�5b
 UH)�H��H��H��H��?H�H��t▒H�!
 H��t
     ]��f�]�@f.��=
 u/H�=�  UH��t
����H�����    H� ]����fDUH��]�f���UH��H�=�������]�f.�DAWAVI��AUATL�%F UH�-F SA��I��L)�H�H���W���H��t 1��L��L��D��A��H��H9�u�H�[]A\A]A^A_Ðf.���H�H��*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}<��������▒���X"����H��������0zRx
                                       ����+zRx
                                              $X��� F▒J
R                                                      �?▒;*3$"DP��\R���A�C
D|X���eB�B▒�E �B(�H0�H8�M@r8A0A(B B▒B�����0�
���o�`�                                     �
�
 GCC: (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.08Tt��`�
�
 �
 �  ▒ ��
 �▒�� �$ z  @R �Yx �  ���`e�▒▒ ~0+�▒ �:� � �"�
8#TT 1tt$D���o�N                              �crtstuff.cderegister_tm_clones__do_global_dtor�� ��0)@▒leted.7(;▒�                                                                                             tnamet.c__FRAME_END____init_array_end_DYNAMIC__init_array_start__GNU_EH_F┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ find files fang-of-haynekhtnamet 
find: ‘files’: No such file or directory
fang-of-haynekhtnamet
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ file fang-of-haynekhtnamet      
fang-of-haynekhtnamet: ELF 64-bit LSB pie executable, x86-64, version 1 (SYSV), dynamically linked, interpreter /lib64/ld-linux-x86-64.so.2, for GNU/Linux 3.2.0, BuildID[sha1]=5fffe70019957f0a27a70bb886b2cfb9f9b21d6e, not stripped
                                                                                                                                                                                             
┌──(kali㉿kali)-[~/…/Assurnabitashpi/Maelkashishi/Onnissiralis/Ularradallaku]
└─$ ./fang-of-haynekhtnamet 
*ZAP!* picoCTF{l3v3l_up!_t4k3_4_r35t!_76266e38}
                                                                    
```

## Notas Adicionales 



### Referencias

