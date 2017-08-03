# LeSS

El día de hoy vengo a hablar del Less con el cual se empieza un futuro sin fin de oportunidades en el mundo, ¿por que digo esto? Bueno lo que pasa es que css es el único lenguaje de diseño que se usa de forma productiva (no quiero decir que no existan mas sino que es el mas fuerte y los otros no tiene ganas de alcanzarlo), entonces less es la manera como se le esta diciendo al mundo, oiga no le gusta css?, cree que le falta algo mas? Pues le tengo la solución, y es así como están saliendo varios lenguajes de mas alto nivel como less y SAS, esto es el equivalente a decir c como lenguaje madre y c++, c#, java entre otros que compilan sobre c, entonces en que compila less? Pues claro en css, y así entonces es como podemos decir que aparecerán muchos locos con ganas de crear su propio lenguaje y darle un vuelco a esta cosa, se mejora el diseño, se arregla problemas y se generan implementación cada vez mas rápidas.

¿Como usar less?

Bueno primero que todo, cuando se requeire aprender una nueva tecnología y mas una como estas que casi no tiene mucho acogida y menos documentación en web se requiere estar a el tanto de las paginas promotores de que todo esto sea posible, http://lesscss.org/ en esta pagina encontraran mucha información sobre que es less, que se esta haciendo entre otros.

¿Que se requiere para trabajar less?

Existen dos formas para trabajar less, la primera de ellas es usando una librería bastante interesante que han realizado para trabajar less directamente en nuestras paginas web que es less.js, esta es diseñada en javascript y el papel que cumple es compilar el css en nuestra aplicación, pagina o entorno web de forma productivas; la segunda es el desarrollo de less de una manera mas de programación, y ustedes dirán, ¿pero que es el cuento de la programación?, bueno resulta que existe varias herramientas que veremos ahora, para que cuando se tenga código less realizado se compile y nos arroje un archivo .css, de esta manera se asemejo mucho a la forma de por ejemplo trabajar el lenguaje c.

En lo particular less.js para mi es una idea genial, pero que no tiene mucho tiempo en mercado y que aun le falta un poquito, además de esto para compatibilidad con los navegadores es algo complicado muchas veces, es por esto que yo sugiero, y no es palabra divina, utilizar less.js de manera productiva, ya que no tenemos que estar compilando sacando un nuevo archivo y después mirando, sino que en tiempo real y solo recargado la pagina veremos los cambios que se han realizado y como esta quedando nuestro diseño, Ojo, aunque los creadores dicen que se puede usar de manera productiva, y que si velocidad es bastante similar a hacerlo con css, para mi aun le falta un poco mas, pero que en un futuro con toda seguridad tendré que editar esta entrada y decir que si se podrá trabajar de manera productiva.

Entonces de aquí en adelante todo el tutorial va a ser desarrollado con less.js y utilizares los navegadores Mozilla y Safari para verificar lo que estamos haciendo, el uso de less con las herramientas de compilado va a ser motivo de otra entrada mas adelante.

¿Que se va a hacer en este tutorial?.

Desde la parte anterior de este tutorial, ya traíamos con nosotros un desarrollo bastante interesante de una pagina, la cual lo que realizar es una pequeña calculadora (que solo suma) y además de eso tiene implementado un diseño realizado propiamente con css, con el cual le hemos dados una estructurar muchos mas llamativa.

Sin embargo y aunque ustedes no lo crean, después de una semana de la entrada anterior y cuando decidí realizar esta entrada, vi el código y no recodaba muy bien que era lo que se había hecho, es mas, muchas veces no entendía ni para que se tenia eso hecho y ese es una de las mas usuales reacción a la hora programar, y que cuesta todos los días millones y millones de dólares, ya que el mantenimiento es una de las cosas mas preocupantes, entonces en este momento vamos a tratar de mostrar el potencial que tiene less cambiando la estructura de nuestro css y de esta manera dejar un código mucho mas limpio y adaptable en un futuro.

Usar less.

