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

## ✅ Correcciones aplicadas (devoluciones de pre-entregas)

| Pre-entrega | Devolución | Corrección aplicada |
|---|---|---|
| 6 | Imagen faltante en `index.html` | Todas las rutas apuntan a `assets/img/` (y `../assets/img/` desde `pages/`). 0 recursos rotos. |
| 6 | Placeholders en el README | README reescrito con datos reales del proyecto y del deploy. |
| 7 | Colores hardcodeados en `_header.scss` y `_footer.scss` | Reemplazados por variables de `_variables.scss` (`$color-oscuro`, `$color-primario`, `$sombra-fuerte`, etc.). |
| 7 | Footer al final en SASS | `@use "layout/footer";` es la última línea de `main.scss`. |
| 7 / 8 | Rutas de carpetas en el README | La estructura documentada coincide con la real: `index.html` en la raíz y 4 HTML en `pages/`. |
| 8 | Usar los mixins con parámetros para el responsive | `respond-to()` se invoca en 7 partials (header, nav, footer, tipografía, cards, carousel y media); también se usan `flex-center()`, `imagen-limitada()`, `tarjeta-estilo()` y `tarjeta-sombra()`. |
| 8 | Operadores matemáticos SCSS | `$espaciado * 2`, `$fuente-base * 1.5`, `$bp-tablet - 1px`, `math.div()`. |
| 8 | Archivo `.gitignore` | Agregado (excluye `node_modules/`, `.sass-cache/`, `*.css.map`, `.vscode/`, etc.). |
| 9 | Imágenes huérfanas en `img/` | Eliminadas 6 imágenes sin uso; las 11 restantes están en `assets/img/` y optimizadas. |
| 9 | Open Graph en todas las páginas | `og:title`, `og:description`, `og:image`, `og:url`, `og:type`, `og:locale` y `og:site_name` en las 5 páginas. |
| 9 | Jerarquía de encabezados | Un solo `<h1>` por página; los títulos de modales pasaron de `h5`/`h6` a `h2`/`h3`. |

---

## ⚙️ Cómo compilar el SCSS

Con la extensión **Live Sass Compiler** de VS Code (configurada para guardar en `styles/`) o por terminal:

```bash
sass scss/main.scss styles/main.css --no-source-map
```

---

## 👤 Autora

**Laura Villalba** - Aura Seating
