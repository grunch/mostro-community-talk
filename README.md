# Mostro Community Talk #1 — Slidev Presentation

Primera llamada con comunidades hispanohablantes de `mostro.community`.

## Setup

```bash
# Requiere Node.js 18-22 (recomendado: 20 LTS)
npm install
```

## Run

```bash
npm run dev
# Abre en http://localhost:3030
```

## Presenter Mode

Presiona `P` en el navegador para abrir presenter mode (notas + timer + preview).

## Navigation

- `→` / `Space` — siguiente slide/animación
- `←` — slide anterior
- `O` — overview
- `D` — dark/light toggle
- `F` — fullscreen

## Export to PDF

```bash
npm run export
# Genera slides-export.pdf
```

Si falta Chromium para exportar:

```bash
npx playwright install chromium
npm run export
```

## Customization

- **Slides**: editar `slides.md`
- **Imágenes**: carpeta `public/`
  - `public/mostro-node.png`
  - `public/mostro-mobile.png`
  - `public/mostrix-logo.png`
  - `public/mostro-watchdog.png`

## Estructura de la charla

- Duración objetivo: **20-25 min** + Q&A
- Speaker notes en comentarios HTML (`<!-- -->`)
- Incluye 2 slides backup para preguntas:
  - Disputas
  - Seguridad operativa

## Proyectos clave incluidos

- <https://github.com/MostroP2P/mostro>
- <https://github.com/MostroP2P/mobile>
- <https://github.com/MostroP2P/mostrix>
- <https://github.com/MostroP2P/mostro-watchdog>