Primero que todo recuerden que ya tenemos hechos tres archivos de texto de las entradas anteriores el index.html y el loquesea.js y nuestro archivo anfitrión para esta entrada el estilo.css los cuales pueden descargar del repositorio de github.

A nuestro archivo estilo.css le vamos a cambiar la extensión a .less lo cual deja el archivo como estilo.less y es con el cual vamos a trabajar.

Descargar less

De la pagina oficial de less css nos descargamos el archivo less.js que en estos momentos se encuentra en la versión 1.3.0; cuando lo descarguemos este archivo tendrá el siguiente nombre  less-1.3.0.min.js les recomiendo que lo cambien por algo mas legible y fácil de escribir, yo lo cambiare por less.js y los guardamos en la carpeta donde tengamos el resto de nuestro archivos.

Conceptos Claves de LESS

Variables

Declaración de variables o cosas completas, como por ejemplo colores en hexadecimal usarlos como color (Tutorial)

Mixis

Generar funciones que puede evitar repetir código como por ejemplo los border-radius. (Tutorial)

Operaciones Matemáticas

Realizar operaciones sobre los atributos de css (Tutorial)

Variables.

Nombre: Variables
lenguaje: less.
compatibilidad:  firefox, safari.
Uso: Uno de los grandes y mas visibles pecados en css, es que no cuenta con variables algo que si se han dado cuenta y se usan diferentes colores hace muy complicado el trabajo.
Nota: todos los tributos de css que se utilicen como ayuda para la explicación de este, ya se han mencionado en entradas anteriores.
“Ahora con Less esto es mucho mas sencillo.”

 Si no tuviéramos less con nosotros y quisiéramos hacer un ejemplo sencillo de tres cuadrados en una pagina se haría de la siguiente manera.

Ejemplo1.1 (Implementación de Css)

index.html

1
2
3
4
5
6
7
8
9
10
11
12
13
<html>
 <head>
  <title>Ejemplo1</title>
  <link rel="stylesheet" type="text/css" href="estilo.css">
 </head>

 <body>
  <div class = "num1"></div>
  <div class = "num2"></div>
  <div class = "num3"></div>
 </body>

</html>
estilo.css

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
/*

Color

#ba12e2

*/

div{

border: solid;

margin:20px;

}

.num1{

 width: 200px;
 height: 400px;
 background: #ba12e2;

}

.num2{
 width: 400px;
 height: 200px;
 background: #ba12e2;
}

.num3{
 width: 300px;
 height: 300px;
 background: #ba12e2;
}
Ahora con less es mucho mas legible y entendible ya que con el uso de variables no tengo que aprender un numero en hexadecimal, sino que hago uso de las nemotecnias de tal manera que ele pueda poner un valor mas fácil de identificar.

Ejmplo1.2 (Implementación de Less)

Se declara una variable empezando con un @elnombrequesea y se iguala con lo que se desee guardar en la variables en este caso colores, después de esto se utiliza como un color normal en los atributos.

Index.html



1
2
3
4
5
6
7
8
9
10
11
12
13
<pre>
<html>
 <head>
  <title>Ejemplo1</title>
  <link rel="stylesheet" type="text/css" href="estilo.css">
</head>

 <body>
  <div class = "num1"></div>
  <div class = "num2"></div>
  <div class = "num3"></div>
 </body>
</html>
estilo.less

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
/*LESS*/

/*Variables*/

@color1:#ba12e2;

div{
 border: solid;
 margin:20px;
}

&nbsp;

.num1{
 width: 200px;
 height: 400px;
 background: @color1;
}

.num2{
 width: 400px;
 height: 200px;
 background: @color1;
}

.num3{
 width: 300px;
 height: 300px;
 background: @color1;
}

Mixins.

Nombre: Variables
lenguaje: less.
compatibilidad:  firefox, safari.
Uso: Los mixins son como lo que común mente usamos para hacer la reducción de código, se puede asemejar a una función pero tiene muchas restricciones lógica, aunque para el diseño web es algo muy potente y útil.
Nota: todos los tributos de css que se utilicen como ayuda para la explicación de este, ya se han mencionado en entradas anteriores.
Los mixins es como lo que común mente usamos para hacer la reducción de código, se puede asemejar a una función pero tiene muchas restricciones lógica, aunque para el diseño web es algo muy potente y útil.

