
## Objetivo 
How about trying to match a regular expression

Additional details will be available after launching your challenge instance

## Solución 

Entramos al link, e inspeccionamos la página. Encontramos este codigo

```java 
<script>
	function send_request() {
		let val = document.getElementById("name").value;
		// ^p.....F!?
		fetch(`/flag?input=${val}`)
			.then(res => res.text())
			.then(res => {
				const res_json = JSON.parse(res);
				alert(res_json.flag)
				return false;
			})
		return false;
	}


```


Validar P.....F! en el recuadro, y dar submit




picoCTF{succ3ssfully_matchtheregex_f89ea585

![[{D5605CBF-6DED-4100-8E5B-B4A9468DA2C3}.png]]
## Notas Adicionales 

### Referencias
