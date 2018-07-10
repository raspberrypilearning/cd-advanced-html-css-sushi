## Pas je menu automatisch aan

Een **responsive** website is er een die zich aanpast aan de schermgrootte zodat het er altijd fantastisch uitziet, of je het nu bekijkt op een computer, mobiele telefoon of tablet. Laten je menu zich automatisch aanpassen!

Je begint met de reguliere stijlen: dit is je **default** (standaard) gedrag.

## \--- collapse \---

## title: Wat betekent 'default'?

De default (standaard) stijlen zijn je normale set stijlregels. Ze worden, voordat er speciale voorwaarden worden gecontroleerd, altijd toegepast,.

Je kunt code toevoegen die vervolgens de grootte van het scherm controleert en indien nodig enkele aanpassingen aanbrengt.

\--- /collapse \---

+ Voeg de volgende CSS-regels toe aan je menu. Je hebt waarschijnlijk ook kleuren en randen gedefinieerd; Ik heb ze weggelaten om hier ruimte te sparen! Als je al CSS-regels hebt gedefinieerd voor jouw menu, hoef je alleen maar de eigenschappen en waarden die je mist hieronder toe te voegen of te wijzigen.

```css
    nav ul {
        padding: 0.5em;
        display: flex;
        flex-direction: column;
    }
    nav ul li {
        text-align: center; 
        list-style-type: none;
        margin-right: 0.5em;
        margin-left: 0.5em;
    }
```

Met de bovenstaande CSS-code is je menu het meest geschikt voor kleine schermen. Dit wordt **mobile-first** (mobiel-eerst) genoemd.

![Menu items stacked vertically on a small screen](images/responsiveMenuMobile.png)

## \--- collapse \---

## title: Wat betekent 'mobile-first'?

Heel vaak gebruikt je bij het coderen van een website een computerscherm en je zult waarschijnlijk jouw stijlen definiëren op basis van hoe het eruit ziet op dat scherm.

When you code for mobile first, you instead choose default styles that are suitable for small screens such as smartphones. You then add extra code to make adjustments for bigger screens.

Since more and more people browse the internet on their smartphones or tablets rather than on a computer, it's good practise to develop your website with this in mind.

\--- /collapse \---

+ Now add the following code to your style sheet:

```css
    @media all and (min-width: 1000px) {
        nav ul {
            flex-direction: row;
            justify-content: space-around;
        }
    }
```

The first line of code above checks what size the browser window is. If the window is **1000 pixels** wide or more, it will apply all the style rules inside the block.

![Menu items spaced evenly across one line on a wider screen](images/responsiveMenuMedium.png)

## \--- collapse \---

## title: How does it work?

The block contains new values for only some properties of the `nav ul` menu.

Whenever the window is wider than 1000 pixels, these new values will be applied instead of the ones you already defined for `nav ul`.

The rest of the properties you defined previously for `nav ul` will stay the same.

\--- /collapse \---

+ If you are using Trinket to write code, it might be helpful to download the project so you can test it out on a full-size screen.

\--- challenge \---

## Challenge: make your menu adjust itself for big screens

+ Can you add another block for screens bigger than **1600 pixels**, with `flex-end` instead of `space-around`?

![Menu items to the right on a wide screen](images/responsiveMenuWide.png)

\--- hints \---

\--- hint \---

The following code defines flex properties for menu items when the screen is bigger than 1600 pixels:

```css
    @media all and (min-width: 1600px) {
        nav ul {
            flex-direction: row;
            justify-content: flex-end;
        }
    }  
```

\--- /hint \---

\--- /hints \---

\--- /challenge \---

You can put any CSS rules you like into blocks like these to define different styles for different screen sizes. It’ll be especially useful when you do CSS grid layouts later!