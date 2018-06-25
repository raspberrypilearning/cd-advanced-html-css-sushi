## Carte cliccabili

Ecco una tecnica che puoi utilizzare per creare una galleria fotografica o una pagina del portfolio che mostri i tuoi progetti: poche **schede di anteprima**.

![Scheda di anteprima che mostra una miniatura dell'immagine e del testo](images/cardsPreview.png)

+ Aggiungi il seguente codice HTML al tuo sito web, ovunque desideri. Sto facendo il mio su `index.html`. È possibile modificare l'immagine e il testo per adattarli alle proprie schede di anteprima. Sto andando a fare un sacco di punti salienti delle attrazioni turistiche in Irlanda.

```html
    <article class="card">
        <img src="monkey-2223271_640.jpg" class="tinyPicture">
        <h3>Fota Wildlife Park</h3>
        <p>Fota Island, County Cork</p>
    </article>
```

![Immagine e testo prima dell'applicazione degli stili](images/cardUnstyled.png)

+ Aggiungi il seguente codice CSS per creare le classi `card` e `tinyPicture`:

```css
    .tinyPicture {height: 60px; border-radius: 10px; } .card {width: 200px; altezza: 200 px; border: 2px solid # F0FFFF; border-radius: 10px; dimensionamento della scatola: border-box; imbottitura: 10px; margin-top: 10px; famiglia di font: "Trebuchet MS", sans-serif; } .card: hover {border-color: # 1E90FF; }
```

![Immagine e testo con stile per creare un effetto carta di piccole dimensioni](images/cardStyled.png)

Trasformiamo l'intera scheda di anteprima in un link in modo che le persone possano fare clic per visualizzare ulteriori informazioni.

+ Posiziona l'intero articolo `articolo` all'interno di un elemento di collegamento. Assicurati che il tag di chiusura `</a>` sia dopo il tag di chiusura `</article>`! Sentiti libero di cambiare il link **URL** a qualunque cosa tu voglia collegare. Potrebbe essere un'altra pagina sul tuo sito web o potrebbe essere un altro sito interamente.

```html
    <a href="attractions.html#scFota">  
        <article class="card ">
            <img src="monkey-2223271_640.jpg" class="tinyPicture">
            <h3>Fota Wildlife Park</h3>
            <p>Fota Island, County Cork</p>
        </article>
    </a>
```

![Testo e immagine che sono stati trasformati in un link](images/cardLink.png)

## \--- chiudi \---

## titolo: collegamento a una parte specifica di una pagina

Si noti come il valore di `href` nel mio collegamento termina con `#scFota`? Questo è un trucchetto che puoi usare per saltare a una particolare parte di una pagina.

+ Innanzitutto, digita l'URL della pagina a cui collegarti, seguito da `#`.

+ Nel file di codice per la pagina a cui stai collegando, trova la parte a cui vuoi saltare e assegna a quell'elemento `id`, ad esempio, `<section id = "scFota"`. Il valore dell'ID `` è ciò che scrivi dopo il `#` nel tuo link.

\--- / chiudi \---

## \--- chiudi \---

## titolo: reimpostazione degli stili

Ora che l'intera anteprima è un link, il carattere del testo potrebbe essere cambiato.

+ In tal caso, puoi correggerlo aggiungendo una **classe CSS** al link: `class = "cardLink"`. Ecco il codice CSS da inserire nel tuo foglio di stile:

```css
    .cardLink {color: inherit; decorazione del testo: nessuna; }
```

Impostando il valore di qualsiasi proprietà su `inherit` si usa il valore che ha l'elemento **parent**. In questo caso, il colore del testo corrisponderà al resto del testo sulla home page.

\--- / chiudi \---

+ Crea almeno quattro o cinque di queste carte. Se lavori dal mio sito Web di esempio, puoi eseguirne uno per ciascuna delle sezioni nella pagina delle attrazioni. Sulla prossima Sushi Card imparerai come organizzare le carte con un bel trucco!