## Progettare layout di pagina interessanti

+ Per questa scheda si dovrebbe lavorare con una pagina che contiene un `principale` elemento con tre elementi all'interno: una `articolo` e due `parte`s. Vai avanti e crea questi prima se è necessario. Se vuoi lavorare con il mio sito web, aggiungi il codice `parte` della precedente Sushi Card alla pagina delle attrazioni. 

Ecco tre diversi layout di pagina che applicherai:

![](images/cssGridLayouts.png)

+ Aggiungi nuove classi CSS a `principale` e ognuno dei tre elementi al suo interno.

```html
    <main class="attPageLayoutGrid">
        <article class="attGridArticle">
            <! - altre cose qui-->
        </article>
        <aside class="attGridAside1">
            <! - altre cose qui-->
        </aside>
        <aside class="attGridAside2">
            <! - altre cose qui-->
        </aside>
    </main>
```

Il contenitore che cambierà il layout di è `principale`, ma puoi farlo con qualsiasi tipo di contenitore, come un `div` o `articolo`, o anche l'intera pagina `corpo`. La tecnica che utilizzerai si chiama **griglia CSS**.

In questo esempio, l'intestazione `` e `piè di pagina` saranno esclusi dal progetto, ma è abbastanza comune includerli anche nella griglia.

+ Imposta la proprietà `display` su `grid` sul contenitore generale:

```css
    .attPageLayoutGrid {display: grid; grid-column-gap: 0.5em; grid-row-gap: 1em; }
```

Cosa ne pensi delle proprietà `griglia-colonna-gap` e `griglia-fila-spazio`?

+ Successivamente, nominerai una `area della griglia` per ciascun elemento: 

```css
    .attGridArticle {grid-area: agArticle; } .attGridAside1 {grid-area: agAside1; } .attGridAside2 {grid-area: agAside2; }
```

Quindi progetta il tuo layout! Mettiamo i due `elementi di fianco` affiancati nella parte inferiore della pagina. Per questo hai bisogno di due **colonne** di uguale larghezza. Puoi mantenere l'altezza della riga</strong> **automatica.</p> 

+ Inserisci il codice seguente all'interno delle regole CSS `.attPageLayoutGrid`:

```css
    grid-template-rows: auto; grid-template-columns: 1fr 1fr; grid-template-areas: "agArticle agArticle" "agAside1 agAside2";
```

`fr` sta per **frazione**. Notate come si effettua il `articolo` prende tutto lo spazio sopra le due colonne.

## \--- chiudi \---

## titolo: Aiuto! Ho degli errori e degli avvertimenti!

Se stai usando Trinket, potresti notare alcuni errori e avvertimenti, anche se hai digitato il codice esattamente come sopra. Questo perché Trinket non riconosce ancora le proprietà della griglia CSS. Tuttavia, il codice funzionerà ancora.

Se il codice di griglia CSS fornisce avvisi di 'proprietà sconosciuta' o un errore come 'token imprevisto 1fr', puoi semplicemente ignorarli.

\--- / chiudi \---

![Accanto al fondo sono affiancati](images/cssGridAsidesAtBottom.png)

Mettiamo gli `elementi di cui sopra` sulla destra e rendiamoli la metà della larghezza del `articolo`.

+ Modifica i valori di `grid-template-columns` e `grid-template-areas` in:

```css
    grid-template-columns: 2fr 1fr; grid-template-areas: "agArticle agAside1" "agArticle agAside2";
```

![A parte sono in basso a destra](images/cssGridAsidesOnRight.png)

+ Se non vuoi che gli elementi `parte` si estendano fino in fondo, puoi aggiungere uno spazio vuoto usando un punto: 

```css
    grid-template-areas: "agArticle agAside1" "agArticle agAside2" "agArticle. ";
```

![Oltre a destra e non disteso](images/cssGridAsidesTopRight.png)

\--- sfida \---

## Sfida: crea layout diversi per dimensioni dello schermo diverse

+ È possibile utilizzare i controlli delle dimensioni dello schermo aggiunti in precedenza per modificare il layout in base alla larghezza dello schermo? Nota: se hai già creato blocchi CSS per ogni dimensione dello schermo, puoi aggiungere il nuovo codice CSS a quei blocchi invece di crearne di nuovi.

\--- suggerimenti \---

\--- suggerimento \---

Il seguente codice definisce un layout per la classe CSS sopra quando lo schermo è più grande di 1000 pixel:

```css
    @media all e (min-width: 1000px) {.attPageLayoutGrid {grid-template-columns: 1fr 1fr; grid-template-areas: "agArticle agArticle" "agAside1 agAside2"; }}  
```

\--- / suggerimento \---

\--- suggerimento \---

Il seguente codice definisce un layout per la classe CSS sopra quando lo schermo è più grande di 1600 pixel:

```css
    @media all e (min-width: 1600px) {.attPageLayoutGrid {grid-template-columns: 1fr 1fr; grid-template-areas: "agArticle agAside1" "agArticle agAside2" "agArticle."; }}  
```

\--- / suggerimento \---

\--- / suggerimenti \---

\--- / challenge \---

Con **griglia**CSS, puoi realizzare quasi tutti i layout che ti piacciono. Se vuoi saperne di più, vai a [dojo.soy/html3-css-grid](http://dojo.soy/html3-css-grid){: target = "_ blank"}