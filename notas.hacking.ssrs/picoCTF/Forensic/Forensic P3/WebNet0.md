## Objetivo 

We found this [packet capture](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap) and [key](https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key). Recover the flag.
## Solución  

```java
┌──(kali㉿kali)-[~/Downloads/WebNet0]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap'
--2024-10-09 13:03:50--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13163 (13K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap             100%[===============================>]  12.85K  --.-KB/s    in 0s      

2024-10-09 13:03:58 (155 MB/s) - ‘capture.pcap’ saved [13163/13163]

                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet0]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key'
--2024-10-09 13:04:12--  https://jupiter.challenges.picoctf.org/static/0c84d3636dd088d9fe4efd5d0d869a06/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key             100%[===============================>]   1.66K  --.-KB/s    in 0s      

2024-10-09 13:04:20 (35.6 MB/s) - ‘picopico.key’ saved [1704/1704]

                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet0]
└─$ file *                        
capture.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 65535)
picopico.key: OpenSSH private key (no password)
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet0]
└─$ cat capture.pcap                   
�ò����
Y�r%�-E@@+����������"�������j
�\��
YE<@@j��܀����ߒ�7��"���h��.#
!���\��
Y�r%�-E@@+���������������}j
�\��
YE<@@j��܀��������       E���    �h��.#
!���\��
��r%�-E4@+Ā��������"����7��
�\�!�
gWr%�-E9@+}����������"����7��▒
�\�!����ش��>�}���Ǖ�.�O]Ee
                         d��Nr�0�,�(�$��
���kih976�2�.�*�&���=5�/�+�'�#��        ���g?>310�1�-�)�%���</��
�a752ec2-18-223-184-200.us-east-2.compute.amazonaws.com

▒▒▒


 ��
YE4V�@@�܀����ߒ�7��"�����&
!���\��
YE#V�@@)�܀����ߒ�7��"���▒��
!���\�51*���^�ߐr�g!x�y��_�!Uw�f���U             �#�
        *�H��                                      ���0��0���R.�&j���>Lf���$�0
0\1
   0    UUS10U
            Michigan10U
                        Kalamazoo10U

Pico CTF10U


200811154129Z0\1
                0       UUS10U
                            Michigan10U
                                        Kalamazoo10U

Pico CTF10U


�0�eshar*�H��0
��*QO4��x�y���S�w�w�� {��(V.v��8K:�9Ȃ�G�(�-�
                                            ����pi7�?c���qD`��Ԍ0��a��+.D��l��eE5e��!C�A{OZ_}�0�dA$�[�e�m��;d�pC▒�BQe�    ��]Е�(�1���ߨ�p�0Ǎq�^ј���y#����]�▒��g����!��A&▒▒�w�8�t�
                                                                              �s�#���I���I���OȄl
������H7*�H�����4������$��&xo�S0Q0U!��8�<����`%z�l(�0U#▒0�!��8�<����`%z�l(�0U�0�0
�ip�su�x��'8{�z�ߝes���/�HL���Ij�QšL&������%�    r��gJ6�29�T"�*8�n       ��n~+*��J�6��ǝ�yG"�7}��oOmo��E��yNd��f�p�▒[m�b��zq�����:
����0&��9s�
           �C�pԾ��~�Qv�����������y�E��A]��� \�D�2=Cc� B�m�r&�
��r%�-E4@+Ā����������   ��      F�                           `]��BBA�
�\�!���
H�r%�-E9@+}������������ ��      F�▒
�\�!�����▒�B{   �|���h��C��SX   DrȚ�ف�gr�0�,�(�$��
���kih976�2�.�*�&���=5�/�+�'�#��        ���g?>310�1�-�)�%���</��
�a752ec2-18-223-184-200.us-east-2.compute.amazonaws.com

▒▒▒


 ��
YE4h@@��܀�������        F������&
!��\ƴ
Y�r%�-E4@+Ā��������"����;�����
�\�!���
YE#h@@���܀�������hA�    F����▒��
��p�-ȷ���N�Nɘ�mD�#�
        *�H��      ���0��0���R.�&j���>Lf���$�0
0\1
   0    UUS10U
            Michigan10U
                        Kalamazoo10U

Pico CTF10U


200811154129Z0\1
                0       UUS10U
                            Michigan10U
                                        Kalamazoo10U

Pico CTF10U


�0�eshar*�H��0
��*QO4��x�y���S�w�w�� {��(V.v��8K:�9Ȃ�G�(�-�
                                            ����pi7�?c���qD`��Ԍ0��a��+.D��l��eE5e��!C�A{OZ_}�0�dA$�[�e�m��;d�pC▒�BQe�    ��]Е�(�1���ߨ�p�0Ǎq�^ј���y#����]�▒��g����!��A&▒▒�w�8�t�
                                                                              �s�#���I���I���OȄl
������H7*�H�����4������$��&xo�S0Q0U!��8�<����`%z�l(�0U#▒0�!��8�<����`%z�l(�0U�0�0
�ip�su�x��'8{�z�ߝes���/�HL���Ij�QšL&������%�    r��gJ6�29�T"�*8�n       ��n~+*��J�6��ǝ�yG"�7}��oOmo��E��yNd��f�p�▒[m�b��zq�����:
����0&��9s�
           �C�pԾ��~�Qv�����������y�E��A]��� \�D�2=Cc� B�m�r&�
Y�r%�-Er@+~����������"����;��tE                              `]H���A�
�\�!��m%�
��g'\S�G#(����t�(1Z9�PMB�;p�^#��PS��]�ȓ�y|��
                                            ��mc�Vb��N����B[Ç�_���nES�.�
�;p�0�|O��f�u▒F�5id4�1 g�\���X�f�Ϗ����Å▒2=eHJ&�ib�G�9����k;G-M�9 ��c#H
                                                                      R��&�n��~�L�4Hk������g�{rv���~_�����j
          �-��4vJ��h��ց��_A��%7g�(���B�r.�zZ)��w�PRFD��:Ζz�DCX>�O���F�#J�
YE6V�@@�܀����ߒ�;��"�Ā▒��(                                                `]�DDr%�-hA�
!�      �\���,�NVDI62����ǂ㉅}�Ja#�Fx�7��G�!��o�F;ۊ^T�L��K�▒8���i�E�▒�=F� �P�����j���"$���7�#�g�dd�
 s�=Ԍ�V�_����I0R���9|�
�����                 ���厔�#=,��xIK��Qx�[v�__c���
     ��w���я���(
�-3��s��xTM��q�*�(Ϲ5�]f�s�
F�O��������7s�߅~�޸�-�ô
5����-E4@+Ā������������]�SBBA�
�\�!��
Y�r%�-E@@+��������������! j
�\��
YE<@@j��܀������)#T���h��.#
!�(�\��
5��>�-Er@+~��������������
�\�!�H   ,��`�fx_
                 �m;V�ܨ`K���BgaNj�Z�by�}���b����:5��B▒}J��������a�q�Wݬ�Qj��n���ET���K�8���5�������
 ���c�(��x��VAz�ᩔ�~3������~�D�)^����'�O��cS}���^0l�|���ڹ�"=���XHi����O�I��
                                                                          9�}�06��}y�f�{c!��,�"B��ı�}w��Ӯ�8���������e<��$n!(�$1
�) А
    Nt����������>?�j�C��:����
