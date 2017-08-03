# Ubicación de elementos & más!

  * Propiedades de padres e hijos
  * Gradientes en CSS
  * Transiciones
  * Transformación
  * Animación en CSS

### Propiedades de padres e hijos

**Propiedades para aplicar en el contenedor flexible**

* display: flex
* flex-direction
* flex-wrap
* flex-flow
* justify-content
* align-items
* align-content

**Propiedades para aplicar a los flex items**

* order
* flex-grow
* flex-shrink
* flex-basis
* flex
* align-self

------------------------------

### ¿Cómo empezamos con Flexbox?

para comenzar a utilizar las bondades de Flexbox lo primero que debemos de hacer es establecer la propiedad display con el valor flex en el elemento padre.

```
.flex-container {
  display: flex;
}
```

**display: flex** es la única propiedad que necesitamos para configurar el contenedor principal y de esta manera todos sus hijos inmediatos se convertirán en elementos flexibles de forma automática.


![](http://i.imgur.com/FOmQ2Xv.jpg)

El conjunto de propiedades que nos presenta la especificación CSS3 en cuanto al modulo Flexbox las podemos dividir en dos grupos, las propiedades para el elemento contenedor flex y las otras propiedades para los elementos hijos flexibles.

# Propiedades para el contenedor Flex

--------------------------

### 1. flex-direction

Esta propiedad me va a permitir manejar el direccionamiento de los flex items, es decir me va a permitir cambiar el flujo normal de los elementos flexibles en el main axis. Esta propiedad tiene múltiples valores que nos van a permitir variar de todas las formas el direccionamiento de los elementos hijos flexibles. En conclusión esta propiedad nos va a permitir especificar si queremos que los flex items se dispongan en filas o columnas.

Veamos los valores de flex-direction:

** flex-direction: row;**

```
.flex-container {
      display: flex;
      flex-direction: row;
}
```

Con el valor row los flex items se apilan en una fila de izquierda a derecha tomando como eje principal el main axis, este es el valor que se aplica por defecto en la propiedad flex-direction.

![](http://i.imgur.com/fwJI90K.jpg)

**flex-direction: row-reverse;**

```
.flex-container {
      display: flex;
      flex-direction: row-reverse;
}
```
Con el valor row-reverse (fila inversa) los flex items se apilan en una fila de derecha a izquierda.


![](http://i.imgur.com/TAN9gEq.jpg)

**flex-direction: column;**

```
.flex-container {
      display: flex;
      flex-direction: column;
}
```
Con el valor column los flex items se apilan en una columna de arriba hacia abajo, esta vez tomando como eje principal el cross axis.


![](http://i.imgur.com/74bzHvR.jpg)

**flex-direction: column-reverse;**

```
.flex-container {
      display: flex;
      flex-direction: column-reverse;
}
```

Con el valor column-reverse los flex items se apilan en una columna de abajo hacia arriba, tomando como eje principal el cross axis.


![](http://i.imgur.com/QVz5jpS.jpg)

---------------------------

### 2. flex-wrap

El comportamiento inicial del contenedor flexible es poder mantener los flex items en su main axis o eje horizontal sin importar que las dimensiones de estos items cambien, pero hay ocasiones donde vamos a querer controlar este alineamiento y hacer que los elementos puedan saltar de linea para poder mantener una apariencia deseada en estos flex items. Con flex-wrap vamos a poder especificar si queremos que los items puedan saltar a una nueva linea si el contenedor flexible se queda sin espacio.

Veamos los valores de la propiedad flex-wrap:

**flex-wrap: nowrap;**

```
.flex-container {
      display: flex;
      flex-wrap: nowrap;
}
```

nowrap es el valor que se aplica por defecto en la propiedad flex-wrap, este valor hace que los elementos encajen en el ancho del contenedor flexible aun modificando la apariencia de estos, este es el valor que se aplica por defecto en la propiedad flex-wrap.


![](http://i.imgur.com/YIsbNmC.jpg)

**flex-wrap: wrap;**

```
.flex-container {
    display: flex;
    flex-wrap: wrap;
}
```

Con este valor en la propiedad flex-wrap los flex items pueden romper la linea del eje horizontal si les es necesario para así conservar las características de dimensiones de los flex items. Esto es de izquierda a derecha y de arriba a abajo.

![](http://i.imgur.com/NhqxHDi.jpg)

**flex-wrap: wrap-reverse;**

```
.flex-container {
    display: flex;
    flex-wrap: wrap-reverse;
}
```

Con el valor wrap-reverse la propiedad flex-wrap los flex items también pueden romper la linea del eje horizontal si les es necesario. Pero esta vez el orden es de izquierda a derecha y de abajo a arriba.

![](http://i.imgur.com/r0jiWhG.jpg)

------------------------------

### 3. flex-flow

La propiedad flex-flow es simplemente la forma shorthand o forma rápida para las propiedades flex-direction y flex-wrap vistas anteriormente. Los valores que se aplican por defecto a esta propiedad son las mismas que se aplican a las propiedades que están actuando como valor. row nowrap.

**Valores:**

* valores de la propiedad flex-direction
* valores de la proiedad flex-wrap

```
.flex-container {
    display: flex;
    flex-wrap: row-reverse wrap;
}
```

------------------------------

### 4. justify-content

Justify-content nos va a permitir alinear los elementos en el main axis de la linea actual del contenedor flexible, esto puede ser de forma vertical o horizontal según lo especifiquemos con flex-direction, también nos va a ayudar a distribuir los flex items en el contenedor flexible cuando los items no utilicen todo el espacio disponible en su eje principal actual. Esto es declarar la forma en que el navegador debe distribuir el espacio disponible entre los items flexibles.

Veamos los valores de la propiedad justify-content:

** justify-content: flex-start;**

```
.flex-container {
    display: flex;
    justify-content: flex-start;
}
```

El valor flex-start de la propiedad justify-content lo que hace es alinear los flex items en el main start del contenedor flexible es decir alineados al lado izquierdo, este es el valor que se aplica por defecto en la propiedad justify-content.

![](http://i.imgur.com/BM7WPcx.jpg)

** justify-content: flex-end;**

```
.flex-container {
    display: flex;
    justify-content: flex-end;
}
```

El valor flex-end de la propiedad justify-content lo que hace es alinear los flex items en el main end del contenedor flexible es decir alineados al lado derecho.

![](http://i.imgur.com/gOpbic9.jpg)

** justify-content: center;**

```
.flex-container {
    display: flex;
    justify-content: center;
}
```

El valor flex-center lo que hace es alinear los flex items en el centro del contenedor flexible.

![](http://i.imgur.com/lNq0tgx.jpg)

**justify-content: space-between;**

```
.flex-container {
    display: flex;
    justify-content: space-between;
}
```

space-between va a hacer que los flex items se tomen la misma distancia o espaciado entre ellos dentro del contenedor flexible quedando el primer y ultimo elemento alineados con los bordes del contenedor en el eje principal.


![](http://i.imgur.com/qqw0Wes.jpg)

**justify-content: space-around;**

```
.flex-container {
    display: flex;
    justify-content: space-around;
}
```

space-around muestra los flex items con el mismo espacio de separación entre si, en diferencia del valor space-between los items primero y ultimo toman también el espaciado entre los bordes del contenedor flexible.

![](http://i.imgur.com/H7z6l3i.jpg)

-----------------------

### 5. align-items

Align-items nos permite establecer la alineación que tendrán por defecto los flex item incluyendo los anónimos, es similar a la propiedad justify-content pero esta vez la dirección es perpendicular. Es decir align-items nos va a permitir los items en el eje secundario del contenedor flex.

Veamos los valores de la propiedad flex-wrap:

**align-items: stretch;**

```
.flex-container {
    display: flex;
    align-items: stretch;
}
```

El valor stretch (estirar) para la propiedad align-items lo que va a hacer es tratar de llenar toda la altura (o anchura) desde el cross start hasta el cross end del contenedor flexible, siempre y cuando los items no tengan propiedades de dimensión definidas.

![](http://i.imgur.com/9RWdwTw.jpg)

**align-items: flex-start;**

```
.flex-container {
    display: flex;
    align-items: flex-start;
}
```

Con flex-start los flex items se apilan en el cross start del contenedor flexible, es decir en el inicio transversal, este es el valor que se aplica por defecto en la propiedad align-items.

![](http://i.imgur.com/DTszFeV.jpg)

**align-items: flex-end;**

.flex-container {
    display: flex;
    align-items: flex-end;
}

Con flex-end los flex items se apilan en el cross end del contenedor flexible.


![](http://i.imgur.com/x7uzwKw.jpg)

**align-items: center;**

```
.flex-container {
    display: flex;
    align-items: center;
}
```

Con center los flex items se apilan en el centro del cross axis del contenedor flexible, osea en el eje transversal.


![](http://i.imgur.com/CGbD2Vt.jpg)

**align-items: baseline;**

```
.flex-container {
    display: flex;
    align-items: baseline;
}
```

baseline alinea los flex items sus propias lineas de base, esta se define en base de los texto de cada item.

![](http://i.imgur.com/KT2e57h.jpg)

------------------------------

### 6. align-content

La propiedad align-content alinea los flex items cuando estos no usan todo el espacio disponible en el cross axis del contenedor flexible, que de forma predeterminada es verticalmente.

**Nota:** Esta propiedad sólo tiene efecto cuando el contenedor flexible tiene varias líneas de flex items. Si se colocan en una sola línea esta propiedad no tiene ningún efecto sobre el diseño.

Veamos los valores de la propiedad align-content:

**align-content: stretch;**

```
.flex-container {
    display: flex;
    align-content: stretch;
}
```

Con el valor stretch los flex items son mostrados con espacios distribuidos después de cada fila compuestas elementos flexibles dentro de su contenedor, este es el valor que se aplica por defecto en la propiedad align-content.


![](http://i.imgur.com/9rK9tTD.jpg)

**align-content: flex-start;**

```
.flex-container {
    display: flex;
    align-content: flex-start;
}
```

El valor flex-start lo que hace es apilar los flex items partiendo en el inicio transversal (cross start) del contenedor flexible.


![](http://i.imgur.com/zCwjgeG.jpg)

**align-content: flex-end;**

```
.flex-container {
    display: flex;
    align-content: flex-end;
}
```

El valor flex-end apila los flex items hacia el cross end del contenedor flexible.

![](http://i.imgur.com/r1bz1FO.jpg)

**align-content: flex-center;**

```
.flex-container {
    display: flex;
    align-content: center;
}
```

El valor flex-end apila los flex items en el cross axis del contenedor flexible.

![](http://i.imgur.com/iyQNtTc.jpg)

**align-content: space-between;**

```
.flex-container {
    display: flex;
    align-content: space-between;
}
```

space-between en la propiedad align-content va a hacer que los flex items se tomen la misma distancia o espaciado entre ellos dentro del contenedor flexible quedando el primer y ultimo elemento alineados con los bordes del contenedor en el eje principal (cross axis predeterminado).

![](http://i.imgur.com/BNRoijl.jpg)

** align-content: space-around;**

```
.flex-container {
    display: flex;
    align-content: space-around;
}
```

space-around en la propiedad align-content muestra los flex items con el mismo espacio de separación entre si, en diferencia del valor space-between los items primero y ultimo toman también el espaciado entre los bordes del contenedor flexible.

![](http://i.imgur.com/Pa4ymtz.jpg)

# Propiedades para los Flex items

Esta sección describe las propiedades que se le pueden asignar a los items como tal. Algunas de ellas sobreescriben propiedades que se configuran en el container.

--------

### flex-grow

Esta propiedad define la capacidad de un elemento de crecer cuando en el contenedor todavia hay espacio sobrante. Esta propiedad se configura con un valor numérico entero natural (no acepta negativos). Por defecto el valor viene configurado en "0" por lo tanto el elemento no crecera de manera horizontal. Si este valor es configurado en 1 para todos los items, todos ellos crecerán de igual manera por lo que ocuparan la misma cantidad de espacio dentro del contenedor, si a uno de ellos el valor se configura en "2" dicho elemento ocupará el doble de los demás.

![](http://i.imgur.com/4nhAofp.png)

```
.item {
  flex-grow: <numero>; /* por defecto 0 */
}
```

----------------

### flex-shrink

El shrink configura la posibilidad de un elemento de encogerse en caso del máximo ancho del contenedor sea alcanzado por todos los elementos.

```
.item {
  flex-shrink: <numero>; /* por defecto 1 */
}
```

-----------------

### flex-basis

Define el ancho de un elemento antes del espacio restante de un contenedor. Este valor por defecto viene configurado en 0.

```
.item {
  flex-basis: <ancho> | auto; /* default auto */
}
```

-----------------------

### flex

El flex es la manera rápida de configurar a un item las tres propiedades anteriores, es decir, en una sola propiedad se configura el "flex-grow", "flex-shrink" y "flex-basis", es ese orden exacto.

```
.item {
  flex: none | <'flex-grow'> <'flex-shrink'> <flex-basis'>
}
```

### order

Esta propiedad permite modificar el orden de aparición de un elemento. Recibe como valor numeros enteros.

![](http://i.imgur.com/dA2STJY.png)

```
#item2 {
  order: <integer>;
}
```

# Gradientes

CSS3 ha agregado la opción de crear gradientes (fondos en degradé) sin la necesidad de usar imágenes.

Los gradientes en CSS son de dos tipos: lineales (```linear-gradient```) o radiales (```radial-gradient```). En el gradiente lineal, la transformación de color va avanzando línea a línea, mientras que en el radial, la transformación de color se produce debido a que sucesivos círculos concéntricos van cambiando de color.

La propiedad que utilizamos para realizar gradientes lineales, se llama ```linear-gradient``` y esta se agrega al atributo ```background```, que ya vimos con anterioridad.

Esta propiedad maneja dos opciones de parámetros, podemos elegir el punto de inicio o sea si queremos que lo aplique arriba, abajo, a la derecha o a la izquierda de nuestra caja o podemos elegir los grados de inclinación que queremos que tenga nuestro gradiente.

Los puntos de inicio pueden ser ```top```, ```right```, ```left``` o ```bottom```.

Entonces, supongamos que queremos aplicarle a nuestra caja un gradiente que va de negro a gris desde la parte de arriba de la misma. La sintaxis sería la siguiente:

```
div {
  background: linear-gradient (to top, #000, #ccc)
}
```

Si lo que queremos es aplicar un gradiente de 90º, entonces la sintaxis sería así:

```
div {
  background: linear-gradient (90deg, #000, #ccc)
}
```

Algunas cosas a tener en cuenta, la propiedad ```linear-gradient``` no genera un color de fondo, sino una imagen sin dimensiones específicas, esta se va a adaptar automáticamente para cubrir todo el espacio disponible.

Por otro lado, no todos los navegadores soportan esta propiedad.

# Transformaciones

Las transformaciones CSS ofrecen la posibilidad de modificar el desplazamiento, escala, rotación, sesgo de elementos y en combinación con las transiciones nos permite crear animaciones css modificando gradualmente sus propiedades.

De las transformaciones de CSS3 en 2D, las más usadas son:

* **Rotate**: Rotate te permite rotar un elemento dándole un ángulo de giro en grados.
* **Scale**: Scale te permite escalar un elemento, toma valores positivos y negativos y se le pueden poner decimales.
* **Translate**: Translate nos permite trasladar un elemento a la vez en el eje de las X y de las Y, dándole las coordenadas iniciales y finales.
* **Trasladar**: Esta propiedad de CSS3 no hace propiamente una transición, sino que hace que un elemento pase de estar en una posición a estar en otra. Con las transiciones y las animaciones de CSS3 vamos a poder darle un efecto visual de movimiento.

Ejemplo:

```
transform: translate(10px, 20px);
```

![](https://coderhouse.gitbooks.io/clase-5-fundamentos/content/Captura%20de%20pantalla%202015-10-08%2011.59.56.png)

**Rotación**: Se puede aplicar tanto a elemento inline como a elementos de bloque.

![](https://coderhouse.gitbooks.io/clase-5-fundamentos/content/Captura%20de%20pantalla%202015-10-08%2012.00.04.png)

```
.ejemplo {
  transform: rotate (45deg);
}
```

Los grados se marcan en positivo si el elemento se rota en el sentido de las agujas del reloj y en negativo si es al revés.

Por defecto, el punto de referencia que toma como eje para hacer la rotación es el centro, pero también se puede especificar otro punto.

**Escalar**: Otro punto interesante va a ser escalar un elemento con CSS3.

![](https://coderhouse.gitbooks.io/clase-5-fundamentos/content/Captura%20de%20pantalla%202015-10-08%2012.00.12.png)

Si el valor es positivo, el elemento se hace más grande, y si es negativo se hace más pequeño.

--------------------

# Transiciones

Las transiciones permiten controlar la velocidad a la que se van a modificar las propiedades de un elemento inclusive se pueden aplicar curvas de aceleración permitiendo de esta forma crear animaciones.

# Animaciones

Una animación tiene lugar en el tiempo, con lo que vamos a tener que tomar diferentes puntos dentro de un fragmento de tiempo para especificar que sucede en cada uno de ellos. Es lo que se llaman **keyframes**. Para los que ya han trabajado en Flash u otros programas de animación ya conocen el concepto. En cada keyframe podemos introducir un cambio y la suma de estos cambios es lo que va a dar lugar a la animación final.

Para indicar la duración de una animación utilizaremos la propiedad ```animation-duration```.

La velocidad de la animación estará gestionado por la propiedad ```animation-timing-function```.

También en las animaciones de CSS3 podemos especificar un tiempo de espera antes de iniciar la animación con la propiedad ```animation-delay```.

Con la propiedad ```animation-direction``` podremos indicarle que la propiedad se haga en sentido inverso al habitual, es decir, que empiece por el final.

Para aprender más sobre esto, pueden ver [http://daneden.github.io/animate.css/](http://daneden.github.io/animate.css/)
