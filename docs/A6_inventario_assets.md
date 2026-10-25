# A6 - Inventario de assets

Los iconos van como VectorDrawable, importados del SVG de Figma, y las fotos como WebP en drawable-xxhdpi, exportadas en PNG a 3x. Lo que es solo un color con esquinas va en XML. Los SVG y PNG exportados están en la carpeta [figma](figma).

| Asset | Formato | Carpeta | Origen | Por qué |
|---|---|---|---|---|
| ic_menu, ic_buscar, ic_carrito | VectorDrawable | drawable | SVG de Figma | Es vectorial, vale para todas las densidades. |
| ic_favorito | VectorDrawable | drawable | SVG de Figma | Se repite en cada tarjeta. |
| ic_nav_inicio, ic_nav_catalogo, ic_nav_favoritos | VectorDrawable | drawable | SVG de Figma | Iconos de la barra de navegación. |
| img_pijama_dinosaurios, img_vestido_punto | WebP (calidad 75 %) | drawable-xxhdpi | PNG a 3x de Figma (fotos de Unsplash) | Son fotos. 3x es la densidad xxhdpi. |
| bg_buscador, bg_badge_carrito, bg_favorito | XML (shape) | drawable | No se exporta | Solo son un color con esquinas o un círculo. |
| roboto_regular.ttf, roboto_medium.ttf | TTF | font | Roboto para Android | Los dos pesos que usa la pantalla. |
| Tarjetas, barra de navegación y botón "Ver todo" | - | - | No se exportan | Los dibujan los componentes de Material. |

| Foto | PNG | WebP | Ahorro |
|---|---|---|---|
| img_pijama_dinosaurios | 382 KB | 17 KB | 95 % |
| img_vestido_punto | 353 KB | 15 KB | 96 % |
