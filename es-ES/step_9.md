## collage de fotos

En esta tarjeta, aprenderá a usar CSS para ubicar exactamente los elementos HTML y hacer un collage de fotos.

![](images/photoCollageWithText_wide.png)

+ Agregue un `div` a su página y coloque tantas imágenes como desee. Proporcione `div` y `img` elementos `id` valores.

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

Las fotos aparecerán una detrás de otra en la página web, en el orden en que aparecen en tu código.

+ En su archivo CSS, agregue la siguiente clase de CSS para los elementos dentro de `div`: 

```css
    .absPos {position: absolute; }
```

+ A continuación, debe agregar la propiedad `posición: relativa;` al contenedor mismo y defina un tamaño para él. Esto hace que las posiciones de los demás elementos se definan **relación con** (es decir, dentro) del contenedor.

```css
    .relPos {position: relative; } #photoBox {ancho: 800px; altura: 400px; }
```

+ Luego, cree un conjunto de reglas de estilo para cada uno de los elementos utilizando **selectores de id.** para establecer sus tamaños (`propiedades de ancho` y / o `altura` ), así como sus posiciones exactas.

Para definir la posición de un elemento, hay cuatro propiedades que puede usar: `izquierda`, `derecha`, `arriba`y `abajo`. Representan qué tan lejos deben estar cada uno de los bordes desde el borde del padre. Utilice `arriba` o `abajo` para la posición vertical, y `izquierda` o `derecha` para la posición horizontal.

![Diagrama que muestra cómo las propiedades superior, izquierda, inferior y derecha se relacionan con el contenedor principal](images/cssPositionProperties.png)

+ Elija las posiciones exactas para cada una de sus imágenes y use cualquiera de las propiedades `izquierda`, `derecha`, `arriba`y `abajo` para definir esas posiciones en sus reglas de CSS. Por ejemplo, este código coloca la imagen del gato a 100 píxeles de la parte superior y 60 píxeles de la izquierda:

```css
    #imgTeaCat {ancho: 250px; arriba: 100 px; izquierda: 60px; }
```

Nota: ¡Los valores de posición también pueden ser negativos! Si usa un valor negativo, empujará el elemento fuera del contenedor, sobre cualquier borde que haya especificado.

### Hacer que las cosas se superpongan

Es posible que desee que algunas de las imágenes se superpongan. ¿Pero cómo eliges cuál va arriba?

+ Elige dos imágenes y dales posiciones que hagan que se superpongan.

+ Agregue una propiedad adicional, `z-index: 10;` a uno de ellos, y luego agregue `z-index: 7;` a la otra.

+ Eche un vistazo al resultado en su página web.

![](images/horse10Cat7.png)

+ Ahora intercambie los valores de `z-index` , de modo que el `7` y el `10` sean al revés. ¿Ves alguna diferencia en tu página web?

![](images/horse7Cat10.png)

## \--- colapso \---

## title: ¿Cómo funciona el índice z?

La propiedad `z-index` permite decidir cómo se superponen dos o más elementos. El valor puede ser cualquier número entero.

El elemento con el número **más alto** termina en **top** del montón, o en otras palabras, en el mismo **front**. El elemento con el siguiente número más alto está detrás de eso, y delante de los demás, y así sucesivamente, hasta llegar al elemento con el número más bajo, que aparece detrás de todos los otros elementos.

\--- /colapso \---

Puede colocar cualquier elemento HTML de esta manera, no solo imágenes. Por ejemplo, podría usar un elemento `p` para agregar texto sobre una foto.

\--- desafío \---

## Desafío: hacer un collage de fotos

+ ¡Intenta crear tu propio collage de fotos como el que se muestra a continuación! Use el posicionamiento exacto junto con diferentes valores de `z-index` para obtener el efecto de superposición de la manera que desee.

\--- consejos \---

\--- insinuación \---

A continuación se muestra el código HTML para el collage de fotos en mi sitio web de Irlanda. Hay seis fotos y un texto dentro de un `div`.

```html
    <div id="photoBox" class="relPos">
        <img id="imgStreet" class="collagePhoto absPos" src="ireland-1474045_640.jpg" alt="Irish town" />
        <img id="imgTeaCat" class="collagePhoto absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
        <img id="imgCoast" class="collagePhoto absPos" src="cattle-2369463_640.jpg" alt="Cows at the coast" />
        <img id="imgTrees" class="collagePhoto absPos" src="ireland-2614852_640.jpg" alt="Tree tunnel" />
        <img id="imgSheep" class="collagePhoto absPos" src="sheep-456989_640.jpg" alt="Sheep on the road" />
        <img id="imgHorse" class="collagePhoto absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <p id="photoText" class="absPos">Irlanda</p>
    </div>
```

\--- /insinuación \---

\--- insinuación \---

Aquí están las reglas de CSS que establecen las posiciones para cada una de mis imágenes en el collage:

```css
    #imgHorse {width: 120px; arriba: 200px; izquierda: 390px; índice z: 10; } #imgSheep {ancho: 200px; arriba: 100 px; izquierda: 20px; índice z: 8; } #imgCoast {ancho: 150px; arriba: 250px; izquierda: 10px; índice z: 5; } #imgTrees {ancho: 110px; arriba: 65px; izquierda: 205px; índice z: 9; } #imgTeaCat {ancho: 250px; arriba: 210px; izquierda: 160px; índice z: 7; } #imgStreet {ancho: 180px; arriba: 90px; izquierda: 310px; índice z: 6; } #photoText {font-family: "script script MT"; color: verde claro; tamaño de letra: 4em; izquierda: 35px; arriba: 15px; índice z: 20; }
```

\--- /insinuación \---

\--- insinuación \---

Estas son las clases de CSS que he usado:

```css
    .collagePhoto {border: 1px blanco sólido; } .relPos {position: relative; } .absPos {position: absolute; }
```

\--- /insinuación \---

\--- / consejos \---

![Collage de fotos con texto en la parte superior](images/photoCollageExample.png)

\--- / desafío \---