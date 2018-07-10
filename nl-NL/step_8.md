## Ontwerp coole pagina-layouts

+ Voor deze kaart zou je moeten werken met een pagina die een `main` element bevat met daarbinnen drie elementen: één `article` en twee `aside` elementen. Ga je gang en maak deze eerst als dat nodig is. Als je met mijn website wilt werken, voeg je de `aside` code van de vorige Sushi Card toe aan de Attracties pagina. 

Hier zijn drie verschillende pagina layouts die je gaat toepassen:

![](images/cssGridLayouts.png)

+ Voeg nieuwe CSS klassen toe aan `main` en elk van de drie elementen daarbinnen.

```html
    <main class="attPageLayoutGrid">
        <article class="attGridArticle">
            <!--andere dingen hier-->
        </article>
        <aside class="attGridAside1">
            <!--andere dingen hier-->
        </aside>
        <aside class="attGridAside2">
            <!--andere dingen hier-->
        </aside>
    </main>
```

The container you'll change the layout of is `main`, but you could do this with any kind of container, like a `div` or `article`, or even the whole page `body`. The technique you're going to use is called **CSS grid**.

In this example, the `header` and `footer` will be left out of the design, but it's quite common to include them in the grid too.

+ Set the `display` property to `grid` on the overall container:

```css
    .attPageLayoutGrid {
        display: grid;
        grid-column-gap: 0.5em;
        grid-row-gap: 1em;
    }
```

What do you think the `grid-column-gap` and `grid-row-gap` properties do?

+ Next, you name a `grid-area` for each element: 

```css
    .attGridArticle {
        grid-area: agArticle;
    }
    .attGridAside1 {
        grid-area: agAside1;
    }
    .attGridAside2 {
        grid-area: agAside2;
    }
```

Then you design your layout! Let's put the two `aside` elements side by side at the bottom of the page. For this you need two **columns** of equal width. You can keep the **row** height automatic.

+ Put the following code inside the `.attPageLayoutGrid` CSS rules:

```css
    grid-template-rows: auto;
    grid-template-columns: 1fr 1fr;
    grid-template-areas: 
        "agArticle agArticle"
        "agAside1 agAside2";
```

`fr` stands for **fraction**. Notice how you make the `article` take up all the space over the two columns.

## \--- collapse \---

## title: Help! I got errors and warnings!

If you are using Trinket, you may notice some errors and warnings appear, even if you typed the code exactly as above. This is because Trinket does not yet recognise the CSS grid properties. However, the code will still work.

If the CSS grid code gives you 'unknown property' warnings or an error like 'unexpected token 1fr', you can simply ignore these.

\--- /collapse \---

![Asides are side by side at the bottom](images/cssGridAsidesAtBottom.png)

Let's put the `aside` elements over on the right and make them half the width of the `article`.

+ Change the values of `grid-template-columns` and `grid-template-areas` to:

```css
    grid-template-columns: 2fr 1fr;
    grid-template-areas: 
        "agArticle agAside1"
        "agArticle agAside2";
```

![Asides are down the right hand side](images/cssGridAsidesOnRight.png)

+ If you don't want the `aside` elements to stretch all the way to the bottom, you can add a blank space using a dot: 

```css
    grid-template-areas: 
        "agArticle agAside1"
        "agArticle agAside2"
        "agArticle . ";
```

![Asides on the right and not stretched down](images/cssGridAsidesTopRight.png)

\--- challenge \---

## Challenge: make different layouts for different screen sizes

+ Can you use the screen size checks you added earlier to make the layout change depending on how wide the screen is? Note: if you already created CSS blocks for each screen size, you can add the new CSS code to those blocks instead of creating new ones.

\--- hints \---

\--- hint \---

The following code defines a layout for the CSS class above when the screen is bigger than 1000 pixels:

```css
    @media all and (min-width: 1000px) {
        .attPageLayoutGrid {
            grid-template-columns: 1fr 1fr;
            grid-template-areas: 
                "agArticle agArticle"
                "agAside1 agAside2";
        }
    }  
```

\--- /hint \---

\--- hint \---

The following code defines a layout for the CSS class above when the screen is bigger than 1600 pixels:

```css
    @media all and (min-width: 1600px) {
        .attPageLayoutGrid {
            grid-template-columns: 1fr 1fr;
            grid-template-areas: 
                "agArticle agAside1"
                "agArticle agAside2"
                "agArticle .";
        }
    }  
```

\--- /hint \---

\--- /hints \---

\--- /challenge \---

With **CSS grid**, you can make almost any layout you like. If you want to learn more, go to [dojo.soy/html3-css-grid](http://dojo.soy/html3-css-grid){:target="_blank"}