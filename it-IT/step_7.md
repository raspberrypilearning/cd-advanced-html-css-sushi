## Didascalie e note a margine

Su questa scheda imparerai altri due tipi di elementi **container** : uno che puoi usare per aggiungere una didascalia (un testo come un titolo o una breve descrizione) ad un'immagine, e un'altra per quando hai roba extra che non in realtà appartengono alle informazioni principali su una pagina.

### Immagini con didascalie

+ Trova un elemento `img` cui hai testo sopra o sotto che va con l'immagine. Sto lavorando con l'immagine di Tito su `index.html`, ma puoi andare con qualunque cosa si trovi sul tuo sito web. 

```html
  <img id="titoPicture" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />          
  <p>
    Guida turistica Tito!
  </p>
```

+ Sulla riga sopra il codice, aggiungi il tag di apertura `<figure>`. Su una nuova riga sotto il codice, posiziona il tag di chiusura `<\ figura>`.

+ Successivamente, rimuovi i tag `p` o qualsiasi tag che hai intorno al testo (forse è un'intestazione, come `h2`?), E metti il ​​testo tra i `<figcaption> <\ figcaption>` tag. Il tutto dovrebbe assomigliare a questo:

```html
  <figure>
      <img id="titoPicture" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />          
      <figcaption>
      Guida turistica Tito!
      </figcaption>
  </figure>
```

L'elemento `figcaption` è il tuo **caption**. Può andare sopra l'elemento `img` o sotto di esso.

![Immagine di Tito con didascalia](images/figureAndCaption.png)

## \--- chiudi \---

## titolo: Perché è utile?

L'elemento `figura` agisce come una sorta di **contenitore** per la tua immagine e la sua didascalia. Questo ti permette di trattarli come una sola unità quando definisci gli stili.

Raggrupparli insieme logicamente aiuta anche a mantenere una buona struttura nel codice del tuo sito web.

\--- / chiudi \---

Puoi usare il codice CSS per disegnare `figure` e `figcaption` come faresti con qualsiasi altro elemento usando classi, ID o selettori di elementi. Sto aggiungendo le seguenti regole per rimuovere la spaziatura aggiuntiva che è stata aggiunta dal nuovo contenitore:

```css
  figura {margin-top: 0px; margin-bottom: 0px; margin-left: 0px; margin-right: 0px; }
```

### Note a margine

La pagina delle attrazioni sul mio sito Web è un elenco di luoghi da visitare. Voglio aggiungere alcune note sul tempo e su come spostarsi. Quell'informazione non appartiene veramente all'elemento `articolo` con tutte le attrazioni. Questo è un esempio di quando puoi usare l'elemento `parte`.

+ Vai a una pagina del tuo sito web che contiene un elemento articolo `` - Sto utilizzando `attrazioni.html`.

+ **Al di fuori** dell'articolo `dell'articolo` , aggiungi una o più paia di `<aside> <\ aside>` tag contenenti le tue cose extra.

```html
  <aside class="sideNoteStyle">
      <h2>Come muoversi</h2>
      <h3>Treno e autobus</h3>
      <p>È possibile raggiungere la maggior parte delle città principali in treno da Dublino. Ci sono molti autobus che effettuano visite a luoghi popolari e attrazioni turistiche.</p>
      <h3>Car</h3>
      <p>Il modo più semplice per spostarsi fuori città è in auto.</p>
    </aside>
    <aside class="sideNoteStyle">
      <h2>Meteo</h2>
      <p>Il tempo in Irlanda è <span class="specialText">molto imprevedibile!</span> E 'meglio <span class="specialText">essere pronti</span> per qualsiasi tipo di tempo, anche se è una bella giornata!</p>
  </aside>
```

## \--- chiudi \---

## titolo: Perché è utile?

Il `parte`, `articolo`, e altri contenitori sono tutti simili. L'unica vera differenza è nello **significa**, cioè, per cosa li usi.

È importante utilizzare elementi HTML significativi ogni volta che puoi. Dà al tuo sito una migliore struttura ed è particolarmente utile per chi usa **screen reader**.

\--- / chiudi \---

Hai notato l'altro elemento, `span`? Questo è un tag speciale che puoi usare solo per aggiungere un ulteriore codice CSS! Puoi inserire qualsiasi cosa tra una coppia di tag `span`. È utile per cose come lo styling di una **parte** del testo in un paragrafo.

+ Aggiungi il seguente codice CSS al tuo foglio di stile per completare lo stile per il codice HTML sopra.

```css
  .sideNoteStyle {border: punteggiato 1px purple; colore di sfondo: # c1ebec; imbottitura: 0,5em; margine: 0,5em; } .specialText {color: # FF4500; dimensione del carattere: più grande; }
```

![Note aggiuntive con il proprio stile](images/asidesStyled.png)

Sulla prossima carta, imparerai come rendere più interessante il layout del tuo sito web!

+ Per essere pronti, crea una pagina che contenga uno `articolo` e due `lato` elementi all'interno dei tag `<main> </main>`. O se preferisci, puoi lavorare con la pagina Attrazioni sul mio sito web.