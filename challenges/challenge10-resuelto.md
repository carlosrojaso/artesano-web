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
          <nav class="navbar navbar-default">
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
          <div class="jumbotron">
            <div class="container">
              <h1>CoderHouse</h1>
              <p>La mejor manera de aprender a programar</p>
              <p><a class="btn btn-primary btn-lg" href="#" role="button">Comienza Ya!</a></p>
            </div>
          </div>
          <div class="container-fluid">
            <div class="row">
              <div class="col-sm-12 col-md-4">
                Columna 1
              </div>
              <div class="col-sm-12 col-md-4">
                Columna 2
              </div>
              <div class="col-sm-12 col-md-4">
                Columna 3
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
          </div>
        </body>
      </html>

