## Objetivo 
I've hidden a flag in this file. Can you find it? [Forensics is fun.pptm](https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics is fun.pptm)

## Solución  

```java 
                                                                                                
┌──(kali㉿kali)-[~/Downloads/TunnelVision]
└─$ cd ..          
                                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ mkdir MacroHard    
                                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ cd MacroHard 
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ w get https://play.picoctf.org/practice/challenge/130
 12:48:47 up 26 min,  1 user,  load average: 1.59, 1.24, 0.90
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ w get https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics%20is%20fun.pptm
 12:49:05 up 27 min,  1 user,  load average: 1.67, 1.28, 0.92
USER     TTY      FROM             LOGIN@   IDLE   JCPU   PCPU WHAT
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ wget https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics%20is%20fun.pptm 
--2024-10-09 12:51:09--  https://mercury.picoctf.net/static/52da699e0f203321c7c90ab56ea912d8/Forensics%20is%20fun.pptm
Resolving mercury.picoctf.net (mercury.picoctf.net)... 18.189.209.142
Connecting to mercury.picoctf.net (mercury.picoctf.net)|18.189.209.142|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 100093 (98K) [application/octet-stream]
Saving to: ‘Forensics is fun.pptm’

Forensics is fun.pptm    100%[===============================>]  97.75K   161KB/s    in 0.6s    

2024-10-09 12:51:20 (161 KB/s) - ‘Forensics is fun.pptm’ saved [100093/100093]

                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ ls
'Forensics is fun.pptm'
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ librooffice 
Command 'librooffice' not found, did you mean:
  command 'libreoffice' from deb libreoffice-common
Try: sudo apt install <deb name>
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ file ./Forensics\ is\ fun.pptm 
./Forensics is fun.pptm: Microsoft PowerPoint 2007+
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ unzip ./Forensics\ is\ fun.pptm 
Archive:  ./Forensics is fun.pptm
  inflating: [Content_Types].xml     
  inflating: _rels/.rels             
  inflating: ppt/presentation.xml    
  inflating: ppt/slides/_rels/slide46.xml.rels  
  inflating: ppt/slides/slide1.xml   
  inflating: ppt/slides/slide2.xml   
  inflating: ppt/slides/slide3.xml   
  inflating: ppt/slides/slide4.xml   
  inflating: ppt/slides/slide5.xml   
  inflating: ppt/slides/slide6.xml   
  inflating: ppt/slides/slide7.xml   
  inflating: ppt/slides/slide8.xml   
  inflating: ppt/slides/slide9.xml   
  inflating: ppt/slides/slide10.xml  
  inflating: ppt/slides/slide11.xml  
  inflating: ppt/slides/slide12.xml  
  inflating: ppt/slides/slide13.xml  
  inflating: ppt/slides/slide14.xml  
  inflating: ppt/slides/slide15.xml  
  inflating: ppt/slides/slide16.xml  
  inflating: ppt/slides/slide17.xml  
  inflating: ppt/slides/slide18.xml  
  inflating: ppt/slides/slide19.xml  
  inflating: ppt/slides/slide20.xml  
  inflating: ppt/slides/slide21.xml  
  inflating: ppt/slides/slide22.xml  
  inflating: ppt/slides/slide23.xml  
  inflating: ppt/slides/slide24.xml  
  inflating: ppt/slides/slide25.xml  
  inflating: ppt/slides/slide26.xml  
  inflating: ppt/slides/slide27.xml  
  inflating: ppt/slides/slide28.xml  
  inflating: ppt/slides/slide29.xml  
  inflating: ppt/slides/slide30.xml  
  inflating: ppt/slides/slide31.xml  
  inflating: ppt/slides/slide32.xml  
  inflating: ppt/slides/slide33.xml  
  inflating: ppt/slides/slide34.xml  
  inflating: ppt/slides/slide35.xml  
  inflating: ppt/slides/slide36.xml  
  inflating: ppt/slides/slide37.xml  
  inflating: ppt/slides/slide38.xml  
  inflating: ppt/slides/slide39.xml  
  inflating: ppt/slides/slide40.xml  
  inflating: ppt/slides/slide41.xml  
  inflating: ppt/slides/slide42.xml  
  inflating: ppt/slides/slide43.xml  
  inflating: ppt/slides/slide44.xml  
  inflating: ppt/slides/slide45.xml  
  inflating: ppt/slides/slide46.xml  
  inflating: ppt/slides/slide47.xml  
  inflating: ppt/slides/slide48.xml  
  inflating: ppt/slides/slide49.xml  
  inflating: ppt/slides/slide50.xml  
  inflating: ppt/slides/slide51.xml  
  inflating: ppt/slides/slide52.xml  
  inflating: ppt/slides/slide53.xml  
  inflating: ppt/slides/slide54.xml  
  inflating: ppt/slides/slide55.xml  
  inflating: ppt/slides/slide56.xml  
  inflating: ppt/slides/slide57.xml  
  inflating: ppt/slides/slide58.xml  
  inflating: ppt/slides/_rels/slide47.xml.rels  
  inflating: ppt/slides/_rels/slide48.xml.rels  
  inflating: ppt/slides/_rels/slide49.xml.rels  
  inflating: ppt/slides/_rels/slide50.xml.rels  
  inflating: ppt/slides/_rels/slide32.xml.rels  
  inflating: ppt/slides/_rels/slide52.xml.rels  
  inflating: ppt/slides/_rels/slide53.xml.rels  
  inflating: ppt/slides/_rels/slide54.xml.rels  
  inflating: ppt/slides/_rels/slide55.xml.rels  
  inflating: ppt/slides/_rels/slide56.xml.rels  
  inflating: ppt/slides/_rels/slide57.xml.rels  
  inflating: ppt/slides/_rels/slide58.xml.rels  
  inflating: ppt/slides/_rels/slide51.xml.rels  
  inflating: ppt/slides/_rels/slide13.xml.rels  
  inflating: ppt/_rels/presentation.xml.rels  
  inflating: ppt/slides/_rels/slide1.xml.rels  
  inflating: ppt/slides/_rels/slide2.xml.rels  
  inflating: ppt/slides/_rels/slide3.xml.rels  
  inflating: ppt/slides/_rels/slide4.xml.rels  
  inflating: ppt/slides/_rels/slide5.xml.rels  
  inflating: ppt/slides/_rels/slide6.xml.rels  
  inflating: ppt/slides/_rels/slide7.xml.rels  
  inflating: ppt/slides/_rels/slide8.xml.rels  
  inflating: ppt/slides/_rels/slide9.xml.rels  
  inflating: ppt/slides/_rels/slide10.xml.rels  
  inflating: ppt/slides/_rels/slide11.xml.rels  
  inflating: ppt/slides/_rels/slide12.xml.rels  
  inflating: ppt/slides/_rels/slide14.xml.rels  
  inflating: ppt/slides/_rels/slide15.xml.rels  
  inflating: ppt/slides/_rels/slide16.xml.rels  
  inflating: ppt/slides/_rels/slide17.xml.rels  
  inflating: ppt/slides/_rels/slide18.xml.rels  
  inflating: ppt/slides/_rels/slide19.xml.rels  
  inflating: ppt/slides/_rels/slide20.xml.rels  
  inflating: ppt/slides/_rels/slide21.xml.rels  
  inflating: ppt/slides/_rels/slide22.xml.rels  
  inflating: ppt/slides/_rels/slide23.xml.rels  
  inflating: ppt/slides/_rels/slide24.xml.rels  
  inflating: ppt/slides/_rels/slide25.xml.rels  
  inflating: ppt/slides/_rels/slide26.xml.rels  
  inflating: ppt/slides/_rels/slide27.xml.rels  
  inflating: ppt/slides/_rels/slide28.xml.rels  
  inflating: ppt/slides/_rels/slide29.xml.rels  
  inflating: ppt/slides/_rels/slide30.xml.rels  
  inflating: ppt/slides/_rels/slide31.xml.rels  
  inflating: ppt/slides/_rels/slide33.xml.rels  
  inflating: ppt/slides/_rels/slide34.xml.rels  
  inflating: ppt/slides/_rels/slide35.xml.rels  
  inflating: ppt/slides/_rels/slide36.xml.rels  
  inflating: ppt/slides/_rels/slide37.xml.rels  
  inflating: ppt/slides/_rels/slide38.xml.rels  
  inflating: ppt/slides/_rels/slide39.xml.rels  
  inflating: ppt/slides/_rels/slide40.xml.rels  
  inflating: ppt/slides/_rels/slide41.xml.rels  
  inflating: ppt/slides/_rels/slide42.xml.rels  
  inflating: ppt/slides/_rels/slide43.xml.rels  
  inflating: ppt/slides/_rels/slide44.xml.rels  
  inflating: ppt/slides/_rels/slide45.xml.rels  
  inflating: ppt/slideMasters/slideMaster1.xml  
  inflating: ppt/slideLayouts/slideLayout1.xml  
  inflating: ppt/slideLayouts/slideLayout2.xml  
  inflating: ppt/slideLayouts/slideLayout3.xml  
  inflating: ppt/slideLayouts/slideLayout4.xml  
  inflating: ppt/slideLayouts/slideLayout5.xml  
  inflating: ppt/slideLayouts/slideLayout6.xml  
  inflating: ppt/slideLayouts/slideLayout7.xml  
  inflating: ppt/slideLayouts/slideLayout8.xml  
  inflating: ppt/slideLayouts/slideLayout9.xml  
  inflating: ppt/slideLayouts/slideLayout10.xml  
  inflating: ppt/slideLayouts/slideLayout11.xml  
  inflating: ppt/slideMasters/_rels/slideMaster1.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout1.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout2.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout3.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout4.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout5.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout6.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout7.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout8.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout9.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout10.xml.rels  
  inflating: ppt/slideLayouts/_rels/slideLayout11.xml.rels  
  inflating: ppt/theme/theme1.xml    
 extracting: docProps/thumbnail.jpeg  
  inflating: ppt/vbaProject.bin      
  inflating: ppt/presProps.xml       
  inflating: ppt/viewProps.xml       
  inflating: ppt/tableStyles.xml     
  inflating: docProps/core.xml       
  inflating: docProps/app.xml        
  inflating: ppt/slideMasters/hidden  
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ ! .xml$ !.rel   
zsh: event not found: .rel
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$     cat ./ppt/vbaProject.bin
��ࡱ▒�>��        ���������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������


��������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������Root Entry��������@VB����������PGk����PGk��di�������������Module1���_����


▒����!"#$%&'()*+,-./0123456789:;<=����?@ABC����������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������ű�0*�       pH�d�
VBAProje�ct4@j
=
r       �I�a�
             J<
h%^*\G{00�020430C
0046}#2.0#0#C:\Windows\Syst em32\e2.tlb#OLE Automation`�EOffDic�EOf�i�c�E�����E2DF8D04C-5BFA-10�1B-BDE5�E�AA�C4�2�E��gram Files\CommonMicrosoft Shared\OFFICE16\MSO.0DLL#��M 1@6.0 Ob�� �LibraryKE������
Mod�ule1G�du�1▒ �
                 H�B1�pꀉB�,B▒��!+BB��������(����������������������������x��ME��������������������������������������������������������������������������������������������������������������������������������������������(6
����<��<▒��<���������������@�&��������8���������������%
                                                       *����`�������������������������`�*�����������������H@��������������������@�������������������������������������������������������I�a$*\Rffff*0461814a28��� ����@�@o��p]���sorry_but_this_isn't_it'*����@����q�Attribute VB_Name = "Module1"
Sub not_flag()
 DimL As� S�ng6V�@sorry_�_this_isn 't_it�End �
�a��            � *\G{000204EF-0000-0000-C000-000000000046}#4.2#9#C:\Program Files\Common Files\Microsoft Shared\VBA\VBA7.1\VBE7.DLL#Visual Basic For Applications$*\G{91493440-5A91-11CF-_VBA_PROJECT▒������������▒PROJECT����>^PROJECTwm������������D▒������������8700-00AA0060263B}#2.c#0#C:\Program Files\Microsoft Office\root\Office16\MSPPT.OLB#Microsoft PowerPoint 16.0 Object Library�*\G{00020430-0000-0000-C000-000000000046}#2.0#0#C:\Windows\System32\stdole2.tlb#OLE Automation(*\G{2DF8D04C-5BFA-101B-BDE5-00AA0044DE52}#2.8#0#C:\Program Files\Common Files\Microsoft Shared\OFFICE16\MSO.DLL#Microsoft Office 16.0 Object Library▒▒"���������I�a����������������������������������������������������������������Module10461814a28��&Module1����������� ������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������������L��CsXz�>��������`�L+���������������������������������������������������������������������3
PowerPointVBA��Win16�~Win32Win64xMac��VBA6�#VBA7�Project1
stdole�`
VBAProject��OfficeuModule1b     ��_Evaluate▒���not_flag ���H��'������������������������������������ ��"����$����
               ID="{111D4352-E1AC-46B0-8500-E5E7DFB7004C}"
Module=Module1
Name="VBAProject"
HelpContextID="0"
VersionCompatible32="393222000"
CMG="3436F0FDF000F400F400F400F4"
DPB="3B39FFFA07FB07FB07"
GC="424086038C048C0473"

[Host Extender Info]
&H00000001={3832D640-CF90-11CF-8E43-00A0C911005A};VBE;&H00000000

[Workspace]
Module1=26, 26, 668, 718, 
Module1Module1                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$     cat ./ppt/slideMasters/hidden
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ cat hidden | tr -d ' '
cat: hidden: No such file or directory
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard]
└─$ cd ppt                
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard/ppt]
└─$ cd slideMasters 
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard/ppt/slideMasters]
└─$ cat hidden            
Z m x h Z z o g c G l j b 0 N U R n t E M W R f d V 9 r b j B 3 X 3 B w d H N f c l 9 6 M X A 1 f Q                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard/ppt/slideMasters]
└─$ cat hidden | tr -d '  '
ZmxhZzogcGljb0NURntEMWRfdV9rbjB3X3BwdHNfcl96MXA1fQ                                                                                                 
┌──(kali㉿kali)-[~/Downloads/MacroHard/ppt/slideMasters]
└─$ cat hidden | tr -d '  ' | base64 -d
flag: picoCTF{D1d_u_kn0w_ppts_r_z1p5}base64: invalid input
                                                                                                



```
picoCTF{D1d_u_kn0w_ppts_r_z1p5}
## Notas Adicionales 

### Referencias
