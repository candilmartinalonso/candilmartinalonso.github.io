# Portfolio de Martín Alonso Candil

Portfolio profesional de Martín Alonso Candil, Licenciado en Relaciones Laborales. Presenta perfil, experiencia, competencias, formación y canales de contacto en una interfaz rápida y accesible.

## Características

- Diseño responsive con HTML semántico y CSS propio.
- Navegación accesible, foco visible y soporte para movimiento reducido.
- Experiencia profesional organizada en paneles expandibles nativos.
- Fotografía optimizada en WebP con fallback JPEG.
- SEO técnico, datos estructurados, Open Graph, sitemap y página 404.
- Assets minificados y versionados mediante Vite.
- Build automático en pull requests y despliegue a GitHub Pages desde `main`.

## Desarrollo local

Requiere Node.js 22 o superior.

```bash
npm install
npm run dev
```

Build de producción:

```bash
npm run build
npm run preview
```

## Estructura

```text
.
├── .github/workflows/pages.yml
├── public/
├── source/
│   └── profile-original.jpg
├── src/
│   ├── assets/
│   ├── main.js
│   └── styles.css
├── index.html
└── vite.config.js
```

## Contenido

Los datos profesionales se editan en `index.html`. Después de actualizar puestos, fechas o formación, verificá que los metadatos del `<head>` y los datos estructurados sigan siendo correctos.

## Despliegue

El workflow `pages.yml` valida el build en cada pull request. Al fusionar en `main`, publica el directorio `dist` en GitHub Pages.

URL: <https://candilmartinalonso.github.io/>

## Contribuciones

Creá una rama desde `main`, verificá `npm run build` y abrí un pull request con el alcance del cambio.
