## Objetivo 
Can you find the flag in [file](https://jupiter.challenges.picoctf.org/static/5bd86036f013ac3b9c958499adf3e2e2/strings) without running it?
## Solución  


```bash


.symtab
.strtab
.shstrtab
.interp
.note.ABI-tag
.note.gnu.build-id
.gnu.hash
.dynsym
.dynstr
.gnu.version
.gnu.version_r
.rela.dyn
.rela.plt
.init
.plt.got
.text
.fini
.rodata
.eh_frame_hdr
.eh_frame
.init_array
.fini_array
.dynamic
.data
.bss
.comment
biank-picoctf@webshell:~$ strings strings | grep "picoCTF"
picoCTF{5tRIng5_1T_827aee91}
biank-picoctf@webshell:~$ 


```
## Notas Adicionales 

**strings** - permite obtener las cadenas de texto que hay en un archivo binario.

### Referencias
