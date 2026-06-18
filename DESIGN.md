---
name: Omar Ortiz · Portfolio
description: Portfolio profesional de Omar Eduardo Ortiz Vega — DevOps Engineer & Full Stack Developer.
colors:
  navy: "#0B0146"
  teal: "#349980"
  accent: "#7FC4FF"
  heading: "#005086"
  surface: "#e0e0e2"
  card: "#f4fbff"
  ink: "#1a1a2e"
  white: "#ffffff"
typography:
  display:
    fontFamily: "'Fjalla One', sans-serif"
    fontSize: "clamp(1.75rem, 1.1rem + 3vw, 2.75rem)"
    fontWeight: 400
    lineHeight: 1.45
    letterSpacing: "0.06em"
  headline:
    fontFamily: "'Fjalla One', sans-serif"
    fontSize: "clamp(1.4rem, 1.1rem + 1.2vw, 1.875rem)"
    fontWeight: 400
    letterSpacing: "0.04em"
  title:
    fontFamily: "'Fjalla One', sans-serif"
    fontSize: "clamp(1.1rem, 1rem + 0.5vw, 1.375rem)"
    fontWeight: 400
  body:
    fontFamily: "'Source Sans Pro', sans-serif"
    fontSize: "1.0625rem"
    fontWeight: 400
    lineHeight: 1.6
  label:
    fontFamily: "'Source Sans Pro', sans-serif"
    fontSize: "0.85rem"
    fontWeight: 700
    letterSpacing: "0.06em"
    textTransform: "uppercase"
rounded:
  sm: "4px"
  md: "8px"
  lg: "10px"
  full: "50%"
spacing:
  "2xs": "0.5rem"
  xs: "1rem"
  sm: "1.5rem"
  md: "2.5rem"
  lg: "clamp(3rem, 6vw, 5rem)"
components:
  button-primary:
    backgroundColor: "{colors.navy}"
    textColor: "{colors.white}"
    rounded: "{rounded.sm}"
    padding: "12px 24px"
  button-primary-hover:
    backgroundColor: "{colors.teal}"
    textColor: "{colors.white}"
  project-card:
    backgroundColor: "{colors.white}"
    rounded: "{rounded.lg}"
    padding: "clamp(1.25rem, 1rem + 1.5vw, 1.875rem)"
  experience-card:
    backgroundColor: "{colors.card}"
    rounded: "{rounded.lg}"
  social-icon:
    rounded: "{rounded.md}"
    size: "50px"
    width: "50px"
    height: "50px"
---

# Design System: Omar Ortiz · Portfolio

## 1. Overview

**Creative North Star: "El Ingeniero Directo"**

Este portafolio no vende ilusiones — vende trayectoria. La filosofía visual parte de una premisa técnica: cada decisión de diseño debe justificarse con un propósito funcional, igual que cada línea de código. El sistema usa color de forma comprometida (un navy profundo como superficie dominante, un teal de ingeniería como acento estructural) y rechaza cualquier ornamento que no aporte información.

La densidad es una virtud, no un defecto. Las tarjetas de experiencia son compactas y apiladas como cards en un tablero Kanban; los proyectos se presentan en fila como registros de sistema. La tipografía combina dos familias con propósitos distintos: Fjalla One para identidad y títulos (impacto, condensación, autoridad técnica) y Source Sans Pro para lectura de contenido (neutralidad, legibilidad sostenida). No se mezclan cuando no hay razón para ello.

El sitio debe sentirse como un README bien escrito: estructurado, directo, sin palabrería. Lo que se ve es lo que hay.

**Key Characteristics:**
- Fondo navy profundo como lienzo principal del hero y contacto
- Teal estructural como color de chrome (header, footer)
- Acento azul claro (`#7FC4FF`) reservado exclusivamente para énfasis en el hero
- Tipografía en dos roles claros: identidad (Fjalla One) y contenido (Source Sans Pro)
- Sin gradientes, sin glassmorphism, sin sombras decorativas
- Reveal on scroll con IntersectionObserver, siempre con `prefers-reduced-motion` respetado

