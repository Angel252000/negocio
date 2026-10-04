# CLAUDE.md

Landing page de una sola página para Basilico Italian Bistro (restaurante italiano
en la BINAES, San Salvador).

## Stack

HTML + CSS + JavaScript puro. Sin build, sin `package.json`, sin backend.
Google Fonts (Playfair Display + Inter) y Font Awesome 6.4 por CDN.

## Archivos

| Archivo | Rol |
|---|---|
| `index.html` | Todo el contenido: hero, nosotros, menú, ubicación, reservas, footer |
| `css/style.css` | Estilos. Colores en variables `:root` (`--primary-gold`, `--primary-dark`) |
| `js/main.js` | Scroll suave, fade-in con IntersectionObserver, fondo del header al hacer scroll, menú móvil, año del footer |

## Comandos

```bash
python3 -m http.server 8000   # abrir http://localhost:8000
```

No hay tests ni linter configurados.

## Gotchas

- El scroll suave intercepta todos los `a[href^="#"]`. Un `href="#"` solo no es un
  selector válido; el handler lo trata aparte (sube al inicio). Mantener ese caso
  si se toca el handler.
- El menú móvil es un `div.mobile-menu` con `role="button"`; `aria-expanded` se
  actualiza desde `main.js`. Si se cambia a `<button>`, revisar los estilos.
- Placeholders pendientes: `.about-image-placeholder` y `.location-map` son cajas
  de color, y el teléfono `+503 7369 9652` es de ejemplo. Los enlaces de redes
  sociales apuntan a `#`.
- El año del footer lo pone JS; el `2026` del HTML es solo respaldo.
