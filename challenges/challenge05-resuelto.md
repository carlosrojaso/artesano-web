```html
<!DOCTYPE html>
    <html>
        <head>
            <meta charset="UTF-8">
            <title>Colores</title>
            <style>
              .container{
                  display: flex;
                  flex-direction: row-reverse;
              }
              .clase-1{
                  background-color: #000;
                  font-size: 18px;
                  color: #00f;
                  flex-grow: 1;
              }
              .clase-2{
                  background-color: #ff5588;
                  font-size: 22px;
                  color: green;
                  font-family: sans-serif;
                  flex-grow: 1;
              }
              .clase-3{
                  background-color: blue;
                  font-size: 12px;
                  color: yellow;
                  font-family: monospace;
                  flex-grow: 2;
              }
              .clase-4{
                  background-color: rgb(15,64,0);
                  font-size: 1.5em;
                  color: #3c27bd;
                  flex-grow: 1;
              }
              .clase-5{
                  background-color: rgb(34,56,200);
                  font-size: 0.8em;
                  color: rgb(146, 175, 136);
                  flex-grow: 1;
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

# Efectos
* Agregar un tipo de transición diferente a los 3 elementos
* Poner de color de fondo un gradiente circular en el elemento central
* Crear una animación al pasar el mouse sobre algún elemento de la página

## Resolución

```html
 <!DOCTYPE html>
  <html>
      <head>
          <meta charset="UTF-8">
          <title>Colores</title>
          <style>
            @keyframes cambioColor {
                from {background-color: blue;}
                to {background-color: yellow;}
            }
            .clase-1{
                background-color: #000;
                font-size: 18px;
                color: #00f;
                transition: width 2s;
            }
            .clase-2{
                background-color: radial-gradient(red, yellow, green);;
                font-size: 22px;
                color: green;
                font-family: sans-serif;
                transition: height 2s;
            }
            .clase-3{
                background-color: blue;
                font-size: 12px;
                color: yellow;
                font-family: monospace;

            }
            .clase-1:hover{
                width: 400px;
            }
            .clase-2:hover{
                height: 300px;
            }
            .clase-3:hover{
                animation-name: cambioColor;
                animation-duration: 4s;
            }
          </style>
      </head>
      <body>
        <div class="clase-1">
          Primer Elemento
        </div>
        <div class="clase-2">
          Segundo Elemento
        </div>
        <div class="clase-3">
          Tercer Elemento
        </div>
      </body>
  </html>
```