## 2. Colors

Una paleta de dos polos (navy de ingeniería y teal de chrome) con un único acento de alta legibilidad. Todo lo demás es neutro.

### Primary
- **Navy Profundo** (`#0B0146`): El color dominante. Fondo del hero, sección de contacto y cualquier superficie de alto impacto. Transmite autoridad técnica sin caer en el negro genérico.
- **Teal de Chrome** (`#349980`): El color estructural. Header y footer únicamente. Funciona como el "frame" del sistema — no aparece dentro del contenido.

### Secondary
- **Azul Acento** (`#7FC4FF`): El único toque de color expresivo. Reservado para las palabras en `<span>` dentro del `<h1>` del hero. Su escasez es su potencia. No usar en ningún otro contexto.

### Tertiary
- **Azul Heading** (`#005086`): Color para encabezados de sección (`<h2>`) y links de proyectos. Oscuro suficiente para contraste sobre fondos claros. Funciona como puente semántico entre navy y acento.

### Neutral
- **Tinta** (`#1a1a2e`): Color base del cuerpo de texto. Navy muy oscuro, no negro puro — mantiene coherencia cromática con el resto del sistema.
- **Superficie Gris** (`#e0e0e2`): Fondo de la sección de proyectos. Separa visualmente del fondo blanco sin recurrir a un segundo color de marca.
- **Card Azul Frío** (`#f4fbff`): Fondo de tarjetas de experiencia. Tinte azul casi imperceptible que mantiene las tarjetas en familia con el sistema.
- **Blanco** (`#ffffff`): Texto sobre fondos oscuros, fondo de tarjetas de proyectos.

### Named Rules
**La Regla del Acento Escaso.** `#7FC4FF` aparece únicamente en los spans del `<h1>` del hero. Si aparece en cualquier otro elemento, pierde su carácter. Prohibido usarlo en botones, badges, iconos, ni títulos de sección.

**La Regla del Chrome.** El teal (`#349980`) es el color del frame del sitio (header y footer), no del contenido. No debe aparecer dentro de ninguna sección de contenido excepto como `color` del label `.experience-date`.

## 3. Typography

**Display Font:** Fjalla One (condensed geometric sans-serif; Google Fonts)
**Body Font:** Source Sans Pro (humanist sans-serif; Google Fonts)

**Character:** Una pareja de contraste máximo: Fjalla One aporta impacto condensado y lectura rápida para identidad y títulos; Source Sans Pro entrega neutralidad legible para todo lo que requiere lectura sostenida. No son similares — son opuestos en el eje condensado/abierto, lo que los hace compatibles.

### Hierarchy
- **Display** (normal weight, `clamp(1.75rem, 1.1rem + 3vw, 2.75rem)`, line-height 1.45): Brand name en header (`OMAR ORTIZ`, uppercase, letter-spacing 0.06em) y `<h1>` del hero. El texto más grande del sistema.
- **Headline** (normal weight, `clamp(1.4rem, 1.1rem + 1.2vw, 1.875rem)`, letter-spacing 0.04em): Encabezados de sección (`<h2>`) en uppercase. Usa Source Sans Pro, no Fjalla One — por decisión deliberada para separar identidad de estructura.
- **Title** (normal weight, `clamp(1.1rem, 1rem + 0.5vw, 1.375rem)`): Títulos de proyectos y experiencias (`<h3>`). Fjalla One, sin uppercase.
- **Body** (400, `1.0625rem`, line-height 1.6): Descripciones de proyectos y experiencia. Source Sans Pro. Líneas justificadas `text-align: left` por defecto; las tarjetas de experiencia centran el título pero no la descripción.
- **Label** (700, `0.85rem`, uppercase, letter-spacing 0.06em): Fechas de experiencia (`.experience-date`). Teal sobre fondo claro. Señalética de bajo impacto.

