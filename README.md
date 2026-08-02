# Portafolio — Michel Benzant Lorenzo

Sitio personal de una sola página, construido en HTML/CSS/JS puro (sin frameworks ni dependencias) y publicado con GitHub Pages.

🔗 **Sitio en vivo:** `https://<tu-usuario>.github.io/<nombre-del-repo>/`

## Contenido

- **Hero** — nombre, rol y un fondo animado en SVG que dibuja un grafo de nodos (React, Node.js, Docker, n8n, etc.), como referencia visual a la automatización de flujos.
- **Sobre mí** — perfil profesional y el reconocimiento del Hackathon UTEL × Tiendanube.
- **Stack técnico** — herramientas agrupadas por categoría (Frontend, Backend, Mobile, Automatización & IA, Infraestructura, Bases de datos).
- **Proyecto destacado** — Hackathon "Innovación para Ecommerce" (UTEL × Tiendanube, 1er lugar, marzo 2026).
- **Experiencia en proyectos** — línea de tiempo tipo workflow con los proyectos aplicados por área.
- **Contacto** — enlaces a LinkedIn y correo.

## Estructura

```
.
├── index.html   # todo el sitio: HTML, CSS y JS en un solo archivo
└── README.md
```

## Editar el contenido

Todo vive en `index.html`, no hay build ni compilación:

| Qué cambiar | Dónde buscar |
|---|---|
| Textos (perfil, proyecto, experiencia) | Secciones `<section id="about">`, `#project`, `#experience` |
| Colores | Variables `:root` al inicio del `<style>` (`--bg`, `--cyan`, `--amber`, etc.) |
| Correo de contacto | Atributo `href="mailto:..."` en `#contact` |
| Nodos del fondo animado | Array `labels` dentro del `<script>` al final del archivo |

Después de editar, solo hace falta guardar el archivo y subir el cambio (`git add`, `commit`, `push`) 
