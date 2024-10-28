## Objetivo 
The developer of this website mistakenly left an important artifact in the website source, can you find it?

Additional details will be available after launching your challenge instance.

## Solución  
```JAVA 
┌──(kali㉿kali)-[~/Downloads/SegundoExamenParcial/searchsource]
└─$ httrack http://saturn.picoctf.net:54372/
Mirror launched on Sun, 27 Oct 2024 00:59:38 by HTTrack Website Copier/3.49-5 [XR&CO'2014]
mirroring http://saturn.picoctf.net:54372/ with the wizard help..
* saturn.picoctf.net:54372/js/bootstrap.bundle.min.js (70808 bytes) - * saturn.picoctf.net:54372/js/jquery.mCustomScrollbar.concat.min.js (43/24: saturn.picoctf.net:54372/css/bootstrap.min.css (140421 bytes) - 4/24: saturn.picoctf.net:54372/css/owl.carousel.min.css (3351 bytes) -21/26: saturn.picoctf.net:54372/js/jquery.mCustomScrollbar.concat.min.23/26: saturn.picoctf.net:54372/images/maps-and-flags.png (153 bytes) 24/26: saturn.picoctf.net:54372/css/owl.video.play.png (153 bytes) - 4Done.: saturn.picoctf.net:54372/images/fevicon.png (153 bytes) - 404
Thanks for using HTTrack!
                                                                      
┌──(kali㉿kali)-[~/Downloads/SegundoExamenParcial/searchsource]
└─$ grep -nr picoCTF                        
saturn.picoctf.net_54372/css/style.css:328:/** banner_main picoCTF{1nsp3ti0n_0f_w3bpag3s_ec95fa49} **/
                                                                     
```

## Notas Adicionales 

resuelto por: Bianca 7A

### Referencias
