## Objetivo 

Download this image and find the flag.

- [Download image](https://artifacts.picoctf.net/c/216/pico.flag.png)

## Solución  
```java
┌──(kali㉿kali)-[~/Downloads/St3go]
└─$ wget https://artifacts.picoctf.net/c/216/pico.flag.png                                                
--2024-10-27 05:29:24--  https://artifacts.picoctf.net/c/216/pico.flag.png
Resolving artifacts.picoctf.net (artifacts.picoctf.net)... 3.161.55.61, 3.161.55.64, 3.161.55.100, ...
Connecting to artifacts.picoctf.net (artifacts.picoctf.net)|3.161.55.61|:443... connected.
HTTP request sent, awaiting response... 200 OK
Length: 13441 (13K) [application/octet-stream]
Saving to: ‘pico.flag.png’

pico.flag.png                100%[==============================================>]  13.13K  --.-KB/s    in 0.002s  

2024-10-27 05:29:25 (7.26 MB/s) - ‘pico.flag.png’ saved [13441/13441]

                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/St3go]
└─$ ls
pico.flag.png
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/St3go]
└─$ eog pico.flag.png                                          
                                                                                                                    
┌──(kali㉿kali)-[~/Downloads/St3go]
└─$ zsteg -a pico.flag.png | grep pico
b1,rgb,lsb,xy       .. text: "picoCTF{7h3r3_15_n0_5p00n_a1062667}$t3g0"
/var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s': stack level too deep (SystemStackError)
        from /var/lib/gems/3.1.0/gems/iostruct-0.1.3/lib/iostruct.rb:159:in `inspect'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.1.0/gems/iostruct-0.1.3/lib/iostruct.rb:159:in `inspect'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.1.0/gems/iostruct-0.1.3/lib/iostruct.rb:159:in `inspect'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
        from /var/lib/gems/3.1.0/gems/iostruct-0.1.3/lib/iostruct.rb:159:in `inspect'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg/checker/wbstego.rb:41:in `to_s'
         ... 10066 levels...
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/lib/zsteg.rb:26:in `run'
        from /var/lib/gems/3.1.0/gems/zsteg-0.2.13/bin/zsteg:8:in `<top (required)>'
        from /usr/local/bin/zsteg:25:in `load'
        from /usr/local/bin/zsteg:25:in `<main>'
```


picoCTF{7h3r3_15_n0_5p00n_a1062667}
## Notas Adicionales 

### Referencias
