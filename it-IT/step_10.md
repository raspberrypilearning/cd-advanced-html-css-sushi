## Effetti speciali

Su questa scheda imparerai alcuni effetti più belli che puoi ottenere con i CSS.

### Ombre e movimento

Aggiungiamo un piccolo movimento quando posizioni il cursore sulle carte che hai creato in precedenza.

+ Trova la scheda `: hover` classe CSS precedente e modificala come segue:

```css
    .card: hover {box-shadow: 0px 2px 2px rgba (0,0,0,0,2); transform: translateY (-2px); }
```

+ Prova diversi valori nella funzione `translate`!

--- chiudi ---

## title: La proprietà `transform`

Se hai completato le schede intermedie HTML / CSS Sushi, potresti ricordare di utilizzare la proprietà `trasformazione` in alcune animazioni di `@keyframes`. Qui puoi vedere che puoi anche usare la proprietà da sola all'interno di un normale blocco CSS.

Un tipo di valore che puoi impostare è `ruota`, per far girare un elemento. Altri sono `translateY`, che sposta qualcosa in alto o in basso, e `translateX`, per il movimento da un lato all'altro.

--- / chiudi ---

+ Gioca con diversi valori di pixel nella proprietà `box-shadow` per vedere cosa fanno. 

--- chiudi ---

## titolo: Cos'è `rgba`?

`rgba (0,0,0,0.2)` è un altro modo di definire un colore.

Ha i soliti tre numeri (da `0` fino a `255`) per rosso, verde e blu.

Il quarto numero, chiamato valore **alfa** , definisce come **trasparente** (o trasparente). È un numero decimale compreso tra `0` e `1`, dove `1` non è affatto trasparente e `0` completamente invisibile. Ciò significa che più basso è il valore alfa di un elemento, più è trasparente.

--- / chiudi ---

+ Infine, rendi il movimento scorrevole aggiungendo la seguente proprietà alla classe `.card` di prima: 

```css
    transizione: tutti gli anni '70 di alleggerimento;
```

Una durata di `0,2 s` significa che la `transizione` dura per 0,2 secondi.

### ID

Un altro effetto che probabilmente hai visto su molti siti web è **lightbox**: fai clic su qualcosa e il sito si oscura mentre qualcos'altro, come una foto più grande o una finestra popup, appare di fronte a tutto.

![Effetto lightbox in azione](images/lightboxLemur.png)

Per ottenere questo effetto, creerai due link: uno per il lightbox reale (il bit che si apre) e uno per la cosa che fai clic per far apparire la lightbox. Farò il mio nella pagina delle attrazioni del mio sito web. Vai con qualunque pagina hai foto!

+ Decidi quali cose vuoi che vengano visualizzate quando fai clic e aggiungili alla tua pagina tra un insieme di tag `a` per creare un collegamento. Assicurati di dare il link un `id`. Il codice può andare ovunque sulla pagina: renderete gli elementi invisibili nel prossimo passo!

```html
    <a href="#_" class="lightbox" id="boxLemur">
        <h3>Lemure !!</h3>
        <img src="monkey-2223271_640.jpg" alt="Picture of a lemur" />
        <p>Un lemure che si gode un piccolo spuntino</p>
    </a>
```

Puoi mettere tutto ciò che ti piace tra i tag link. Ho una grande immagine, un titolo e del testo. Forse vuoi solo una foto e nessun testo!

+ Aggiungi il seguente codice CSS per la lightbox. Puoi capire cosa fa un po '?

```css
    .lightbox {background: rgba (0,0,0,0,8); colore: #ffffff; allineamento del testo: centro; decorazione del testo: nessuna; larghezza: 100%; altezza: 100%; inizio: 0; a sinistra: 0; posizione: fissa; visibilità: nascosta; z-index: 999; }
```

Nota: l'impostazione della proprietà `posizione` su `fissa` indica che la posizione impostata sarà relativa alla finestra del browser, quindi rimarrà chiusa durante lo scorrimento.

+ Quindi, decidi quale cosa vuoi cliccare per far apparire la lightbox, e aggiungi aggiungi un paio di tag `a` attorno a quell'elemento (nel mio caso è un'immagine più piccola di un lemure). Il **target** del link sarà il lightbox, che hai impostato usando il `id`. Potresti riconoscere questa tecnica da prima!

```html
    <a href="#boxLemur">
        <img src="monkey-2223271_640.jpg" class="mediumPics">
    </a>
```

+ Infine aggiungi il seguente codice CSS. Si noti che questo è un **pseudo-classe**; dovrebbe andare dopo il codice per la classe `.lightbox` e non dentro!

```css
    .lightbox: target {visibility: visible; }
```

La pseudo-classe `: target` viene applicata ogni volta che la lightbox è stata la destinazione dell'ultimo link cliccato. Quindi, quando fai clic ovunque, la visibilità `` sarà impostata su `nascosto`.

+ Prova a fare clic sul tuo nuovo link per vedere la lightbox apparire! Per farlo andare via, basta cliccare in qualsiasi punto della pagina.

Puoi aggiungere tutti i lightbox che vuoi a una pagina. Tutti possono utilizzare la stessa classe CSS - basta assicurarsi che ognuno ha un diverso `id`! Per ognuno di essi, devi creare qualcosa sulla tua pagina web in un link che puoi fare clic per far apparire la lightbox, e quindi utilizzare l'id `` come valore `href` in quel link, proprio come hai fatto sopra!