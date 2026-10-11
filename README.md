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

## Agregar fotos 360° (girar el plato deslizando)
1. Poné el plato sobre una mesa giratoria (o caminá alrededor) y sacá 24 fotos, una cada 15° aprox., siempre a la misma altura y distancia.
2. Nombralas así: `giro-cheesecake-01.webp`, `giro-cheesecake-02.webp` … `giro-cheesecake-24.webp` (el nombre del medio es el `id` del plato). Sirven también en .jpg si cambiás la extensión en el código.
3. Subilas al repo y en el plato agregá `giro: 24`.

## Agregar un plato en 3D con realidad aumentada ("Ver en tu mesa")
1. Escaneá el plato con una app gratuita como **KIRI Engine**, **Polycam** o **Luma AI**: caminá despacio alrededor del plato (2 o 3 vueltas a distintas alturas), con buena luz y sin brillos fuertes.
2. Exportá el modelo como **.glb** (y, si la app lo permite, también **.usdz** para iPhone). Que pese menos de 5 MB.
3. Subí el archivo al repo con un nombre simple, por ejemplo `cheesecake.glb`.
4. En el plato agregá `modelo: 'cheesecake.glb'` (y opcionalmente `modeloIOS: 'cheesecake.usdz'`).
5. Al abrir el plato aparece el visor 3D y el botón **Ver en tu mesa**, que abre la cámara y coloca el plato sobre la mesa.

## Pendiente antes de producción
- Confirmar alérgenos con la cocina (los actuales son orientativos, deducidos de las descripciones).
- Reseñas compartidas entre todos los clientes (base de datos, por ejemplo Firebase o Supabase).
- Código QR para las mesas.
