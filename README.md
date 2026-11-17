# xabimauleon

Portfolio de Xabier Mauleón — xabimauleon.netlify.app

Una sola página estática. No hay compilación, no hay dependencias, no hay
nada que instalar: lo que ves en el repositorio es exactamente lo que se
publica.

## Qué hay dentro

```
index.html              la página entera — maqueta, estilos y guion
img/retrato.webp        el retrato
img/mk/*.webp           las piezas de los veinte proyectos
cv-xabier-mauleon.pdf   el CV, enlazado desde el pie
og.jpg                  la tarjeta de 1200×630 para compartir en redes
favicon.svg
icono-180.png           icono para iOS
netlify.toml            carpeta publicada, redirecciones y caché
```

## Cómo se despliega

Netlify está enlazado a la rama `main`. Cada push publica. No hay comando de
compilación: `netlify.toml` declara la raíz del repositorio como carpeta
publicada.

## Cómo se edita

Los proyectos viven en el array `OBRA` dentro de `index.html`. Los seis
primeros son los destacados de la lista grande; el resto sale en el índice
del bloque negro. La constante `PRINCIPALES` marca dónde está el corte.

Cada entrada lleva nombre, cliente, disciplina, año, descripción, la lista de
piezas con su proporción, las decisiones de proyecto y los enlaces en vivo.
Las proporciones de `mk` son ancho dividido por alto de cada imagen: si
cambias una imagen, cambia el número.

La maqueta de escritorio son coordenadas absolutas multiplicadas por `--k`,
que vale 1 a 1440 px y escala con la ventana. Por debajo de 1180 px todo pasa
a flujo normal y mandan los márgenes de las media queries.

## Las imágenes

WebP a calidad 82, con el ancho tope en 1600 px. El montaje no llega a pedir
más ni en una pantalla grande a doble densidad.
