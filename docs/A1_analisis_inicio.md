# A1 - Análisis de la pantalla Inicio

Pantalla elegida: Inicio de Estirón (frame activity_inicio, 360x800 dp).

<img src="img/pantalla_inicio_figma.png" width="250" alt="Pantalla Inicio en la copia de Figma">

## Árbol de bloques

Leyenda: [NP] no se programa, [SUP] se superpone a otro bloque y [REP] se repite.

```
activity_inicio (ConstraintLayout, 360x800 dp)
├── tb_inicio (MaterialToolbar)
│   ├── tv_titulo (TextView "Estirón")
│   ├── fl_carrito (FrameLayout)
│   │   ├── ib_carrito (ImageButton)
│   │   └── tv_badge_carrito (TextView "1")  [SUP]
│   └── icono inicial y capas ocultas  [NP]
├── ll_buscador (LinearLayout horizontal)
│   ├── ib_menu (ImageButton)
│   ├── et_buscar (EditText)
│   └── ib_buscar (ImageButton)
├── ll_categorias (LinearLayout horizontal)  [REP] x3
│   ├── cv_bebe (MaterialCardView)
│   │   └── ll_bebe (LinearLayout vertical)
│   │       ├── tv_bebe (TextView "Bebé")  [SUP] en Figma
│   │       └── tv_bebe_edad (TextView "0-24 m")
│   ├── cv_nina -> ll_nina -> tv_nina, tv_nina_edad
│   └── cv_nino -> ll_nino -> tv_nino, tv_nino_edad
├── tv_novedades (TextView "Novedades")
├── btn_ver_todo (MaterialButton de texto)
├── rv_novedades (RecyclerView horizontal)  [REP]
│   └── cv_producto (MaterialCardView, item_producto.xml)
│       └── cl_producto (ConstraintLayout)
│           ├── iv_producto (ImageView)
│           ├── ib_favorito (ImageButton)  [SUP]
│           ├── tv_nombre_producto (TextView)
│           └── tv_precio_producto (TextView)
├── bnv_inicio (BottomNavigationView)  [REP] x3
│   └── nav_inicio, nav_catalogo, nav_favoritos (menú)
└── zonas transparentes del prototipo  [NP] [SUP]
```

Solo se programan dos superposiciones: el número del carrito sobre su icono y el corazón sobre la foto (los textos de las categorías solo se superponen en Figma). Lo que se repite se hace una vez: las categorías con un estilo común, los productos con un adaptador y la barra con un menú.

## Comparación con el panel de capas

Solo llevan prefijo las capas que van a ser una vista. Los marcos para agrupar, las zonas del prototipo y las capas internas del kit no se programan y se quedan con su nombre.

<img src="img/capas_figma.png" width="230" alt="Panel de capas de Figma con los prefijos de Android">

| En Figma | En Android | Por qué |
|---|---|---|
| Marcos para agrupar (Barra superior, Buscador, Barra de navegación). | No existen. | En Android cada vista se coloca con restricciones. |
| Badge es un marco suelto encima de la barra. | fl_carrito con ib_carrito y tv_badge_carrito. | Hace falta un FrameLayout para poner el número encima del icono. |
| Las categorías tienen los textos encima de la tarjeta. | Los textos van dentro de la tarjeta (ll_bebe, ll_nina, ll_nino). | En Android la tarjeta es un contenedor. |
| Las tarjetas de producto son instancias de item_producto. | rv_novedades con item_producto.xml. | Se hace una vez y se rellena con datos. |
| Capas internas del kit y zonas transparentes del prototipo. | No existen. | Las dibuja el componente o no se programan. |
