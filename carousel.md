# carrusel en Bootstrap 5

Us adjunto el codi per fer un carrusel a Bootstrap 5 amb 3 imatges, text descriptiu, butons per navegar entre imatges i butons per desplaçar-nos endavant i endarrere de la galeria.

Codi:

```
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1">
  <title>Carrusel Bootstrap 5</title>

  <!-- Enlace a Bootstrap 5 (CDN) -->
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/css/bootstrap.min.css" rel="stylesheet">
    <style>
        .carousel-item img {
            height: 600px;
            object-fit: cover; /* recorta sin deformar */
        }
    </style>
</head>
<body class="bg-light">

<div id="miCarrusel" class="carousel slide" data-bs-ride="carousel">

  <!-- 🔘 Botones indicadores -->
  <div class="carousel-indicators">
    <button type="button" data-bs-target="#miCarrusel" data-bs-slide-to="0" class="active" aria-current="true" aria-label="Imagen 1"></button>
    <button type="button" data-bs-target="#miCarrusel" data-bs-slide-to="1" aria-label="Imagen 2"></button>
    <button type="button" data-bs-target="#miCarrusel" data-bs-slide-to="2" aria-label="Imagen 3"></button>
  </div>

  <!-- 🖼️ Imágenes -->
  <div class="carousel-inner">
    <!-- Imagen 1 -->
    <div class="carousel-item active">
      <img src="wall1.jpg" class="d-block w-100 img-fluid" alt="Primera imagen">
      <div class="carousel-caption d-none d-md-block">
        <h5>Primera imagen</h5>
        <p>Texto descriptivo para la primera imagen.</p>
      </div>
    </div>

    <!-- Imagen 2 -->
    <div class="carousel-item">
      <img src="wall2.jpg" class="d-block w-100 img-fluid" alt="Segunda imagen">
      <div class="carousel-caption d-none d-md-block">
        <h5>Segunda imagen</h5>
        <p>Otro texto para la segunda imagen.</p>
      </div>
    </div>

    <!-- Imagen 3 -->
    <div class="carousel-item">
      <img src="wall3.jpg" class="d-block w-100 img-fluid" alt="Tercera imagen">
      <div class="carousel-caption d-none d-md-block">
        <h5>Tercera imagen</h5>
        <p>Texto para la tercera imagen del carrusel.</p>
      </div>
    </div>
  </div>

  <!-- ⏪⏩ Botones de navegación -->
  <button class="carousel-control-prev" type="button" data-bs-target="#miCarrusel" data-bs-slide="prev">
    <span class="carousel-control-prev-icon bg-dark rounded-circle p-3" aria-hidden="true"></span>
    <span class="visually-hidden">Anterior</span>
  </button>
  <button class="carousel-control-next" type="button" data-bs-target="#miCarrusel" data-bs-slide="next">
    <span class="carousel-control-next-icon bg-dark rounded-circle p-3" aria-hidden="true"></span>
    <span class="visually-hidden">Siguiente</span>
  </button>
</div>

<!-- Script de Bootstrap -->
<script src="https://cdn.jsdelivr.net/npm/bootstrap@5.3.3/dist/js/bootstrap.bundle.min.js"></script>
</body>
</html>
```

Les imatges són [wall1](wall1.jpg), [wall2](wall2.jpg) i [wall3](wall3.jpg).

## Canviar el tamany de les imatges

Les imatges són d'aquest estil:

```
<img class="d-block w-100 img-fluid">
```

Podem canviar la classe del tamany w-100 per un de més petit: w-50 (50% ample), w-75 (75% ample), w-auto (tamany original de la imatge).

Podem canviar l'altura de la imatge retallant la imatge sense deformar-la afegint aquest codi al HEAD del document:

```
.carousel-item img {
  height: 400px;
  object-fit: cover; /* recorta sin deformar */
}
```

## Els botons de navegació:

Els botons de fons són imatges SVG amb fons transparent, per donar-li color es pot utilitzar CSS ```background-color``` o classes de Boostrap:

A l'exemple tenim:
- bg-dark → fons negre (es pot canviar per bg-primary, bg-danger...).
- rounded-circle → fa el botó circular.
- p-3 → padding intern.

## El color de fons del carrusel:

Per canviar el color de fons podem afegir una classe de color de Boostrap o CSS.

```
<div id="miCarrusel" class="carousel slide bg-dark text-white" data-bs-ride="carousel">
```

A l'exemple el color el marca la classe bg-dark, podem canviar per bg-primary, bg-warning...

text-white fa que el text sigui blanc, podeu canviar el color de text també.