### Named Rules
**La Regla de los Dos Registros.** Fjalla One es identidad y titulación; Source Sans Pro es lectura. Los `<h2>` usan Source Sans Pro porque son señalética de sección, no identidad de marca. No mezclar en el mismo nivel jerárquico.

## 4. Elevation

El sistema es **plano por defecto**. La única sombra que existe es la de las tarjetas de proyectos (`0px 4px 20px rgba(0,0,0,0.18)`), y cumple una función estructural: separar tarjetas blancas de una superficie gris (`#e0e0e2`). No hay sombras decorativas, hover-shadows, ni efectos de profundidad en el header, footer o sección de contacto.

El truco de elevación más llamativo del sistema no usa `box-shadow` sino `margin-top: -40px`: la caja de texto de cada tarjeta de experiencia se superpone sobre la imagen de cabecera, creando un efecto de overlap sin sombras adicionales. Profundidad mediante posicionamiento, no iluminación simulada.

### Shadow Vocabulary
- **Tarjeta de proyecto** (`0px 4px 20px rgba(0,0,0,0.18)`): Única sombra en el sistema. Usada solo en `.project` sobre fondo `#e0e0e2`.

### Named Rules
**La Regla Plana Por Defecto.** Ningún elemento tiene sombra en estado de reposo excepto `.project`. Si se necesita separación visual, usar diferencia de color de fondo o borde, nunca añadir `box-shadow` a nuevos componentes sin aprobación explícita.

## 5. Components

### Buttons
- **Shape:** Ligeramente redondeado (4px radius — `{rounded.sm}`). Táctil pero controlado, nunca "pill".
- **Primary:** Fondo navy (`#0B0146`), texto blanco, borde `1px solid #fff`, padding `12px 24px`. El borde blanco hace visible el botón sobre fondos también oscuros (aparece sobre `--color-navy`).
- **Hover / Focus:** Fondo cambia a teal (`#349980`), texto permanece blanco. Transición `0.2s cubic-bezier(0.16, 1, 0.3, 1)`. `focus-visible` usa el mismo tratamiento que hover.
- **No existe variante ghost ni secundaria.** Un solo botón en el sistema, en la sección de contacto. Cualquier llamada a la acción nueva debe seguir este mismo estilo.

### Cards / Containers
**Tarjetas de Proyecto:**
- **Corner Style:** Gently curved (10px — `{rounded.lg}`)
- **Background:** Blanco (`#ffffff`) sobre superficie gris (`#e0e0e2`)
- **Shadow:** Sombra estructural `0px 4px 20px rgba(0,0,0,0.18)`
- **Internal Padding:** `clamp(1.25rem, 1rem + 1.5vw, 1.875rem)` — fluido, generoso
- **Layout:** `flex-direction: column-reverse` en mobile (imagen arriba, texto abajo); `flex-direction: row` en ≥768px

**Tarjetas de Experiencia:**
- **Corner Style:** 10px radius
- **Background:** `#f4fbff` (card) para el contenedor exterior; `#ffffff` para la caja de texto interior que se superpone con `margin-top: -40px`
- **Image header:** 200px de alto, `object-fit: cover`. El logo de AXA Colpatria usa `object-fit: contain` con fondo blanco y `padding: 1.5rem` como excepción documentada.
- **Shadow:** Ninguna — la superposición crea la sensación de profundidad sin sombra.
- **Grid:** `repeat(auto-fit, minmax(min(100%, 280px), 1fr))` — sin breakpoints explícitos para el grid.