Ahora vamos a mejorar el ejemplo anterior, y lo vamos a ver como quedaría en .css y en .less para mirar las diferencias existente y los ahorro de códigos, en el cual vamos a ponerle bordes redondos a los tres cuadrados que tenemos.

Ejemplo 2.1(Implementación de Css)

index.html

1
2
3
4
5
6
7
8
9
10
11
12
13
<html>
 <head>
  <title>hola mundo</title>
  <link rel="stylesheet" type="text/css" href="estilo.css">
 </head>

 <body>
  <div class = "num1"></div>
  <div class = "num2"></div>
  <div class = "num3"></div>
 </body>

</html>
estilos.css

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
/*

Color

#ba12e2

*/

div{
 border: solid;
 margin:20px;
}

.num1{

 width: 200px;
 height: 400px;
 background: #ba12e2;

 border-radius:10px;
 -webkit-border-radius:10px;
 -moz-border-radius:10px;
}

.num2{

 width: 400px;
 height: 200px;
 background: #ba12e2;

 border-radius:10px;
 -webkit-border-radius:10px;
 -moz-border-radius:10px;

}

.num3{

 width: 300px;
 height: 300px;
 background: #ba12e2;

 border-radius:10px;
 -webkit-border-radius:10px;
 -moz-border-radius:10px;

}
Ejemplo 2.2 (Implementación de Less)

Los bordes son un muy buen ejemplo por que gracias a la poca estandarización que tienes los navegadores par el uso de css, se deben generar diferentes bordes con relación a el tipo de navegador y esto se puede tornar monótono a la hora de escribir varias veces lo mismo, en less solo lo debemos realizar una vez e instanciarlo las veces que queramos en las etiquetas que queramos.

index.html

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
<html>
 <head>
  <title>hola mundo</title>
  <link rel="stylesheet/less" type="text/css" href="estilo.less">
  <script src = "less.js" type="text/javascript" ></script>
 </head>

 <body>

  <div class = "num1"></div>
  <div class = "num2"></div>
  <div class = "num3"></div>
 </body>

</html>
estilo.css

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
/*LESS*/

//------------------------- Variables -------------------------

@color1:#ba12e2;

//------------------------- Maxis -----------------------------

.esquinas-redondeadas(@radio : 5px){
 border-radius:@radio;
 -webkit-border-radius:@radio;
 -moz-border-radius:@radio;
}

div{
 border: solid;
 margin:20px;
}

.num1{

 width: 200px;
 height: 400px;
 background: @color1;
 .esquinas-redondeadas;
}

.num2{
 width: 400px;
 height: 200px;
 background: @color1;
 .esquinas-redondeadas(10px);
}

.num3{
 width: 300px;
 height: 300px;
 background: @color1;
 .esquinas-redondeadas(15px);
}
Si se dan cuenta creamos un bloque de código llamado, .esquinas-redondeadas(@radio : 5px) el cual le esta entrando una variable por parámetro que se explico anteriormente, esta se define como un efecto defaul, después de esto podemos hacer el llamado de este bloque de código en las tres etiquetas y mas aun se potencio aun mas y ahora le podemos pasar para parámetros el radio de las esquinas para no tener que hacer cambios y que sea mucho mas genérico.

Proyecto corriendo

Operaciones Matemáticas.

Nombre: Operaciones Matemáticas
lenguaje: less.
compatibilidad:  firefox, safari.
Uso: Las operaciones  son elementos que no usamos mucho por que nunca los hemos requerido, pero con ellos el diseño es mucho mas rápido, la codificación mas legible, y el diseño mas apropiado a lo que requerimos de la pagina..
Nota: todos los tributos de css que se utilicen como ayuda para la explicación de este, ya se han mencionado en entradas anteriores.
Vamos a mejorar los ejemplos que tenemos desde antes, los colores de nuestros cuadrados  pueden quedar mucho mas agradable si cambiamos los bordes y el color interior por colores mas vistosos y agradables. Para ellos le daremos tres colores, uno para cada etiqueta el cual esta en el borde y el fondo el mismo color pero mas claro.