Y�r%�-E4@+Ā��������"�Ē�<���� `]\hBBA�
�\�!�   �
5���L�▒��(��������-hA�
!�*�\���,�NVDI62����ǂ㉅}X�k�x;z���b�"�ʬ;(ٳ���Nv-%!�@��g09���2�r�iP�^���|'����ב�\��u     �7C~ZHd����/��ԩ�p�R��F$�
               ��v�� �B�b*vP]��f�x���h�򻲼{f��e�▒Fv��'�ڌ��K�oש(�bv�5�ntSՖ�(
                                                                         ��Jv��3H{t�'�ԏ,���+t�i� s���u�qiϕ��
           `]
=�r%�-E4@+Ā����������)#U�
�\�!�(�
��r%�-E9@+}������������)#U�▒
K�:ʱp����NN���_����LG�,r�0�,�(�$��
���kih976�2�.�*�&���=5�/�+�'�#��        ���g?>310�1�-�)�%���</��
�a752ec2-18-223-184-200.us-east-2.compute.amazonaws.com

▒▒▒


 ��
YE4B=@@(��܀������)#U�����&
!�F�\��
YE#B>@@$��܀������)#U���▒��
!�F�\�51�
         �Cγ����I��7�1�O��V.�Z�ɏ���     �#�
        *�H��                              ���0��0���R.�&j���>Lf���$�0
0\1
   0    UUS10U
            Michigan10U
                        Kalamazoo10U

Pico CTF10U


200811154129Z0\1
                0       UUS10U
                            Michigan10U
                                        Kalamazoo10U

Pico CTF10U


�0�eshar*�H��0
��*QO4��x�y���S�w�w�� {��(V.v��8K:�9Ȃ�G�(�-�
                                            ����pi7�?c���qD`��Ԍ0��a��+.D��l��eE5e��!C�A{OZ_}�0�dA$�[�e�m��;d�pC▒�BQe�    ��]Е�(�1���ߨ�p�0Ǎq�^ј���y#����]�▒��g����!��A&▒▒�w�8�t�
                                                                              �s�#���I���I���OȄl
������H7*�H�����4������$��&xo�S0Q0U!��8�<����`%z�l(�0U#▒0�!��8�<����`%z�l(�0U�0�0
�ip�su�x��'8{�z�ߝes���/�HL���Ij�QšL&������%�    r��gJ6�29�T"�*8�n       ��n~+*��J�6��ǝ�yG"�7}��oOmo��E��yNd��f�p�▒[m�b��zq�����:
����0&��9s�
           �C�pԾ��~�Qv�����������y�E��A]��� \�D�2=Cc� B�m�r&�
Y�r%�-E4@+Ā����������L��7���e                                `]��BBA�
�\�!�*�
Y�r%�-E4@+Ā����������)'D��7�
�]!�F�
Y�r%�-Er@+~������������)'D�F
�]!�F�5�F[�s�TQ�B��S}%rC�4g~;.��Ր���q�K�/���u�O�_rkX�|\z�����$  ��§��Ct��5S3�����쾪h���U0;�H
                                                                                            �[��f�5�RaY▒bu�M�S8�`�''~�t���U_lu�U/Q:8�껂Oħp�ݖ�$���2S�?h�🚃��Aͼ,�_nE���}�`��<�r�P
a��'                       st   ���hLj5�\���(DQ>���
�����y��μRE�8�b�s'E�R�
YE6B?@@'��܀������)'D�׀▒��(Dr%�-hA�
!�e�]��,�NVDI62����ǂ㉅}�<Gf��▒
                              0+�x1
                                   �i��u���<�U��I����!i�T��{0"A��М�}D>�.���sp?�v�ݹ�����ju����)�:��5h�mD���D���L���▒N͹z���v�q9u�▒���w�!Y w        )��▒����@��:
�Ж8!{u2�8�(�o��U���ALHN$�вB�|�l�_�▒c!˿ZO]1�5���             ��l6�����0
Y�r%�-E4@+Ā����������)(F��5N                   `]�BBA�
�]6!�e�
Y�r%�-E�@+~�A�
           �����������)(F�=X
�]9!�e�DQ>������xZ���v�b��o��&�Q/R��.�
                                      �@��'
