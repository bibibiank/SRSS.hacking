
## Objetivo 
Can you get the flag?Download this [binary](https://artifacts.picoctf.net/c/86/gdbme).Here's the test drive instructions:

- `$ chmod +x gdbme`
- `$ gdb gdbme`
- `(gdb) layout asm`
- `(gdb) break *(main+99)`
- `(gdb) run`
- `(gdb) jump *(main+104)`

## Solución  

```java 

──(kali㉿kali)-[~/Downloads/GDBtestDrive]
└─$ gdb -q gdbme                
Reading symbols from gdbme...
(No debugging symbols found in gdbme)
(gdb) layout asm
Undefined command: "layout".  Try "help".
(gdb) info functions 
All defined functions:

Non-debugging symbols:
0x0000000000001000  _init
0x00000000000010a0  __cxa_finalize@plt
0x00000000000010b0  free@plt
0x00000000000010c0  putchar@plt
0x00000000000010d0  strlen@plt
0x00000000000010e0  __stack_chk_fail@plt
0x00000000000010f0  fputs@plt
0x0000000000001100  strdup@plt
0x0000000000001110  sleep@plt
0x0000000000001120  _start
0x0000000000001150  deregister_tm_clones
0x0000000000001180  register_tm_clones
0x00000000000011c0  __do_global_dtors_aux
0x0000000000001200  frame_dummy
0x0000000000001209  rotate_encrypt
0x00000000000012c7  main
0x0000000000001390  __libc_csu_init
0x0000000000001400  __libc_csu_fini
0x0000000000001408  _fini
(gdb) layout asm 
Undefined command: "layout".  Try "help".
(gdb) break  *(main+99)
Breakpoint 1 at 0x132a
(gdb) info breakpoints 
Num     Type           Disp Enb Address            What
1       breakpoint     keep y   0x000000000000132a <main+99>
(gdb) delete 1
(gdb) delete 2
No breakpoint number 2.
(gdb) i b
No breakpoints, watchpoints, tracepoints, or catchpoints.
(gdb) break  *(main+99)
Breakpoint 2 at 0x132a
(gdb) i b
Num     Type           Disp Enb Address            What
2       breakpoint     keep y   0x000000000000132a <main+99>
(gdb) 




```



```java 
(gdb) i b
Num     Type           Disp Enb Address            What
2       breakpoint     keep y   0x000000000000132a <main+99>
(gdb) run 
Starting program: /home/kali/Downloads/GDBtestDrive/gdbme 
[Thread debugging using libthread_db enabled]
Using host libthread_db library "/lib/x86_64-linux-gnu/libthread_db.so.1".

Breakpoint 2, 0x000055555555532a in main ()
(gdb) jump *(main+104)
Continuing at 0x55555555532f.
picoCTF{d3bugg3r_dr1v3_72bd8355}
[Inferior 1 (process 14353) exited normally]
(gdb) 











```

## Notas Adicionales 

### Referencias
