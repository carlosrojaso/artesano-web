
```CSS
  $color_principal: #556789;
  $color_secundario: #445678;
  $auxiliar: #667789;

  @mixin border-radius($radius) {
    -webkit-border-radius: $radius;
       -moz-border-radius: $radius;
        -ms-border-radius: $radius;
            border-radius: $radius;
  }

  .container {
    width: 600px / 960px * 100%;
  }
```
