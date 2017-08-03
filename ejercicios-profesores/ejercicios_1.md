# Ejercicios Clase 1

### 1
* Vamos a crear un documento html

```html
<!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>Mi primer sitio web</title>
        </head>
        <body>
            ¡Este es mi primer sitio web!
        </body>
    </html>
```

### 2
* Vamos a utilizar etiquetas que modifiquen el texto

```html
	<p>
		<strong> negrita </strong>
		<em> Cursiva </em>
		<del> Subrayado </del>
		<big> Grande </big>
		<small> pequeño </small>
		Esto es un <sub> subíndice </sub>
		Y esto un <sup> superíndice </sup>
	</p>
```

### 3
* El uso de las etiquetas semanticas es de gran ayuda en HTML5

```html
<body>

  <header>
    <h1>Bienvenido a nuestro sitio Web</h1>
    <p>Aquí nuestro logo y slogan</p>
  </header>

  <nav>
    <header>
      <h2>Seleccione su interés</h2>
    </header>
    <ul>
      <li>Menu 1</li>
      <li>Menu 2</li>
      <li>Menu 3</li>
    </ul>
  </nav>

  <article>
    <header>
      <h1>Titulo del Articulo (e.g. "Ejemplo 1")</h1>
      <h2>Subtitulo del Articulo</h2>
    </header>

    <section>
      <h3>Primera parte lógica (e.g. "Ejemplo 1.1")</h3>
      <p>Parrafo uno</p>

      <h4>Subtitulo de la sección 1</h4>
      <p>Parrafo 2 de la sección</p>
    </section>

    <section>
      <h3>Segunda Sección Lógica (e.g. "Ejemplo 1.2")</h3>
      <p>Parrafo 1 de la sección 2</p>
      <p>Parrafo 2 de la sección 2</p>
    </section>

    <footer>
      <h4>Biografía</h4>
      <p>Parrafó del pie del articulo</p>
    </footer>

  </article>

  <aside>

    <h2>Conocenos Mejor</h2>

    <section>
      <h3>Post Populares</h3>
      <ul>...</ul>
    </section>

    <section>
      <h3>Auspiciadores</h3>
      <ul>...</ul>
    </section>

    <section>
      <h3>Testimonios</h3>
      <ul>...</ul>
    </section>

  </aside>

  <footer>
    <ul>
      <li>Copyright</li>
      <li>Social Media Links</li>
    </ul>
  </footer>

</body>
```