�9���                                      �N�.
     Z�Ў�=���)�\b?�c&&2Ȃ*�Q�6�?6��e����_^�^���v�j�c4+
                                                     �"ȕ�n����X
�t�>���D 9�n�I"/Z�ag,� ;�:�/��!&=b+�v
���N� �uJm��i��M3�½^�S��AP���?Ӌ���E#�%��1��Co�0�t���w^���"��M�rk� @>�u�L�Tbq��������wG��3*���V���k�����#?5�3�f��E#�ޥǖ��ȑ6�cF�]��d>���B�׽��sIOvw�D�v�V�uI��.�&��G|0��h���h�oA�w�Ʒ�q/u�,
                                                                                     :`���|&}�f����Љ��-
      ▒��CA��"iC�
YEB@@@#��܀������)(F�r%�-��▒���
�0��λI�"�Z▒�4#Je�Z]꽣�  �!

                          ���'nY���|�]#ͻy���>j�!������-O�=*@S�z��)��
                                                                    @���ԩ����a����W��X�^���,S��qmԾ�M6�-fKR��
           ��Mi�?yX�X'����z�C`u��jê#C��V����x�󄭟���Fb/'�Ya�'���I�        ��▒�^B�mP�����p�u▒k�~��Jʮ�qm4��3�WL3�]*�#�ƅ<ӛ
