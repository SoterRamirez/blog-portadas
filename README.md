# Portadas del blog de Dirección de Proyectos

Imágenes de portada para los artículos de
[blog.soterramirez.dev](https://blog.soterramirez.dev).

Este repositorio existe por una razón técnica: **la API de Blogger no permite subir
archivos**, así que las portadas tienen que estar alojadas fuera y referenciarse por URL.
Se sirven por GitHub Pages, que entrega los PNG con el tipo MIME correcto
(`raw.githubusercontent.com` no sirve: manda los archivos como texto plano).

## Contenido

811 portadas de 1200×630 px (tamaño estándar de Open Graph), una por tema, agrupadas por
serie. Cada una lleva el nombre de la serie, el título del artículo y su referencia
`Serie N · Semana N · Tema N.N`. Una paleta por serie, para que el lector reconozca de
qué materia es cada artículo de un vistazo.

## Cómo se generan

No se dibujan a mano: las genera `src/blogdp/covers.py` del repositorio del pipeline como
SVG deterministas (el mismo tema produce siempre la misma portada) y se convierten a PNG
con `rsvg-convert`. Regenerarlas todas toma unos 15 segundos.

## Uso

```
https://soterramirez.github.io/blog-portadas/covers/<serie-slug>/<tema-slug>.png
```

## Licencia

Contenido original. Los títulos provienen de artículos propios del blog.
