<template>
  <head>
  <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css">
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet"
      integrity="sha384-QWTKZyjpPEjISv5WaRU9OFeRpok6YctnYmDr5pNlyT2bRjXh0JMhjY6hW+ALEwIH" crossorigin="anonymous">
  <title>Motos Deportivas</title>
</head>

<body>
  <div class="container">
      <nav class="navbar navbar-expand-lg" data-bs-theme="dark" style="background: url('https://www.shutterstock.com/image-photo/motorcycle-parked-alone-on-sunny-260nw-2153623869.jpg') no-repeat center center; background-size: cover; padding: 15px;">
          <div class="container-fluid" style="background: rgba(2, 2, 2, 0.5); padding: 10px; border-radius: 10px;">
              <a class="navbar-brand text-white" href="#">Motos Deportivas</a>
              <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
                  aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
                  <span class="navbar-toggler-icon"></span>
              </button>
              <div class="collapse navbar-collapse" id="navbarNav">
                  <ul class="navbar-nav">
                      <li class="nav-item">
                          <a class="nav-link active text-white" aria-current="page" href="#">
                              <i class="bi bi-house-fill"></i> Inicio
                          </a>
                      </li>
                      <li class="nav-item">
                          <a class="nav-link text-white" href="#objetivo">
                              <i class="bi bi-bullseye"></i> Objetivo
                          </a>
                      </li>
                      <li class="nav-item">
                          <a class="nav-link text-white" href="#tipos">
                              <i class="bi bi-lightning-fill"></i> Tipos
                          </a>
                      </li>
                      <li class="nav-item">
                          <a class="nav-link text-white" href="#historia">
                              <i class="bi bi-book-half"></i> Historia
                          </a>
                      </li>
                  </ul>
              </div>
              
          </div>
      </nav>

      <div class="card mt-3">
          <div style="height: 630px;" class="card">
          <div class="card-body">
              <div id="carouselExample" class="carousel slide">
                  <div class="carousel-inner">
                      <div class="carousel-item active">
                          <img src="https://pueyrredonmotos.com/wp-content/uploads/2018/01/Screenshot_1-9.png"
                              class="d-block w-100" alt="..." style="height: 600px; width: 400px;">
                      </div>
                      <div class="carousel-item">
                          <img src="https://static.wixstatic.com/media/ff08fe_0d8829b5e1de418c8392a2b813eeaa73~mv2.png/v1/fill/w_1920,h_960,al_c/ff08fe_0d8829b5e1de418c8392a2b813eeaa73~mv2.png"
                              class="d-block w-100" alt="..." style="height: 600px;">
                      </div>
                      <div class="carousel-item">
                          <img src="https://upload.wikimedia.org/wikipedia/commons/thumb/4/4f/Kawasaki_Ninja_H2.jpg/640px-Kawasaki_Ninja_H2.jpg"
                              class="d-block w-100" alt="..." style="height: 600px;">
                      </div>
                  </div>
                  <button class="carousel-control-prev" type="button" data-bs-target="#carouselExample" data-bs-slide="prev">
                      <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                      <span class="visually-hidden">Previous</span>
                  </button>
                  <button class="carousel-control-next" type="button" data-bs-target="#carouselExample" data-bs-slide="next">
                      <span class="carousel-control-next-icon" aria-hidden="true"></span>
                      <span class="visually-hidden">Next</span>
                  </button>
              </div>
          </div>
          </div>
      </div>
      

      <div id="objetivo" class="mt-5">
     

                  <div class="card col-md-12 text-center" style="background-color: lightblue; border: 2px solid #007bff;">
                      <div class="card-header" style="background-color: #1074df; color: white;">
                  <h2>Objetivo</h2>
              </div>
              <div class="card-body">
                  <p>
                      El objetivo de esta página es dar a conocer los distintos tipos de motos deportivas
                      disponibles y proporcionar información para quienes aún no comprenden el concepto de
                      una moto deportiva. Buscamos que más personas se interesen y se conviertan en verdaderos
                      fanáticos de estas impresionantes máquinas.
                  </p>
              </div>
          </div>
      </div>

      <div id="tipos" class="mt-5 row">
          <div class="col-md-6">
              <div class="card text-center">
                  <div class="card-header" style="background-color: #ff3300; color: white;">
                      <h3>Superbike</h3>
                  </div>
                  <div class="card-body">
                      <img src="https://ducatimadrid.com/wp-content/uploads/2024/05/diferencias-entre-motogp-y-superbike.jpg.webp"
                          class="rounded-circle" alt="Superbike" style="width: 150px; height: 150px;">
                      <p>
                          Las Superbikes son motocicletas de alto rendimiento diseñadas para circuitos y calles.
                          Destacan por su potencia, aerodinámica y tecnología avanzada.
                      </p>
                      <button style="padding: 10px 20px; font-size: 16px; background-color: #e63946; color: white; border: none; border-radius: 20px; cursor: pointer;">
                          Más información
                      </button>
                  </div>
              </div>
          </div>
          <div class="col-md-6">
              <div class="card text-center">
                  <div class="card-header" style="background-color: #e08c0d; color: white;">
                      <h3>Sport Touring</h3>
                  </div>
                  <div class="card-body">
                      <img src="https://s7g10.scene7.com/is/image/ktm/MY23-890-SMT-Stage?wid=1000&dpr=off"
                          class="rounded-circle" alt="Sport Touring" style="width: 150px; height: 150px;">
                      <p>
                          Las motos Sport Touring combinan velocidad y comodidad para viajes largos, ofreciendo un
                          equilibrio entre rendimiento y ergonomía.
                      </p>
                      <button style="padding: 10px 20px; font-size: 16px; background-color: #ffb703; color: white; border: none; border-radius: 20px; cursor: pointer;">
                          Más información
                      </button>
                  </div>
              </div>
          </div>

          <div class="col-md-6 mt-3">
              <div class="card text-center">
                  <div class="card-header" style="background-color: #e7d910; color: white;">
                      <h3>HyperSport</h3>
                  </div>
                  <div class="card-body">
                      <img src="https://img.remediosdigitales.com/c88dfa/damon-hypersport-se/450_1000.jpg"
                          class="rounded-circle" alt="HyperSport" style="width: 150px; height: 150px;">
                      <p>
                          Las motos HyperSport son las más potentes y rápidas, diseñadas para la máxima velocidad y
                          rendimiento en pista y carretera.
                      </p>
                      <button style="padding: 10px 20px; font-size: 16px; background-color: #ffb703; color: white; border: none; border-radius: 20px; cursor: pointer;">
                          Más información
                      </button>
                      
                  </div>
              </div>
          </div>
          <div class="col-md-6 mt-3">
              <div class="card text-center">
                  <div class="card-header">
                      <h3>Formulario</h3>
                  </div>
                  <div class="card-body">
                      <form>
                          <div class="mb-3">
                              <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css">
                              <label for="nombre" class="form-label">
                                  <i class="bi bi-person-fill"></i> Nombre:</label>
                              <input type="text" class="form-control" id="nombre" placeholder="Tu nombre">
                          </div>

                          <div class="mb-3">
                              <link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/bootstrap-icons/font/bootstrap-icons.css">
                              <label for="email" class="form-label">
                                  <i class="bi bi-envelope-fill"></i> Correo Electrónico:
                              </label>
                              <input type="email" class="form-control" id="email" placeholder="Tu correo">
                          </div>

                         <div class="mb-3">
                           <label for="mensaje" class="form-label">
                              <i class="bi bi-motorcycle"></i> Detalles sobre otras motos:</label>
                              <textarea class="form-control" id="mensaje" rows="3" placeholder="Escribe aquí..."></textarea>
                          </div>

                          <button type="submit" class="btn btn-primary"><i class="bi bi-send"></i> Enviar
                            </button>
                      </form>
                  </div>
              </div>
          </div>
          
          <div id="historia" class="mt-5 row">
              <div class="col-md-12">
                  <div class="card text-center">
                      <div class="card-header" style="background-color: #4891da; color: white;">
                          <h3>Historia</h3>
                      </div>
                      <div class="card-body">
                          <img src="https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcQZZoCrc6iVuqfsJ2uyJ3pqP6PojiwyHGGyYA&s"
                              class="rounded-circle" alt="Sport Touring" style="width: 150px; height: 150px;">
          
                          <!-- Inicio del Carrusel -->
                          <div id="historiaCarousel" class="carousel slide mt-3" data-bs-ride="carousel">
                              <div class="carousel-inner">
                                  <div class="carousel-item active">
                                      <p>
                                          Las motos deportivas son motocicletas diseñadas para ofrecer alto rendimiento, 
                                          velocidad y agilidad. Se caracterizan por su aerodinámica avanzada, motores potentes 
                                          y chasis ligeros, ideales para circuitos de competición y carretera.
                                      </p>
                                  </div>
                                  <div class="carousel-item">
                                      <p>
                                          En la década de 1980, marcas como Honda, Yamaha y Kawasaki revolucionaron el mercado 
                                          con motos como la CBR, la R1 y la Ninja, elevando los estándares de velocidad y diseño.
                                      </p>
                                  </div>
                                  <div class="carousel-item">
                                      <p>
                                          Hoy en día, las motos deportivas incorporan tecnología avanzada como frenos ABS, 
                                          control de tracción y suspensiones electrónicas, ofreciendo una experiencia segura y emocionante.
                                      </p>
                                  </div>
                              </div>
          
                              <!-- Controles de navegación con efecto difuminado -->
                              <button class="carousel-control-prev" type="button" data-bs-target="#historiaCarousel" data-bs-slide="prev" 
                                  style="opacity: 0.5;">
                                  <span class="carousel-control-prev-icon" aria-hidden="true"></span>
                                  <span class="visually-hidden">Previous</span>
                              </button>
                              <button class="carousel-control-next" type="button" data-bs-target="#historiaCarousel" data-bs-slide="next" 
                                  style="opacity: 0.5;">
                                  <span class="carousel-control-next-icon" aria-hidden="true"></span>
                                  <span class="visually-hidden">Next</span>
                              </button>
                          </div>
                      </div>
                  </div>
              </div>
          </div>
          
                              
          

      </div>
  </div>
</body>

</template>
<style>
body {
  background: linear-gradient(to bottom, gray, red);
  color: black;
}
</style>