:-�d?�������R�<Mв�Cm������[�����LO���CwO�!�}�S�l~�bq��g`��G[��:
                                                               4=▒

y/[$�r���[����B*��rXY�Nf▒y"�7;▒v]+&@�Q��▒;���@�/E�������3c�0�@� ����8&��Ǵ�>��M�<:������5f3�A���?�}X�����u >�q�AW��G�����v�:���0Q ����h���<qH���������Ne�\��� a`Ñ[q��5#0{��8�eaLg�]����x�gNL���LQ��(;l
   ��J�
[d��S��s!��w���Cgh�N.o}�,4�\��8Ӝ��g}'Aª��
                                         �@�D�1����e�����p~��}=VP�e��ynK�Y�Cq��
                                                                               Qn�-�
�
 �v����ߩ>a��G�U_J��g6O9��#�S�Zm�%b@˹ej��r����y���ay�5��m�5
                                                          ff,��<���%�&{�r�'���
_<�$��7��g+u�����Q��g�|^�;p����zn0/bI-'
��|S׽�mcb}?���9��頇������N�2 Α�U�
                                 ��Y��
�l�.��'�U�l���D�[��OuQċ~��n(�y� ���s�"�����u_O�{
z��:����H6�35yj���4�ZD�v�<����\����u�t�=�T�Q�e�����     �6
      Z��*�J��+��*
                  #��*S���G��wy`Sc�܊��0i�A▒w��B/�h��W����&���h�*        ��@�pTh}s�LL�x�};QiA��c�~��7�쭱՛�XZ#�b�cՠ$��:��#�A���Ey��
                                ?�z��-��� ����g�G�Ը9�:�';f��
                                                            OP
��]�R����Wsŵ�=/���F�
Y�r%�-E4@+Ā��������  `]���)-��.�BBA�
�]X!���
       `]9m
Y�r%�-E�@+}����������"�Ē�<����
;E�+*�<�1�n��sG+N��畞���}W��{�217��<}�7��[?��+�k�Ɉ�J�P��Y��m��
�@(�k�����N%▒�ٴ�k v�����yQ�K&�i�s�
�b�`�i��Z/��`wpY�H
                  ˺<�]W=��
                          @���L(O<�2-1aou�:r�ط-���2!�Vv�`�D�YR��1y�
=W��f�|��A���eZ-G��▒G   #eզ[�w6-U��OP&&������H��9��[ߩ׻3g�e�~�[���4
t_�Z�r���7�����/e�g<����%�&>��C��p3�M�:�Z�Ə�,uп�����8>��P�9�K▒$��*���
                                                                     ?��~2|p�i=e,�aܐi�l���fHDMg*7Z���uK��S��
           `]�n
YE2V�@@▒�܀����ߒ�<��"���▒��$
!�1�]��Ϲ5�]fc����G����W�j�I��x�;�*D~XlX�9eY�@f��XG�f���|�k�l����$3��:g�Y��)e}�  �?K'    �ێ�J�]X�;7�cw����$�PX�_)7���P]�
                      B��$�Պ���xK��O���3�~G��G�Tz��c6�O��*�5��QT�f��h���[B~��|��G��a�L�8�u��@�2����<9�J��r#����
              ��5:i�Y �fG� ��_��d���"*�1([^����˚��K��6"��Y����v𯿮�����v3iL���0Ez~#�b|��]%P�o�
M��l�����6�XkCw�i▒���輶��
                         O���;��Aɝ���1bɴ�������Ƀ��
                                                  �:��gp����v4�5����Kf�����QK--�~X
                                                                                  ɲ6���@
                                                                                        `�$��vê�ҿ9�'scC?�5k
U�����\���;L"�w�nebd    V%��ح�"��ϩ+m���
                                       `]�
Y�r%�-E4@+Ā��������"����>����             BBA�
�]�!�1�
Y�r%�-E�@+~P���������"����>���V
�_�!�1o���B�r.����_aa��M
                        �&�M��o��
�y=*yѢ���5�L�lm4�ʄߓ�-*�'H3H�OQS���'��_�:5"�L�� 4)
4��Nt�e�6?���5�9�3'�l�������%�=���恼��٦�=
         �NO��X�^�>�hA�:�
J~HH9�����`m��*�G���RdA���`vOo^�ƨ#      �~.X�������v�/z����]/*L��]-��GX���� �E��-4������K�������R�*�w��w.�ђ��Ȟ�&��\
]@ns▒�� \���M2���geM)
�
��tN�܆D��ח�|�▒�{���Pentoxo�▒%Ԅpo�O��Z{
YEoV�@@ڬ܀����ߒ�>��"���▒��a
!���_�6Ϲ5�]fc��,�T=��u��v��0G�?ν��!am��+
                                        g(5O]�4\o��(|G����      �Hr����_ߓ�j5��{ȡj�W!�,}7����w�u0Y���
pŋg�y~m��.�%Ӿ�m
7�����)����U��T1�8r�#��$Zx�qr�1?�b���`�;�0▒h��I��td�V���
                                                        �&��-�S6(�3���qB�t%��ཟ ��LkpN�\B�FH(=JW���w�N�8�[`:�Z�YxK�#��f����r�W����\���wҷ^���$�O����.T��KGW��O��`0��t�ȎJIMq�0Dԭ갬��5�ƕ����Ż��5!���|)'�7���sȑ��a������(j�uZU��Fzbn�=S�I��LKq)Ex�.������U?�th�w� g���u8�6�y�'�gV�zUO�}E
             ǽ�nƈ��9�F���Q1���}ѵ
Y�r%�-E4@+Ā��������"����A$����  `]:�BBA�
�_�!��                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet0]
└─$ cat picopico.key 
-----BEGIN PRIVATE KEY-----
MIIEvQIBADANBgkqhkiG9w0BAQEFAASCBKcwggSjAgEAAoIBAQCwKlFPNKjseJF5
puCJU5x38XcT1eQge5zOKNahAlYudvGVOEs61TnIgvcER4ko8i3OCwak2/atcGk3
oz9jFKep7XFEYNP31IwwD9j/YazlKy4DRLGObOyIZUU1f2WRA7Uhf0POQXsDT1oU
X32jMKZkQSSDW4MRZd9trJYdO2TrcEPMsBiZQlFlvgnNwl3QlawozTHLAJKI36j1
cPwSMMeNca1e0Zi1s7R5IxfhpNXOBF0FmxiWvmeOHbaspyHg8UEmGBrkd4k4wXSK
GQvrc8QjycP4ScEdquxJiYnDT8iEbAq70/7f/5NIN1DE9YoGJqKYjTS9nRPB4Yvj
JN/SJnhvAgMBAAECggEACCnd3LrG/TZVH3sROqvqO1CwQPYPfUXdLVyNHab7EWon
pc+XBOHurJENG2CpRYF7h+nQ5ADhfIYSCicBf/jsEB7VueJ20CxEVtHVL3h6R6Bp
oHMle0Em8OcofuMpdL/kO+om3T8BkVSzCvCl5NMTUuAF7iRmfX7oDLALwM0IzzQv
2un+2UmT15rgAZfl3IL1PGvJhbhLxfeeyPE9MBy1SqBjQ9rNFn8sQv959J6BHz4b
EpK//ErtNP2yh7oiVBBgKEQ1gEuOjQC/4oxoqCFfZaf9XNRCxB/zY1nUprvJyz09
NMQWNF2EmvmBVGfoTxmuut5N0GbVr2UyHxWMKm2sOQKBgQDpb2+AWgWlGtetuLKJ
fJs8dnd6LhnafbKCOXMOT68qMBRoTpBtVTLRVSNvWCm8m4TTEazX4+ZA+bJFwUFw
aATDmHcr6lMI3tNKrcsnY2F7o5I4z6mwuRuSeszq/ndxZqCzwCu4nKixh3cznp7j
JiElNG0d8Lu5eQgmVAK1AhWXfQKBgQDBMa9ga7VJUP4pzcHnWAoi34OpfjvQYeGl
IKL3AKO4OedaHdH9qid41PQHnL7O3xzN669SkLZ5s0d88A/LFLk4oZNMKdkSTQIQ
+AMbXH01HGFvnCOuPg/FbNp1wS7zJEg5u5HFQWyMPNJLr/hZ6g2Yp+UGpAcGTwM/
RCPVAPhLWwKBgQDAB0OaOnPaVjKGXiHAqBirrGiswa/S5QQrzEaxxys5cUPYaoi0
6BldysPTnJr45JZna2rcTkXjvYTBjTDf3zHMFWgzYBfefC8kh8NPK5nNs8ldorbd
AemEnjBkP+DSELKyK6vLulOrdtzAQgRCp+MsT+xTbO2ArefeX826SXSpoQKBgC2v
nDOHBQXje1dTawlUToFUrgQE8AwlOYEdKKyUoCLOvqEW8DO2a0MtyM+MB6tQI7Wm
iH1T73L0LHGlK3bw3aRAwV5/fu/O+jAdFk8AHjPTFE+acu2fi4c6aKb0GjAxYksU
yjIFeK/pKinv4SESMkjpW0WowGiDgtcRPBAA/LaFAoGAfEM1rfM0v3UmB7PS6u0m
P3ckP2CFCdaryXPfC52GBcJ3Q46YpsQvLTVotM+teHvTjNw2jwwZxIl4NenGSEj3
KDhQoOiQC9BrDD+DB4I9+T9nxT3g7R6MrgITghB4We7TVhL/PljnJTyDqpjNA4kY
TveAJPv6Xq1ERt5PUtX3BqQ=
-----END PRIVATE KEY-----
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet0]
└─$ wireshark capture.pcap  &
[1] 23125
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet0]
└─$ 
```
```

