Los colores que se utilizaran serán

1
2
3
#ba12e2
#a2e212
#123ae2
Los colores claros serán

1
2
3
#dc76f4
#bff14f
#4f6ff1
En css debemos ponerle a cada fondo un color claro y en borde un color oscuro, para lograr el objetivo, pero esto hace repetitivo y desgastante ya que primero se debe usar colores en hexadecimal y segundo usar también colores claros.

Ejemplo 3.1 (Implementación de Css)

Index.html

1
2
3
4
5
6
7
8
9
10
11
12
13
<html>
<head>
    <title>hola mundo</title>
    <link rel="stylesheet" type="text/css" href="estilo.css">
    <script src = "less.js" type="text/javascript" ></script>
</head>

<body>
    <div class = "num1"></div>
    <div class = "num2"></div>
    <div class = "num3"></div>
</body>
</html>
Estilo.css

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
45
46
47
48
49
50
51
52
53
/*
    Color
    #ba12e2
    #a2e212
    #123ae2

    Color claro.
    #dc76f4
    #bff14f
    #4f6ff1

*/
div{
    border: solid;
    margin:20px;
}

.num1{
    width: 200px;
    height: 400px;

    background: #dc76f4;
    color:#ba12e2;

    border-radius:10px;
    -webkit-border-radius:10px;
    -moz-border-radius:10px;

}

.num2{
    width: 400px;
    height: 200px;
    background: #bff14f;
    color:#a2e212;

    border-radius:10px;
    -webkit-border-radius:10px;
    -moz-border-radius:10px;

}

.num3{
    width: 300px;
    height: 300px;
    background: #4f6ff1;
    color:#123ae2;

    border-radius:10px;
    -webkit-border-radius:10px;
    -moz-border-radius:10px;

}
Mientras tanto si se usa less,  no se deben usar 6 colores ya que con las operaciones matemáticas podemos disminuir o aumentar los colores, además de eso, el uso de variables hace mucho mas eficiente el trabajo.

Cunado se realizan operación sobre colores, las multiplicaciones y sumas oscurecen los colores y cuando se divide y resta se aclaran.

Ejemplo 3.2 (Implementación de Less)

Index.html

1
2
3
4
5
6
7
8
9
10
11
12
13
<html>
<head>
    <title>hola mundo</title>
    <link rel="stylesheet/less" type="text/css" href="estilo.less">
    <script src = "less.js" type="text/javascript" ></script>
</head>

<body>
    <div class = "num1"></div>
    <div class = "num2"></div>
    <div class = "num3"></div>
</body>
</html>
Estilo.less

1
2
3
4
5
6
7
8
9
10
11
12
13
14
15
16
17
18
19
20
21
22
23
24
25
26
27
28
29
30
31
32
33
34
35
36
37
38
39
40
41
42
43
44
/*LESS*/

//------------------------- Variables -------------------------

@color1:#ba12e2;
@color2:#a2e212;
@color3:#123ae2;

//------------------------- Maxis -----------------------------

.esquinas-redondeadas(@radio : 5px){
    border-radius:@radio;
    -webkit-border-radius:@radio;
    -moz-border-radius:@radio;
}

div{
    border: solid;
    margin:20px;
}

.num1{
    width: 200px;
    height: 400px;
    background: @color1/0.2;
    color: @color1;
    .esquinas-redondeadas;
}

.num2{
    width: 400px;
    height: 200px;
    background: @color2/0.2;
    color: @color2;
    .esquinas-redondeadas(10px);
}

.num3{
    width: 300px;
    height: 300px;
    background: @color3/0.2;
    color: @color3;
    .esquinas-redondeadas(15px);
}
