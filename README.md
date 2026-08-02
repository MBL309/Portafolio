# Portafolio — Michell Benzant Lorenzo

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

Después de editar, solo hace falta guardar el archivo y subir el cambio (`git add`, `commit`, `push`) — GitHub Pages lo redepliega automáticamente.

## Publicar / actualizar en GitHub Pages

1. Sube los cambios a la rama configurada como fuente de Pages (normalmente `main`):
   ```bash
   git add index.html
   git commit -m "Actualiza contenido del portafolio"
   git push
   ```
2. En el repositorio: **Settings → Pages** → confirma que la fuente sea la rama y carpeta correctas (`main` / `root`, o `docs` si moviste el archivo ahí).
3. El despliegue tarda uno o dos minutos; el sitio queda disponible en la URL indicada arriba.

## Notas técnicas

- Sin dependencias externas ni paso de build — es un solo archivo servible desde cualquier hosting estático.
- Tipografías: `Space Grotesk` (títulos), `Inter` (cuerpo) y `JetBrains Mono` (etiquetas/código) — si no están instaladas localmente, el navegador usa los *fallbacks* del CSS.
- Respeta `prefers-reduced-motion`: las animaciones se desactivan si el usuario lo indica en su sistema.
- Diseño responsive, probado desde ~360px de ancho en adelante.