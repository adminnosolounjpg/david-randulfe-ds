# David Randulfe — Design System

Sistema de diseño completo para presentaciones, landings y comunicación visual de David Randulfe. Pensado para conectarse a [Claude Design](https://claude.ai/design) (vía GitHub) y para uso directo del equipo.

## Estructura

```
david-randulfe/
├── tokens.css              ← Fuente única de verdad: paleta, tipografía, componentes
├── preview.html            ← Catálogo visual de todas las plantillas y diagrams
├── README.md               ← Este archivo
├── assets/
│   ├── fonts/              ← Inter (9 pesos, .ttf)
│   ├── logos/              ← Variantes del logo (lockup, color, blanco)
│   └── bg/                 ← Fondos originales (lila claro / cobalto brand, con "R" + arc)
├── lib/
│   └── iw-interact.js      ← Sistema de interactividad (hover, dimming, stagger)
├── slides/                 ← 10 plantillas base
└── diagrams/               ← 19 smart diagrams
```

## Tokens de marca

| Token | Valor | Uso |
|---|---|---|
| `--iw-primary` | `#3430D2` | Cobalto brand — acentos, highlights, CTA, líneas |
| `--iw-dark` | `#1A1857` | Navy profundo — texto principal, fondos hero |
| `--iw-light` | `#DFDDFF` | Cards, pills, badges (al 45-50% transparencia) |
| `--iw-mid` | `#A8A8E5` | Tono lila medio (texto oscuro por contraste con fondo) |
| `--iw-ink` | `#1A1857` | Texto principal |
| `--iw-ink-soft` | `#4B5563` | Texto secundario |
| Fuente | Inter | 9 pesos disponibles (100 → 900) |
| Ratio slides | 16:9 (1920×1080) | Lienzo base |

Cualquier modificación de marca se hace en **`tokens.css`** y se propaga a todas las plantillas.

## Detalles específicos de la identidad

- **Pesos altos OK:** mantiene 800-900 para títulos (feel tech, masculino, con presencia)
- **Strokes estándar:** SVG con `stroke-width: 2`
- **Sin estrellitas decorativas.** Bullets clásicos con dot circular en cobalto.
- **Highlights** en `.iw-hl` con bold + cobalto (igual que IW, no italic).
- **Cover con logo** `randulfe-34.png` a 52px de altura.

## Cómo previsualizar

### Servidor local (recomendado)

```bash
cd david-randulfe
python -m http.server 8765
```

Luego abre [http://localhost:8765/preview.html](http://localhost:8765/preview.html).

### Opción directa

Doble click sobre `preview.html`. Si el navegador bloquea fuentes locales con `file://`, usa el servidor.

## Cómo añadir contenido nuevo

### Reemplazar el placeholder vacío por una imagen

Cualquier `<div class="iw-media">…</div>` acepta una imagen:

```html
<div class="iw-media">
  <img src="../assets/photos/david-portada.jpg" alt="David Randulfe">
</div>
```

### Crear una nueva diapositiva

1. Copia la plantilla más cercana (ej: `slides/02-content-bullets.html`).
2. Renómbrala.
3. Cambia el contenido. Reutiliza componentes globales (`iw-h1`, `iw-checklist`, `iw-pill`, etc.).
4. Si necesitas un componente nuevo, añádelo a `tokens.css` con prefijo `iw-`.

## Conexión con Claude Design

Al crear un design system para David Randulfe:

1. **Link code on GitHub:** apunta a este repo.
2. **Add fonts, logos and assets:** sube manualmente los logos de `assets/logos/`.
3. **Any other notes:** la voz y tono del cliente se gestiona desde las skills de texto de la agencia, no en este repo.

## Reglas no negociables del sistema

- **Logo solo en portada (slide 01).** El resto de slides sin logo.
- **Fondo de marca en TODOS los slides:** `assets/bg/fondos-10.jpg`.
- **Fondos lavanda con 40–50% transparencia.** Excepción: círculos contenedores de iconos sólidos.
- **Nunca flechas hand-drawn SVG.**
- **Iconos estilo Lucide** (viewBox 24, stroke 2, line caps redondos).
- **Minimalismo extremo:** whitespace > densidad.
- **Jerarquía visual obligatoria.**
- **Brand puro `#3430D2` → contenido siempre blanco.** Mid `#A8A8E5` → texto oscuro (contraste insuficiente con blanco sobre fondo claro).
- **Sin elementos místicos** (estrellas, italics decorativos). El feel es tech, no espiritual.
- **NUNCA usar eyebrow/kicker/texto sobre los headlines**. Los títulos abren la slide sin texto encima — la diapositiva empieza directamente por el h1. Composición limpia.
- **Peso del h1: 700** (no 800). Presencia sin machacar.

## Mantenimiento

- **Source of truth:** este repo. Cualquier cambio se commitea aquí.
- **Distribución:** `git pull` en local. Claude Design re-lee al refrescar.
- **Cambios visuales:** en `tokens.css`. NO en cada slide individual.