### Navigation
- **Style:** Header teal (`#349980`), texto blanco, `min-height: 70px`, `display: flex`, `justify-content: space-between`.
- **Brand:** Fjalla One uppercase, `clamp(1.75rem, 1.1rem + 3vw, 2.75rem)`, `letter-spacing: 0.06em`. Misma escala tipográfica que el `<h1>`.
- **Nav links:** Source Sans Pro, `clamp(0.8rem, 0.7rem + 0.5vw, 1rem)`, blanco en reposo → navy (`#0B0146`) en hover/focus. `white-space: nowrap` para evitar wrap.
- **Mobile:** Sin menú hamburguesa — los tres ítems permanecen en línea y se escalan con `clamp`. Espacio entre ítems via `margin-left: clamp(0.75rem, 1.5vw, 1.5rem)`.

### Social Icons
- **Style:** 50×50px, `border-radius: 8px` (`{rounded.md}`), background-image SVG a 50×50px.
- **Hover / Focus:** `transform: translateY(-3px)`, `opacity: 0.85`. Transición `0.2s cubic-bezier(0.16, 1, 0.3, 1)`. Sin outline en focus-visible para mantener limpieza visual (el `aria-label` garantiza accesibilidad).
- **Assets:** `img/linkedin.svg` (LinkedIn azul `#0A66C2` sobre rect redondeado blanco), `github.svg` S3 (blanco sobre transparente).

### Reveal Animation (Signature Component)
Cada sección y tarjeta usa `.reveal` + IntersectionObserver. En `prefers-reduced-motion: no-preference`: `opacity: 0 → 1` + `translateY(24px) → none`, duración `0.7s`, easing `cubic-bezier(0.16, 1, 0.3, 1)`, threshold `0.15`, rootMargin `-40px` en bottom. En `prefers-reduced-motion: reduce` o sin IntersectionObserver support: visibilidad inmediata vía clase `is-visible` en JS init. El contenido NUNCA queda oculto.

## 6. Do's and Don'ts

### Do:
- **Do** usar `#0B0146` como único fondo de surfaces de alto impacto (hero, contacto). Su oscuridad casi-negra con tinte morado es el carácter del sistema.
- **Do** mantener `#7FC4FF` estrictamente en los `<span>` del `<h1>`. Su valor viene de su escasez.
- **Do** añadir `prefers-reduced-motion: reduce` a cualquier nueva animación antes de shipper.
- **Do** escalar tipografía con `clamp()`. Ningún tamaño de fuente debe ser un valor fijo sin cláusula responsive.
- **Do** usar `object-fit: cover` para todas las imágenes de header de experiencias, salvo logos de marca con fondo claro que requieren `contain` + `padding`.
- **Do** probar contraste: texto claro sobre `#0B0146` cumple WCAG AA/AAA; `#005086` sobre blanco también. `#7FC4FF` sobre `#0B0146` supera 4.5:1.
- **Do** añadir `target="_blank" rel="noopener"` a todos los links externos.

### Don't:
- **Don't** usar gradientes de ningún tipo — ni en texto (`background-clip: text`), ni en backgrounds, ni en bordes.
- **Don't** usar `glassmorphism`: sin `backdrop-filter`, sin tarjetas translúcidas, sin blur decorativo.
- **Don't** replicar el patrón de portafolio genérico de bootcamp: sin fondos oscuros con acentos neón, sin grids de cards idénticas con íconos, sin animaciones de typing effect.
- **Don't** replicar portafolios de diseñador gráfico: sin tipografías decorativas, sin layouts asimétricos por estética, sin animaciones de carga elaboradas.
- **Don't** usar `border-left` mayor a 1px como acento de color en cards o callouts. Si se necesita separación, usar tinte de fondo o ausencia de borde.
- **Don't** añadir el teal (`#349980`) dentro del contenido. Es exclusivo del chrome (header y footer) y del label `.experience-date`. No en botones internos, badges, ni links de sección.
- **Don't** inventar una variante de botón "secundaria" o "ghost" sin definirla en este sistema primero. Un solo tipo de botón mantiene la voz directa del ingeniero.
- **Don't** añadir sombras a nuevos componentes por defecto. El sistema es plano; cada sombra nueva debe tener justificación funcional.
