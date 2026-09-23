# Basilico Italian Bistro

Landing page de un restaurante italiano en San Salvador, ubicado en el nivel
superior de la Biblioteca Nacional de El Salvador (BINAES). Sitio estático de
una sola página: hero, sobre el restaurante, menú, ubicación y reservas.

## Stack

HTML + CSS + JavaScript puro. Sin build, sin backend, sin dependencias de
Node — todo corre en el navegador.

- `index.html` — contenido y estructura
- `css/style.css` — estilos, variables de color, responsive
- `js/main.js` — scroll suave, animaciones al hacer scroll (IntersectionObserver), menú hamburguesa en móvil, año del footer

Fuentes vía Google Fonts (Playfair Display + Inter) e iconos vía Font Awesome,
ambos por CDN.

## Correr en local

```bash
python3 -m http.server 8000
```

Y abrir `http://localhost:8000`.

## Qué le falta

- `about-image-placeholder` y `location-map` son cajas de color de relleno,
  no una foto real del restaurante ni un mapa embebido
- Botones "Llamar" y "WhatsApp" usan un número de ejemplo
  (`+503 7369 9652`) — confirmar el real antes de publicitar el sitio
