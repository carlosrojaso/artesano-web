# Introducción

* ¿Qué es SASS?
* ¿Por qué es útil?

## ¿Qué es SASS?

Sass significa “Syntactically Awesome Stylesheets”, es una herramienta escrita en Ruby que nos permite crear hojas de estilos estructuradas, limpias y fáciles de mantener.

Con SASS vamos a poder escribir hojas de estilo que nos ayudará a generar ficheros CSS más optimizados, incorporando mayor contenido semántico y permitiendo utilizar funcionalidades que normalmente encontraríamos en lenguajes de programación tradicionales, como el uso de variables, creación de funciones, etc.

## ¿Por qué es útil?

Normalmente crear una hoja de estilos es relativamente sencillo. Lo malo es cuando el proyecto va creciendo en tamaño: su CSS puede acabar siendo muy extenso.

Sass nos permite una sintaxis más simple, más elegante, implementando además bastantes características extras para hacer más manejable nuestra hoja de estilos.

# Variables

* Sintaxis
* Crear variables

## Sintaxis

En Sass contamos con dos diferentes tipos de sintaxis: **scss y sass**.

La primera y más popular es conocida como SCSS (Sassy CSS), es muy similar a la sintaxis nativa de CSS, tanto así que nos permite importar hojas de estilos CSS (copiar y pegar) directamente en un archivo SCSS y obtener un resultado válido.

Para utilizarla solo debemos crear un archivo con terminación .scss de la siguiente manera: **archivo.scss**

La segunda opción, es conocida como Indented Syntax (sintaxis deindentación). Utiliza la indentación en lugar de corchetes para expresar el anidamiento de selectores y saltos de línea en lugar de punto y coma para separar las diferentes propiedades que se declaren. Usarla también es muy sencillo, creamos un archivo con terminación .sass de la siguiente manera: **archivo.sass**

## Crear variables

Las variables son una manera de guardar información que necesites reutilizar en tus hojas de estilos: colores, dimensiones, fuentes o cualquier otro valor. Sass utiliza el símbolo dólar ($) al principio de la palabra clave para crear una variable.

Estas variables se comportan como atributos CSS, y su valor puede ser cualquier valor que pudiera adquirir cualquier atributo CSS.

```
// creando variable
$color: #FF0000;

body {
  // aplicando el valor de $color
  background-color: $color;
}
```

Una variable se podrá definir fuera o dentro de algún selector. Si se define fuera, dicha variable será global y podrá utilizarse en cualquier bloque, pero si se define dentro de un selector, la variable será local y únicamente se podrá utilizar en el selector que la contiene y en sus selectores anidados.

Una buena práctica común consiste en definir todas las variables globales al principio del fichero, para que puedan localizarse rápidamente.

**Uso de !default en las variables**

Si en el ejemplo anterior, hacemos:

```
$color: #FF0000;
$color: #000000;
```

El color que se usará es el ```#000000```. Pero si hacemos:

```
$color: #333333;
$color: #000000 !default;
```

El color que se usará será ```#333333```. Ya que esta directiva indicará que la asignación que estamos realizando a la variable solo se haga en caso de que dicha variable no se haya definido anteriormente.

# Instalación

Para poder utilizar SASS necesitamos disponer del compilador que nos permita convertir nuestros ficheros en sintaxis SCSS a CSS, para instalar dicho compilador debemos instalar previamente Ruby.

Antes de comenzar con la instalación; vamos a explicar el motivo:  Sass es un gem (joya) de Ruby. RubyGems es el gestor de paquetes de Ruby que provee un formato estándar para distribuir paquetes/librerías (Gems). Fue diseñado para manejar fácilmente la construcción, instalación y distribución de librerías.

