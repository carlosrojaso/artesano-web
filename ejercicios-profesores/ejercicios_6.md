* Crear un gradiente lineal

````html
<!DOCTYPE html>
<html>
<head>
<style>
#grad1 {
    height: 200px;
    background: red; /* For browsers that do not support gradients */
    background: -webkit-linear-gradient(red, yellow); /* For Safari 5.1 to 6.0 */
    background: -o-linear-gradient(red, yellow); /* For Opera 11.1 to 12.0 */
    background: -moz-linear-gradient(red, yellow); /* For Firefox 3.6 to 15 */
    background: linear-gradient(red, yellow); /* Standard syntax (must be last) */
}
</style>
</head>
<body>

<h3>Gradiente Lineal</h3>

<div id="grad1"></div>

</body>
</html>

````

* Crear un gradiente con transparencia.

````html

<!DOCTYPE html>
<html>
<head>
<style>
#grad1 {
    height: 200px;
    background: -webkit-linear-gradient(left, rgba(255,0,0,0), rgba(255,0,0,1)); /* For Safari 5.1 to 6.0 */
    background: -o-linear-gradient(right, rgba(255,0,0,0), rgba(255,0,0,1)); /* For Opera 11.1 to 12.0 */
    background: -moz-linear-gradient(right, rgba(255,0,0,0), rgba(255,0,0,1)); /* For Firefox 3.6 to 15 */
    background: linear-gradient(to right, rgba(255,0,0,0), rgba(255,0,0,1)); /* Standard syntax (must be last) */
}
</style>
</head>
<body>

<h3>Gradiente con transparencia</h3>

<div id="grad1"></div>

</body>
</html>

````

* Crear un ejemplo rotando un elemento.

````html

<!DOCTYPE html>
<html>
<head>
<style>
div {
    width: 200px;
    height: 100px;
    background-color: yellow;
    /* Rotate div */
    -ms-transform: rotate(7deg); /* IE 9 */
    -webkit-transform: rotate(7deg); /* Chrome, Safari, Opera */
    transform: rotate(7deg);
}
</style>
</head>
<body>

<div>Hola</div>
<br>

</body>
</html>

````

* Crear un ejemplo de una animación.

````html

<!DOCTYPE html>
<html>
<head>
<style>
div {
    width: 100px;
    height: 100px;
    position: relative;
    background-color: red;
    animation-name: example;
    animation-duration: 2s;
}

@keyframes example {
    0%   {background-color: red; left:0px;}
    50%  {background-color: yellow; left:200px;}
    100% {background-color: red; left:0px;}
}
</style>
</head>
<body>

<div></div>

</body>
</html>

````
* Crear un sitio con media queries.

````html

<!DOCTYPE html>
<html>
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<style>
* {
    box-sizing: border-box;
}
.row::after {
    content: "";
    clear: both;
    display: block;
}
[class*="col-"] {
    float: left;
    padding: 15px;
}
html {
    font-family: "Lucida Sans", sans-serif;
}
.header {
    background-color: #9933cc;
    color: #ffffff;
    padding: 15px;
}
.menu ul {
    list-style-type: none;
    margin: 0;
    padding: 0;
}
.menu li {
    padding: 8px;
    margin-bottom: 7px;
    background-color :#33b5e5;
    color: #ffffff;
    box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
}
.menu li:hover {
    background-color: #0099cc;
}
.aside {
    background-color: #33b5e5;
    padding: 15px;
    color: #ffffff;
    text-align: center;
    font-size: 14px;
    box-shadow: 0 1px 3px rgba(0,0,0,0.12), 0 1px 2px rgba(0,0,0,0.24);
}
.footer {
    background-color: #0099cc;
    color: #ffffff;
    text-align: center;
    font-size: 12px;
    padding: 15px;
}
/* For mobile phones: */
[class*="col-"] {
    width: 100%;
}
@media only screen and (min-width: 600px) {
    /* For tablets: */
    .col-m-1 {width: 8.33%;}
    .col-m-2 {width: 16.66%;}
    .col-m-3 {width: 25%;}
    .col-m-4 {width: 33.33%;}
    .col-m-5 {width: 41.66%;}
    .col-m-6 {width: 50%;}
    .col-m-7 {width: 58.33%;}
    .col-m-8 {width: 66.66%;}
    .col-m-9 {width: 75%;}
    .col-m-10 {width: 83.33%;}
    .col-m-11 {width: 91.66%;}
    .col-m-12 {width: 100%;}
}
@media only screen and (min-width: 768px) {
    /* For desktop: */
    .col-1 {width: 8.33%;}
    .col-2 {width: 16.66%;}
    .col-3 {width: 25%;}
    .col-4 {width: 33.33%;}
    .col-5 {width: 41.66%;}
    .col-6 {width: 50%;}
    .col-7 {width: 58.33%;}
    .col-8 {width: 66.66%;}
    .col-9 {width: 75%;}
    .col-10 {width: 83.33%;}
    .col-11 {width: 91.66%;}
    .col-12 {width: 100%;}
}
</style>
</head>
<body>

<div class="header">
<h1>Coderhouse</h1>
</div>

<div class="row">
<div class="col-3 col-m-3 menu">
<ul>
<li>HTML</li>
<li>Javascript</li>
<li>CSS</li>
<li>Bootstrap</li>
</ul>
</div>

<div class="col-6 col-m-9">
<h1>Coderhouse</h1>
<p>Escuela de programación.</p>
</div>

<div class="col-3 col-m-12">
<div class="aside">
<h2>¿ Que ?</h2>
<p>Loren Ipsum.</p>
<h2>¿ Donde ?</h2>
<p>Loren Ipsum.</p>
<h2>¿ Como ?</h2>
<p>Loren Ipsum.</p>
</div>
</div>

</div>

<div class="footer">
<p>Pie de Pagina</p>
</div>

</body>
</html>

````
***Crear una cuenta en Github.com***

* Crear un repositorio en Github.com
* Clonar repositorio.
```
$ git clone https://github.com/USUARIO/REPOSITORIO
```
* Clonar repositorio utilizando la aplicación de Github
