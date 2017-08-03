# Introducción

El dominio en Internet, es la dirección que ingresamos en el navegador para acceder al sitio web deseado.

Ej: [www.css-tricks.com](http://www.css-tricks.com)

## Dominios de nivel superior

Los dominios de nivel superior (TLD, de sus siglas en inglés Top Level Domain) son el nivel más alto en la jerarquía de nombres en Internet, por ejemplo en ```www.ejemplo.com``` el dominio de nivel superior es .com.

La administración de estos dominios de nivel superior se lleva a cabo por la organización llamada ICANN que son las siglas de Internet Corporation for Assigned Names and Numbers.

## Dominios de internet genéricos

El dominio de Internet genérico (gLTD por sus siglas en inglés de generic top-level domain) es una sub-categoría de dominio de nivel superior (TLD), y es responsabilidad de la IANA (Internet Assigned Numbers Authority), el cual es un departamento más dentro de ICANN.

Los principales dominios de Internet genéricos más conocidos son **.com**, **.net**, **.org** y **.info**. Otros dominios como **.biz**, **.name** y **.pro** son asignados únicamente a organizaciones que demuestren su hecho. Ej: para registrar un dominio **.pro** se debe demostrar que el registrante es un profesional.

Existen tres clasificaciones de dominios de Internet genéricos:

* **No restringidos**: Son dominios disponibles para ser usados por cualquier organización o persona, sin restricción en cuanto al uso que se le dará (**.com**, **.net**, etc).
* **Patrocinados**: Son dominios que proponen diferentes empresas para establecer una regla de uso específico. Ej: **.tel** (para compañías de telefonía), **.edu** (Educación), etc.
* **Geográficos**: Son los que identifican al territorio geográfico, geopolítico o lingüístico. Ej: **.ar** (Argentina), **.be** (Bélgica), **.fr** (Francia), etc.

## Registro de dominios

Para poder disponer del dominio debemos registrarlo bajo nuestro nombre o el nombre de la empresa. Dependiendo el tipo de dominio que se quiera registrar serán diferentes los requerimientos y pasos a seguir.

**Registro de dominios en Argentina**

La entidad registrante de dominios de internet en Argentina es NIC.AR ([www.nic.ar](http://www.nic.ar)).

Para registrar un dominio, es necesario ingresar al sitio web, crearse un usuario, consultar por el dominio deseado y luego seguir los pasos para finalizar el registro. Actualmente (año 2015) se abona un costo anual de $160. Ej: [www.mercadolibre.com.ar](http://www.mercadolibre.com.ar).

Para registrar un dominio **.com** se hace un trámite muy similar pero a través de otra entidad de registro de dominios .com. Ej: [www.godaddy.com](http://www.godaddy.com). Éste es uno de los sitios que se pueden utilizar.

# Introducción

El alojamiento web es el servicio que el servidor le provee al desarrollador web para poder almacenar archivos de código (html, css, js, php, etc), imágenes, vídeo, o cualquier contenido accesible vía web.

Al alojar los archivos en un servidor, tenemos la posibilidad de acceder a los mismos introduciendo una url específica en el navegador.

## Planes de hosting

Como todos sabemos, cada sitio web es diferente, acceden distintas cantidades de usuarios, ocupan diferente espacio en disco, etc. Por lo tanto es necesario contratar un servicio de hosting que cubra con los requerimientos de nuestra web.

Los servidores son empresas que almacenan computadoras con discos rígidos (en donde son alojados los sitios web), y cada una está equipada con distinto hardware. Esto, entre otros detalles técnicos, permite brindar distintos planes en los que difieren el espacio en disco, la memoria de los CPU, las cantidad de casillas de mail que se puedan crear, el ancho de banda que se le asignará al sitio, etc. Estos planes tienen un valor asignado que puede ser abonado de forma mensual o anual.

A continuación se muestra un ejemplo de uno de los servidores más conocidos del mercado:

![](https://coderhouse.gitbooks.io/clase-13-fundamentos/content/Captura%20de%20pantalla%202015-10-08%2017.24.58.png)

## Alojar sitio web en el servidor contratado

Una vez que elegimos el plan adecuado para nuestro sitio web recibiremos toda la información necesaria para poder subir los archivos al servidor y visualizar nuestra web finalmente online. Para realizar la subida de todos los archivos existen distintos métodos, el más común y generalmente más simple es a través de un cliente FTP.

Para elegir correctamente el plan podemos asesorarnos con el soporte técnico del hosting, que nos pedirá una serie de datos referidos a nuestro sistema web para poder darnos su opinión.

## Hosting y dominio (DNS)

Teniendo en claro lo que es un dominio en Internet, nos falta el paso de relacionarlo con el servidor que hemos contratado, donde se encuentran los archivos que forman el sitio web. Para esto, tenemos que informarle a la entidad registrante del dominio cual son los DNS de nuestro servidor.

La principal tarea de un servidor de DNS es traducir el nombre del dominio ([www.coderhouse.com](http://www.coderhouse.com)) en una dirección IP.

Las direcciones IP (Internet Protocol) constan de un número único e irrepetible con el cual se identifica una computadora conectada a una red que corre el protocolo IP. Ésta computadora es la que nos brinda el servidor para alojar nuestro sitio.

Una dirección IP es un conjunto de cuatro números del 0 al 255 separados por puntos. Ej: la IP de coderhouse.com es: 184.107.100.88.

Para asignar los DNS al dominio debemos acceder al panel de la cuenta que hemos creado en la entidad registrante de dominios, buscar la opción de “Delegación de dominio”, o “DNS” (su nombre puede variar), y asignamos 2 o 3 de los DNS que figuren en el email que nos envió el servidor tras haber contratado el servicio de hosting.

Por lo general una dirección DNS suele ser como en el siguiente ejemplo: ns1.panelboxmanager.com, ns2.panelboxmanager.com, ns3.panelboxmanager.com.

## Soporte técnico

Todos los servidores brindan soporte para sus clientes, con la finalidad de brindar un servicio estable y seguro. Los métodos más comunes son a través de un chat online, asistencia telefónica, un sistema de tickets, etc. Éste último está disponible en el panel de control, una vez que ya tengamos creada nuestra cuenta en el sitio del hosting.

Ej: Se crea un ticket, en donde escribimos nuestra consulta, y luego recibimos la respuesta por parte de un asistente técnico del servidor. Esto simularía una conversación o un intercambio de emails).

## Alojamiento gratuito

Existen servicios de host gratuitos pero no son recomendables ya que no brindan un servicio a nivel profesional, solo puede servirnos para realizar alguna prueba.

# Introducción

Ya hemos aprendido cómo confeccionar correctamente un formulario en html. Lo que veremos en este capítulo será cómo enviar los datos del formulario por mail a una casilla de correos.

## Conexión

Para establecer la conexión correspondiente con el servidor, necesitamos autenticarnos con tres datos esenciales provistos por el servicio de hosting que hayamos contratado previamente: dirección de host, usuario y contraseña.

Para eso debemos abrir el Gestor de sitios:

![](https://coderhouse.gitbooks.io/clase-13-fundamentos/content/Captura%20de%20pantalla%202015-10-08%2017.39.34.png)

En esta imagen se puede ver que se creó un sitio llamado Coderhouse y se completaron los campos Servidor, Usuario y Contraseña. Luego al presionar Conectar pasamos a visualizar la estructura de directorios tanto del entorno local (izquierda) como del servidor remoto (derecha).

![](https://coderhouse.gitbooks.io/clase-13-fundamentos/content/Captura%20de%20pantalla%202015-10-08%2017.39.43.png)

De esta forma se visualiza el Sitio local y el Sitio remoto. Haciendo click derecho sobre los archivos podemos ver las distintas opciones para manipularlos (Subir, Descargar, Borrar, Crear Directorio, etc).

## Directorio raíz

Siempre que nos conectemos a un servidor vamos acceder al directorio raíz del mismo. En donde podemos encontrar una serie de carpetas que van a variar dependiendo del hosting que estamos utilizando.

Entre las carpetas que se listen, debemos identificar el directorio indicado para subir los archivos de nuestro sitio web. Esto también varía según el servidor, los nombres más comunes pueden ser: **public_html**, **htdocs**, **var**, **www**. De no estar seguros cuál es el directorio indicado, podemos consultarle al soporte técnico del hosting.

# Tips para un programador web

A continuación te detallamos algunos tips que todo programador debe tener en cuenta siempre!

**Comentar el código**

Es importante comentar el código en los lenguajes que estemos utilizando. En los estilos, en los códigos en Javascript, en los elementos ubicados en el html, etc.

Esto nos facilitará la tarea a la hora de retomar el proyecto por algun cambio o actualización que nos haya pedido el cliente.

Otro ejemplo, que pasa muy seguido, es que el código que hemos desarrollado, sea consultado por otro programador, integrante del equipo de trabajo, un programador contratado por el cliente, o incluso uno mísmo si pasó mucho tiempo ya no recuerda los detalles.

**Código limpio**

Siempre hay que recordar que debemos separar el contenido html con imágenes y texto, de los estilos del diseño en archivos diferentes. Para eso siempre será necesario linkear un archivo estilos.css al html que hayamos creado. Esto permite trabajar de manera ordenada y eficiente.

**Análisis y síntesis**

Por lo general los tiempos para los desarrollos son ajustados, pero no debemos dejar de tener en cuenta que una vez que desarrollamos un script, podemos tomarnos unos minutos extra para corroborar que el código es óptimo.

En muchos casos un código que se repite muchas veces, se puede pensar un poco más y crear una función que al recibir parámetros cambie su comportamiento y nos arroje los resultados esperados.

**Google**

Generalmente todo empieza aquí. Nunca dudes en preguntar, no solo a tus colegas sino también a los motores de búsqueda. Un consejo que siempre aplico es “a alguien ya le pasó el error que te está ocurriendo en tu sitio!”. Y por lo general probando distintos términos de búsqueda terminarás encontrando la solución.

**Opinión de colegas**

Es muy importante que te mantengas rodeado de un buen equipo de trabajo o colegas. Siempre se aprende del que se tiene al lado, a veces aprendes qué hacer y otras qué no hacer!

Si tiene la oportunidad de consultarle a tus colegas acerca del código que has desarrollado, siempre es bueno tener una segunda opinión que podrá sin dudas optimizar o detectar algún punto débil en el funcionamiento. O quizás simplemente puedes ayudarlo a él en algo que esté haciendo, y te sirve a vos también para aprender.

**Trabajo en equipo y Técnicas de comunicación**

Para poder cumplir los objetivos de un proyecto es importante saber comunicarse con el resto de los que formen parte. Como el cliente, el diseñador, el administrador de la cuenta, un asistente, etc. Por lo tanto, nunca está demas preocuparse por aprender a transmitir de manera decuada el mensaje que queremos dar. De esta manera los demás podrán entender las necesidades que tenemos para poder llevar a cabo eficientemente nuestro trabajo.

**Mantenerse actualizado**

En internet siempre todo avanza constantemente. Las tecnologías cambian, las empresas de desarrollo de software, los celulares, las computadoras, etc. Es necesario estar al día de las tecnologías actuales para poder aplicarlas y poder brindar una solución actualizada del producto. Esto le permitirá al cliente estar a la altura de la competencia y así facilitar su estrategia de comunicación.

**Estudiar**

No dudes en leer un párrafo acerca de un código, una librería, una tendencia, un slider, etc. Para estar al día es necesario ver videotutoriales, leer artículos, libros para poder expandir nuestro conocimiento y habilidades profesionales.

**Espiar el código de los sitios que visitas**

Utiliza el Inspector de Elementos de tu navegador web para ver cómo hicieron algo que te gustó de la web que estás viendo. Más de una vez se aprenden técnicas y formas óptimas de lograr diferentes diseños o elementos.

**Librería personal de funcionalidades y plug-ins**

Armá tu propia librería de códigos. Guardá tus funciones de manera ordenada en archivos diferentes para poder tener un fácil acceso a ellas mientras estás desarrollando tus proyectos.

Por lo general los sitios web comparten muchas similitudes, como un Acordion, un Slider, una Galería de Imágenes. Por lo tanto no dudes en reutilizar tu código utilizando distintos estilos de diseño.


**Mantener adecuadamente tus herramientas de trabajo**

Ocúpate de tu computadora que es tu elemento de trabajo. Mantenla actualizada, limpia ordenada. Esto evitará que funcione lenta y haga tu día a día una frustración constante.

Como así también se deben mantener actualizados los navegadores para desarrollar los sitios de manera óptima.

**Estándares web**

**Zona segura**

Revisa los diseños que recibas para maquetar, porque luego cuando el cliente lo ve en su computadora anticuada con una resolución menor a la más actual de todas, te dirán que no se ve correcamente. Muchas veces nos llegan diseños en medidas que no cumplen los estandares web y debemos saber trasmitirselo al cliente y a los diseñadores de manera adecuada.

**Optimización de contenido**

Recuerda siempre trabajar con archivos optimizados en su relación peso calidad. Tanto las imágenes (JPG, GIF, PNG), como en los archivos de texto. Evita usar espacios exagerados o comentarios muy extensos para alivinar al máximo el peso de tus archivos html, php, js, css, etc

# Navegadores o exploradores web más utilizados en internet
Tradicionalmente el navegador más utilizado de internet ha sido Internet Explorer, esta ventaja es debido a su característica de estar integrado en todas las instalaciones de Windows.

Durante los últimos años esta ventaja disminuye cada vez más, pese a las mejoras implementadas en la aplicacion.
La disminución de su empleo por los usuarios se debe a la popularidad alcanzada por otros navegadores alternativos, que han conseguido superarlo en velocidad y rendimiento.

Algunos sitios de internet están especializados con la recopilación de estadísticas del uso de los navegadores, destacan: <a href=http://gs.statcounter.com/ target="_blank">StatCounter</a> (quizás el más popular), NetMarketShare y GlobalStats.
No obstante los resultados no son absolutos, factores como la zona geográfica, los sitios donde se muestrea el tráfico y otros influyen.

Nosotros solo podemos asegurar cuales son los navegadores más usados para entrar a nuestro sitio, usando las estadísticas que nos ofrece el servicio de Google Analytics. Quizás no representan la realidad del tráfico global, pero da una idea aproximada.

Los navegadores más usados para entrar a NorfiPC son los siguientes ordenados por su empleo:

* Google Chrome (alrededor del 65% del tráfico). Navegador de Google para PC y dispositivos portables.
* Android Browser. Navegador incluido en dispositivos que usan el SO Android.
* Safari. Navegador incluido en dispositivos de Apple como el IPhone e iPad, aunque también está disponible para la computadora.
* Mozilla Firefox. Navegador libre de internet para PC y dispositivos portables.
* Opera Mini. (Dispositivos portables).
* Internet Explorer. Incluido en Windows XP, Vista, 7 y 8.
* Opera (para PC).

Otros navegadores que constituyen menos del 1% del total del tráfico son: UC Browser, BlackBerry (dispositivos portables), Microsoft Edge (incluido en Windows 10), MxNitro de Maxthon (para PC) y Vivaldi (para PC).


### Características de los principales navegadores web


#### Características y cualidades de Google Chrome
* Navegador minimalista, es decir posee las funciones esenciales y básicas por lo que es ideal para personas con poco dominio en la navegación web.
* Velocidad súper-rápida del navegador, para eso emplea recursos como un motor de renderizado de Javascript V8 y prefetching (precarga) de DNS para mejorar el rendimiento en la carga de páginas web. Esta última característica es una innovación reciente, Google Chrome es el único navegador que la implementa por defecto, resuelve la relación IP/Nombre de dominio y la mantiene en su cache cierto tiempo por si es solicitada nuevamente. El sistema tradicional usado hasta ahora por los otros navegadores, es que Windows es el que la almacena y la libera al apagar el sistema.
Para ver el registro del prefetching de DNS que tienes actualmente en tu navegador escribe en la barra de direcciones **about:dns** te mostrará la dirección url, el nombre de host, tiempo de respuesta, hora a la que se resolvió, etc.
* Es el navegador más favorecido a la hora de hacer una búsqueda web, solo es necesario escribir la palabra o termino de búsqueda en la barra de direcciones que es multiuso.
* Permite ver estadísticas de la memoria consumida en cada pestaña con sus detalles, inclusive la que consumen otros navegadores si se están usando simultáneamente en la misma PC. Para eso abre una nueva pestaña (CONTROL+T) y escribe: **about:memory**.
* Google ofrece la actualización automática del navegador, lo que asegura siempre tener instalada la última versión estable y tener disponible la blacklist, lista que contiene información sobre phishing (sitios de suplantación de identidad) y malware más reciente en la red.
* Ofrece similar a Internet Explorer la opción de navegar en forma de Incognito, las páginas a las que se accedan no quedarán registradas en el historial del navegador ni en el historial de búsquedas, y tampoco dejarán otros rastros en el equipo (como cookies).
* En la página de inicio (como introdujo Opera) muestra miniaturas de las páginas visitadas, lo que puedes usar como una especie de Bookmarks involuntarios.

#### Características, cualidades y ventajas de usar el navegador Internet Explorer

* Brinda un elevado nivel de seguridad, que a veces llega a ser desesperante pero muy efectivo, posee distintos niveles de seguridad dividido en zonas cada una con sus limitaciones.
* La exploración de InPrivate permite navegar por Internet sin guardar ningún dato de la sesión de exploración, como cookies, archivos temporales de Internet, historial y otros datos.
* Es el único navegador que ofrece soporte en las páginas web para ActiveX y VBScript.
* Compatible con paginas HTA, formato de páginas web que permiten interactuar con programas y archivos del equipo donde se ejecuten.
* Soporte para los applets de Java que funcionan mejor que en cualquier otro navegador.
* Al ser el explorador nativo de Windows puede descargar e instalar updates (actualizaciones) para el sistema operativo desde el sitio de Microsoft.
* Los Bookmarks, marcadores o favoritos son legítimos accesos directos que se pueden editar y modificar fácilmente por el usuario.
* A partir de la versión 8 incorpora nuevas funcionalidades como el uso de las WebSlice (Icono de color verde que puedes ver en esta página, en la barra de comandos del navegador), compatibilidad con el estándar CSS, la posibilidad de elegir otros motores de búsquedas, disponibilidad de multitud de complementos (llamados aceleradores), etc.

#### Características, cualidades y ventajas de usar el navegador Mozilla Firefox

* Software de código abierto es un navegador totalmente configurable, tanto su funcionamiento, configuración, aspecto, add-ons o complementos. En su sitio web Mozilla ofrece toda la información técnica necesaria a desarrolladores y usuarios en general.
* Alto nivel de seguridad, efectiva la protección contra el spyware y otros tipos de malware, bloqueo asegurado contra pop-up y otras formas de publicidad comunes en la web, ActiveX no está permitido por considerarse un riesgo.
* Sus desarrolladores aseguran una fuente casi infinita de extensiones hechas para todo tipo de propósito.
* Permite crear y utilizar simultáneamente varios perfiles o preferencias en el mismo navegador, lo cual en la práctica es muy útil, es decir puedes tener una configuración diferente para usar Firefox en tus tareas laborales o estudiantiles y otra para tu uso privado o familiar, todo con el mismo navegador en la misma PC.

#### Opera
Es reconocido por su velocidad, seguridad, soporte de estándares (especialmente CSS), tamaño reducido y constante innovación.
Implementó ya desde sus primeras versiones la navegación por pestañas, el Speed Dial, los movimientos del ratón en la navegación, personalización por sitio, y la vista en miniatura por pestaña, tiene su versión para móviles y tabletas.
Las últimas versiones de Opera usa el motor WebKit, el mismo que Chrome y Safari.
Usa un nuevo diseño, bastante más limpio.
La migración a Chromium trae una mejor compatibilidad, más rapidez y ahora las extensiones usan el mismo formato de Google Chrome.
Se introducen dos nuevas funciones: Discover y Stash.
La primera es una pestaña con las noticias más relevantes del día que se puede personalizar.
Stash es para guardar páginas y después poderlas rescatar, solo es necesario dar un clic en el icono del corazón.
La función Opera Turbo, ahora es llamado "Off the road" o "Todo terreno", ahora soportan SPDY para acelerar aún más la navegación.

#### Safari
Es el complemento indispensable para los usuarios de Mac OS X, para donde fue ideado inicialmente que iba a ejecutarse y donde están la gran mayoría de usuarios que lo utilizan dentro de alrededor del 4% de usuarios en el mundo. Es un navegador que se ha distinguido por su desempeño, velocidad y soporte de los estándares. Aunque Safari no es tan reconocido para usuarios de otros sistemas operativos diferentes a Mac OS, se ha vuelto una opción interesante desde que salió su versión para Windows.
Es el navegador predeterminado de todos los iDevice (iPhone, iTouch y iPad), pero es usado también en varios teléfonos y otros dispositivos portables que no son de Apple, por lo que es actualmente el navegador más utilizado en los móviles.


### Los navegadores más usados en teléfonos celulares y tabletas
A diferencia de en la computadora, los usuarios de los teléfonos o tabletas generalmente usan el navegador incluido en su dispositivo, aunque siempre existe la opción de elegir uno diferente al predeterminado.
Los navegadores más usados en los dispositivos portables, porque están incluidos en el sistema operativo son: Safari, Android Browser, Opera Mini y Blacberry.


### Navegadores alternos para usar en dispositivos portables
Actualmente es fácil instalar otros navegadores en los teléfonos celulares y tabletas, solo descargando la aplicación.
Los más descargados y usados son:

* Google Chrome
* Firefox
* Dolphin. Navegador muy eficiente y rápido disponible para el iPhone y Android, incluye características propias que lo hacen muy original como son el sonar (navegación mediante la voz), el panel para gestos (navegación mediante gestos), navegación de incognito, etc. Está disponible en GooglePlay y en la AppStore. http://dolphin-browser.com/
* UCBrowser. Navegador popular en Asia que según se dice está planeando la conquista del Oeste. Está disponible para Android, iOs, Java y Symbian, es extremadamente rápido y eficaz a la hora de navegar por Internet, teniendo más de 300 millones de usuarios. http://www.ucweb.com/

# OBJETIVOS DEL W3C
El objetivo del W3C es guiar la Web hacia su máximo potencial a través del desarrollo de protocolos y pautas que aseguren el crecimiento futuro de la Web. Debajo tratamos importantes aspectos de este objetivo, los cuales promueven la visión del W3C de Web Única.

# Principios
Los siguientes principios guían el trabajo del W3C.

## Web para todo el mundo
El valor social que aporta la Web, es que ésta hace posible la comunicación humana, el comercio y las oportunidades para compartir conocimiento. Uno de los objetivos principales del W3C es hacer que estos beneficios estén disponibles para todo el mundo, independientemente del hardware, software, infraestructura de red, idioma, cultura, localización geográfica, o habilidad física o mental.

## Web desde cualquier dispositivo
La cantidad de dispositivos diferentes para acceder a la Web ha crecido exponencialmente. Actualmente, los teléfonos móviles, teléfonos inteligentes, PDAs, sistemas de televisión interactiva, sistemas de respuesta de voz, puntos de información e incluso algunos pequeños electrodomésticos pueden acceder a la Web.

## Visión
La visión del W3C para la Web incluye la participación, compartir conocimiento y, de esta forma, construir confianza a gran escala.

## Web de los Autores y Consumidores
La Web fue creada como una herramienta de comunicación para permitir el intercambio de información entre todo el mundo y desde cualquier lugar. Durante muchos años, para muchas personas la Web fue una herramienta de "solo lectura". Los blogs y wikis trajeron más autores a la Web y las redes sociales emergieron del próspero mercado para crear contenido y personalizar las experiencias en la Web. Los estándares del W3C han apoyado esta evolución gracias a la robusta arquitectura y a los principios de diseño.

## Web de los Datos y Servicios
Algunas personas ven la Web como un repositorio gigante de datos enlazados mientras otros como un conjunto enorme de servicios que intercambian mensajes. Ambas vistas son complementarias y los requisitos de cada aplicación pueden ser los mejores determinantes para decidir que aproximación elegir para solucionar progresivamente los problemas complejos mediante tecnología Web.

## Web de Confianza
La Web ha cambiado la forma en la que nos comunicamos. Al ocurrir esto, la naturaleza de nuestras relaciones sociales ha cambiado también. En la actualidad, las personas se "conocen en Internet", y llevan a cabo relaciones personales y comerciales sin haberse visto en persona anteriormente. El W3C reconoce que la confianza es un fenómeno social, pero el diseño de las tecnologías puede fomentar la confianza y la responsabilidad. A medida que cualquier actividad se hace a través de la Web, cada vez es más importante apoyar las interacciones complejas entre distintas partes alrededor del mundo.

# ¿Qué es Github Pages?

GitHub Pages es un servicio de alojamiento gratuito de GitHub para páginas web públicas y estáticas. Es mayormente utilizado para alojar blogs personales y sitios web de proyectos. Es una plataforma para blogging avanzado, ya que para su uso debes estar familiarizado con GitHub y por ende con la terminal o la linea de comandos.

La red esta llena de blogs, de propósitos tan diversos como sus temáticas. Cualquier persona con un poco de curiosidad puede hacerse un blog sencillo con herramientas como Blogspot y Tumblr, o algo un poco más elaborado con WordPress, una de las plataformas más populares. Sin embargo, siempre es importante que hayan alternativas y más si son de calidad y gratuitas.

Para crear una página  disponemos de la opción de generar de forma automática las páginas utilizando una herramienta gráfica, pero en este caso nos vamos a centrar en la creación y modificación de páginas web usando la línea de comandos con el comando git.

Tenemos dos alternativas para crear una página web con esta herramienta:

* **Páginas de usuario u organización:** Es necesario crear un repositorio especial donde se va a almacenar todos el contenido del sitio web. Si por ejemplo el nombre de usuario de Github es josedom24, el nombre del repositorio debe ser josedom24.github.io. Todos los ficheros que se van a publicar deben estar en la rama “master“. Por último indicar que la URL para acceder a la ṕagina sería http://josedom24.github.io.

* **Páginas de proyecto o repositorio:** A diferencia de las anteriores están asociada a cualquier repositorio que tengamos en Github (por ejemplo supongamos que el repositorio se llama “prueba“). En este caso los ficheros que se van a publicar deben estar en una rama del proyecto llamada gh-pages. La URL de acceso al sitio será http://josedom24.github.io/prueba.

# Creación manual de páginas

Mientras que las páginas de usuario son fáciles de crear, ya que simplemente debemos crear el repositorio y clonarlo en nuestro equipo (git clone) y empezar a crear ficheros que estarán guardados en la rama master, las páginas de repositorio pueden ser un poco más complejas ya que hay que crear la nueva rama que tenemos que llamar gh-pages, siguiendo el manual de Github Pages los pasos a dar son los siguientes:

```
$ git clone https://github.com/user/repository.git
# Clone our repository
# Cloning into 'repository'...
# remote: Counting objects: 2791, done.
# remote: Compressing objects: 100% (1225/1225), done.
# remote: Total 2791 (delta 1722), reused 2513 (delta 1493)
# Receiving objects: 100% (2791/2791), 3.77 MiB | 969 KiB/s, done.
# Resolving deltas: 100% (1722/1722), done.
```

A continuación tenemos que crear la nueva rama:

```
$ cd repository
$ git checkout --orphan gh-pages
# Creates our branch, without any parents (it's an orphan!)
# Switched to a new branch 'gh-pages'
$ git rm -rf .
# Remove all files from the old working tree
# rm '.gitignore'
```

Para terminar subiendo el primer fichero de nuestra página:

```
$ echo "My GitHub Page" > index.html
$ git add index.html
$ git commit -a -m "First pages commit"
$ git push origin gh-pages
```

# Cómo podemos construir nuestras páginas web

La forma más sencilla de construir nuestro sitio es subir a nuestro repositorio todos los ficheros necesarios: ficheros html, hojas de estilos, javascript, imágenes, etc. Si sólo tuviéramos esta opción de edición de páginas no tendríamos grandes ventajas para decidirnos a escoger este servicio de hosting.

Lo que realmente hace esta herramienta una opción muy potente es que Github Pages suporta Jekyll, herramienta escrita en Ruby que nos permite generar, de una forma muy sencilla, ficheros HTML estáticos. Aunque esta herramienta esta pensada para generar blogs, nosotros vamos a utilizar algunas de sus funcionalidades para crear páginas estáticas convencionales.

---------

## Usando Jekyll para crear páginas web

La principal característica de Jekylls es la generación de html estático a partir de dos recursos muy simples:

* Plantillas (templates): Ficheros que contienen el esqueleto de las página html que se van a generar. Estos ficheros normalmente se escriben siguiendo la sintaxis de Liquid.

* Ficheros de contenido: Normalmente escritos en sintaxis Markdown y que contienen el contenido de la página que se va a generar.

Por lo tanto una vez que tengo definidas mis plantillas, lo único que tengo que hacer es centrarme en  el contenido escribiendo los diferentes de ficheros de contenido.

----------

## Usando plantillas

Las plantillas son ficheros de texto con extensión html. Deben estar guardados en un directorio _layouts creado en la raíz de nuestro repositorio. Además del contenido html de las páginas que se van a generar, se pueden indicar distintas etiquetas que se sustituirán por diferentes valores. Veamos algunas etiquetas:

* La etiqueta más importante es {{ content }} que es sustituida por el contenido que definimos en los ficheros de contenido.

* La etiqueta {{ site.path }} será sustituida por el path del repositorio.

* Además se podrá definir en los ficheros de contenidos distintas variables que podrán ser sustituidas con etiquetas del tipo {{ page.nombredevariable }}.

Todas las referencia a ficheros de hojas de estilo, javascripts o imágenes que se definan en la plantilla deben estar guardados en nuestro repositorio.

-----------

## Usando Markdown para escribir el contenido de nuestras páginas

Los distintos contenidos de nuestras páginas serán definidos en ficheros Maarkdown con extensión md. La sintaxis de este lenguaje de marcas es muy sencilla y fácilmente convertible a html. Para practicar las distintas opciones puedes usar este editor online.

Sin entrar a definir la sintaxis del lenguaje, nos vamos a fijar en la primera parte de los ficheros donde se define la plantilla que se va a utilizar, y las distintas variables que son accesibles desde la plantilla.

```
---
layout: index

title: Servicios de red
tagline: CFGM SMR
---
```

Con la variable layout indicamos el nombre del fichero html que corresponde a la plantilla que se va a usar para generar la página. Además hemos definido dos variables cuyo valor es accesible desde la plantilla con las etiquetas {{ pages.title }} y {{ page.tagline }}.

Por último indicar como se accede a las distintas páginas, suponiendo que tenemos definido una página de usuario en la URL josedom24.github.io, si tenemos un fichero en la raíz proyecto.md, sería accesible con la URL josedom24.github.io/proyecto. Si el fichero proyecto.md esta dentro de una carpeta llamada “ejemplo”, sería accesible con la URL josedom24.github.io/ejemplo/proyecto. De forma similar a como funcionan los servidores web si tenemos un fichero index.md no será necesario indicar el nombre en la URL.