Los usuarios de Windows podrán hacerlo fácilmente a través de [http://rubyinstaller.org](http://rubyinstaller.org), los usuarios de Mac OS X ya lo llevan instalado de serie, y los usuarios de Linux podrán instalarlo con su gestor de paquetes preferido. Una vez instalado Ruby y su gestor de paquetes Ruby Gems, instalar Sass será tan sencillo como introducir esta línea en nuestra consola de comandos.

La instalación es muy sencilla:

1. Abrimos la **línea de comandos** (en Windows ejecutan el programa “cmd”).

2. Usamos RubyGems para la instalación, recuerden Ruby usa Gems para manejar la variedad de paquetes/librerías. Escribimos lo siguiente:

```
$ gem install sass
```

3. El comando instalará Sass y todas las dependencias requeridas. Si la línea de comandos imprime un mensaje de error, es probable que necesites usar el comando sudo para instalar Sass satisfactoriamente.

```
$ sudo gem install sass
```

Para comprobar que la instalación fue exitosa, copiamos y pegamos el siguiente comando:

```
$ sass -v
```

Nos imprimirá la versión de Sass: **Sass 3.4.7.**

# Usos  de anidación

La principal caraterística de Sass es poder definir reglas de maquetación de forma anidada, evitando que tengamos que repetir constantemente los prefijos de alcance en los selectores CSS. Uno de los problemas de los selectores CSS es que cuanto más específicos sean estos, más tendremos que repetir una y otra vez la cadena de elementos que conforman el selector.

Ejemplo:

```
#content            { border: 1px solid black; }
#content p.info     { color: #fff; }
#content p.info a   { text-decoration: none; }
```

Como se puede ver en el ejemplo, tenemos que ir repitiendo los elementos base del selector según vamos estilizando los elementos más internos. Esto trae algunos problemas.

1. El documento CSS se hace poco legible.
2. Tenemos que hacer un uso excesivo de elementos repetitivos y por consiguiente copy/paste, lo cual induce a errores.
Sass evita estos inconvenientes ofreciéndonos la posibilidad de anidar selectores unos dentro de otros.

El ejemplo anterior, se haría de la siguiente manera:

```
#content {
  border: 1px solid black;
  p.info {
    color: #fff;
    a { text-decoration:none;}
  }
}
```

De esta manera, no tenemos que repetir las cadenas de selección completas pues Sass se encargará de introducirlas cuando lo compilemos a CSS.

Además de anidar selectores también podremos anidar propiedades de forma que no tengamos que repetir constantemente cosas como ```border-left```. Podemos verlo en este ejemplo:

```
.boxborder {
  border: {
    style: solid;
    left: {
      width: 4px;
      color: #888;
    }
    right: {
      width: 2px;
      color: #ccc;
    }
  }
```

# Importar

El uso de @import es diferente en Sass que en CSS. En una hoja de estilos CSS supone una nueva llamada al servidor para cargar otra hoja de estilos y esperar a que se cargue para aplicar los nuevos estilos.

En Sass es diferente. La importación en un archivo .scss o .sass se produce durante la compilación.

Vamos a crear un nuevo archivo menu.scss que sea por ejemplo así:

```
.menu {
  margin: 0;
  padding: 0;
  list-style-type: none;
}
.menu > li {
  display: inline-block;
  margin: 0 0 10px 10px;
}
```

Y en main.css ponemos:

```
// Importamos los estilos de menu.scss
// cuando se compile main.scss
@import "menu";
```

Esto es lo que ocurre:

![](http://i.imgur.com/rdqsAPB.jpg)

En el CSS resultante main.css estarán compilados tanto el contenido de main.scss como el de menu.scss. Pero como vemos también se creará una hoja de estilos independiente menu.css sólo con los estilos de menu.scss.

Para evitar esto debemos grabar el archivo menu.scss con un guión inferior previo, es decir _menu.scss. Es lo que se llama un “partial” (parcial).

![](http://i.imgur.com/ntBitkj.jpg)

La sintaxis dentro del archivo .scss sigue siendo la misma:

```
// Importamos los estilos de _menu.scss
// cuando se compile estilos.scss
@import "menu";
```

De esta forma los estilos de _menu.scss pasarán a formar parte una vez compilado de main.css sin crear una hoja de estilos aparte. Por regla general, un archivo como main.scss debería incluir únicamente importaciones de diferentes archivos scss (por ejemplo, _reset.scss, _menu.scss, _header.scss, etc..) sin tener estilos propios.

# Mixins
Nos permiten definir estilos que puedan ser reutilizados en nuestro proyecto, sin necesidad de recurrir a las clases helpers que ya comentamos, también pueden contener complejas reglas de CSS.

### Cómo usar los Mixins en Sass:

Para crearlos debemos utilizar ```@``` seguido de ```mixin``` y por último el nombre que queramos darle al mixin. Luego, para declararlo dentro de un componente, usamos ```@include```, seguido de un espacio, el nombre y por último entre paréntesis ```()``` escribimos los argumentos requeridos por nuestro Mixin. Los argumentos son opcionales.

Por ejemplo, para evitar la repetición de alto y ancho de un componente a lo largo de un proyecto, podemos crear un pequeño Mixin que transforme las habituales dos líneas de código en una sola:

```
@mixin sizes($width, $height: $width) {
  height: $height;
  width: $width;
}

.box {
  @include sizes(100px);
}
```

# Extends / Placeholders:

Es una de las más poderosas características de Sass. Nos permite crear un fragmento de estilos que luego podamos reutilizar fácilmente en cualquier componente.

### Cómo usarlo:
Para declarar y crear un fragmento de estilos que necesitamos reutilizar, usamos ```%``` seguido de un nombre, sin espacios. Luego, para imprimir o reutilizar el Extend dentro de un componente, usamos ```@extend``` seguido de un espacio y por último, el nombre que asignamos a nuestro fragmento.

Por ejemplo, si queremos crear un componente básico para imprimir mensajes del sistema, debemos tener una clase para mensajes exitosos, de advertencia y de errores.

```
// vars
$bg-success: green;
$bg-error: red;
$bg-warning: orange;

// extend
%message {
  border-radius: 2px;
  color: white;
  padding: 5px;
  text-align: center;
}

.message-success {
  @extend %message;
  background-color: $bg-success;
}

.message-error {
  @extend %message;
  background-color: $bg-error;
}

.message-warning {
  @extend %message;
  background-color: $bg-warning;
```


###### Sass nos imprimirá el siguiente CSS:

```
.message-success, .message-error, .message-warning {
  border-radius: 2px;
  color: white;
  padding: 5px;
  text-align: center;
}

.message-success {
  background-color: green;
}

.message-error {
  background-color: red;
}

.message-warning {
  background-color: orange;
}
```

Sass, agrupará las clases o atributos que tengan estilos comunes, evitando repetirlos por separado.

# Operadores:

Realizar operaciones matemáticas en CSS, es posible gracias a Sass. Contamos con un puñado de operadores: (+, -, *, / y %) que trabajan de la misma forma que las operaciones matemáticas básicas.

Por ejemplo, para crear un simple grid basado en 960px y que el ancho de cada elemento sea expresado en porcentajes:

```
$wrap: 960px;

article[role="main"] {
  float: left;
  width: 630px / $wrap * 100%;
}

aside[role="complimentary"] {
  float: left;
  width: 330px / $wrap * 100%;
}
```

###### Sass nos imprimirá el siguiente CSS:
```
article[role="main"] {
  float: left;
  width: 65.625%;
}

aside[role="complimentary"] {
  float: left;
  width: 34.375%;
}
```

De esta manera  tenemos un grid básico que nos permite estructurar nuestro contenido de una manera agradable en dos columnas.

# BEM

La metodología de trabajo BEM (Block,Element,Modifier) que se implementa en las hojas de estilos de los sitios web, se puede definir como una buena practica para crear estilos de manera ordenada, fácil de entender y escalable cuando se utilizan desarrollos que deben ser trabajados por un equipo de personas y se trabajan sitios web de manera modular. Cuando se utiliza esta metodología, el uso de identificadores para los estilos visuales  en la estructura del HTML y dentro de las hojas de estilos deja de servir, ya que la metodología sugiere manejar todo el estilo visual del sitio web mediante el uso de clases; Solo se deben utilizar los identificadores cuando se va a ejecutar alguna acción mediante Javascript.

Yandex es el buscador web más popular  en Rusia, incluso superando al poderoso Google. Este buscador se plantó y estructuró como un ecosistema de servicios web y soluciones online, en un momento de su potencial crecimiento sintió la necesidad de cambiar para mejorar su arquitectura frontend e implementar una metodología que les ayudase a tener su código de estilos rigurosamente estructurado, es así como en el 2010 surgió la idea de estructurar por medio de Bloques, Elementos y Modificadores (BEM), que va más que una metodología de arquitectura CSS, de hecho este es un marco completo para el sistema frontend  que incluye una serie de reglas y herramientas para un desarrollo frontend global.

Esta metodología sugiere una estructura para nombrar tus clases, basado en las propiedades del elemento en cuestión. Si alguna vez has visto un nombre de una clase como header_from-email eso es precisamente BEM en acción. Cuando utilices la metodología BEM, debes tomar en cuenta que solamente usarás nombres de clases (no IDs). Los nombres de clases te permiten repetir el nombre BEM si es necesario, y crear una estructura de código más consistente.

# Ventajas y Desventaja

--------------------

## Ventajas

* Permite el trabajo de módulos para reutilizar de una manera sencilla en el flujo del html.
* Permite el trabajo entre varios desarrolladores ya que promueve la organización de una manera lógica en las hojas de estilos.
* Se puede trabajar de manera muy sencilla con pre procesadores como SASS o STYLUS.

-----------------

## Desventajas

* Las clases pueden quedar muy largas al momento de utilizar la metodología.

# Bloque

El bloque es un contenedor o contexto donde el elemento se encuentra presente. Piensa como si fueran partes estructurales de código más grandes. Puede que tengas un encabezado, pie de página, una barra lateral y un área de contenido principal; cada uno de estos sería considerado como un bloque. Mira la imagen de abajo:

![](http://i.imgur.com/srDeDhQ.jpg)

El bloque de elementos forma la raíz de la clase y siempre irá primero. Solo debes saber que una vez que has definido tu bloque, estarás listo para comenzar a nombrar tus elementos.

# Elemento

El elemento es una pieza de un bloque. El boque es el todo y los elementos son las piezas. Cada elemento se escribe luego del bloque conectado por dos barras bajas.

```
.block__element
```

Es algo extraño al principio pero una vez que comienzas a usarlo te preguntarás cómo es que has escrito CSS sin usar BEM. La doble barra baja te permite visualizar, navegar rápidamente y manipular tu código.

Aquí hay algunos ejemplos de cómo funciona la metodología de elementos:

```
.header__logo {}
.header__tagline {}
.header__searchbar {}
.header__navigation {}
```

Como puedes ver, hay espacio para la creatividad y hacer de esta metodología tuya. En el ejemplo, "navigation" puede ser cambiado a "nav", "tagline" puede cambiarse a "tag" o "tagLine". El punto es mantener los nombres simples, claros, y precisos. No lo pienses demasiado, y solo porque tus hojas de estilos y html serán estáticos, no quiere decir que tengas que volver a repetir el mismo código. Actualizar el nombre de las clases no debería ser un problema cuando encuentras una mejor semántica que funcione (solo debes tratar de ser consistente y apegarte a ella). Los elementos se convertirán en el centro de los nombres de tus clases, y te ayudarán a entender cómo estructurar tus hojas de estilos y cómo manejar tu diseño.

# Modificadores

Cuando nombras una clase, la intención es ayudar a que ese elemento pueda ser repetido para que no tengas que escribir nuevas clases en otras áreas del sitio si los elementos de estilo son los mismos. Cuando necesitas modificar el estilo de un elemento específico, puedes usar un modificador. Para lograr esto, añades un doble guión -- luego del elemento (o bloque). Aquí tenemos un corto ejemplo:

```
.block--modifier {}
.block__element--modifier {}
```

Ten cuidado al usar los modificadores, recuerda que se quiere mantener todo más simple y no tener que repetir lo mismo o crear clases extras a menos que sea absolutamente necesario. Lo explicaremos con un código usando el encabezado del sitio como nuestro bloque:

```
.header__navigation {}
.header__navigation--secondary {}
```

Si estás usando una segunda navegación, lo más probable es que el diseño y espaciado no cambien, pero puede que la navegación secundaria tenga un color distinto. Puedes ya sea, duplicar los estilos originales, o mejor aún, usar un pre-procesador. Con Sass, podrías @extender el elemento principal (así el elemento secundario heredará todas las propiedades) y cambiar los estilos apropiados.

```
.header__navigation {
background: #008cba;
    padding: 1rem 0;
    margin: 2rem 0;
    text-transform: uppercase;
    }

.header__navigation--secondary {
    @extend .header__navigation;
    background: #dfe0e0;
    }
```

Es probable pensar que el nombre de la clase es muy largo.  Sin embargo, los nombres de las clases BEM son específicos, claros, fáciles de leer dentro del html, y comunican claramente para qué existen.

Una ventaja de los nombres de las clases cuando usamos BEM es que solo tienes que usar un nombre de clase por cada etiqueta html. Fíjate cómo funcionaría para la etiqueta "label". Selectores estándares:

```
.label .label-default {}
.label .label-alert {}
```
vs. selectores BEM:

```
.label {}
.label--alert {}
```

Los lenguajes como Sass (específicamente Scss) nos permiten rápidamente tener elementos, compartir los mismos estilos con pequeñas excepciones. El ejemplo de abajo nos evita duplicar estilos, mas bien cambiamos sólo lo necesario. Otro punto importante de la metodologéa BEM es que no tienes que combinar clases ambiguas como "panel panel-default col-md-3". Si utilizas un framework como Foundation puedes comenzar a nivelar las diferencias. Pero para un ejemplo simple, pongamos estilo a las etiquetas que acabamos de definir.

```
.label {
background: #eee;
  border-radius: 505;
  color: #333;
  font-size: 1rem;
}

.label--alert {
  @extend .label;
  background: #da4531;
  color: #fff;
}
```
