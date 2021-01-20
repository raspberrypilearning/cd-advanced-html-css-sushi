## Collage de fotos

En esta tarjeta aprenderás a usar CSS para colocar exactamente los elementos HTML y hacer un collage de fotos.

![](images/photoCollageWithText_wide.png)

+ Add a `div` to your page and put as many images in it as you like. Give the `div` and the `img` elements `id` values.

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

Las fotos aparecerán una tras otra en la página web, en el orden en que aparecen en tu código.

+ En tu archivo CSS, añade la siguiente clase CSS para los elementos dentro del `div`: 

```css
    .absPos {
        position: absolute;
    }
```

+ Next, you need to add the property `position: relative;` to the container itself and define a size for it. This makes it so that the positions of the other elements are defined **relative to** (that is, within) the container.

```css
    .relPos {
        position: relative;
    }

    #photoBox {
        width: 800px;
        height: 400px;
    }
```

+ Then create a set of style rules for each of the elements using **id selectors** to set their sizes (`width` and/or `height` properties) as well as their exact positions.

To define the position of an element, there are four properties you can use: `left`, `right`, `top`, and `bottom`. They represent how far each of the edges should be from the parent's edge. Use either `top` or `bottom` for the vertical position, and either `left` or `right` for the horizontal position.

![Diagrama que muestra cómo se relacionan las propiedades superior, izquierda, inferior y derecha con el contenedor padre](images/cssPositionProperties.png)

+ Choose exact positions for each of your pictures, and use any of the properties `left`, `right`, `top`, and `bottom` to define those positions in your CSS rules. Por ejemplo, este código coloca la imagen del gato 100 píxeles de la parte superior y 60 píxeles de la izquierda:

```css
    #imgTeaCat {
        width: 250px;
        top: 100px;
        left: 60px;
    }
```

Note: The position values can also be negative! If you use a negative value, it will push the element off outside the container, over whichever edge you've specified.

### Making things overlap

You might want to have some of the pictures overlapping. But how do you choose which one goes on top?

+ Choose two images and give them positions that cause them to overlap.

+ Agrega una propiedad adicional, `z-index: 10;` a uno de ellos, y luego añade `z-index: 7;` al otro.

+ Take a look at the result on your webpage.

![](images/horse10Cat7.png)

+ Now swap the `z-index` values, so that the `7` and the `10` are the other way around. ¿Ves alguna diferencia en tu página web?

![](images/horse7Cat10.png)

## \--- collapse \---

## title: How does z-index work?

The `z-index` property lets you decide how two or more elements should overlap. El valor puede ser cualquier número entero.

El elemento con el número **más alto** termina en **superior** de la pila, o en otras palabras, en el mismo **delante**. The element with the next highest number is behind that, and in front of the others, and so on, until you get to the element with the lowest number, which appears at the back behind all of the other elements.

\--- /collapse \---

Puedes colocar cualquier elemento HTML de esta manera, no sólo imágenes. For example, you could use a `p` element to add some text over a photo.

\--- challenge \---

## Challenge: make a photo collage

+ ¡Intenta crear tu propio collage de fotos como el que se muestra a continuación! Usa la posición exacta junto con diferentes valores `z-index` para obtener el efecto de superposición de la manera que quieras.

\--- hints \---

\--- hint \---

A continuación se muestra el código HTML para el collage de fotos en mi sitio web de Irlanda. There are six photos and a piece of text all inside a `div`.

```html
    0>
        <img id="imgStreet" class="collagePhoto absPos" src="ireland-1474045_640.jpg" alt="Irish town" />
        <img id="imgTeaCat" class="collagePhoto absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
        <img id="imgCoast" class="collagePhoto absPos" src="cattle-2369463_640.jpg" alt="Cows at the coast" />
        <img id="imgTrees" class="collagePhoto absPos" src="ireland-2614852_640.jpg" alt="Tree tunnel" />
        <img id="imgSheep" class="collagePhoto absPos" src="sheep-456989_640.jpg" alt="Sheep on the road" />
        <img id="imgHorse" class="collagePhoto absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <p id="photoText" class="absPos">Irlanda</p>
    </0
```

\--- /hint \---

\--- hint \---

Aquí están las reglas CSS que establecen las posiciones para cada una de mis fotos en el collage:

```css
    #imgHorse {
        width: 120px;
        top: 200px;
        left: 390px;
        z-index: 10;
    }
    #imgSheep {
        width: 200px;
        top: 100px;
        left: 20px;
        z-index: 8;
    }
    #imgCoast {
        width: 150px;
        top: 250px;
        left: 10px;
        z-index: 5;
    }
    #imgTrees {
        width: 110px;
        top: 65px;
        left: 205px;
        z-index: 9;
    }
    #imgTeaCat {
        width: 250px;
        top: 210px;
        left: 160px;
        z-index: 7;
    }
    #imgStreet {
        width: 180px;
        top: 90px;
        left: 310px;
        z-index: 6;
    }
    #photoText {
        font-family: "brush script MT";
        color: lightgreen;
        font-size: 4em;
        left: 35px;
        top: 15px;
        z-index: 20;
    }
```

\--- /hint \---

\--- hint \---

Aquí están las clases CSS que he utilizado:

```css
    .collagePhoto {
        border: 1px solid white;
    }
    .relPos {
        position: relative;
    }
    .absPos {
        position: absolute;
    }
```

\--- /hint \---

\--- /hints \---

![Collage de fotos con texto en la parte superior](images/photoCollageExample.png)

\--- /challenge \---