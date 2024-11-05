## Objetivo 

## Solución  

```java 


                                                                                  
┌──(kali㉿kali)-[~/Downloads/WebNet0]
└─$ cd ..     
                                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ mkdir WebNet1
                                                                                                 
┌──(kali㉿kali)-[~/Downloads]
└─$ cd WebNet1 
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet1]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap'
--2024-10-09 13:16:35--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/capture.pcap
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 92525 (90K) [application/octet-stream]
Saving to: ‘capture.pcap’

capture.pcap             100%[===============================>]  90.36K   149KB/s    in 0.6s    

2024-10-09 13:16:44 (149 KB/s) - ‘capture.pcap’ saved [92525/92525]

                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet1]
└─$ wget 'https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key'
--2024-10-09 13:16:57--  https://jupiter.challenges.picoctf.org/static/fbf98e695555a2a48fe42c9a245de376/picopico.key
Resolving jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)... 3.131.60.8
Connecting to jupiter.challenges.picoctf.org (jupiter.challenges.picoctf.org)|3.131.60.8|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 1704 (1.7K) [application/octet-stream]
Saving to: ‘picopico.key’

picopico.key             100%[===============================>]   1.66K  --.-KB/s    in 0s      

2024-10-09 13:17:06 (33.2 MB/s) - ‘picopico.key’ saved [1704/1704]

                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet1]
└─$ wireshark capture.pcap  &
[2] 28838
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet1]
└─$ ls          
capture.pcap  favicon.ico  picopico.key  second.html  starter-template.css  vulture.jpg
                                                                                                 
┌──(kali㉿kali)-[~/Downloads/WebNet1]
└─$ cat vulture.jpg 
����JFIF���ExifMM▒J(;ZpicoCTF{honey.roasted.peanuts}��ICC_PROFILE
                                                                 lcmsmntrRGB XYZ �)9acspAPPL���-lcms
desc�^cprt\
           wtpthbkpt|rXYZ�gXYZ�bXYZ�rTRC�@gTRC�@bTRC�@descc2textFBXYZ ���-XYZ 3�XYZ o�8��XYZ b���▒�XYZ $����curv▒��ck
                    �?Q!�)�2▒;�FQw]�kpz���|�i�}���0����C






▒▒ )/'%'/9339GDG]]}��C






▒▒ )/'%'/9339GDG]]}���"��

���}!1AQa"q2��#B��R��$3br�
▒▒%&'()*456789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz���������������������������������������������������������������������������

���w!1AQaq"2B����       #3R�br�
$4�%�▒▒&'()*56789:CDEFGHIJSTUVWXYZcdefghijstuvwxyz��������������������������������������������������������������������������
                           ?����m�A�~=�@�w�#�f�6J}�f����KE���S�i�b��M���M��6ԔP"=�m�(������.�i�P&�G���%\�=�m�(����6ԔQq�
sN���-�O���`Q�ZVE]      �iԘ��.��iB��9�.�m_JZuz
6�U:�f�6�ڟHh�����K{����&ږ���G���%#�Fڒ�G����mJ(��Ѷ�����1�i6���F}�*�h_�sK��K�j3�@��ҫ�Rm��PK�f�F�QO��^�F��S�F(
*��4ݧҟE���F������b`v�W'�>�`3m�▒}Xm��h��>�f���6/�>�3@"Q��n��ڕ�%R*�#�?�F��ڒ�c#��(��*J(=��¤��$�&�"��\��4�BiԀ.(���4�P�BQK�E�(����(��(��+�-���&))أ�)أ����PR��P;R‷��R��▒�aK�M�PPQE(4����C���qKE▒���Q(4��%QL�(�V�(�S�
(�4��(�A�1E
ǥ%Q�Q�(��(������:�@��(�ES��)X�(�`▒y�Ԕ��4Ɲ���4�4��ih��Ɲ(���ޔ
                                                           S�����Q@Y(�-�
(��X(��▒0��)\���Z.0�▒��w�hLQ�-�Nh斊�Nh斊�J:R�▒  a�))$�8�f`}j[f���}4��.��؉��5"���3IH��hӤ5A�xܝ�▒�P�D�h�CN�tecTqKU��7r��ѓVю�<PV\�iH=i����-%-N�����@Y       ���@Y   ���@Y   �����
JZ($LQ�Z(�R�E�m▒��▒%QL▒Rcޖ�
��LQ�u%�1KEl(���wb�b�њm����XQE�(��c
(��
�Pcޗ�P(��M��`�(�)-@aL��>P{�QQ��٦�$�K��R���[�Q��/�@�Fj=Ի�d�&�i��ȥ�p$�EG�R����J7S
                                                                               {�wQfU�6i3L
.E!���34���ъLѺ�
�ZJL�g$

ɯ{s��5�Z�rc"��tW�M���o"Tӣ��IV?0?M����Xү����%���u�Q^?��#���-g����0H▒;u3�9��F�����e�U�ӱ�S����|ۋ�� el�j����{�������v�D�▒���(�ͻC��>�E�R�ZkBT%$z}���7S3��▒f�a�V>��. 03�ݫc�s�cK<N�K��ɲU=k_J�#�Y$@K.GE+yՒ���3V�aRJ�FE5��nm� ��.�`�w'E�0�⨋�I���6x����4�N6=&9d&6��jJ��K��4$���/�]%z�j������Z�����>ԣ�B+cϵ��������4�PEPR�b�
             �JN�QN�%   EPIK��3]G�����*12��T�z�5�)M7�JZW]�gk������W3bQE\V
0v��;�6�IAih]�)7UM���&��e��R��[�/��X������Z���M�փ�x2␲�-����0�ox�K�T��F��I�������5G��N�V▒V.��n�^m.�z,��o�{���N(��Z/�7w+��带�<sI�,T��x��OX��Z�1s�);���������QG��";8z��WO�L�Լc��З���X�ZǸ����b�LPlޣ.�zW�*\խ�}�
        :8H�����m&�kƹ�bۉ
                        �����
jD�� �+���Z����ܩ�����W|0��⩘Nk�H�r�      �p��U�:��5
                                  Ʋ�%�ˎq�Z<�u��I|�ȿ)�;��)�b"ݼ�K3d���{V�������G(����oµP��#˯���R��m-��E}n[p�-�j�Ԟݣ�9a�@�l��x׍|5jY�m��ףc
                                    [�U���2�ir�Ґ!��"Q�׭r�!�uy��y�]�p�PVϙ
                                                                        !��"�g�Fڌ������
                                                                                       �S
��{q!\2�y���^c�S��lJ�6kƯ��Q>�}�3[C�n�o▒�<פ���B���f�i&;vڤ�t5�`)N�.Ytg���Ns\��њ�q�q�IGM�|�F�������c�c"�"���q���E��2*��M�r����iA�o�y���.Z�MȪ����޵/A���*�$⫛��?�c��4.��       ��+:�J�����X{x�����4�Dg�3�@�}�4q��▒����m-n"�7����)�/AX���}k0�2�Ƀ�5JWW:h�R���Iyl�O�q�c�+
h��0j
     4�N@>�W�|@������D����▒�b   ��J���W�x���$:yC����u��)I�m�kIh}7/����;+k�����vS�]�A��=��<F,�D�i1�Ǩ�J��V�5���I+���*)�敬o��Ҡ�EX��z�AR���|���Z1I���ЅaqIE�'�Q(�������z3M+�SM$`�l}�"q�i�v$-L-������V
                                                                                               �y��y�ƒ�X��
         �w�Q��P/o�4=R�����@X����GΣ�4   �^w�T��U���ށ;{�j�:!=?��`���[��4�8=�A0��E��Jx�4��2�u���w���������<���Q��F��F��=��o�b��V�ﴂ:▒v*7��GjO;��i
                          �:ԉpz������Z���5/�O��4���N��fy�������A/=i�L��Y"oz�&�p*YI-<����$ז�"=��$LR�Ԟ\��L��im��s��+:��Ӭ�ƀ�▒$����0�U�.z�5�▒���UUNg��Z����{��@E
]/A��K<)gisp\�;dG�իO]]�,g�TB�5���-���֍
                                      1�n��X�5����NT�sǼ+�"%x�|E�/�-c(>��F�ce�ZCeal�[��D▒Ϲ�cN�j�U���g�@?��G�?�%or�i-3 ���Ƥ��j��1&��$���/�>�y����6�X���a���2�6�4<��I���6����F��}iC����6������io�����3ޗ���&h��0Hݽ5Ad�˗e�9<FǊƴ�)��y�w1o.�2��Goz����z�޹f�#�9g�`�ƣ%�)��$��#��y����v�"R�&����|���n�      p��r�l�ҨG▒��kTs��+��5
                    ���V�$?1<c�WC�x��`��Y�_z��7%����j����yB�`���O▒�UV�;Tr����l����wT����I��J($�犯�YG�Os�-��2"Y��|��ב\Ί��vg�_�a�KC�"�F�����I��WRZ/C���?R�lR���^i��        }i���uV��}D��gw�.���Zpq�EE�z��ҋ �$��
           ����Lg�dL^���ޘd^I1�4�j�#�� ���8^�(��oz��fIp  �f���f��=�������}�ހ�7���I����?����}�g�r�|��Z_<Vځ�@�&�8��gޓ�5��.rs@a��K�t��?yy�ޣɤ����|��h��3#֌�ZkrGo�ҍ��L&��*���/�G�2�Թj���hZ�9��jn�\�Zx'i�C�Fi]�7�Ɯ%z�G4�SN�N%<b����B��
                             K,{�"�j�pn�!�°���TZ�g▒������>SQ*��p�oc���YI��t��j:xefr62��;�ff��7����j��2��ee�;��$��vg�ev��!���]NHLe��J��T&����`�����?
��@m�،��eP��
            w�0�qon�^M��|�W���B��Ǝ���V�v�Y▒�q����^զ)��l`?�� ��W��f{�oDR\<�.r��^���cҶ�狘%▒$�{�v���ڪ��ɭ��▒"ozp�޲�SHX��4
                    ��ǭF��^���HX��4��?�⏴VO�Gza�'�Q�KZ�zp�z���޴o>����6<��)�h�����5W]ʷ��'��<N1��l▒O1��-�m����y���A3*O0�ԧ��n��(�Y$P7�O��Y�:��NOB��8�qi�rI�w���x�Rմ�R�U���<2�W�|Pӵ
                                                                             kH��&�$ja*xS��k����-�D��U
�       kZe���\�^Z$��W#�>Ƹ���'~S��u&�b|Q��ۆh�)Q�Q��3⇈���q"�F:�㊧��\J�#���x�+��P>oC]t�I�*>��E�F�X�j��ɥ��u-��4���iy��K�e���<�LV6ă>�����.=�Q>{�#S��4M�G�}Ei���4���1�4�=��t�j6�=MQy�ޠy��
ry������X�v'4���j,Ԃ���EZ��>��g�!�i�r��A:�▒g������F                                 y�lUW�9���9�
                                                  z�x�E=h�IH
                                                            �Ҍ��i�i�c@����R�9�6�pPE;��WzRQڟHE;�Ȋ����m4�4\.3mZ6��
)@�(Ԙ�#�4��PG4�4�Z@)@�QE�A����tH'�+�T�DTV�ͼ���p�d�
��
   
   q^c/�#M^��]�k��w�aך�/�o�è���-���)�h�YN�0����V5�>Yla��M[��-դXq^��nv����U�1������h~`G���!�����2�6�����ss8�#��~δZq<�-
դ\Z����c5�C�[@Ib�0~U-��t�6_5�G�
                                ����m��-���r.
                                             ��qV禧t(B�ڊgU�/�I�Aw���X���vRƖ��sm�Q����M.#n-����u�x���?k�3��R%�-�5�2��9NsMZ�RfF�z��n��}&K��K���Ү�▒��V�oj��+�O▒��d�sz�.▒g��9*6�d�o�>�*�޳�J^h�B��.z��q����;Ӻ
      ▒�q��     �Q޳ޣ&BiscE��;���sU���cҥ����cޡrXsҞz�b��X�h��SmJpQE��K�RSh��Jy���a���▒w��Q@Xf(���nsb��F�I��� F�`j,��@h�����?�.�@杴���h\S���▒W�Q�&)p)h�n�S�4��ҝ��▒�@ R���F�Lb
           ������|U�A��sC=���uo+���j�hT>$|�t��5s��������\�Z�Һ[In���'�Z�֍>�ҔW�ߺw<��+�X��<_h�H'�¹T����kv5/t�F�T�<�
               &FW����}?K®���l����՜w▒F��D���r� ���k��/�E�����j��n��R>����5W{�;K�]a]���g�[����s#����I��O<>j�▒�����_�'ɹ�{t��+�I��T�����1�&���uq{�y���o�$�^�.���Dq�#��      �7����0M�鉝���'޷��Ǖ��g����ΐƩ�s�I���1M���8ta�á��EҒ�#����''$��?�{-�2Cgn��ʃ1)�Zބ�z�՛-��Q]W1�M��QL�ъ~(�G�\▒u�cC1K��F*y�������E�J)h�AE��&�:��*G�.k^��4�6���\H?�8���iN7gD��m
                                            ���ڼ�Q��zڒ���M��j�c�����gК1���==+��W��P��y��p▒�iI]3��~�;�H�,P>

```

## Notas Adicionales 

### Referencias
