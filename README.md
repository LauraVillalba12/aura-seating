# Aura Seating - Sillas Gamer y Ejecutivas 🪑🎮

Sitio web estático de 5 páginas para **Aura Seating**, un emprendimiento dedicado al diseño y distribución de sillas ergonómicas de alto rendimiento para gaming y entornos de trabajo ejecutivos.

Proyecto final del curso de Desarrollo Web.

---

## 🌐 Sitio desplegado

👉 **[https://aura-seating.vercel.app](https://aura-seating.vercel.app)** (Vercel)

📂 Repositorio: [https://github.com/LauraVillalba12/aura-seating](https://github.com/LauraVillalba12/aura-seating)

---

## 📁 Estructura del proyecto

```
aura-seating/
├── index.html                  → Página principal (banner, carrusel, catálogo y modales)
├── pages/
│   ├── sobre-mi.html           → Historia del emprendimiento
│   ├── servicios.html          → Asesoramiento, equipamiento y soporte
│   ├── proyectos.html          → Instalaciones en eSports y oficinas
│   └── contacto.html           → Formulario de consultas con modal de confirmación
├── assets/
│   └── img/                    → Imágenes y logo del sitio
├── scss/
│   ├── main.scss               → Solo importa los partials con @use
│   ├── utilities/
│   │   ├── _variables.scss     → Colores, fuentes, espaciados y breakpoints
│   │   └── _mixins.scss        → Mixins con parámetros (respond-to, flex-center, etc.)
│   ├── base/
│   │   ├── _base.scss          → Estilos generales del documento
│   │   ├── _tipografia.scss    → Jerarquía de títulos responsiva
│   │   └── _animaciones.scss   → @keyframes nativos
│   ├── layout/
│   │   ├── _header.scss        → Cabecera fija y marca
│   │   ├── _nav.scss           → Navbar de Bootstrap personalizada
│   │   └── _footer.scss        → Pie de página (importado al final)
│   └── components/
│       ├── _buttons.scss       → Botones con @extend y animación
│       ├── _cards.scss         → Tarjetas y grillas responsivas
│       ├── _carousel.scss      → Carrusel de Bootstrap personalizado
│       ├── _forms.scss         → Formulario de contacto
│       └── _media.scss         → Imágenes, promo y modales
├── styles/
│   └── main.css                → CSS compilado desde scss/main.scss
├── .gitignore
└── README.md
```

---

## 🛠️ Tecnologías utilizadas

* **HTML5** semántico (`header`, `nav`, `main`, `section`, `article`, `figure`, `footer`).
* **SCSS** con arquitectura de partials: variables, nesting, mixins con parámetros, `@extend` (placeholders `%btn-base` y `%tarjeta-base`) y operadores matemáticos (`$espaciado * 2`, `math.div()`).
* **Bootstrap 5.3**: navbar responsiva con menú hamburguesa, grillas, cards, carousel y modales.
* **AOS (Animate On Scroll)**: animaciones de entrada al hacer scroll.
* **Animaciones nativas SCSS**: `@keyframes` (`pulso-suave`, `aparecer`) y `transition` en tarjetas, botones y links del menú.
* **Git, GitHub y Vercel**: control de versiones y despliegue.

---

## 📱 Responsive

Diseño *mobile first* con media queries propias generadas desde el mixin `respond-to()`:

| Breakpoint | Ancho |
|---|---|
| Mobile | hasta 767px |
| Tablet | desde 768px |
| Desktop | desde 1024px |
| Large | desde 1200px |

---

## 🚀 SEO y accesibilidad

* `<title>`, `<meta description>` y `<meta keywords>` únicos en cada una de las 5 páginas.
* Etiquetas **Open Graph** (`og:title`, `og:description`, `og:image`, `og:url`) en todas las páginas.
* Un único `<h1>` por página y jerarquía de encabezados ordenada.
* Atributo `alt` descriptivo en el 100% de las imágenes y nombres de archivo descriptivos.
* Imágenes optimizadas y sin archivos huérfanos en `assets/img/`.

---

## ⚙️ Cómo compilar el SCSS

Con la extensión **Live Sass Compiler** de VS Code (configurada para guardar en `styles/`) o por terminal:

```bash
sass scss/main.scss styles/main.css --no-source-map
```

---

## 👤 Autora

**Laura Villalba** - Aura Seating
