```html
<!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>BOX MODEL</title>
            <style>
              .BoxModel{
                  padding-top: 50%;
                  padding-left: 40%;
                  border-color: black;
                  border-width: 20px;
                  height: 75%;
                  width:75%;
                  margin: 40px;
              }
            </style>
        </head>
        <body>
          <div class="BoxModel">
            Caja
          </div>
        </body>
    </html>
```

# Posicionamiento
* Crear un contenedor con 5 elementos dentro (individualizar con colores o texto cada uno de los elementos interiores)
* Posicionar los primeros 3 elementos alineados a la derecha
* Posicionar los siguientes 2 elementos la izquierda

## Resolución

```html
<!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>Colores</title>
            <style>
              .clase-1{
                  background-color: #000;
                  font-size: 18px;
                  color: #00f;
                  float: right;
              }
              .clase-2{
                  background-color: #ff5588;
                  font-size: 22px;
                  color: green;
                  font-family: sans-serif;
                  float: right;
              }
              .clase-3{
                  background-color: blue;
                  font-size: 12px;
                  color: yellow;
                  font-family: monospace;
                  float: right;
              }
              .clase-4{
                  background-color: rgb(15,64,0);
                  font-size: 1.5em;
                  color: #3c27bd;
                  float: left;
              }
              .clase-5{
                  background-color: rgb(34,56,200);
                  font-size: 0.8em;
                  color: rgb(146, 175, 136);
                  float: left;
              }
            </style>
        </head>
        <body>
          <div class="container">
            <div class="clase-1">
              Primer Elemento
            </div>
            <div class="clase-2">
              Segundo Elemento
            </div>
            <div class="clase-3">
              Tercer Elemento
            </div>
            <div class="clase-4">
              Cuardo Elemento
            </div>
            <div class="clase-5">
              Quinto Elemento
            </div>
          </div>
        </body>
    </html>
```
