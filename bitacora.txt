# Bitácora del sitio web "Rueda Libre"

Basada únicamente en el código enviado: 5 páginas HTML.

## 1. Estructura general

| N.º | Página | Título (`<title>`) | Archivo (según los enlaces) |
| --- | --- | --- | --- |
| 1 | Inicio | Rueda Libre \| Alquiler de bicicletas en Medellín | `index.html` |
| 2 | Correo | Correo | `pages/correo.html` |
| 3 | Encuentranos | Encuentranos | `pages/encuentranos.html` |
| 4 | Reservas | Reservas | `pages/reservas.html` |
| 5 | Tarifas | Tarifas | `pages/tarifas.html` |

Todas usan `lang="en"`, `charset="UTF-8"` y la etiqueta `viewport`.

## 2. Página 1: Inicio

### Cabecera

- Etiqueta `<meta name="Alquiler de bicicletas y recorridos guiados por Medellín">` (sin atributo `content`).
- Una etiqueta `<img>` vacía, sin atributos, antes del menú.

### Menú (`<menu>`)

- Tarifas → `pages/tarifas.html`
- Reservas → `pages/reservas.html`

### Contenido

- `<h1>`: Rueda Libre
- Imagen: `img/portada.jpeg`, alt "portada"

### `<main>`, sección 1

- **¿Quiénes somos?**: se describen como una marca dedicada a la venta de bicicletas, con calidad, comodidad y libertad, que promueve un estilo de vida saludable y sostenible.
- **Nuestros servicios**:
  - Alquiler de bicicletas: incluye casco y candado (en `<strong>`).
  - Alquiler de patinetas eléctricas (`<h4>`): incluye cargador y equipo de protección.
  - Alquiler de equipos deportivos (`<h4>`): incluye accesorios básicos según el equipo seleccionado.

### `<main>`, sección 2

- **¿Cómo alquilar?** (lista ordenada, 4 pasos):
  1. Seleccionar el producto o servicio.
  2. Consultar disponibilidad y tarifas.
  3. Completar el formulario y realizar la reserva.
  4. Recibir el producto o disfrutar del servicio.
- **Beneficios del servicio** (lista no ordenada, 3 ítems):
  - Ahorro de dinero al no tener que comprar.
  - Proceso de alquiler fácil y rápido.
  - Flexibilidad para alquilar según tus necesidades.

### Pie de página

- Encuentranos → `pages/encuentranos.html`
- Ubicacion → `https://maps.app.goo.gl/HRqvATrAugZNDYvh9`
- Nuestro Correo y Horarios → `pages/correo.html`

## 3. Página 2: Correo

### Menú

- Inicio → `/index.html`
- Reservas → `reservas.html`
- Tarifas → `tarifas.html`

### Contenido

- `<h2>` **Contacto**: correo electrónico `contacto@ruedalibre.com` (enlace `mailto:`).
- `<h2>` **Horario de atención** (lista de definición):

| Día | Horario |
| --- | --- |
| Lunes a viernes | 8:00 a. m. - 6:00 p. m. |
| Sábado | 9:00 a. m. - 4:00 p. m. |
| Domingo | 10:00 a. m. - 2:00 p. m. |
| Días festivos | Cerrado |

- `<h3>` **Escribenos tus inquietudes**, seguido de un `<input type="">` (sin otros atributos).

### Pie de página

- Encuentranos → `encuentranos.html`
- Ubicacion → enlace de Google Maps
- Nuestro Correo y Horarios → `correo.html`

## 4. Página 3: Encuentranos

### Menú

- Inicio → `/index.html`
- Tarifas → `tarifas.html`
- Reservas → `reservas.html`

### Contenido

- `<h1>` **Redes sociales** (lista, todos con `target="_blank"`):
  - Instagram → `instagram.com/ruedalibre_bikes/`
  - Facebook → `facebook.com/ruedalibre.bicicletas/`
  - TikTok → `tiktok.com/@ruedalibre_bikes`
  - YouTube → `youtube.com/@RuedaLibreBikes`
- Imagen: `../img/logo.png`, con `alt` vacío.

### Pie de página

Los mismos tres enlaces que en Correo.

## 5. Página 4: Reservas

### Menú

- Inicio → `/index.html`
- Tarifas → `tarifas.html`
- Hay una etiqueta `</a>` de cierre suelta al final del menú. No hay enlace a Reservas.

### Formulario

`<section>` con `<form action="#" method="post">`, `<h1>` **Reserva tu bicicleta**.

### Fieldset 1: "Datos Comprador"

Contiene además una segunda `<legend>`: "ingresa tus datos".

