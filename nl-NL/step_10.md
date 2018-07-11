## Speciale effecten

Op deze kaart leer je een paar leuke effecten die je met CSS kunt bereiken.

### Schaduwen en beweging

Laten we een kleine beweging toevoegen als je jouw muisaanwijzer over de kaarten, die je eerder hebt gemaakt, laat gaan.

+ Vind de `.card:hover` CSS klasse van eerder en verander het naar het volgende:

```css
    .card:hover {
        box-shadow: 0px 2px 2px rgba(0,0,0,0.2); 
        transform: translateY(-2px);
    }
```

+ Probeer verschillende waarden uit in de `translate` functie!

## \--- collapse \---

## title: de `tyransform` eigenschap

Als je de Intermediate HTML/CSS Sushi kaarten hebt voltooid, weet je wellicht nog dat je de `transform` eigenschap in sommige `@keyframes` animaties hebt gebruikt. Hier zie je dat je de eigenschap ook kunt gebruiken in een standaard CSS-blok.

Een waarde die je kunt gebruiken is `rotate` (draaien), om een ​​element te laten draaien. Andere zijn `translateY`, dat iets naar boven of naar onder verplaatst, en `translateX`, voor beweging van links naar rechts.

\--- /collapse \---

+ Speel met verschillende pixelwaarden in de `box-shadow` eigendom om te zien wat ze doen. 

## \--- collapse \---

## title: Wat is `rgba`?

`rgba(0,0,0,0.2)` is een andere manier om een ​​kleur te definiëren.

Het heeft de gebruikelijke drie nummers (van `0` tot `255`) voor rood, groen en blauw.

Het vierde nummer, de **alpha** waarde, definieert hoe **transparant** (of doorzichtig) iets is. Het is een decimaal getal tussen `0` en `1`, met `1` geheel ondoorzichtig, en `0` volledig doorzichtig. Dit betekent dat hoe lager de alpha waarde van een element, hoe doorzichtiger het is.

\--- /collapse \---

+ Maak tenslotte de beweging vloeiend door de volgende eigenschap aan de `.card` class van eerder toe te voegen: 

```css
    transition: all 0.2s ease-out;
```

Een tijd van `0,2s` betekent de `transition` (overgang) duurt 0,2 seconden.

### Lightbox

Een ander effect dat je waarschijnlijk op veel websites hebt gezien, is **lightbox**: je klikt ergens op en de website dimt terwijl iets anders, zoals een grotere afbeelding of een pop-up venster ervoor verschijnt.

![Lightbox effect in action](images/lightboxLemur.png)

Om dit effect te krijgen, maak je twee links: één voor de daadwerkelijke lightbox (het ding dat verschijnt) en één voor het ding dat je klikt om de lightbox te laten verschijnen. Ik ga de mijne op de pagina Attracties van mijn website doen. Ga naar een pagina waarop je foto's hebt staan!

+ Bepaal welke dingen je wilt weergeven wanneer je klikt en voeg ze allemaal toe aan jouw pagina tussen een set van `a` tags om een ​​link te maken. Zorg ervoor dat je de link een `id` geeft. De code kan overal op de pagina verschijnen: je zult de elementen in de volgende stap onzichtbaar maken!

```html
    <a href="#_" class="lightbox" id="boxLemur">
        <h3>Lemur!!</h3>
        <img src="monkey-2223271_640.jpg" alt="Picture of a lemur" />
        <p>A lemur enjoying a little snack</p>
    </a>
```

Je kunt alles wat je wilt tussen de link tags plaatsen. I've got a big picture, a heading, and some text. Maybe you just want a picture and no text!

+ Add the following CSS code for the lightbox. Can you work out what some of it does?

```css
    .lightbox{
        background: rgba(0,0,0,0.8);
        color: #ffffff;
        text-align: center;
        text-decoration: none;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        position: fixed;
        visibility: hidden;
        z-index: 999;
    }
```

Note: Setting the `position` property to `fixed` means the position you set will be relative to the browser window, so it will stay put when you scroll.

+ Next, decide what thing you want to click to make the lightbox appear, and add add a pair of `a` tags around that element (in my case it's a smaller picture of a lemur). The **target** of the link will be the lightbox, which you set using the `id`. You might recognise this technique from earlier!

```html
    <a href="#boxLemur">
        <img src="monkey-2223271_640.jpg" class="mediumPics">
    </a>
```

+ Finally add the following CSS code. Note that this is a **pseudo-class**; it should go after the code for the `.lightbox` class and not inside it!

```css
    .lightbox:target {
        visibility: visible;
    }
```

The `:target` pseudo-class gets applied whenever the lightbox was the target of the last link clicked. So when you click anywhere, the `visibility` will be set back to `hidden`.

+ Try clicking your new link to see the lightbox appear! To make it go away, just click anywhere on the page.

You can add as many lightboxes as you want to a page. They can all use the same CSS class — just make sure each one has a different `id`! For each one, you need to make something on your webpage into a link that you can click to make the lightbox appear, and then use the `id` as the `href` value in that link, just as you've done above!