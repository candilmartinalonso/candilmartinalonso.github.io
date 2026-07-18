# Auditoría técnica y de experiencia

## Hallazgos iniciales

- La URL principal devolvía 404 pese a existir el repositorio de usuario.
- Tailwind se compilaba en el navegador y el sitio cargaba cinco librerías visuales externas.
- Partículas, tilt, texto escrito, confeti y efectos de puntero aumentaban CPU, transferencia y distracción.
- El CSS estaba repartido entre un bloque inline y un archivo `styles.css` que no se enlazaba.
- Había una declaración CSS inválida (`transition: background-color: 0.3s ease`).
- La fotografía JPEG de 1280 × 960 se descargaba completa para mostrarse en un recorte pequeño.
- Los enlaces externos con `target="_blank"` no incluían `rel="noreferrer"`.
- Faltaban favicon propio, URL canónica, Open Graph completo, datos estructurados, sitemap, página 404 y CI/CD.

## Decisiones aplicadas

- Se reemplazó Tailwind y todas las librerías visuales por HTML, CSS y JavaScript propios.
- La narrativa prioriza propuesta profesional, experiencia verificable y contacto.
- La trayectoria usa elementos `details` nativos, utilizables con mouse, teclado o lector de pantalla.
- La imagen se procesa en WebP y JPEG cuadrados; se conserva el original en `source/`.
- Vite minifica y versiona assets. GitHub Actions valida pull requests y despliega `main`.
- Se incorporaron navegación accesible, foco visible, contenido saltable y movimiento reducido.

## Ambigüedades preservadas

- Se mantuvieron empleadores, fechas, formación y estado “presente” del contenido existente; no se verificaron externamente.
- El texto original indica búsqueda activa. Se conserva como “abierto a nuevos desafíos”.
- No se agregó teléfono, ubicación, CV descargable ni proyectos porque no había datos o archivos confirmados.

## Revisión recomendada de contenido

- Confirmar periódicamente que la experiencia marcada como actual siga vigente.
- Agregar resultados cuantificables solo cuando puedan respaldarse.
- Incorporar un CV descargable si se dispone de una versión pública actualizada.

## Validación realizada

- `npm run build`: HTML válido y build de producción correcto.
- Revisión visual completa en 1440 px y 390 px, sin desbordes horizontales ni recursos faltantes.
- Axe en desktop y móvil: sin infracciones WCAG A/AA detectadas.
- Lighthouse móvil local: 100 en Rendimiento, Accesibilidad, Buenas prácticas y SEO.
- Métricas de laboratorio: LCP 1,4 s, TBT 0 ms, CLS 0 y transferencia inicial aproximada de 61 KiB.

Los resultados de Lighthouse son mediciones de laboratorio y pueden variar en producción según el dispositivo y la red.