| Campo | id / name | Tipo | Atributos |
| --- | --- | --- | --- |
| Nombre Completo | `nombre` | text | required, minlength 3 |
| Número de documento | `documento` | text | inputmode numeric, pattern `[0-9]{6,10}`, minlength 6, maxlength 10, placeholder "Ingrese su documento", required; `oninput` elimina lo que no sea número |
| Correo | `correo` | email | sin required |
| Telefono | `telefono` | tel | required, pattern `[0-9],{10}`, title "Escibre almenos 10 numeros" |
| Fecha del alquiler | `fecha` | date | min 2026-11-01, max 2026-12-31, required |

### Fieldset 2: "Datos Bicicleta"

`<h3>` Escoge tu bicicleta.

| Campo | id / name | Tipo | Detalle |
| --- | --- | --- | --- |
| Tipo de bicicleta | `bicicleta` | select, required | Opción inicial deshabilitada "Seleccione una bicicleta"; opciones: Montaña, Ruta, Urbana, Eléctrica |
| Plan de alquiler | `plan` | select, required | Opción inicial deshabilitada "Seleccione un plan"; opciones: Por horas, Por día, Por semana |
| Cantidad de bicicletas | `cantidad` | number | min 1, max 6, step 1, required |
| Comentarios | `comentarios` | textarea | maxlength 300, placeholder "Escriba sus comentarios (opcional)" |
| Acepto las políticas de alquiler | `politicas` | checkbox | value "aceptadas", required |

### Botón

Submit, "Enviar formulario".

### Pie de página

Los mismos tres enlaces.

## 6. Página 5: Tarifas

### Menú

- Inicio → `/index.html`
- Reservas → `reservas.html`

### Tabla 1: Tarifas de alquiler de bicicletas

Caption: "Precios de alquiler de bicicletas".

| Tipo de bicicleta | 1 hora | Medio día (4 h) | Día completo |
| --- | --- | --- | --- |
| Urbana | $10.000 | $30.000 | $50.000 |
| Montaña | $15.000 | $45.000 | $70.000 |
| Eléctrica | $25.000 | $70.000 | $110.000 |

### Tabla 2: Recorridos guiados

`<section id="recorridos-guiados">`, caption: "Precios de recorridos guiados".

| Recorrido | Distancia | Duración | Nivel | Precio por persona |
| --- | --- | --- | --- | --- |
| Río y Parques | 12 km | 2 h | Fácil | $45.000 |
| Sabores de Barrio | 18 km | 3 h | Medio | $60.000 |
| Reto Las Palmas | 25 km | 4 h | Difícil | $85.000 |

### Texto informativo

Todas las tarifas incluyen casco y candado. Los recorridos salen sábados y domingos a las 7:00 a. m. Qué llevar: ropa cómoda, agua, protector solar y documento de identidad.

### Imagen

`/img/tarifas.png`, 90 × 90 px (estilo en línea), alt "tafifa-img".

### Pie de página

Los mismos tres enlaces.

## 7. Mapa de enlaces

| Desde | Enlaza a |
| --- | --- |
| Inicio | Tarifas, Reservas (menú); Encuentranos, Ubicación, Correo y Horarios (pie) |
| Correo | Inicio, Reservas, Tarifas (menú); pie estándar |
| Encuentranos | Inicio, Tarifas, Reservas (menú); 4 redes sociales; pie estándar |
| Reservas | Inicio, Tarifas (menú); pie estándar |
| Tarifas | Inicio, Reservas (menú); pie estándar |

## 8. Observaciones técnicas del código

Son hechos observables en el código, sin cambios ni sugerencias aplicadas.

- **Inicio:** hay una `<img>` sin atributos antes del menú. El archivo no tiene etiqueta `<body>` de apertura, pero sí `</body>` de cierre. La etiqueta `<meta name="...">` no tiene `content`.
- **Correo:** el `<input type="">` no tiene tipo definido, `id`, `name` ni etiqueta asociada.
- **Reservas:** el patrón del teléfono `[0-9],{10}` incluye una coma literal. El menú no incluye enlace a Reservas y tiene un `</a>` suelto. El campo correo no es obligatorio. Hay dos `<legend>` dentro del primer fieldset.
- **Tarifas vs. Reservas:** Reservas ofrece el tipo "Ruta" y el plan "Por semana", que no aparecen en la tabla de Tarifas.
- **Rutas:** los enlaces al inicio usan `/index.html` (ruta absoluta) en las páginas internas, y `pages/...` en el índice.
- **Idioma:** todas las páginas declaran `lang="en"` con contenido en español.

## 9. Despliegue de la pagina en Github Pages

-https://nilsonvelasco1802.github.io/Rueda-Libre/