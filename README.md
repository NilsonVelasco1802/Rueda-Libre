# 🚲 Rueda Libre

Sitio web de **Rueda Libre**, una empresa ficticia dedicada al **alquiler de bicicletas** y a los **recorridos guiados por la ciudad de Medellín**. El proyecto está construido con **HTML, CSS y Bootstrap 5**, y es un trabajo de práctica de desarrollo web *front-end*.

🌐 **Demo en línea:** https://nilsonvelasco1802.github.io/Rueda-Libre/

---

## 📋 Tabla de contenido

- [Descripción](#-descripción)
- [Características](#-características)
- [Tecnologías](#-tecnologías)
- [Estructura del proyecto](#-estructura-del-proyecto)
- [Páginas del sitio](#-páginas-del-sitio)
- [Tarifas y recorridos](#-tarifas-y-recorridos)
- [Sistema de diseño](#-sistema-de-diseño)
- [Cómo ejecutar el proyecto](#-cómo-ejecutar-el-proyecto)
- [Prototipo "Rueda Nocturna"](#-prototipo-rueda-nocturna-tailwind)
- [Pendientes y mejoras](#-pendientes-y-mejoras)
- [Historial de desarrollo](#-historial-de-desarrollo)
- [Autores](#-autores)

---

## 📖 Descripción

Rueda Libre promueve una forma de recorrer Medellín que sea cómoda, saludable y sostenible. El sitio permite al visitante:

- Conocer los servicios de la empresa (alquiler de bicicletas, bicicletas eléctricas y rutas).
- Explorar la flota disponible con su precio por hora.
- Consultar las tarifas de alquiler y de recorridos guiados.
- Reservar una bicicleta mediante un formulario con validación.
- Contactar a la empresa por correo, WhatsApp y redes sociales.

## ✨ Características

- **Diseño responsive** con la cuadrícula de Bootstrap (`row`, `col-*`) y *media queries* propias para móvil, tablet y escritorio.
- **Menú de navegación colapsable** (hamburguesa) con la *navbar* de Bootstrap.
- **Carrusel de promociones** en la página de inicio, con tres imágenes SVG y rotación automática cada 4 segundos.
- **Tarjetas de servicios y de flota** con componentes `card` de Bootstrap, efectos *hover* y una etiqueta "Nuevo".
- **Formulario de reserva validado**:
  - Validación nativa de HTML5 y estilos de validación de Bootstrap (`needs-validation`, `invalid-feedback`).
  - Teléfono (10 dígitos) y documento (6 a 10 dígitos) aceptan solo números.
  - Fecha limitada entre el 2 de noviembre y el 31 de diciembre de 2026.
  - Cantidad de bicicletas entre 1 y 6.
  - **Modal** con las políticas de alquiler y **alerta descartable** con un aviso importante.
- **Tablas de tarifas** con `table-striped`, `table-hover` y `table-responsive`.
- **Botón flotante de WhatsApp** en todas las páginas.
- **Paleta de colores verde** definida con variables CSS reutilizables.
- Despliegue en **GitHub Pages**.

## 🛠 Tecnologías

| Tecnología | Uso |
| --- | --- |
| **HTML5** | Estructura semántica (`header`, `nav`, `main`, `section`, `article`, `footer`) |
| **CSS3** | Estilos propios, variables CSS, *flexbox*, *grid* y *media queries* |
| **Bootstrap 5.3.3** (CDN) | Navbar, carrusel, tarjetas, formularios, modal, alertas y tablas |
| **Google Fonts** | Tipografías *Rubik*, *Roboto Condensed* y *Montserrat* |
| **Tailwind CSS 4** | Solo en el prototipo experimental "Rueda Nocturna" |
| **Git y GitHub / GitHub Pages** | Control de versiones y publicación |

> El sitio no usa JavaScript propio de forma relevante: solo el *bundle* de Bootstrap y un par de *handlers* `oninput` en el formulario.

## 📁 Estructura del proyecto

```
Rueda-Libre/
├── index.html                  # Página de inicio
├── pages/
│   ├── tarifas.html            # Tarifas de alquiler y recorridos guiados
│   ├── reservas.html           # Formulario de reserva y rutas
│   ├── correo.html             # Contacto y horarios de atención
│   ├── encuentranos.html       # Redes sociales
│   ├── catalogo-bootstrap.html # Catálogo de flota (prototipo)
│   └── nocturna/
│       └── prototipo.html      # Prototipo "Rueda Nocturna" con Tailwind
├── css/
│   ├── style.css               # Estilos globales, variables y navbar
│   ├── index.css               # Estilos de la página de inicio
│   ├── tarifas.css
│   ├── reservas.css
│   ├── correo.css
│   └── encuentranos.css
├── img/                        # Logos, banners, promociones (SVG), íconos de redes
├── src/
│   ├── input.css               # Entrada de Tailwind (variables y tema)
│   └── output.css              # CSS generado por Tailwind
├── bitacora.md                 # Bitácora de análisis del sitio
├── package.json                # Dependencias de Tailwind
└── package-lock.json
```

## 🗺 Páginas del sitio

| Página | Archivo | Contenido |
| --- | --- | --- |
| **Inicio** | `index.html` | Banner de bienvenida, carrusel de promociones, servicios, pasos para alquilar, flota (7 bicicletas) y beneficios |
| **Tarifas** | `pages/tarifas.html` | Tablas de precios de bicicletas y de recorridos guiados, información de salidas y botón "Reservar Ahora" |
| **Reservas** | `pages/reservas.html` | Formulario de reserva, políticas de alquiler (modal), información de contacto y galería de rutas |
| **Correo** | `pages/correo.html` | Correo de contacto y horarios de atención |
| **Encuéntranos** | `pages/encuentranos.html` | Enlaces a YouTube, Instagram, Facebook y TikTok |

**Navegación:** el menú superior enlaza a *Inicio*, *Tarifas* y *Reserva*. El pie de página enlaza a *Encuéntranos*, *Ubicación* (Google Maps) y *Nuestro Correo y Horarios*.

### Flota (página de inicio)

| Bicicleta | Descripción | Precio por hora |
| --- | --- | --- |
| Urbana Clásica | Cómoda y liviana para las ciclorrutas | $10.000 |
| Urbana Plegable | Se dobla en segundos; ideal para combinar con el metro | $12.000 |
| Montaña Trail | Suspensión delantera y 21 cambios | $15.000 |
| Gravel Aventura | Para rutas mixtas de asfalto y destapado | $18.000 |
| Eléctrica Urbana | Asistencia eléctrica con 45 km de autonomía | $25.000 |
| Infantil | Para niños de 6 a 10 años | $8.000 |
| Tándem | Para dos personas | $20.000 |

## 💰 Tarifas y recorridos

### Alquiler de bicicletas

| Tipo | 1 hora | Medio día (4 h) | Día completo |
| --- | --- | --- | --- |
| Urbana | $10.000 | $30.000 | $50.000 |
| Montaña | $15.000 | $45.000 | $70.000 |
| Eléctrica | $25.000 | $70.000 | $110.000 |

### Recorridos guiados

| Recorrido | Distancia | Duración | Nivel | Precio por persona |
| --- | --- | --- | --- | --- |
| Río y Parques | 12 km | 2 h | Fácil | $45.000 |
| Sabores de Barrio | 18 km | 3 h | Medio | $60.000 |
| Reto Las Palmas | 25 km | 4 h | Difícil | $85.000 |

- Todas las tarifas incluyen **casco y candado**.
- Los recorridos salen **sábados y domingos a las 7:00 a. m.**
- Qué llevar: ropa cómoda, agua, protector solar y documento de identidad.

### Horarios de atención

| Día | Horario |
| --- | --- |
| Lunes a viernes | 8:00 a. m. – 6:00 p. m. |
| Sábado | 9:00 a. m. – 4:00 p. m. |
| Domingo | 10:00 a. m. – 2:00 p. m. |
| Días festivos | Cerrado |

## 🎨 Sistema de diseño

Los colores y estilos base están definidos como variables CSS en `css/style.css`:

| Variable | Color | Uso |
| --- | --- | --- |
| `--color-primary` | `#1B4332` | Verde oscuro: encabezados, botones, fondos |
| `--color-secondary` | `#2D6A4F` | Verde medio: botones de Bootstrap, enlaces |
| `--color-accent` | `#52B788` | Verde claro: detalles y acentos |
| `--color-background` | `#FFFFFF` | Fondo principal |
| `--color-background-secondary` | `#F1F5F3` | Fondo secundario |
| `--color-text` | `#212529` | Texto principal |
| `--color-border` | `#ADB5BD` | Bordes |

Además se personalizó el botón `.btn-primary` de Bootstrap con la paleta verde de la marca.

## 🚀 Cómo ejecutar el proyecto

El sitio es estático, así que no requiere instalación ni compilación.

**1. Clonar el repositorio**

```bash
git clone https://github.com/NilsonVelasco1802/Rueda-Libre.git
cd Rueda-Libre
```

**2. Abrir el sitio**

- Abre `index.html` directamente en el navegador, **o**
- Usa un servidor local, por ejemplo la extensión **Live Server** de VS Code (el proyecto se probó en `http://127.0.0.1:5500/`).

> Se necesita conexión a internet para cargar Bootstrap y las fuentes desde sus CDN.

## 🌙 Prototipo "Rueda Nocturna" (Tailwind)

En `pages/nocturna/prototipo.html` hay una propuesta de *landing* para una futura campaña de **recorridos nocturnos** (jueves a sábado, 3 rutas, desde $55.000). Es un experimento aparte, hecho con **Tailwind CSS 4** y la misma paleta verde del sitio principal.

Si quieres regenerar el CSS de Tailwind:

```bash
npm install
npx @tailwindcss/cli -i ./src/input.css -o ./src/output.css --watch
```

## 🔧 Pendientes y mejoras

Detectados al revisar el código; sirven como lista de tareas para próximas versiones:

- [ ] `correo.html`: el campo `<input type="">` no tiene tipo, `name` ni etiqueta, y no hay botón de envío.
- [ ] `catalogo-bootstrap.html`: referencia `../css/catalogo-bootstrap.css`, que no existe; sus botones apuntan a `./pages/reservas.html` (debería ser `./reservas.html`) y la página no está enlazada desde el menú.
- [ ] `tarifas.html`, `reservas.html`, `correo.html` y `encuentranos.html` declaran `lang="en"` pero el contenido está en español (debería ser `lang="es"`).
- [ ] El formulario de reserva usa `action="#"`: no envía los datos a ningún servidor ni a un servicio de correo.
- [ ] Las opciones de recorrido del formulario ("Medellín", "Norte", "Sur") no coinciden con los recorridos de la página de tarifas ("Río y Parques", "Sabores de Barrio", "Reto Las Palmas").
- [ ] El formulario ofrece el tipo "Ruta" y el plan "Por semana", que no aparecen en la tabla de tarifas.
- [ ] En `index.html` varios `id` se repiten (`tarjeta-flota`, `beneficios`); los `id` deben ser únicos, así que conviene cambiarlos por clases.
- [ ] En la flota, todas las tarjetas usan el mismo `logo1.png`; faltan fotos reales de cada bicicleta.
- [ ] La tarjeta de bicicleta eléctrica tiene un `alt` que dice "patinetas eléctricas".
- [ ] `bitacora.md` está desactualizada (describe solo 5 páginas) y `bitacora.txt` es un duplicado idéntico.
- [ ] Falta un `.gitignore` (por ejemplo para `node_modules/`).
- [ ] Falta una licencia (`package.json` indica ISC por defecto).

## 🕑 Historial de desarrollo

El proyecto ha evolucionado en etapas, según los *commits* del repositorio:

1. **Base:** estructura HTML y CSS propios, con *flexbox*.
2. **Migración a Bootstrap:** navbar, galería con *grid*, tarjetas y sección de beneficios.
3. **Interactividad:** menú desplegable, carrusel de promociones y *media queries* para distintos dispositivos.
4. **Formularios:** validación con Bootstrap, modal de políticas y alerta informativa.
5. **Experimentos:** prototipo nocturno con Tailwind y ajustes de pantalla completa.

Las ramas del repositorio son `main` y `respaldo-antes-de-recuperacion`.

## 👥 Autores

- **Nilson Velasco** – [@NilsonVelasco1802](https://github.com/NilsonVelasco1802)
- Colaboración de **Simón Salva Muñoz**

---

> *Rueda Libre es una empresa ficticia creada con fines educativos.*
