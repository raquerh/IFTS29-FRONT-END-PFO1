# Raquel.dev — Portfolio Personal

## Descripción del Proyecto

Este es la **Práctica Formativa Obligatoria N° 1** de la materia FRONT END, correspondiente a la **Tecnicatura Superior en Desarrollo de Software (IFTS N°29)**.

Landing page de portfolio personal construida con **HTML5 y CSS3 puro** (sin frameworks ni librerías de JS). El diseño sigue una estética de terminal oscura / sci-fi, inspirada en el universo visual del anime cyberpunk y la ciencia ficción distópica.

**URL publicada:** https://ifts-29-front-end-pfo-1.vercel.app/

---

## Checklist — Práctica Formativa Obligatoria 1

### Estructura del Proyecto

- [x] Archivo `index.html` ubicado en la raíz.
- [x] Carpeta `css` que contenga el archivo `styles.css`.
- [x] (Opcional) Carpeta `media/img` para recursos gráficos.
- [x] Archivo `README.md` creado, que incluya una breve descripción del TP y este checklist.

### Repositorio y Publicación

- [x] Repositorio en GitHub creado.
- [x] Proyecto subido al repositorio.
- [x] Proyecto publicado utilizando Vercel (alternativa a GitHub Pages).
- [x] En el `README.md` se indica la URL de publicación.

### Uso de Google Fonts

- [x] Enlace a Google Fonts incluido en la sección `head` del HTML.
- [x] La tipografía importada se aplica en el sitio.
- [x] **¿Por qué elegí esa fuente?**

  Usé **Fira Code** como fuente principal porque es monoespaciada y fue diseñada para código, lo que refuerza directamente la estética de terminal del sitio — cada carácter ocupa el mismo ancho, como en una consola real. **Syne** se usa para títulos y display: tiene una geometría muy marcada y peso tipográfico fuerte que contrasta bien con lo técnico de Fira Code. Juntas dicen "desarrolladora con criterio de diseño propio", no "template genérico".

### HTML

- [x] El documento inicia con la declaración `DOCTYPE` y usa el atributo `lang="es"`.
- [x] Se han incluido las metaetiquetas obligatorias: `charset` y `viewport`.
- [x] Se ha definido un título descriptivo.
- [x] Se han vinculado correctamente el archivo CSS y el enlace a Google Fonts.

**Secciones obligatorias en `main`:**

- [x] **Presentación Personal** (id `sobre-mi`): Incluye párrafo descriptivo e imagen con atributo `alt`.
- [x] **Tarjetas/Columnas** (id `tarjetas`): Contiene 6 tarjetas (más de las 2 requeridas), cada una con imagen y texto, organizadas con CSS Grid.
- [x] **Listado de Habilidades** (id `habilidades`): Muestra de forma organizada mediante tabla las tecnologías que domino y las que deseo aprender.
- [x] **Formulario de Contacto** (id `contacto`): Incluye campos Nombre, Apellido, Email, Teléfono y botón submit.
- [x] **Películas Favoritas** (id `peliculas`): Presenta 3 películas con título, imagen y descripción.

- [x] Barra de navegación (`nav`) presente y contiene 5 enlaces (más de los 3 requeridos).
- [x] Se han insertado más de 4 comentarios explicativos en el código HTML.

### CSS

- [x] Existe el archivo `styles.css` con estilos personalizados.
- [x] Se utilizan selectores basados en clases e identificadores.
- [x] La tipografía importada desde Google Fonts se aplica correctamente en todos los elementos.

**Layout y Organización:**

- [x] Se ha organizado el layout (especialmente en la sección `tarjetas`) utilizando CSS Grid.
- [x] **¿Qué ventajas encontraste al utilizar Flexbox o Grid en tu proyecto?**

  CSS Grid me permitió manejar layouts bidimensionales: por ejemplo, en las tarjetas una card con clase `card--wide` puede ocupar dos columnas con un solo `grid-column: span 2`, sin necesitar JavaScript ni cálculos manuales. Flexbox fue la herramienta ideal para elementos de una sola dimensión — una fila de links, un conjunto de tags, el nav — donde lo que importa es el flujo y el alineamiento, no la posición en una grilla. Usar ambos en conjunto es la práctica estándar en CSS moderno: cada uno resuelve lo que el otro no resuelve.

