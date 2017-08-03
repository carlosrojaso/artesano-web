* Vamos a crear nuestros primeros contenedores.

````html
<!DOCTYPE html>
<html>
<head>
<style>
.flex-container {
    display: -webkit-flex;
    display: flex;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}

.flex-item {
    background-color: Black;
    color: white;
    width: 100px;
    height: 100px;
    margin: 10px;
}
</style>
</head>
<body>

<div class="flex-container">
  <div class="flex-item">El item 1</div>
  <div class="flex-item">El item 2</div>
  <div class="flex-item">El item 3</div>
</div>

</body>
</html>

````

* Vamos a crear unos contenedores con row-reverse

````html
<!DOCTYPE html>
<html>
<head>
<style>
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: row-reverse;
    flex-direction: row-reverse;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}

.flex-item {
    background-color: black;
    color: white;
    width: 100px;
    height: 100px;
    margin: 10px;
}
</style>
</head>
<body>

<div class="flex-container">
  <div class="flex-item">El item 1</div>
  <div class="flex-item">El item 2</div>
  <div class="flex-item">El item 3</div>
</div>

</body>
</html>


````

* Vamos a crear unos contenedores con dirección column.

````html
<!DOCTYPE html>
<html>
<head>
<style>
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-flex-direction: column;
    flex-direction: column;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}

.flex-item {
    background-color: black;
    color: white;
    width: 100px;
    height: 100px;
    margin: 10px;
}
</style>
</head>
<body>

<div class="flex-container">
  <div class="flex-item">El item 1</div>
  <div class="flex-item">El item 2</div>
  <div class="flex-item">El item 3</div>
</div>

</body>
</html>

````

* Vamos a alinear el contenido de algunos flex-items.

````html
<!DOCTYPE html>
<html>
<head>
<style>
.flex-container {
    display: -webkit-flex;
    display: flex;
    -webkit-justify-content: flex-end;
    justify-content: flex-end;
    width: 400px;
    height: 250px;
    background-color: lightgrey;
}

.flex-item {
    background-color: black;
    color: white;
    width: 100px;
    height: 100px;
    margin: 10px;
}
</style>
</head>
<body>

<div class="flex-container">
  <div class="flex-item">El item 1</div>
  <div class="flex-item">El item 2</div>
  <div class="flex-item">El item 3</div>
</div>

</body>
</html>

````

* Podemos variar los ejercicios anteriores con variaciones de las propiedades.

```
justify-content: flex-start | flex-end | center | space-between | space-around;
```

```
flex-direction: row | row-reverse | column | column-reverse;
```