GET / HTTP/1.1

Host: ec2-18-223-184-200.us-east-2.compute.amazonaws.com

User-Agent: Mozilla/5.0 (Macintosh; Intel Mac OS X 10.14; rv:68.0) Gecko/20100101 Firefox/68.0

Accept: text/html,application/xhtml+xml,application/xml;q=0.9,*/*;q=0.8

Accept-Language: en-US,en;q=0.5

Accept-Encoding: gzip, deflate, br

Connection: keep-alive

Upgrade-Insecure-Requests: 1

Pragma: no-cache

Cache-Control: no-cache

  

HTTP/1.1 200 OK

Date: Fri, 23 Aug 2019 15:56:36 GMT

Server: Apache/2.4.29 (Ubuntu)

Last-Modified: Mon, 12 Aug 2019 16:50:05 GMT

ETag: "5ff-58fee50dc3fb0-gzip"

Accept-Ranges: bytes

Vary: Accept-Encoding

Content-Encoding: gzip

Pico-Flag: picoCTF{nongshim.shrimp.crackers}

Content-Length: 821

Keep-Alive: timeout=5, max=100

Connection: Keep-Alive

Content-Type: text/html

  

<!doctype html>

<html lang="en">

<head>

<!-- Required meta tags -->

<meta charset="utf-8">

<meta name="viewport" content="width=device-width, initial-scale=1, shrink-to-fit=no">

  

<!-- Bootstrap CSS -->

<link rel="stylesheet" href="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/css/bootstrap.min.css" integrity="sha384-ggOyR0iXCbMQv3Xipma34MD+dH/1fQ784/j6cY/iJTQUOhcWr7x9JvoRxT2MZw1T" crossorigin="anonymous">

<!-- Custom styles for this template -->

<link href="starter-template.css" rel="stylesheet">

  

<title>Hello, world!</title>

</head>

<body>

<div class="container">

<div class="starter-template">

<h1>Welcome to A Sample Page</h1>

<p class="lead">

There is legit nothing to see here.<br>

</p>

</div>

</div><!-- /.container -->

  

<!-- Optional JavaScript -->

<!-- jQuery first, then Popper.js, then Bootstrap JS -->

<script src="https://code.jquery.com/jquery-3.3.1.slim.min.js" integrity="sha384-q8i/X+965DzO0rT7abK41JStQIAqVgRVzpbzo5smXKp4YfRvH+8abtTE1Pi6jizo" crossorigin="anonymous"></script>

<script src="https://cdnjs.cloudflare.com/ajax/libs/popper.js/1.14.7/umd/popper.min.js" integrity="sha384-UO2eT0CpHqdSJQ6hJty5KVphtPhzWj9WO1clHTMGa3JDZwrnQq4sF86dIHNDz0W1" crossorigin="anonymous"></script>

<script src="https://stackpath.bootstrapcdn.com/bootstrap/4.3.1/js/bootstrap.min.js" integrity="sha384-JjSmVgyd0p3pXB1rRibZUAYoIIy6OrQ6VrjIEaFf/nJGzIxFDsf4x0xIM+B07jRM" crossorigin="anonymous"></script>

</body>

</html>
```
## Notas Adicionales 

### Referencias
