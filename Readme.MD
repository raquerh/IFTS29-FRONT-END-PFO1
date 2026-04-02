# Raquel.dev — Portfolio Personal

## Descripción del Proyecto

Este es la **Practica Formativa Obligatoria N° 1** de la materia FRONT END, correspondiente a la **Tecnicatura Superior en Desarrollo de Software (IFTS N°29)**.

Landing page de portfolio personal construida con **HTML5 y CSS3 puro** (sin frameworks ni librerías de JS). El diseño sigue una estética de terminal oscura / sci-fi, inspirada en el universo visual del anime cyberpunk y la ciencia ficción distópica.

**URL publicada:** _[completar con link de Vercel tras el deploy]_

---

## Checklist — Práctica Formativa Obligatoria 1

### Estructura del Proyecto

- [x] Archivo `index.html` ubicado en la raíz.
- [x] Carpeta `css` que contenga el archivo `styles.css`.
- [x] Carpeta `img` (opcional — las imágenes se referencian desde URLs externas de Unsplash y DiceBear).
- [x] Archivo `README.md` creado con descripción del TP y este checklist.

### Repositorio y Publicación

- [x] Repositorio en GitHub creado.
- [x] Proyecto subido al repositorio.
- [x] Proyecto publicado en Vercel.
- [x] URL de publicación indicada en este `README.md`.

### Uso de Google Fonts

- [x] Enlace a Google Fonts incluido en la sección `head` del HTML (con `preconnect` para optimizar la carga).
- [x] La tipografía importada se aplica en el sitio.
- [x] **¿Por qué elegí estas fuentes?**

  Usé **Fira Code** como fuente principal porque es monoespaciada y fue diseñada para código, lo que refuerza directamente la estética de terminal del sitio — cada carácter ocupa el mismo ancho, como en una consola real. **Syne** se usa para títulos y display: tiene una geometría muy marcada y peso tipográfico fuerte que contrasta bien con lo técnico de Fira Code. Juntas dicen "desarrolladora con criterio de diseño propio", no "template genérico".

### HTML

- [x] El documento inicia con la declaración `DOCTYPE` y usa `lang="es"`.
- [x] Metaetiquetas obligatorias: `charset` y `viewport`.
- [x] Metaetiquetas adicionales: `description`, `keywords`, `author` y Open Graph para redes sociales.
- [x] Título descriptivo: `Raquel.dev | Portfolio`.
- [x] CSS y Google Fonts vinculados correctamente en el `head`.
- [x] Barra de navegación (`nav`) con `aria-label` y 5 enlaces.
- [x] `<main id="main">` correctamente identificado para el skip link de accesibilidad.

#### Secciones obligatorias en `main`:

- [x] `#sobre-mi` — Presentación personal con imagen (avatar) y descripción.
- [x] `#tarjetas` — 6 tarjetas de proyectos reales organizadas con CSS Grid.
- [x] `#habilidades` — Grid de skills con tabla de XP + lista de tecnologías a aprender + soft skills.
- [x] `#peliculas` — 3 películas favoritas (The Terminator, Ghost in the Shell, The Matrix) con imagen, año, título, descripción y director.
- [x] `#contacto` — Formulario con campos nombre, apellido, email y teléfono, con `autocomplete` y `required`.

- [x] Al menos 4 comentarios explicativos en el HTML (hay más de 8, incluyendo notas de mejora futura).

### CSS

- [x] Archivo `styles.css` con estilos personalizados.
- [x] Selectores por clases e IDs en uso.
- [x] Tipografía de Google Fonts aplicada globalmente con variables CSS (`--font-mono`, `--font-display`).

#### Layout y Organización:

- [x] **CSS Grid** en: `.cards-grid`, `.habilidades-layout`, `.movies-grid`, `.skills-grid`, `.skill-item`, `.form-row`.
- [x] **Flexbox** en: header, nav, `.sobre-mi-img-wrapper`, `.skills-quick`, `.card-top`, `.card-tags`, `.card-links-row`, footer y sus componentes internos.
- [x] **¿Qué ventajas encontré al usar Flexbox o Grid?**

  CSS Grid me permitió manejar layouts bidimensionales: por ejemplo, en las tarjetas una card con clase `card--wide` puede ocupar dos columnas con un solo `grid-column: span 2`, sin necesitar JavaScript ni cálculos manuales. Flexbox fue la herramienta ideal para elementos de una sola dimensión — una fila de links, un conjunto de tags, el nav — donde lo que importa es el flujo y el alineamiento, no la posición en una grilla. Usar ambos en conjunto es la práctica estándar en CSS moderno: cada uno resuelve lo que el otro no resuelve.

#### Estilización de Componentes:

- [x] Tabla de habilidades (`.skills-grid`) con header, filas y columnas personalizadas.
- [x] Botones (`.btn-submit`, `.card-link`) con estilos personalizados y estado `:hover`/`:focus-visible`.
- [x] Links de navegación y sociales con transiciones.
- [x] Formulario con `input` personalizados, estados `:focus`, placeholder coloreado y labels destacados.
- [x] Unidades relativas: `rem`, `%`, `vw`, `vh`, `ch`, `clamp()` usadas en todo el archivo.
- [x] **Animaciones y transiciones implementadas:**
  - **Glitch en el título** (`@keyframes glitch-1` y `glitch-2`): pseudo-elementos `::before`/`::after` con `clip-path` que simulan interferencia de señal. Es la primera cosa que ve el usuario y define la estética completa del sitio.
  - **Cursor parpadeante** (`@keyframes blink`): simula un cursor de terminal activo. Pequeño detalle, alto impacto de inmersión.
  - **Pulso del status dot** (`@keyframes pulse-dot`): el punto verde del header pulsa suavemente, reforzando la idea de "sistema online".
  - **Borde animado del avatar** (`@keyframes border-rotate`): gradiente en rotación continua alrededor de la imagen de perfil.
  - **Barras de XP** (`@keyframes load-bar`): se cargan de 0% al valor real al entrar a la página, como un RPG.
  - **Hover en cards** (`transform: translateY(-4px)` + `box-shadow`): retroalimentación visual clara al interactuar.
  - **Hover en botón submit** (`translateX(4px)` + fill de fondo): la animación horizontal refuerza la metáfora de "enviar".

### Consideraciones Adicionales

- [x] Diseño responsivo con breakpoints en `900px` y `600px`.
- [x] Accesibilidad: `alt` descriptivos en todas las imágenes, `aria-label` en nav y links de redes, `aria-hidden="true"` en elementos puramente decorativos, `autocomplete` en inputs del formulario, skip link funcional.
- [x] `transition: all` reemplazado por propiedades específicas en todos los selectores (mejor performance).
- [x] `rel="noopener noreferrer"` en todos los `target="_blank"`.
- [x] SVG de Next.js y Express con `fill="currentColor"` para visibilidad en tema oscuro.
- [x] Inline `style` eliminado; reemplazado por clase `.card-links-row`.
- [x] Nesting incorrecto de `.habilidades-col` corregido.
- [x] `fill` de los SVGs de redes sociales unificado a `currentColor`.

---

*PFO1 · TSDS · IFTS N°29 · 2026*
