## Todos en un renglón

En esta tarjeta aprenderá algunos trucos para organizar cosas **horizontalmente** en una página. Primero, verá cómo centrar las cosas. Después, colocará los elementos uno al lado del otro en una fila.

+ Añada las siguientes propiedades CSS a la clase `.card`:

```css
    margen izquierdo: auto;
    margen derecho: auto;
```

Debería ver que las cartas se mueven al centro de la página. Al establecer los márgenes izquierdos y derecho a `auto`, puede hacer que cualquier elemento esté en el medio en lugar de a la izquierda.

![Las tarjetas aparecen en el medio en lugar de a la izquierda](images/marginAuto.png)

+ Arrastre el borde de la ventana del navegador para hacer que la página sea más estrecha y ancha: observe que las tarjetas permanecen centradas.

+ Ponga todos los enlaces de la tarjeta que acaba de hacer en un nuevo elemento de contenedor. No va a ser un `artículo` o una `sección`, sino uno llamado `div`. Este es un contenedor de uso general que puede usar para agrupar cosas y hacer diseños bonitos.

```html
    <div class="cardContainer">
```

+ Añade el siguiente código CSS a tu archivo de hoja de estilo:

```css
    .cardContainer {
        mostrar: flex;
        flex-wrap: wrap;
        justifique-conido: space-around;
        relleno: 10px;
    }
```

Voilà! ¡Gracias a **Flex**, sus tarjetas se muestran ahora una junto a la otra!

+ Arrastre el borde de su ventana para hacer que el sitio web sea más ancho y más estrecho, y observe cómo se mueven las tarjetas para que se ajusten al tamaño de la ventana, a veces ajustándose a la siguiente línea.

![Las tarjetas están organizadas en dos filas espaciadas uniformemente para ajustarse al ancho del navegador](images/flexSideBySide.png)

+ Intente eliminar las propiedades `anchura` y `altura` de la clase `.card` y vea lo que sucede: `flex` encaja las tarjetas juntas como un rompecabezas, manteniendo la misma altura a lo largo de todo lo que está en la misma fila.

![Las tarjetas están colocadas una al lado de la otra con el ancho automatizado](images/flexAutoWidths.png)

Si tiene un menú de navegación en la parte superior de su página, ese es otro lugar donde puede utilizar este truco. Su menú debe estar compuesto por elementos de lista(`li`) para este próximo fragmento. Si lo prefiere, puede probarlo con mi sitio web.

+ Encuentre las reglas CSS para el menú. En mi sitio web, son los bloques ` nav ul `, ` nav ul li `, y ` nav ul li a `.

+ Elimine la propiedad `mostrar: inline;` de los elementos de la lista. Luego, en la lista `nav ul`, añada:

```css
    mostrar: flex;
    justifique-contenido: flex-start;
```

![Menú con elementos alineados a la izquierda](images/flexMenuStart.png)

Básicamente, acaba con el mismo menú, ¿verdad? Lo interesante de `flex` es que puedes controlar el diseño con la propiedad `justifique-contenido`.

+ Cambie el valor de `justifique-contenido` a `flex-end` y vea lo que sucede. O cambielo a `space-around` para hacer que los elementos del menú se espacien uniformemente, como lo hiciste para las tarjetas.

![Menú con elementos espaciados uniformemente](images/flexMenuSpace.png)

![Menú con elementos alineados a la derecha](images/flexMenuEnd.png)

**`flex`** es una herramienta de diseño muy potente con la que podríamos rellenar toda una serie de tarjetas Sushi — puede aprender más sobre ella en [dojo.soy/html3-flex](http://dojo.soy/html3-flex).