
```html
<!DOCTYPE html>
  <html>
    <head>
      <meta charset="UTF-8">
      <title>Bootstrap</title>
      <link rel="stylesheet" href="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/css/bootstrap.min.css" integrity="sha384-BVYiiSIFeK1dGmJRAkycuHAHRg32OmUcww7on3RYdg4Va+PmSTsz/K68vbdEjh4u" crossorigin="anonymous">
      <script src="https://maxcdn.bootstrapcdn.com/bootstrap/3.3.7/js/bootstrap.min.js" integrity="sha384-Tc5IQib027qvyjSMfHjOMaLkfuWVxZxUPnCJA7l2mCWNIpG9mGCD8wGNIcPD7Txa" crossorigin="anonymous"></script>
    </head>
    <body>
      <nav class="navbar navbar-default" id="coder-nav">
        <div class="container-fluid">
          <div class="navbar-header">
            <button type="button" class="navbar-toggle collapsed" data-toggle="collapse" data-target="#bs-example-navbar-collapse-1" aria-expanded="false">
              <span class="sr-only">Toggle navigation</span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
              <span class="icon-bar"></span>
            </button>
            <a class="navbar-brand" href="#">Brand</a>
          </div>

          <div class="collapse navbar-collapse" id="bs-example-navbar-collapse-1">
            <ul class="nav navbar-nav navbar-right">
              <li><a href="#">Link</a></li>
              <li class="dropdown">
                <a href="#" class="dropdown-toggle" data-toggle="dropdown" role="button" aria-haspopup="true" aria-expanded="false">Menu Desplegable <span class="caret"></span></a>
                <ul class="dropdown-menu">
                  <li><a href="#">Info</a></li>
                  <li><a href="#">Contacto</a></li>
                  <li><a href="#">Sobre Nosotros</a></li>
                </ul>
              </li>
            </ul>
          </div><!-- /.navbar-collapse -->
        </div><!-- /.container-fluid -->
      </nav>

      <div id="carousel-challenge" class="carousel slide" data-ride="carousel">
        <!-- Indicators -->
        <ol class="carousel-indicators">
          <li data-target="#carousel-challenge" data-slide-to="0" class="active"></li>
          <li data-target="#carousel-challenge" data-slide-to="1"></li>
          <li data-target="#carousel-challenge" data-slide-to="2"></li>
        </ol>

        <!-- Wrapper for slides -->
        <div class="carousel-inner" role="listbox">
          <div class="item active">
            <img src="..." alt="...">
            <div class="carousel-caption">
              ...
            </div>
          </div>
          <div class="item">
            <img src="..." alt="...">
            <div class="carousel-caption">
              ...
            </div>
          </div>
          ...
        </div>

        <!-- Controls -->
        <a class="left carousel-control" href="#carousel-challenge" role="button" data-slide="prev">
          <span class="glyphicon glyphicon-chevron-left" aria-hidden="true"></span>
          <span class="sr-only">Previous</span>
        </a>
        <a class="right carousel-control" href="#carousel-example-generic" role="button" data-slide="next">
          <span class="glyphicon glyphicon-chevron-right" aria-hidden="true"></span>
          <span class="sr-only">Next</span>
        </a>
      </div>

      <div class="container-fluid" data-spy="scroll" data-target="#coder-nav">
        <div class="row">
          <div class="col-sm-12 col-md-4">
            <button type="button" class="btn btn-primary btn-lg" data-toggle="modal" data-target="#columna1">
              Columna 1
            </button>
          </div>
          <div class="col-sm-12 col-md-4">
            <button type="button" class="btn btn-primary btn-lg" data-toggle="modal" data-target="#columna2">
              Columna 2
            </button>
          </div>
          <div class="col-sm-12 col-md-4">
            <button type="button" class="btn btn-primary btn-lg" data-toggle="modal" data-target="#columna3">
              Columna 3
            </button>
          </div>
        </div>

        <div class="row">
          <div class="col-sm-12 col-md-6 col-lg-3">
            Columna 1
          </div>
          <div class="col-sm-12 col-md-6 col-lg-3">
            Columna 2
          </div>
          <div class="col-sm-12 col-md-6 col-lg-3">
            Columna 3
          </div>
          <div class="col-sm-12 col-md-6 col-lg-3">
            Columna 4
          </div>
        </div>

        <div class="row">
          <div class="col-sm-12">
            Sección única
          </div>
        </div>

        <!-- Modal Columna 1-->
        <div class="modal fade" id="columna1" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
          <div class="modal-dialog" role="document">
            <div class="modal-content">
              <div class="modal-header">
                <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
                <h4 class="modal-title" id="myModalLabel">Modal Columna 1</h4>
              </div>
              <div class="modal-body">
                ...
              </div>
              <div class="modal-footer">
                <button type="button" class="btn btn-default" data-dismiss="modal">Cerrar</button>
                <button type="button" class="btn btn-primary">Guardar</button>
              </div>
            </div>
          </div>
        </div>

        <!-- Modal Columna 2-->
        <div class="modal fade" id="columna2" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
          <div class="modal-dialog" role="document">
            <div class="modal-content">
              <div class="modal-header">
                <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
                <h4 class="modal-title" id="myModalLabel">Modal Columna 2</h4>
              </div>
              <div class="modal-body">
                ...
              </div>
              <div class="modal-footer">
                <button type="button" class="btn btn-default" data-dismiss="modal">Cerrar</button>
                <button type="button" class="btn btn-primary">Guardar</button>
              </div>
            </div>
          </div>
        </div>

        <!-- Modal Columna 3-->
        <div class="modal fade" id="columna3" tabindex="-1" role="dialog" aria-labelledby="myModalLabel">
          <div class="modal-dialog" role="document">
            <div class="modal-content">
              <div class="modal-header">
                <button type="button" class="close" data-dismiss="modal" aria-label="Close"><span aria-hidden="true">&times;</span></button>
                <h4 class="modal-title" id="myModalLabel">Modal Columna 3</h4>
              </div>
              <div class="modal-body">
                ...
              </div>
              <div class="modal-footer">
                <button type="button" class="btn btn-default" data-dismiss="modal">Cerrar</button>
                <button type="button" class="btn btn-primary">Guardar</button>
              </div>
            </div>
          </div>
        </div>

      </div>
    </body>
  </html>
```