**Estilización de Componentes:**

- [x] Se han personalizado los estilos de tablas, botones, enlaces y formularios.
- [x] Se han ajustado las dimensiones de imágenes y contenedores utilizando unidades relativas (`%`, `rem`, `vh`, `clamp()`).
- [x] Se ha implementado múltiples animaciones y transiciones (efecto hover en tarjetas, botones, glitch en título, cursor parpadeante, etc.).
- [x] **¿Qué animación o transición implementaste y por qué consideraste que era adecuada para tu proyecto?**

  Implementé múltiples animaciones para crear una experiencia inmersiva:
  - **Glitch en el título** (`@keyframes glitch-1` y `glitch-2`): Simula interferencia de señal con pseudo-elementos y `clip-path`. Define la estética cyberpunk del sitio desde el primer momento.
  - **Cursor parpadeante** (`@keyframes blink`): Refuerza la metáfora de terminal activo.
  - **Pulso del status dot** (`@keyframes pulse-dot`): Indica "sistema online" de forma visual.
  - **Borde animado del avatar** (`@keyframes border-rotate`): Gradiente en rotación continua que añade dinamismo.
  - **Barras de XP** (`@keyframes load-bar`): Se cargan progresivamente como en un videojuego RPG.
  - **Hover en cards y botones**: Retroalimentación visual clara con `transform` y `box-shadow`.

### Consideraciones Adicionales

- [x] El diseño es responsivo y se visualiza correctamente en distintos dispositivos.
- [x] Se aplicaron buenas prácticas de accesibilidad (por ejemplo, uso adecuado de atributos `alt` en las imágenes).
- [x] Se añadieron comentarios adicionales donde se describen decisiones de diseño o la lógica de implementación.

---

## Características Adicionales Implementadas (Más Allá de la Consigna)

El proyecto incluye funcionalidades y mejoras que superan los requerimientos obligatorios:

**Accesibilidad Avanzada:**
- Skip link funcional que permite saltar al contenido principal con teclado (Tab + Enter/Espacio).
- Navegación por teclado completa con estados `:focus-visible` para indicadores visuales claros.
- Atributos ARIA (`aria-label`, `aria-hidden`) usados correctamente en elementos decorativos y de navegación.
- Atributo `autocomplete` en campos del formulario para mejor experiencia de usuario.

**Optimización y Performance:**
- Preconnect a Google Fonts para reducir latencia de carga.
- Loading lazy en imágenes para mejor performance inicial.
- Transiciones específicas (se evita `transition: all`) para mejor rendimiento.
- Variables CSS para sistema de diseño centralizado y mantenible.

**Diseño Visual Avanzado:**
- Fondo Matrix animado (GIF) con opacidad controlada que cubre todo el sitio.
- Footer original estilo terminal con comandos (`whoami`, `ls`, `cat`, `shutdown`) en lugar del típico footer con íconos.
- Efectos visuales: scanlines, glitch effect, bordes animados con gradientes, barras de progreso estilo RPG.
- Scrollbar personalizada para mantener la estética del sitio.
- Responsive fluido con uso extensivo de `clamp()` para escalado gradual sin saltos bruscos.

**Estructura y Semántica:**
- HTML semántico con uso correcto de `<header>`, `<nav>`, `<main>`, `<section>`, `<article>`, `<footer>`.
- Estructura limpia sin divs innecesarios, cada elemento tiene un propósito específico.
- Más de 10 comentarios explicativos distribuidos en el HTML (se requieren mínimo 4).
- 5 enlaces en la navegación (se requieren mínimo 3).
- 6 tarjetas de proyectos (se requieren mínimo 2).

**Seguridad:**
- `rel="noopener noreferrer"` en todos los links externos para prevenir vulnerabilidades.
- Validación de formulario con campos `required` y tipos de input correctos (`email`, `tel`).

---

*PFO1 · TSDS · IFTS N°29 · 2026*
