## Objetivo 

There is some interesting information hidden around this site [http://mercury.picoctf.net:27278/](http://mercury.picoctf.net:27278/). Can you find it?

## Solución  

la primera parte de la flag la encontramos en el source del código
```java
  


||<!doctype html>|
||<html>|
||<head>|
||<title>Scavenger Hunt</title>|
||<link href="[https://fonts.googleapis.com/css?family=Open+Sans\|Roboto](https://fonts.googleapis.com/css?family=Open+Sans\|Roboto)" rel="stylesheet">|
||<link rel="stylesheet" type="text/css" href="[mycss.css](http://mercury.picoctf.net:27278/mycss.css)">|
||<script type="application/javascript" src="[myjs.js](http://mercury.picoctf.net:27278/myjs.js)"></script>|
||</head>|
|||
||<body>|
||<div class="container">|
||<header>|
||<h1>Just some boring HTML</h1>|
||</header>|
|||
||<button class="tablink" onclick="openTab('tabintro', this, '#222')" id="defaultOpen">How</button>|
||<button class="tablink" onclick="openTab('tababout', this, '#222')">What</button>|
|||
||<div id="tabintro" class="tabcontent">|
||<h3>How</h3>|
||<p>How do you like my website?</p>|
||</div>|
|||
||<div id="tababout" class="tabcontent">|
||<h3>What</h3>|
||<p>I used these to make this site: <br/>|
||HTML <br/>|
||CSS <br/>|
||JS (JavaScript)|
||</p>|
||<!-- Here's the first part of the flag: picoCTF{t -->|
||</div>|
|||
||</div>|
|||
||</body>|
||</html>|
||

```


en el mismo codigo nos da un archivo css, en ese encontramos la segunda parte de la bandera 
```java
div.container {
    width: 100%;
}

header {
    background-color: black;
    padding: 1em;
    color: white;
    clear: left;
    text-align: center;
}

body {
    font-family: Roboto;
}

h1 {
    color: white;
}

p {
    font-family: "Open Sans";
}

.tablink {
    background-color: #555;
    color: white;
    float: left;
    border: none;
    outline: none;
    cursor: pointer;
    padding: 14px 16px;
    font-size: 17px;
    width: 50%;
}

.tablink:hover {
    background-color: #777;
}

.tabcontent {
    color: #111;
    display: none;
    padding: 50px;
    text-align: center;
}

#tabintro { background-color: #ccc; }
#tababout { background-color: #ccc; }

CSS makes the page look nice, and yes, it also has part of the flag. Here's part 2: h4ts_4_l0 */


```


la tercera parte de la bandera está en el archivo robots.txt, lo añadimos al link y ahi la encontramos
view-source:mercury.picoctf.net:27278/robots.txt

```java 


|   |   |
|---|---|
||User-agent: *|
||Disallow: /index.html|
||# Part 3: t_0f_pl4c|
||# I think this is an apache server... can you Access the next flag?|
```

para la cuarta parte debemos entrar al fichero del servidor

```java 
http://mercury.picoctf.net:44070/.htaccess

# Part 4: 3s_2_lO0k
# I love making websites on my Mac, I can Store a lot of information there.
```



la quinta parte de la flag  se encuentra en el archivo de almacenamiento macOS
```java

http://mercury.picoctf.net:44070/.DS_Store

Congrats! You completed the scavenger hunt. Part 5: _a69684fd}

```

picoCTF{th4ts_4_l0t_0f_pl4c3s_2_lO0k_7a46d25d}
## Notas Adicionales 


### Referencias