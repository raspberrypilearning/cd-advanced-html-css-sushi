## Foto collage

Op deze kaart leer je CSS te gebruiken om HTML-elementen precies te positioneren en een fotocollage te maken.

![](images/photoCollageWithText_wide.png)

+ Voeg een `div` toe aan je pagina en plaats er zoveel afbeeldingen in als je maar wilt. Geef de `div` en `img` elementen `id` waarden.

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

De foto's verschijnen één na één op de webpagina, in de volgorde waarin ze in je code voorkomen.

+ Voeg in je CSS bestand de volgende CSS klasse toe voor de elementen binnen de `div`: 

```css
    .absPos {
        position: absolute;
    }
```

+ Vervolgens moet je de eigenschap `position: relative;` aan de container zelf toevoegen en definieer daar een grootte voor. Dit maakt het zo dat de posities van de andere elementen **relatief tot** (dat wil zeggen, binnenin) de container worden gedefinieerd.

```css
    .relPos {
        position: relative;
    }

    #photoBox {
        width: 800px;
        height: 400px;
    }
```

+ Maak vervolgens een set stijl regels voor elk van de elementen met behulp van **id-selectors** om hun maten (`width` en/of `height` eigenschappen) en hun exacte posities in te stellen.

Om de positie van een element te bepalen, zijn er vier eigenschappen die je kunt gebruiken: `left`, `right`, `top` en `bottom`. Zij geven aan hoe ver elk van de randen van de rand van het parent element af moet liggen. Gebruik `top` of `bottom` voor de verticale positie en `left` of `right` voor de horizontale positie.

![Diagram showing how the top, left, bottom and right properties relate to the parent container](images/cssPositionProperties.png)

+ Kies de exacte posities voor elk van je afbeeldingen en gebruik een van de eigenschappen `left`, `right`, `top` en `bottom` om die posities in je CSS-regels te definiëren. Bijvoorbeeld plaatst deze code de kat foto 100 pixels vanaf de bovenkant en 60 pixels van links:

```css
    #imgTeaCat {
        width: 250px;
        top: 100px;
        left: 60px;
    }
```

Opmerking: de positie waarden kunnen ook negatief zijn! Als je een negatieve waarde gebruikt, wordt het element buiten de container geduwd, over de rand die je hebt opgegeven.

### Dingen laten overlappen

Je wilt misschien sommige afbeeldingen overlappen. Maar hoe kies je welke er bovenop komt?

+ Kies twee afbeeldingen en geef ze posities waardoor ze elkaar overlappen.

+ Add an extra property, `z-index: 10;` to one of them, and then add `z-index: 7;` to the other.

+ Take a look at the result on your webpage.

![](images/horse10Cat7.png)

+ Now swap the `z-index` values, so that the `7` and the `10` are the other way around. Do you see any difference on your web page?

![](images/horse7Cat10.png)

## \--- collapse \---

## title: How does z-index work?

The `z-index` property lets you decide how two or more elements should overlap. The value can be any whole number.

The element with the **highest** number ends up on **top** of the pile, or in other words at the very **front**. The element with the next highest number is behind that, and in front of the others, and so on, until you get to the element with the lowest number, which appears at the back behind all of the other elements.

\--- /collapse \---

You can position any HTML elements in this way, not just images. For example, you could use a `p` element to add some text over a photo.

\--- challenge \---

## Challenge: make a photo collage

+ Try creating your own collage of photos like the one shown below! Use exact positioning together with different `z-index` values to get the overlap effect the way you want it.

\--- hints \---

\--- hint \---

Below is the HTML code for the photo collage on my Ireland website. There are six photos and a piece of text all inside a `div`.

```html
    <div id="photoBox" class="relPos">
        <img id="imgStreet" class="collagePhoto absPos" src="ireland-1474045_640.jpg" alt="Irish town" />
        <img id="imgTeaCat" class="collagePhoto absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
        <img id="imgCoast" class="collagePhoto absPos" src="cattle-2369463_640.jpg" alt="Cows at the coast" />
        <img id="imgTrees" class="collagePhoto absPos" src="ireland-2614852_640.jpg" alt="Tree tunnel" />
        <img id="imgSheep" class="collagePhoto absPos" src="sheep-456989_640.jpg" alt="Sheep on the road" />
        <img id="imgHorse" class="collagePhoto absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <p id="photoText" class="absPos">Ireland</p>
    </div>
```

\--- /hint \---

\--- hint \---

Here are the CSS rules that set the positions for each of my pictures in the collage:

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

Here are the CSS classes I've used:

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

![Photo collage with text over the top](images/photoCollageExample.png)

\--- /challenge \---