
## Objetivo 

Someone might have hidden the password in the trace file. Find the key to unlock [this file](https://artifacts.picoctf.net/c/492/flag.zip). [This tracefile](https://artifacts.picoctf.net/c/492/dump.pcap) might be good to analyze.

## Solución  
```java 
┌──(kali㉿kali)-[~/Downloads/findAndOpen]
└─$ ls            
dump.pcap  flag.zip

┌──(kali㉿kali)-[~/Downloads/findAndOpen]
└─$ file dump.pcap
dump.pcap: pcap capture file, microsecond ts (little-endian) - version 2.4 (Ethernet, capture length 262144)

┌──(kali㉿kali)-[~/Downloads/findAndOpen]
└─$ file flag.zip 
flag.zip: Zip archive data, at least v1.0 to extract, compression method=store
```

hacemos un wireshark

```java
┌──(kali㉿kali)-[~/Downloads/findAndOpen]
└─$ wireshark dump.pcap &
[1] 42394

┌──(kali㉿kali)-[~/Downloads/findAndOpen]
└─$ Warning: program compiled against libxml 212 using older 209
```

seguimos el TCP stream y encontramos:

```java
iBwaWNvQ1RGe1CouAABBHHPJGTFRLKVGhpcyBpcyB0aGUgc2VjcmV0OiBwaWNvQ1RGe1IzNERJTkdfTE9LZF8=PBwaWUvQ1RGesabababkjaASKBKSBACVVAVSDDSSSSDSKJBJSPBwaWUvQ1RGe1May

```

Desencriptamos el código que encontramos, y nos dará la contraseña para descomprimir el archivo flag

```java 
picoCTF{R34DING_LOKd_
```

hemos conseguido la bandera

```java
┌──(kali㉿kali)-[~/Downloads/FindAndOpen]
└─$ unzip -p flag.zip     
[flag.zip] flag password: 
picoCTF{R34DING_LOKd_fil56_succ3ss_cbf2ebf6}
```
## Notas Adicionales 

### Referencias

