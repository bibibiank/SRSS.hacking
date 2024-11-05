## Objetivo 
Can you look at the data in this binary: [static](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/static)? This [BASH script](https://mercury.picoctf.net/static/7495259e963bd5b67d0fb8b616652618/ltdis.sh) might help!

## Solución  
```bash
──(kali㉿kali)-[~/Downloads]
└─$ ls
 Addadshashanammu       challenge.zip   files                 level2.flag.txt.enc
 Addadshashanammu.zip   codebook.txt    files.zip             level2.py
 big-zip-files.zip      code.py         fixme1.py            'ltdis(1).sh'
'challenge(1).zip'      convertme.py    fixme2.py             ltdis.sh
'challenge(2).zip'      drop-in         flag                  opera-stable_113.0.5230.86_amd64.deb
'challenge(3).zip'      enc_flag        level1.flag.txt.enc   runme.py
'challenge(4).zip'      file            level1.py             static
                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ cat ltdis.sh 
#!/bin/bash



echo "Attempting disassembly of $1 ..."


#This usage of "objdump" disassembles all (-D) of the first file given by 
#invoker, but only prints out the ".text" section (-j .text) (only section
#that matters in almost any compiled program...

objdump -Dj .text $1 > $1.ltdis.x86_64.txt


#Check that $1.ltdis.x86_64.txt is non-empty
#Continue if it is, otherwise print error and eject

if [ -s "$1.ltdis.x86_64.txt" ]
then
        echo "Disassembly successful! Available at: $1.ltdis.x86_64.txt"

        echo "Ripping strings from binary with file offsets..."
        strings -a -t x $1 > $1.ltdis.strings.txt
        echo "Any strings found in $1 have been written to $1.ltdis.strings.txt with file offset"



else
        echo "Disassembly failed!"
        echo "Usage: ltdis.sh <program-file>"
        echo "Bye!"
fi
                                                                                                    
┌──(kali㉿kali)-[~/Downloads]
└─$ cat static                    
 HH/lib64/ld-linux-x86-64.so.2GNUGNU��A+�kpl%h��B0m�'= 
                                                       Y h "libc.so.6puts__cxa_finalize__libc_start_ � � � � � � H�H��M_deregisterTMCloneTable__gmon_start___ITM_registerTMCloneTableu▒i    1�
 H��t��H���5�
 �%�
 @�%�
 h������%�
H�=�����^H��H���PTL��H�
 �DH�=�
 UH��
 H9�H��tH�Z
]��f.�]�@f.�H�=�
 H�5�
 UH)�H��H��H��H��?H�H��t▒H�!
 H��t
     ]��f�]�@f.��=I
 u/H�=�  UH��t
����H����!    H�=�       �
 ]����fDUH��]�f���UH��H�=�������]�f.�DAWAVI��AUATL�%F UH�-F SA��I��L)�H�H���W���H��t 1��L��L��D��A��H��H9�u�H�[]A\A]A^A_Ðf.���H�H��Oh hai! Wait what? A flag? Yes, it's around here somewhere!8����������
 ���T����<��������,zRx
                     ����+zRx
                            $P��� F▒J
R                                    �?▒;*3$"DH��\J���A�C
D|P���eB�B▒�E �B(�H0�H8�M@r8A0A(B B▒B�x���0�
���o�`�                                     �
�
 picoCTF{d15a5m_t34s3r_f6c48608}GCC: (Ubuntu 7.5.0-3ubuntu1~18.04) 7.5.08Tt��`�
�
 �
 �  ▒@ ��
 �$�� � k  1C@ �Ji v  ���`e�▒H o0+�▒@ �:�@ � �   �"�
                                                    �crtstuff.cderegister_tm_clones__do_global_dtors_auxcompleted.7698__do_global_dtors_aux_fini_array_entryframe_dummy__frame_dummy_init_array_entrystatic.c__FRAME_END____init_array_end_DYNAMIC__init_array_start__GNU_EH_FRAME_HDR_GLOBAL_OFFSET_TABLE___libc_csu_fini_ITM_deregisterTMCloneTableputs@@GLIBC_2.2.5_edata__libc_start_main@@GLIBC_2.2.5__data8#TT 1tt$D���o�Nrt____dso_handle_IO_stdin_used__libc_csu_init__bss_startmain__TMC_END___ITM_register�� � @ @ �0@)▒agp�▒V``�^y▒�                                                                                                    .gnu.version.gnu.version_r.rela.dyn.rela.plt.init.plt.got.text.fini.rodat┌──(kali㉿kali)-[~/Downloads]


```

## Notas Adicionales 

### Referencias
