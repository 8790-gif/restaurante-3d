# Capitão · Menú interactivo

Demo de carta digital para Capitão (Ciudad del Este): platos con foto, precios, opciones, alérgenos y reseñas por plato.

## Cómo verlo
Doble clic en `index.html`. Todo está en un solo archivo (las fotos van incluidas adentro).

## Publicarlo con GitHub Pages
1. Subí `index.html` y `README.md` al repositorio.
2. **Settings → Pages** → "Deploy from a branch" → rama **main**, carpeta **/ (root)** → Save.
3. En un par de minutos queda en `https://8790-gif.github.io/NOMBRE-DEL-REPO/`.

## Editar la carta
En `index.html`, buscá `const PLATOS = [`. Cada plato tiene `nombre`, `precio` (o `opciones` con varios precios), `desc`, `contiene` (alérgenos) y opcionalmente `foto` y `modelo`.

## Agregar un plato en 3D
1. Escaneá el plato con Polycam, KIRI Engine o Luma AI y exportalo como `.glb`.
2. Subí el archivo al repo (por ejemplo `cheesecake.glb`).
3. En el plato, agregá `modelo: 'cheesecake.glb'`. Aparece la pestaña **3D** para girarlo.

El 3D funciona una vez publicado en GitHub Pages (abriendo el archivo con doble clic el navegador bloquea la carga del modelo).

## Pendiente antes de producción
- Confirmar alérgenos con la cocina (los actuales son orientativos, deducidos de las descripciones).
- Reseñas compartidas entre todos los clientes (base de datos, por ejemplo Firebase o Supabase).
- Código QR para las mesas.
