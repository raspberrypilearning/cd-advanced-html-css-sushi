## Cree su menú interactivo

Un sitio web **interactivo** es uno que se adapta solo al tamaño de la pantalla para que siempre se vea bien, ya sea en un ordenador, en un teléfono móvil o en una tableta. ¡Vamos a crear su menú interactivo!

Vamos a comenzar con los estilos regulares: este será su comportamiento** predeterminado **.

## \--- collapse \---

## título: ¿Qué significa "predeterminado"?

Los estilos predeterminados son su conjunto normal de reglas de estilo. Se aplican siempre, antes de verificar cualquier condición especial.

Puede añadir un código que compruebe el tamaño de la pantalla y haga algunos ajustes si fuese necesario.

\--- /collapse \---

+ Añada las siguientes reglas CSS a su menú. Probablemente haya también definido los colores y los bordes. ¡Yo los he quitado aquí para ahorrar espacio! Si ya tiene reglas CSS definidas para su menú, simplemente añada o cambie las propiedades y valores de abajo que le falten.

```css
    nav ul {
        relleno: 0.5em;
        display: flex;
        flex-direction: columna;
    }
    nav ul li {
        alineamiento del texto: centro; 
        tipo de estilo de la lista: ninguno;
        margen derecho: 0.5em;
        margen izquierdo: 0.5em;
    }
```

Con el código CSS anterior, su menú se adaptará mejor a pantallas pequeñas. Esto se llama desarrollo** mobile-first **.

![Elementos de menú apilados verticalmente en una pantalla pequeña](images/responsiveMenuMobile.png)

## \--- collapse \---

## título: ¿Qué significa 'mobile-first'?

Con frecuencia, al codificar un sitio web, estará utilizando una pantalla de ordenador y definirá sus estilos basándose en cómo se ve en esa pantalla.

Cuando codifica en primer lugar para dispositivos móviles, elige estilos predeterminados que sean adecuados para dispositivos de pantalla pequeña como los teléfonos inteligentes. Luego añade código adicional para realizar ajustes para pantallas más grandes.

Ya que cada vez más personas navegan por Internet en sus teléfonos inteligentes o tabletas en vez de en un ordenador, es buena práctica desarrollar su sitio web con esto en mente.

\--- /collapse \---

+ Añada el siguiente código a su hoja de estilo:

```css
    @media all y (ancho mínimo: 1000 px) {
        nav ul {
            flex-direction: fila;
            justifique contenido: space-around;
        }
}
```

La primera línea de código de arriba comprueba el tamaño de la ventana del navegador. Si la ventana tiene **1000 pixels** de ancho o más, aplicará todas las reglas de estilo dentro del bloque.

![Elementos del menú espaciados uniformemente a lo largo de una línea en una pantalla más ancha](images/responsiveMenuMedium.png)

## \--- collapse \---

## title: ¿Cómo funciona?

El bloque contiene nuevos valores sólo para algunas propiedades del menú `nav ul`.

Siempre que la ventana tenga más de 1000 píxeles, estos nuevos valores se aplicarán en lugar de los que ya haya definido para `nav ul`.

El resto de las propiedades que definió anteriormente para `nav ul` permanecerán igual.

\--- /collapse \---

+ Si está usando Trinket para escribir código, le será útil descargarse el proyecto para que pueda probarlo en una pantalla de tamaño completo.

\--- challenge \---

## Desafío: haga que su menú se ajuste automáticamente a pantallas grandes

+ ¿Puede añadir otro bloque para pantallas con más de **1600 pixels**, con `flex-end` en lugar de `space-around`?

![Elementos de menú a la derecha en una pantalla amplia](images/responsiveMenuWide.png)

\--- hints \---

\--- hint \---

El siguiente código define las propiedades de flexión para los elementos del menú cuando la pantalla tiene más de 1600 píxeles:

```css
    @media all y (ancho mínimo: 1600px) {
        nav ul {
            flex-direction: fila;
            justifique- contenido: flex-end;
        }
    }  
```

\--- /hint \---

\--- /hints \---

\--- /challenge \---

Puede poner cualquier regla CSS que desee en bloques como estos para definir distintos estilos para diferentes tamaños de pantalla. ¡Será especialmente útil cuando haga disposiciones de cuadrículas CSS más adelante!