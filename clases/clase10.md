# Introducción
​
Bootstrap es un framework desarrollado por Twitter que te permite maquetar una interfaz web con HTML, CSS y JavaScript. La pieza generada con dicha plataforma se adapta automáticamente dependiendo del tamaño del dispositivo en el que se visualice, es decir, se adapta al tamaño del navegador de una computadora de escritorio, un celular o una Tablet sin intervención del usuario. A esto se lo denomina diseño adaptable o Responsive Design.
​
Los diseños creados con Bootstrap son simples, limpios e intuitivos, esto ayuda en la velocidad en que carga la web.
​
El Framework cuenta con varios elementos y estilos predefinidos, los cuales pueden ser modificados de una manera muy simple: Botones, Menus desplegables, Formularios incluyendo todos sus elementos e integración jQuery para ofrecer ventanas y tooltips dinámicos.

# Instalar Bootstrap

Acceder a [http://getbootstrap.com/](http://getbootstrap.com/) y descargar el framework.

Te encontrarás con la siguiente estructura:

```
bootstrap/
    css/
        bootstrap.css
        bootstrap.min.css
        bootstrap-responsive.css
        bootstrap-responsive.min.css
    img/
        glyphicons-halflings-white.png
        glyphicons-halflings.png
    js/
        bootstrap.js
        bootstrap.min.js
```

Como verán, cada archivo se tiene dos variantes, los archivos compilados (bootstrap.*) y los archivos compilados y además comprimidos (bootstrap.min.*), agregándose la palabra “min” que hace referencia a “minificado”. También se incluyen dos imágenes con los iconos de Glyphicons en color blanco y color negro.

# Compatibilidad de Bootstrap

Nunca hay que pasar por alto la comprobación de si la tecnología que estamos aplicando es compatible con los navegadores más usados por los usuarios que visitarán nuestro sitio.

![](https://coderhouse.gitbooks.io/bootstrap/content/captura-6.png)

También suele funcionar correctamente en Chromium (Linux) e Internet Explorer 7, aunque no está información no está oficializada por el sitio web.

Los navegadores Internet Explorer 8 y 9 son soportados, algunas propiedades de CSS3 y tags de HTML5 que no funcionan como lo esperado. Además, Internet Explorer 8 requiere el uso de la librería respond.js para que el diseño web responsive funcione de manera adecuada.

![](https://coderhouse.gitbooks.io/bootstrap/content/captura-7.png)

# Utilizando Bootstrap

A continuación se visualiza un archivo html en donde se puede ver como se utilizan diferentes elementos con las propiedades que brinda Bootstrap.

<iframe height='268' scrolling='no' src='//codepen.io/team/coderhouse/embed/dYboyL/?height=268&theme-id=14781&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/team/coderhouse/pen/dYboyL/'>Bootstrap - 6.4</a> by Coderhouse (<a href='http://codepen.io/coderhouse'>@coderhouse</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

Deberíamos estar visualizando un sitio como este:

![](https://coderhouse.gitbooks.io/bootstrap/content/captura-5.png)

Para visualizar correctamente este archivo utilizando las clases de Bootstrap se debe respetar la siguiente estructura de directorios.

```
index.html
css/
    bootstrap.css
    bootstrap-responsive.css
js/
    	bootstrap.js
```

Ahora vamos a analizar cada uno de los elementos que son clave a la hora de utilizar y entender Bootstrap.

**Encabezado del documento**

```
<!DOCTYPE html>
<html lang="en">
  ...
</html>
```

**Viewport Tag**

Tag para que el sitio se adapte a los estilos responsivos, esencial para dispositivos móviles.

```
<meta name="viewport" content="width=device-width, initial-scale=1">
```

**Normalize.css**

Para mejorar el render que realizarán los navegadores de nuestro sitio web, es recomendable utilizar normalize.css, un proyecto de Nicolas Gallagher y Jonathan Neal.

Solo debemos incluir el archivo css que se encargará de resetear los estilos por defecto que tienen los navegadores, por ejemplo: ```body { margin: 0; }```

**Contenedores**

Bootstrap utiliza dos tipos de contenedores:

```
<div class="container">
  ...
</div>
.container
```

Tiene un ancho variable, que va a depender de la resolución de pantalla del usuario. Esto lo va averiguar bootstrap y va a setearle el ancho correspondiente. Por ejemplo, si el usuario utiliza una resolución de 1024x768, el ancho de ```.container``` va a ser de 970px de ancho.  

```
<div class="container-fluid">
 ...
</div>
```

En este caso, cuando el contendor es fluid, el ancho siempre será de 100%, brindándonos la posibilidad renderizar un div full width.

Una vez que tenemos el contenedor podemos, comenzamos a incluir el resto de los divs que utiliza el framework para lograr un sitio responsivo.

El siguiente div a utilizar son los ```.row```, que serán las filas en donde dividiermos el contenido el bloque que va a reacomodar los divs de su interior, haciendolos más angosotos o anchos dependiendo siempre de la resolución del usuario, lo que nos permitirá reorganizar el contenido de nuestro sitio colocando las cajas por encima o por debajo, dendiendo de los estilos que hayamos utilizado.

Dentro de los divs  ```.col-xx-xx``` se incluirán los divs que dividirán el contenido en columnas, para ser reorganizadas.

# Tipografía en Bootstrap

Todos los tags de ```<h1>``` a ```<h6>``` están estilados por Bootstrap. Como también se puede utilizar el tag ```<small>``` para mostrar un texto secundario:

<iframe height='268' scrolling='no' src='//codepen.io/team/coderhouse/embed/bVbddw/?height=268&theme-id=14781&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/team/coderhouse/pen/bVbddw/'>Bootstrap - 6.6.1</a> by Coderhouse (<a href='http://codepen.io/coderhouse'>@coderhouse</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

Otro ejemplo de estilo de texto puede ser para destacar un párrafo como en el siguiente ejemplo:

```
<p class="lead">...</p>
```

Ver más ejemplos de texto con estilo en [http://getbootstrap.com/css/#type](http://getbootstrap.com/css/#type)

# Sistema de grilla

Bootstrap se basa en un sistema de grilla pensada para dispositivos móviles que permite el diseño responsive.

La grilla se divide en 12 columnas, que varían su ancho dependiendo de la resolución del usuario móvil o de escritorio.

Estas columnas se ubican siempre dentro de una fila, el div .row mencionado anteriormente, y se representan con la clase .col-md-4, por ejemplo, para indicar que la columna ocupará 4 lugares en la grilla, por lo tanto la mitad de la pantalla. .col-md-x indica que el div ocupará 4 columnas en un .container de 970px de ancho (usuario con resolución menor a 992px de ancho, un celular por ejemplo). Si quisieramos que el mismo div ocupe 6 columnas en un dispositivo de 480px de ancho, deberíamos aplicarle dos clases al div para indicarle un comportamiento para cada resolución, como se visualiza en el siguiente ejemplo:

```
<div class="container">
   <div class="row">
     <div class="col-md-4 col-xs-6">columna izquierda</div>
   </div>
</div>
```

Se entenderá mejor con la siguiente imagen:

![](http://i.imgur.com/VHbdy3g.png)

Para generar las columnas de la imágen con código html utilizando las clases de Bootstrap se utilizó el siguiente código:

```
<div class="container">
  <div class="row">
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
  <div class="col-md-1">.col-md-1</div>
 </div>
 <div class="row">
  <div class="col-md-8">.col-md-8</div>
  <div class="col-md-4">.col-md-4</div>
 </div>
 <div class="row">
  <div class="col-md-4">.col-md-4</div>
  <div class="col-md-4">.col-md-4</div>
  <div class="col-md-4">.col-md-4</div>
 </div>
 <div class="row">
  <div class="col-md-6">.col-md-6</div>
  <div class="col-md-6">.col-md-6</div>
 </div>
</div>
```

La grilla puede ser de varios tamaños, como dijimos antes, esto va a depender de la resolución del usuario. A continuación les brindamos las medidas que utiliza el framework para reacomodar los divs con sus respectivas clases:

![](http://i.imgur.com/lZDjreR.png)

Poniendo en palabras lo que expresa la tabla de medidas de dispositivos:

Si utilizamos la clase ```col-xs-4``` en un div, los estilos de esta clase serán cargados solo si la resolución del usuarios es menos a 768px de ancho.

Al utilizar la clase ```col-sm-6```, obtendremos los estilos correspondientes solo si la resolución del dispositivo es mayor a 768px de ancho.

Esto quiere decir que podemos nombrar un div con dos clases diferentes, que proporcionarán distintos estilos al mismo elemento, pero eso no nos preocupará, ya que solo se cargarán los estilos que correspondan según el dispositvo que está renderizando la página en ese momento.

```
<div class="col-md-4 col-sm-6">
```

De esta manera logramos que el elemento ocupe distintas columnas de la grilla, dependiendo de la resolución del usuario, sin agregar o modificar el archivo de estilos, lo cual ahorra mucho tiempo a la hora del ajuste responsivo.

También se pueden ocupar algunas columnas de la grilla dejando un espacio libre a los costados. Para ello se utilizan las clases con offset: ```.col-md-offset-4```

![](http://i.imgur.com/aU94saL.png)

```
<div class="row">
  <div class="col-md-4">.col-md-4</div>
  <div class="col-md-4 col-md-offset-4">.col-md-4 .col-md-offset-4</div>
</div>
<div class="row">
  <div class="col-md-3 col-md-offset-3">.col-md-3 .col-md-offset-3</div>
  <div class="col-md-3 col-md-offset-3">.col-md-3 .col-md-offset-3</div>
</div>
<div class="row">
  <div class="col-md-6 col-md-offset-3">.col-md-6 .col-md-offset-3</div>
</div>
```

Explicando la imágen anterior, en la primer fila el div de la izquierda rellena 4 columnas del centro, en la segunda los dos divs rellenan las columnas del 1 al 3 y del 7 al 9, y en la tercer fila el div central ocupa 6 columnas, dejando el espacio 3 columnas vacías a su izquierda, y sin tener la necesidad de terminar de ocupar las 3 restantes.

# Tablas en Bootstrap

Entre otros elementos, las tablas también están estiladas por el framewoork como se ve en el siguiente ejemplo:

![](https://coderhouse.gitbooks.io/bootstrap/content/captura-13.png)

```
<table class="table table-striped">
  ...
</table>
```

Ver más estilos de tablas en [http://getbootstrap.com/css/#tables](http://getbootstrap.com/css/#tables)

# Formularios en Bootstrap

<iframe height='268' scrolling='no' src='//codepen.io/team/coderhouse/embed/doxQZR/?height=268&theme-id=14781&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/team/coderhouse/pen/doxQZR/'>Bootstrap - 6.8.1 - 1</a> by Coderhouse (<a href='http://codepen.io/coderhouse'>@coderhouse</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

<iframe height='268' scrolling='no' src='//codepen.io/team/coderhouse/embed/RPXqxx/?height=268&theme-id=14781&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/team/coderhouse/pen/RPXqxx/'>Bootstrap - 6.8.1 - 2</a> by Coderhouse (<a href='http://codepen.io/coderhouse'>@coderhouse</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

<iframe height='268' scrolling='no' src='//codepen.io/team/coderhouse/embed/QbeJao/?height=268&theme-id=14781&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/team/coderhouse/pen/QbeJao/'>Bootstrap - 6.8.1 - 3</a> by Coderhouse (<a href='http://codepen.io/coderhouse'>@coderhouse</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

<iframe height='268' scrolling='no' src='//codepen.io/team/coderhouse/embed/gpVQvz/?height=268&theme-id=14781&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/team/coderhouse/pen/gpVQvz/'>Bootstrap - 6.8.1 - 4</a> by Coderhouse (<a href='http://codepen.io/coderhouse'>@coderhouse</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

<iframe height='268' scrolling='no' src='//codepen.io/team/coderhouse/embed/NqQEye/?height=268&theme-id=14781&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/team/coderhouse/pen/NqQEye/'>Bootstrap - 6.8.1 - 5</a> by Coderhouse (<a href='http://codepen.io/coderhouse'>@coderhouse</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

<iframe height='268' scrolling='no' src='//codepen.io/team/coderhouse/embed/yNmQvm/?height=268&theme-id=14781&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/team/coderhouse/pen/yNmQvm/'>Bootstrap - 6.8.1 - 6</a> by Coderhouse (<a href='http://codepen.io/coderhouse'>@coderhouse</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

<iframe height='268' scrolling='no' src='//codepen.io/team/coderhouse/embed/rVXQdO/?height=268&theme-id=14781&default-tab=html' frameborder='no' allowtransparency='true' allowfullscreen='true' style='width: 100%;'>See the Pen <a href='http://codepen.io/team/coderhouse/pen/rVXQdO/'>Bootstrap - 6.8.1 - 7</a> by Coderhouse (<a href='http://codepen.io/coderhouse'>@coderhouse</a>) on <a href='http://codepen.io'>CodePen</a>.
</iframe>

## Imágenes responsive

![](https://coderhouse.gitbooks.io/bootstrap/content/captura-21.png)

```
<img src="..." alt="..." class="img-rounded">
<img src="..." alt="..." class="img-circle">
<img src="..." alt="..." class="img-thumbnail">
```

# Más información

Se le recomienda al alumno mantenerse actualizado acerca del framework que se está utilizando para evitar posibles problemas de visualización y optimización del código.

Ver más en  [http://getbootstrap.com/](http://getbootstrap.com/)

# Dropdowns
![](http://i.imgur.com/V5tNZ8y.jpg)
```
<div class="dropdown">
  <button class="btn btn-default dropdown-toggle" type="button" id="dropdownMenu1" data-toggle="dropdown" aria-haspopup="true"

aria-expanded="true">
    Dropdown
    <span class="caret"></span>
  </button>
  <ul class="dropdown-menu" aria-labelledby="dropdownMenu1">
    <li><a href="#">Action</a></li>
    <li><a href="#">Another action</a></li>
    <li><a href="#">Something else here</a></li>
    <li role="separator" class="divider"></li>
    <li><a href="#">Separated link</a></li>
  </ul>
</div>
```

# Headers
![](http://i.imgur.com/8wgX24t.jpg)
```
<ul class="dropdown-menu" aria-labelledby="dropdownMenu3">
  ...
  <li class="dropdown-header">Dropdown header</li>
  ...
</ul>
```

# Divider
![](http://i.imgur.com/LYDY0bj.jpg)
```
<ul class="dropdown-menu" aria-labelledby="dropdownMenuDivider">
  ...
  <li role="separator" class="divider"></li>
  ...
</ul>
```

# Disabled menu items
![](http://i.imgur.com/tAZvmQ4.jpg)
```
<ul class="dropdown-menu" aria-labelledby="dropdownMenu4">
  <li><a href="#">Regular link</a></li>
  <li class="disabled"><a href="#">Disabled link</a></li>
  <li><a href="#">Another link</a></li>
</ul>
```

# Button groups
![](http://i.imgur.com/ZHa5dAE.jpg)
```
<div class="btn-group" role="group" aria-label="...">
  <button type="button" class="btn btn-default">Left</button>
  <button type="button" class="btn btn-default">Middle</button>
  <button type="button" class="btn btn-default">Right</button>
</div>
```

# Button toolbar
![](http://i.imgur.com/AS0Tggh.jpg)
```
<div class="btn-toolbar" role="toolbar" aria-label="...">
  <div class="btn-group" role="group" aria-label="...">...</div>
  <div class="btn-group" role="group" aria-label="...">...</div>
  <div class="btn-group" role="group" aria-label="...">...</div>
</div>
```

# Sizing
![](http://i.imgur.com/Iojk8ci.jpg)
```
<div class="btn-group btn-group-lg" role="group" aria-label="...">...</div>
<div class="btn-group" role="group" aria-label="...">...</div>
<div class="btn-group btn-group-sm" role="group" aria-label="...">...</div>
<div class="btn-group btn-group-xs" role="group" aria-label="...">...</div>
```

# Nesting
![](http://i.imgur.com/IVnyQmG.jpg)
```
<div class="btn-group" role="group" aria-label="...">
  <button type="button" class="btn btn-default">1</button>
  <button type="button" class="btn btn-default">2</button>

  <div class="btn-group" role="group">
    <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
      Dropdown
      <span class="caret"></span>
    </button>
    <ul class="dropdown-menu">
      <li><a href="#">Dropdown link</a></li>
      <li><a href="#">Dropdown link</a></li>
    </ul>
  </div>
</div>
```

# Vertical variation
![](http://i.imgur.com/JtaTFJa.jpg)
```
<div class="btn-group-vertical" role="group" aria-label="...">
  ...
</div>
```

# Justified button group
![](http://i.imgur.com/mduKqdP.jpg)
```
<div class="btn-group btn-group-justified" role="group" aria-label="...">
  ...
</div>
```

# Single button dropwdown
![](http://i.imgur.com/XR3P4SC.jpg)
```
<!-- Single button -->
<div class="btn-group">
  <button type="button" class="btn btn-default dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    Action <span class="caret"></span>
  </button>
  <ul class="dropdown-menu">
    <li><a href="#">Action</a></li>
    <li><a href="#">Another action</a></li>
    <li><a href="#">Something else here</a></li>
    <li role="separator" class="divider"></li>
    <li><a href="#">Separated link</a></li>
  </ul>
</div>
```

# Split button dropdown
![](http://i.imgur.com/OaPWMgg.jpg)
```
<!-- Split button -->
<div class="btn-group">
  <button type="button" class="btn btn-danger">Action</button>
  <button type="button" class="btn btn-danger dropdown-toggle" data-toggle="dropdown" aria-haspopup="true" aria-expanded="false">
    <span class="caret"></span>
    <span class="sr-only">Toggle Dropdown</span>
  </button>
  <ul class="dropdown-menu">
    <li><a href="#">Action</a></li>
    <li><a href="#">Another action</a></li>
    <li><a href="#">Something else here</a></li>
    <li role="separator" class="divider"></li>
    <li><a href="#">Separated link</a></li>
  </ul>
</div>
```

# Input groups
![](http://i.imgur.com/nlhkvhy.jpg)
```
<div class="input-group">
  <span class="input-group-addon" id="basic-addon1">@</span>
  <input type="text" class="form-control" placeholder="Username" aria-describedby="basic-addon1">
</div>

<div class="input-group">
  <input type="text" class="form-control" placeholder="Recipient's username" aria-describedby="basic-addon2">
  <span class="input-group-addon" id="basic-addon2">@example.com</span>
</div>

<div class="input-group">
  <span class="input-group-addon">$</span>
  <input type="text" class="form-control" aria-label="Amount (to the nearest dollar)">
  <span class="input-group-addon">.00</span>
</div>

<label for="basic-url">Your vanity URL</label>
<div class="input-group">
  <span class="input-group-addon" id="basic-addon3">https://example.com/users/</span>
  <input type="text" class="form-control" id="basic-url" aria-describedby="basic-addon3">
</div>
```

# Nav tabs
![](http://i.imgur.com/8vH7xsH.jpg)
```
<ul class="nav nav-tabs">
  <li role="presentation" class="active"><a href="#">Home</a></li>
  <li role="presentation"><a href="#">Profile</a></li>
  <li role="presentation"><a href="#">Messages</a></li>
</ul>
```

# Nav pills
![](http://i.imgur.com/QqmlKzC.jpg)
```
<ul class="nav nav-pills">
  <li role="presentation" class="active"><a href="#">Home</a></li>
  <li role="presentation"><a href="#">Profile</a></li>
  <li role="presentation"><a href="#">Messages</a></li>
</ul>
```

# Nav justified
![](http://i.imgur.com/jF3YZPw.jpg)
```
<ul class="nav nav-tabs nav-justified">
  ...
</ul>
<ul class="nav nav-pills nav-justified">
  ...
</ul>
```

# Navbar default
![](http://i.imgur.com/O8Dl4il.jpg)

![](http://i.imgur.com/IUTgriT.jpg)
```
<nav class="navbar navbar-default">
  <div class="container-fluid">
    <!-- Brand and toggle get grouped for better mobile display -->
    <div class="navbar-header">
      <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
        <span class="sr-only">Toggle navigation</span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
        <span class="icon-bar"></span>
      </button>
      <a class="navbar-brand" href="#">Brand</a>
    </div>

    <!-- Collect the nav links, forms, and other content for toggling -->
    <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
      <ul class="nav navbar-nav">
        <li class="active"><a href="#">Link <span class="sr-only">(current)</span></a></li>
        <li><a href="#">Link</a></li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
          <ul class="dropdown-menu">
            <li><a href="#">Action</a></li>
            <li><a href="#">Another action</a></li>
            <li><a href="#">Something else here</a></li>
            <li role="separator" class="divider"></li>
            <li><a href="#">Separated link</a></li>
            <li role="separator" class="divider"></li>
            <li><a href="#">One more separated link</a></li>
          </ul>
        </li>
      </ul>
      <form class="navbar-form navbar-left" role="search">
        <div class="form-group">
          <input type="text" class="form-control" placeholder="Search">
        </div>
        <button type="submit" class="btn btn-default">Submit</button>
      </form>
      <ul class="nav navbar-nav navbar-right">
        <li><a href="#">Link</a></li>
        <li class="dropdown">
          <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Dropdown <span class="caret"></span></a>
          <ul class="dropdown-menu">
            <li><a href="#">Action</a></li>
            <li><a href="#">Another action</a></li>
            <li><a href="#">Something else here</a></li>
            <li role="separator" class="divider"></li>
            <li><a href="#">Separated link</a></li>
          </ul>
        </li>
      </ul>
    </div><!-- /.navbar-collapse -->
  </div><!-- /.container-fluid -->
</nav>
```

# Navbar brand image
![](http://i.imgur.com/YVZJdGu.jpg)
```
<nav class="navbar navbar-default">
  <div class="container-fluid">
    <div class="navbar-header">
      <a class="navbar-brand" href="#">
        <img alt="Brand" src="...">
      </a>
    </div>
  </div>
</nav>
```

# Navbar fixed to top
![](http://i.imgur.com/KVz6QcY.jpg)
![](http://i.imgur.com/DHJusht.jpg)
```
<nav class="navbar navbar-default navbar-fixed-top">
  <div class="container">
    ...
  </div>
</nav>
```

*Se requiere agregar ```padding``` al principio del ```<body>```. Por default la barra tiene 50px de alto.*
```
body { padding-top: 70px; }
```

# Navbar inverted
![](http://i.imgur.com/LL4W5tC.jpg)
```
<nav class="navbar navbar-inverse">
  ...
</nav>
```

# Breadcrumbs
![](http://i.imgur.com/szkjVNy.jpg)
```
<ol class="breadcrumb">
  <li><a href="#">Home</a></li>
  <li><a href="#">Library</a></li>
  <li class="active">Data</li>
</ol>
```

# Pagination
![](http://i.imgur.com/GC2biD3.jpg)
```
<nav>
  <ul class="pagination">
    <li>
      <a href="#" aria-label="Previous">
        <span aria-hidden="true">&laquo;</span>
      </a>
    </li>
    <li><a href="#">1</a></li>
    <li><a href="#">2</a></li>
    <li><a href="#">3</a></li>
    <li><a href="#">4</a></li>
    <li><a href="#">5</a></li>
    <li>
      <a href="#" aria-label="Next">
        <span aria-hidden="true">&raquo;</span>
      </a>
    </li>
  </ul>
</nav>
```

# Pagination disabled and active states
![](http://i.imgur.com/tq0TfHx.jpg)
```
<nav>
  <ul class="pagination">
    <li class="disabled"><a href="#" aria-label="Previous"><span aria-hidden="true">&laquo;</span></a></li>
    <li class="active"><a href="#">1 <span class="sr-only">(current)</span></a></li>
    ...
  </ul>
</nav>
```

# Badges
![](http://i.imgur.com/mEx4Tx3.jpg)
```
<a href="#">Inbox <span class="badge">42</span></a>

<button class="btn btn-primary" type="button">
  Messages <span class="badge">4</span>
</button>
```

# Jumbotron
![](http://i.imgur.com/3ykqJuy.jpg)
```
<div class="jumbotron">
  <h1>Hello, world!</h1>
  <p>...</p>
  <p><a class="btn btn-primary btn-lg" href="#" role="button">Learn more</a></p>
</div>
```

# Page header
![](http://i.imgur.com/T7unXQR.jpg)
```
<div class="page-header">
  <h1>Example page header <small>Subtext for header</small></h1>
</div>
```

# Thumbnails
![](http://i.imgur.com/TQ4ykEj.jpg)
```
<div class="row">
  <div class="col-xs-6 col-md-3">
    <a href="#" class="thumbnail">
      <img src="..." alt="...">
    </a>
  </div>
  ...
</div>
```

# Thumbnails custom
![](http://i.imgur.com/2FeW71q.jpg)
```
<div class="row">
  <div class="col-sm-6 col-md-4">
    <div class="thumbnail">
      <img src="..." alt="...">
      <div class="caption">
        <h3>Thumbnail label</h3>
        <p>...</p>
        <p><a href="#" class="btn btn-primary" role="button">Button</a> <a href="#" class="btn btn-default" role="button">Button</a></p>
      </div>
    </div>
  </div>
</div>
```

# Alerts
![](http://i.imgur.com/nKEeAcQ.jpg)
```
<div class="alert alert-success" role="alert">...</div>
<div class="alert alert-info" role="alert">...</div>
<div class="alert alert-warning" role="alert">...</div>
<div class="alert alert-danger" role="alert">...</div>
```

# Progress bars
![](http://i.imgur.com/rkNMSid.jpg)
```
<div class="progress">
  <div class="progress-bar" role="progressbar" aria-valuenow="60" aria-valuemin="0" aria-valuemax="100" style="width: 60%;">
    <span class="sr-only">60% Complete</span>
  </div>
</div>
```

# Progress bars animated
![](http://i.imgur.com/KUiZEz0.jpg)
```
<div class="progress">
  <div class="progress-bar progress-bar-striped active" role="progressbar" aria-valuenow="45" aria-valuemin="0" aria-valuemax="100" style="width: 45%">
    <span class="sr-only">45% Complete</span>
  </div>
</div>
```

# Responsive embed
![(http://i.imgur.com/QFBQOaC.jpg)

```
<!-- 16:9 aspect ratio -->
<div class="embed-responsive embed-responsive-16by9">
  <iframe class="embed-responsive-item" src="..."></iframe>
</div>

<!-- 4:3 aspect ratio -->
<div class="embed-responsive embed-responsive-4by3">
  <iframe class="embed-responsive-item" src="..."></iframe>
</div>
```
