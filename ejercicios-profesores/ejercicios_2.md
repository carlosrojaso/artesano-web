## Ejercicios Clase 2

### 1
* Crear tabla
```html
<table class="table">
    <caption>Lista de alumnos.</caption>
    <thead>
        <tr>
          <th>#</th>
          <th>Nombre</th>
          <th>Apellido</th>
          <th>Usuario</th>
        </tr>
      </thead>
      <tbody>
        <tr>
          <th>1</th>
          <td>Daniel</td>
          <td>López</td>
          <td>@danlopez</td>
        </tr>
        <tr>
          <th>2</th>
          <td>Laura</td>
          <td>Martinez</td>
          <td>@lauram</td>
        </tr>
        <tr>
          <th>3</th>
          <td>Simón</td>
          <td>Luna</td>
          <td>@simonlunar</td>
        </tr>
      </tbody>
    </table>
```

### 2
* Crear un formulario

```html
<form action="action_page.php">
  <fieldset>
    <legend>Información Personal:</legend>
    Nombre:<br>
    <input type="text" name="firstname" value="Nombre"><br>
    Apellido:<br>
    <input type="text" name="lastname" value="Apellido"><br><br>
    <input type="submit" value="Submit">
  </fieldset>
</form>
```

### 3
* Crear una etiqueta video.

```html
<video controls>
  <source src="http://www.w3schools.com/html/mov_bbb.ogg" type="video/ogg">
  <source src="http://www.w3schools.com/html/mov_bbb.mp4" type="video/mp4">
  Tu navegador no implementa el elemento <code>video</code>.
</video>
```
