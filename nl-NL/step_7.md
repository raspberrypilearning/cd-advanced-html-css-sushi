## Onderschriften en kanttekeningen

Op deze kaart leer je meer over twee soorten **container** elementen: een element dat je kunt gebruiken om een ​​bijschrift toe te voegen (een tekst als een titel of een korte beschrijving) aan een foto, en een ander voor wanneer je extra dingen hebt die niet echt bij de hoofdinformatie op een pagina horen.

### Afbeeldingen met bijschriften

+ Zoek een `img` element waar je tekst boven of onder hebt die bij de afbeelding hoort. Ik werk met de Tito-afbeelding op `index.html`, maar je kunt kiezen uit wat er op je website staat. 

```html
  <img id="titoPicture" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />          
  <p>
    Tour gids Tito!
  </p>
```

+ Op de regel boven de code, voeg de openings tag `<figure>` toe. Voeg op een nieuwe regel onder de code de sluit tag `<\figuur>` toe.

+ Verwijder vervolgens de `p` tags, of welke tags je ook hebt gebruikt rond de tekst (misschien is het een kop, zoals `h2`) en plaats de tekst tussen de `<figcaption><\figcaption>` tags. Het geheel zou er ongeveer zo uit moeten zien:

```html
  <figure>
      <img id="titoPicture" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />          
      <figcaption>
      Tour gids Tito!
      </figcaption>
  </figure>
```

Het `figcaption` element is je **bijschrift**. Het kan boven of onder het `img` element komen.

![Picture of Tito with a caption](images/figureAndCaption.png)

## \--- collapse \---

## title: Waarom is dit handig?

Het element `figure` fungeert als een soort **container** voor je afbeelding en bijschrift. Hiermee kun je ze als één geheel behandelen bij het definiëren van stijlen.

Door ze logisch samen te voegen, helpt het je ook om een ​​goede structuur in je website-code te behouden.

\--- /collapse \---

Je kunt, zoals elk ander element dat klassen, ID's of element selectors gebruikt, CSS-code gebruiken om `figure` en `figcaption` te stijlen. Ik voeg de volgende regels toe om de extra spatiëring te verwijderen die door de nieuwe container is toegevoegd:

```css
  figure { 
      margin-top: 0px;
      margin-bottom: 0px;
      margin-left: 0px;
      margin-right: 0px;
  }
```

### Kantlijnnotities

De pagina Attracties op mijn website is een lijst met plaatsen om te bezoeken. Ik wil wat aantekeningen toevoegen over het weer en hoe ik de weg kan vinden. Die informatie hoort niet echt thuis in het `article` element met alle attracties. Dit is een voorbeeld van wanneer je het `aside` element zou kunnen gebruiken.

+ Ga naar een pagina van je website met een `article` element erop - Ik gebruik `attractions.html`.

+ **Buiten** van het `article` element, voeg je een of meer paren `<aside> <\aside>` tags met je extra inhoud toe.

```html
  <aside class="sideNoteStyle">
      <h2>Hoe er te komen</h2>
      <h3>Trein en bus</h3>
      <p>je kunt de meeste grote steden vanaf Dublin per trein bereiken. Er zijn veel tourbussen die je naar populaire locaties en toeristische attracties kunnen brengen. </p>
     <h3>Auto</h3> 
     <p> De makkelijkste manier om buiten de steden rond te reizen, is met de auto. </p>
    </aside>
    <aside class="sideNoteStyle">
       <h2>Weer</h2>
       <p>Het weer in Ierland is <span class="specialText">zeer onvoorspelbaar!</span> Het is het beste om <span class="specialText">voorbereid te zijn</span> op elk weertype, zelfs als het een mooie dag is!</p>
</aside>
```

## \--- collapse \---

## title: Why is this useful?

The `aside`, `article`, and other containers are all similar. The only real difference is in the **meaning**, that is, what you use them for.

It's important to use meaningful HTML elements whenever you can. It gives your website better structure and is especially helpful for people using **screen readers**.

\--- /collapse \---

Did you spot the other element in there, `span`? This is a special tag you can use just for adding extra CSS code! You can put anything in between a pair of `span` tags. It's useful for things like styling a **part** of the text in a paragraph.

+ Add the following CSS code to your style sheet to complete the styling for the HTML code above.

```css
  .sideNoteStyle {
    border: dotted 1px purple;
    background-color: #c1ebec;
    padding: 0.5em;
    margin: 0.5em;
  }
  .specialText {
      color: #FF4500;
      font-size: larger;
  }
```

![Additional notes with their own styling](images/asidesStyled.png)

On the next card, you're going to learn how to make your website's layout more interesting!

+ To get ready, make a page that has one `article` and two `aside` elements inside the `<main> </main>` tags. Or if you prefer, you can work with the Attractions page on my website.