## Klikbare kaarten

Hier is een techniek die je kunt gebruiken om een ​​fotogalerij te maken of een portfolio-pagina die je projecten laat zien: kleine **voorbeeldkaarten**.

![Preview card showing an image thumbnail and some text](images/cardsPreview.png)

+ Voeg de volgende HTML-code waar je maar wilt aan je website toe. Ik doe het in `index.html`. Je kunt de afbeelding en tekst aanpassen aan je eigen voorbeeldkaarten. Ik ga een aantal hoogtepunten van de toeristische attracties in Ierland doen.

```html
    <article class="card">
        <img src="monkey-2223271_640.jpg" class="tinyPicture">
        <h3>Fota Wildlife Park</h3>
        <p>Fota Island, County Cork</p>
    </article>
```

![Image and text before styles are applied](images/cardUnstyled.png)

+ Voeg de volgende CSS-code toe om de klassen `card` en `tinyPicture` te maken:

```css
    .tinyPicture {
        height: 60px;
        border-radius: 10px;
    }
    .card {
        width: 200px;
        height: 200px;
        border: 2px solid #F0FFFF;
        border-radius: 10px;
        box-sizing: border-box;
        padding: 10px;
        margin-top: 10px;
        font-family: "Trebuchet MS", sans-serif;
    }
    .card:hover {
        border-color: #1E90FF;
    }
```

![Image and text with styling to create a small card effect](images/cardStyled.png)

Laten we de hele voorbeeldkaart in een link veranderen zodat mensen kunnen klikken om meer informatie te zien.

+ Plaats het hele `article` element binnen een link element. Zorg ervoor dat de `</a>` tag na het `</article>` label komt! Feel free to change the link **URL** to whatever you want to link to. That could be another page on your website, or it could be another website entirely.

```html
    <a href="attractions.html#scFota">  
        <article class="card ">
            <img src="monkey-2223271_640.jpg" class="tinyPicture">
            <h3>Fota Wildlife Park</h3>
            <p>Fota Island, County Cork</p>
        </article>
    </a>
```

![Text and picture that has been turned into a link](images/cardLink.png)

## \--- collapse \---

## title: Linking to a specific part of a page

Notice how the value of `href` in my link ends in `#scFota`? This is a neat trick you can use to jump to a particular part of a page.

+ First, type the URL of the page to link to, followed by `#`.

+ In the code file for the page you are linking to, find the part you want to jump to and give that element an `id`, for example, `<section id="scFota"`. The value of the `id` is what you type after the `#` in your link.

\--- /collapse \---

## \--- collapse \---

## title: Resetting styles

Now that the whole preview card is a link, the text font may have changed.

+ If so, you can fix it by adding a **CSS class** to the link: `class="cardLink"`. Here's the CSS code to put in your style sheet:

```css
    .cardLink {
        color: inherit;
        text-decoration: none;
    }
```

Setting the value of any property to `inherit` makes it use the value that the **parent** element has. So in this case, the text colour will match the rest of the text on the homepage.

\--- /collapse \---

+ Make at least four or five of these cards. If you are working from my example website, you could do one for each of the sections on the Attractions page. On the next Sushi Card, you'll learn how to arrange the cards with a cool trick!