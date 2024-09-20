## Objetivo 
The factory is hiding things from all of its users. Can you login as Joe and find what they've been looking at? `https://jupiter.challenges.picoctf.org/problem/13594/` ([link](https://jupiter.challenges.picoctf.org/problem/13594/)) or http://jupiter.challenges.picoctf.org:13594

## Solución  

```bash
- iniciar sesión con otro nombre de usuario y contraseña para poder entrar.
- Uzo la herramienta de cookie-editor y modificar False por "True" en el campo de admin.
- Refrescar la pagin y saldra la bandera.

```

**Flag**: `picoCTF{th3_c0nsp1r4cy_l1v3s_d1c24fef}`
## Notas Adicionales 

### Referencias

https://developer.mozilla.org/en-US/docs/Web/HTTP/Headers
https://developer.mozilla.org/en-US/docs/Glossary/Request_header
