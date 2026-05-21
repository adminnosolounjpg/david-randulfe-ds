# David Randulfe — Brand Guidelines

Guía oficial de uso de marca. Aplica a presentaciones, landings, emails, ads, banners, PDFs y cualquier comunicación visual.

> Asesoramos a negocios online que quieren escalar su facturación a más de 1.000.000€ anuales. La estética de David es **tech, masculina, con presencia y solidez** — coherente con su propuesta de sistemas que escalan sin sacrificar margen.

---

## 1. Logo

### Variantes disponibles

| Archivo | Uso |
|---|---|
| `assets/logos/randulfe-34.png` | **Lockup wordmark navy** — navbar, hero sobre fondo claro |
| `assets/logos/randulfe-35.png` | Wordmark cobalto brand — versión color sobre blanco |
| `assets/logos/randulfe-36.png` | Wordmark blanco — footer dark, secciones brand |

### Espacio mínimo (clear space)

Mantén un margen libre alrededor del wordmark equivalente a la altura de la "R" inicial. El feel sólido de David requiere claridad, no apretar márgenes.

### Tamaño mínimo

- **Digital:** 32px de altura mínimo
- **Impreso:** 15mm de altura mínimo

### Prohibiciones (NO hacer)

- ❌ Estirar, comprimir o rotar
- ❌ Cambiar tipografía o pesos del wordmark
- ❌ Aplicar sombras o gradientes
- ❌ Colocar el wordmark sobre fondos con bajo contraste (cobalto sobre navy)
- ❌ Añadir decoraciones (sparkles, ondas) — la marca de David es minimalista tech

### Uso por contexto

- **Slides:** logo SOLO en portada (slide 01), `randulfe-34.png`.
- **Landings:** logo navbar `randulfe-34.png`, footer `randulfe-36.png` (blanco sobre navy).
- **Emails:** logo header `randulfe-34.png` 32-40px de altura.

---

## 2. Paleta de colores

### Paleta primaria (cobalto profundo)

| Token | Hex | Uso |
|---|---|---|
| `--iw-primary` | `#3430D2` | Cobalto brand — CTA, highlights, líneas, fondos de impacto |
| `--iw-primary-hover` | `#2722A8` | Hover de CTA |
| `--iw-dark` | `#1A1857` | Navy profundo (casi morado) — texto principal, fondos hero/cards dark |
| `--iw-light` | `#DFDDFF` | Lila muy claro — cards, decoraciones sobre dark |
| `--iw-light-soft` | `#F0EFFF` | Lila ultra claro — fondos sutiles |
| `--iw-mid` | `#A8A8E5` | Lila medio (texto OSCURO sobre este — bajo contraste con blanco) |
| `--iw-mid-dark` | `#8C89E8` | Lila medio oscuro |

### Texto

| Token | Hex | Uso |
|---|---|---|
| `--iw-ink` | `#1A1857` | Texto principal (navy profundo) |
| `--iw-ink-soft` | `#4B5563` | Texto secundario |
| `--iw-on-dark` | `#FFFFFF` | Texto sobre fondos brand o navy |

### Combinaciones permitidas

- **Navy `#1A1857` + Cobalto `#3430D2`** → patrón mitad-mitad en titulares
- **Cobalto puro → texto siempre BLANCO**
- **Navy profundo → decoraciones en `var(--iw-light)` `#DFDDFF`** (NO en cobalto, no contrasta)
- **Lila claro `#DFDDFF` al 45% transparencia + texto navy** → cards delicados

### Combinaciones PROHIBIDAS

- ❌ Cobalto sobre navy profundo (NO contrasta, ambos son tonos morados oscuros)
- ❌ Texto navy sobre fondo cobalto (siempre blanco sobre cobalto)
- ❌ Lila mid `#A8A8E5` con texto blanco (texto oscuro funciona mejor)

---

## 3. Tipografía

### Familia

**Inter** — sans-serif moderna con 9 pesos (100-900) en `assets/fonts/`.

Fallback CSS: `'Inter', system-ui, -apple-system, 'Segoe UI', sans-serif`

### Jerarquía

| Estilo | Peso | Tamaño | Line-height | Uso |
|---|---|---|---|---|
| Display | 900 | 80-104px | 1.05 | Cover, hero principal |
| H1 | 700 | 52-68px | 1.05 | Titulares de slide / sección |
| H2 | 800 | 48-56px | 1.10 | Sub-titulares mayores |
| H3 | 700 | 32-40px | 1.15 | Cards, sub-secciones |
| Lead | 400 | 24-28px | 1.45 | Subtítulos |
| Body | 400 | 18-22px | 1.55 | Cuerpo principal |

### Reglas para David

- **Pesos altos OK** (800-900 en displays). David vende presencia y solidez, los pesos heavy comunican esto.
- **NO italic decorativo.** Sin GiftenSans ni serifs italics. El feel es tech, no editorial.
- **Patrón mitad-mitad** en titulares: mitad navy + mitad cobalto. La palabra-bisagra en `<span class="iw-hl">…</span>`.
- **Letter-spacing -0.02em** en h1 — densidad tech.
- **NUNCA eyebrow sobre headlines.**

### Ejemplo

```html
<h1>Asesoramos a negocios online que quieren <span class="iw-hl">escalar su facturación</span> a más de 1.000.000€ anuales</h1>
```

---

## 4. Sistema de espaciado

| Token | Valor | Uso |
|---|---|---|
| `--iw-space-2xs` | 8px | Gaps mínimos |
| `--iw-space-xs` | 16px | Gaps entre elementos relacionados |
| `--iw-space-s` | 24px | Padding interno cards |
| `--iw-space-m` | 40px | Margen entre bloques |
| `--iw-space-l` | 64px | Separación entre secciones |
| `--iw-space-xl` | 96px | Padding generoso de slides |

