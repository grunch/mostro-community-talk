# Mostro Community Talk #1 — Slidev Presentation

Primera llamada con comunidades hispanohablantes de `mostro.community`.

**Available in:**
- 🇪🇸 Spanish: [mostro.community](https://mostro.community) (default)
- 🇬🇧 English: [mostro.community/en/](https://mostro.community/en/)

## Setup

```bash
# Requiere Node.js 18-22 (recomendado: 20 LTS)
npm install
```

## Run

```bash
# Spanish version
npm run dev

# English version
npm run dev:en
```

## Presenter Mode

Presiona `P` en el navegador para abrir presenter mode (notas + timer + preview).

## Navigation

- `→` / `Space` — siguiente slide/animación
- `←` — slide anterior
- `O` — overview
- `D` — dark/light toggle
- `F` — fullscreen

## Build

```bash
# Build both versions
npm run build

# Build Spanish only
npm run build:es

# Build English only
npm run build:en
```

Output:
- `dist/` → Spanish version
- `dist/en/` → English version

## Export to PDF

```bash
# Spanish
npm run export

# English
npm run export:en
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
