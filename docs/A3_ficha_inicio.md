# A3 - Ficha de especificaciones de Inicio

El frame está a 1x, así que 1 px de Figma es 1 dp en las medidas y 1 sp en los textos.

## Colores

Cada color tiene el nombre de su función (roles de Material 3). La columna "Oscuro" va en values-night/colors.xml.

| Nombre | Figma | Android | Oscuro | Dónde se usa |
|---|---|---|---|---|
| surface | #F4FBF8 | #FFF4FBF8 | #FF0E1513 | Fondo de la pantalla |
| on_surface | #161D1B | #FF161D1B | #FFDDE4E1 | Título, categorías, "Novedades", nombre y precio |
| on_surface_variant | #3F4947 | #FF3F4947 | #FFBEC9C6 | Iconos, texto del buscador, edades, etiquetas inactivas |
| surface_container | #E9EFED | #FFE9EFED | #FF1A211F | Tarjetas de producto y barra de navegación |
| surface_container_high | #E3EAE7 | #FFE3EAE7 | #FF252B2A | Fondo del buscador |
| surface_container_highest | #DDE4E1 | #FFDDE4E1 | #FF303635 | Tarjetas de categoría |
| secondary_container | #CCE8E2 | #FFCCE8E2 | #FF334B47 | Indicador de la pestaña activa |
| secondary | #4A635F | #FF4A635F | #FFB1CCC6 | Etiqueta activa "Inicio" |
| primary | #006A60 | #FF006A60 | #FF82D5C8 | Texto del botón "Ver todo" |
| on_primary | #FFFFFF | #FFFFFFFF | #FF003731 | Pareja de primary en el tema |
| error | #BA1A1A | #FFBA1A1A | #FFFFB4AB | Fondo del badge del carrito |
| on_error | #FFFFFF | #FFFFFFFF | #FF690005 | Número del badge |
| surface_overlay | #F4FBF8 al 80 % | #CCF4FBF8 | #CC0E1513 | Fondo del corazón sobre la foto |

Transparencias: en Android el canal alfa va delante (#AARRGGBB). El fondo del corazón es surface al 80 %: 0,80 x 255 = 204, que en hexadecimal es CC, así que queda #CCF4FBF8 (surface_overlay).

## Tipografías

Todo es Roboto (en res/font) y sin mayúsculas. El espaciado de Figma viene en px y en Android va en em, así que se divide entre el tamaño de la letra.

| Estilo | Peso | Tamaño | Interlineado | Espaciado (em) | Dónde |
|---|---|---|---|---|---|
| TitleLarge | Regular 400 | 22 sp | 28 sp | 0 | tv_titulo |
| BodyLarge | Regular 400 | 16 sp | 24 sp | 0,5 / 16 = 0,03125 | et_buscar |
| TitleMedium | Medium 500 | 16 sp | 24 sp | 0 | categorías, tv_novedades, tv_precio_producto |
| BodyMedium | Regular 400 | 14 sp | 20 sp | 0 | edades, tv_nombre_producto |
| LabelLarge | Medium 500 | 14 sp | 20 sp | 0,1 / 14 = 0,00714 | btn_ver_todo |
| LabelMedium | Medium 500 | 12 sp | 16 sp | 0,5 / 12 = 0,04167 | etiquetas de bnv_inicio |
| LabelSmall | Medium 500 | 11 sp | 16 sp | 0,5 / 11 = 0,04545 | tv_badge_carrito |

## Medidas (dp)

| Elemento | Tamaño | Esquinas |
|---|---|---|
| Pantalla (activity_inicio) | 360 x 800, márgenes de 16 | - |
| Barra superior (tb_inicio) | 360 x 64 | - |
| Botones de icono | 48 x 48 (icono de 24) | - |
| Buscador (ll_buscador) | 328 x 56 | 28 |
| Tarjetas de categoría | 104 x 120, 8 entre ellas | 12 |
| Tarjeta de producto (cv_producto) | 156 x 284, 16 entre ellas | 12 |
| Barra de navegación (bnv_inicio) | 360 x 64 | - |