### Border-radius

| Token | Valor | Uso |
|---|---|---|
| `--iw-radius-pill` | 12px | Pills, badges |
| `--iw-radius-card` | 16px | Cards estándar |
| `--iw-radius-cardLg` | 24px | Cards grandes, media, widgets |
| `--iw-radius-circle` | 9999px | Avatares, CTAs pill |

---

## 5. Iconografía

### Estilo

**Lucide icons** outline, sin variaciones.

### Specs

- **ViewBox:** `0 0 24 24`
- **Stroke-width:** `2`
- **Stroke-linecap:** `round`
- **Stroke-linejoin:** `round`
- **Fill:** `none`

### Color por contexto

- **Sobre fondo claro:** `var(--iw-primary)` (cobalto brand)
- **Sobre fondo dark (navy profundo):** `var(--iw-light)` `#DFDDFF` o BLANCO — NO cobalto (no contrasta)
- **En slides dark de stats / testimonials:** decoraciones en light, NO en brand

### Prohibiciones

- ❌ Iconos macizos rellenos
- ❌ Sparkles, estrellas o iconos místicos (Anna usa estos, NO David)
- ❌ Iconos en colores no-sistema
- ❌ Mezclar 2 estilos de iconografía

---

## 6. Decoración visual

### Widgets flotantes

Firma visual de David: 2-3 "dashboards/widgets" flotantes superpuestos a la foto principal del hero. Tipos:
- Card light con donut progress + label cobalto
- Card light con número grande + sparkline cobalto
- Card cobalto sólido tipo "Importante" con texto blanco

### Curved arc dividers

David usa transiciones entre secciones con **arco curvo navy** que entra desde arriba (visto en su CTA final). Este patrón es exclusivo de David — IW y Anna NO lo usan.

### Líneas tech

Líneas sutiles cobalto que conectan elementos. Más rectas/limpias que las serpenteantes de IW.

### Fondos

- **Principal:** `assets/bg/fondos-10.jpg` (lila claro `#BFBFFF` + R gigante + arc cobalto sup-izq)
- **Brand intenso:** `assets/bg/fondos-12.jpg` (cobalto sólido + R blanca + arc)
- **Cards delicadas:** `rgba(223, 221, 255, 0.45)` (light al 45%)

### Sin elementos místicos

- ❌ Sparkles ⋆
- ❌ Flor de vida
- ❌ Italics decorativos serif

---

## 7. Fotografía

### Estilo

- **Corporativa, business, profesional.**
- Retratos de David con confianza, mirada directa.
- Iluminación limpia (no cálida ni etérea).
- Composiciones con dashboards, datos, laptops como elementos de credibilidad.

### Tratamiento

- **Border-radius:** 24px o cuadrado con esquinas suavizadas
- **Aspect-ratio:** 4:5 retrato hero, 1:1 cuadrado testimonial
- **Object-fit: cover**

### Testimonials horizontales

A diferencia de IW (foto arriba) y Anna (foto a la izquierda redonda), David usa **foto CUADRADA a la izquierda + quote a la derecha** en sus cards testimoniales. Es su patrón distintivo.

### Prohibiciones

- ❌ Stock photos cliché de "businessman high-five"
- ❌ Filtros vintage o duotone
- ❌ Retratos con tonos cálidos o etéreos (eso es Anna)

### Si no hay foto propia

Usar Unsplash con keywords:
`entrepreneur,laptop,confident`, `business,dashboard`, `data,growth`, `automation,tech`.

---

## 8. Voz y tono

> La voz se gestiona desde las skills de texto de la agencia.

Recordatorio: tuteo directo, frases cortas y afiladas, diagnóstico antes que solución, vocabulario tech (sistema, criterio, escalar, palanca, leverage, compounding). **NUNCA hype ni floreo motivacional.**

---

## 9. Reglas no negociables del sistema

1. **Cobalto brand puro → contenido siempre BLANCO.**
2. **Sobre navy profundo (dark), decoraciones en `var(--iw-light)`, NO en cobalto.** El cobalto sobre navy NO contrasta.
3. **Pesos altos OK** (800-900 en displays). Comunica solidez.
4. **NO sparkles, NO italics serif decorativos.** El feel es tech, no espiritual.
5. **Patrón mitad-mitad** en titulares (navy + cobalto).
6. **NUNCA eyebrow sobre headlines.**
7. **Testimonials horizontales** (foto izquierda + quote derecha) — patrón exclusivo de David.
8. **Widgets flotantes** en heros y secciones de credibilidad — firma visual.
9. **Curved arc dividers** opcionales entre secciones de impacto.
10. **Whitespace > densidad.** Tech limpio, no recargado.

---

## 10. Checklist antes de publicar

- [ ] Cobalto puro → texto blanco
- [ ] Sobre navy: decoraciones en light, no cobalto
- [ ] Tipografía Inter coherente, pesos heavy donde aplique
- [ ] Iconos Lucide stroke 2, sin sparkles ni italics
- [ ] Testimonials horizontales (foto izq + quote der)
- [ ] Widgets flotantes en hero
- [ ] Patrón mitad-mitad en headlines
- [ ] Sin eyebrow sobre headlines
- [ ] Sin elementos místicos (sparkles, mandalas)

---

## Recursos

- **Tokens CSS:** `tokens.css`
- **Catálogo de slides:** `preview.html`
- **Catálogo de componentes:** `preview-components.html`
- **Repositorio:** https://github.com/adminnosolounjpg/david-randulfe-ds
