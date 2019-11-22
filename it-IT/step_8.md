## Collage di foto

Con questa scheda imparerai a usare il CSS per posizionare in modo preciso elementi HTML e creare un collage fotografico.

![](images/photoCollageWithText_wide.png)

+ Aggiungi un `div` alla tua pagina e inserisci tutte le immagini che desideri. Assegna agli elementi `div` e `img` degli `id`.

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

Le foto verranno visualizzate una dopo l'altra nella pagina web, nell'ordine in cui appaiono nel codice.

+ Nel tuo file CSS, aggiungi la seguente classe CSS per gli elementi all'interno di `div`: 

```css
    .absPos {
        position: absolute;
    }
```

+ Successivamente, è necessario aggiungere la proprietà `position: relative;` al contenitore stesso e definire una dimensione per esso. Questo fa sì che le posizioni degli altri elementi siano definite **rispetto a** (cioè, all'interno) del contenitore.

```css
    .relPos {
        position: relative;
    }

    #photoBox {
        width: 800px;
        height: 400px;
    }
```

+ Quindi, crea una serie di regole di stile per ciascuno degli elementi usando **selettori id** per impostare le loro dimensioni (proprietà `width` e/o `height`) e le loro posizioni esatte.

Per definire la posizione di un elemento, sono disponibili quattro proprietà: `left`, `right`, `top`, e `bottom`. Rappresentano quanto devono essere lontani i bordi dal margine dell'elemento genitore. Utilizza `top` o `bottom` per la posizione verticale e `left` o `right` per la posizione orizzontale.

![Diagramma che mostra come le proprietà top, left, bottom e right si riferiscono al contenitore genitore](images/cssPositionProperties.png)

+ Scegli le posizioni precise per ciascuna delle tue immagini e usa una delle proprietà `left`, `right`, `top` e `bottom` per definire quelle posizioni nelle tue regole CSS. Ad esempio, questo codice posiziona l'immagine del gatto a 100 pixel dall'alto e a 60 pixel da sinistra:

```css
    #imgTeaCat {
        width: 250px;
        top: 100px;
        left: 60px;
    }
```

Nota: i valori della posizione possono anche essere negativi! Se si utilizza un valore negativo, si spinge l'elemento fuori dal contenitore, oltre qualsiasi bordo specificato.

### Far sovrapporre gli elementi

Potresti voler sovrapporre alcune delle immagini. Ma come si sceglie quale va in primo piano?

+ Scegli due immagini e dai loro posizioni che le facciano sovrapporre.

+ Aggiungi una proprietà extra, `z-index: 10;`, a uno di essi, quindi aggiungi `z-index: 7;` all'altra.

+ Dai un'occhiata al risultato sulla tua pagina web.

![](images/horse10Cat7.png)

+ Ora scambia i valori di `z-index`, in modo che il `7` e il `10` siano al contrario. Vedi qualche differenza sulla tua pagina web?

![](images/horse7Cat10.png)

## \--- collapse \---

## title: Come funziona z-index?

La proprietà `z-index` ti consente di decidere come sovrapporre due o più elementi. Il valore può essere qualsiasi numero intero.

L'elemento con il valore **più alto** finisce in **primo piano** sulla pila, o in altre parole decisamente **avanti**. L'elemento con il successivo numero più alto va dietro, e davanti agli altri, e così via, finché non si arriva all'elemento con il numero più basso, che appare dietro a tutti gli altri elementi.

\--- /collapse \---

Puoi posizionare qualsiasi elemento HTML in questo modo, non solo le immagini. Ad esempio, puoi usare un elemento `p` per aggiungere del testo sopra una foto.

\--- challenge \---

## Sfida: crea un collage fotografico

+ Prova a creare il tuo collage di foto come quello mostrato di seguito! Usa il posizionamento esatto insieme a diversi valori di `z-index` per ottenere l'effetto di sovrapposizione nel modo desiderato.

\--- hints \---

\--- hint \---

Di seguito è riportato il codice HTML per il collage di foto sul mio sito web sull'Irlanda. Ci sono sei foto e una parte di testo all'interno di un `div`.

```html
    <div id="photoBox" class="relPos">
        <img id="imgStreet" class="collagePhoto absPos" src="ireland-1474045_640.jpg" alt="Irish town" />
        <img id="imgTeaCat" class="collagePhoto absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
        <img id="imgCoast" class="collagePhoto absPos" src="cattle-2369463_640.jpg" alt="Cows at the coast" />
        <img id="imgTrees" class="collagePhoto absPos" src="ireland-2614852_640.jpg" alt="Tree tunnel" />
        <img id="imgSheep" class="collagePhoto absPos" src="sheep-456989_640.jpg" alt="Sheep on the road" />
        <img id="imgHorse" class="collagePhoto absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <p id="photoText" class="absPos">Irlanda</p>
    </div>
```

\--- /hint \---

\--- hint \---

Ecco le regole CSS che definiscono le posizioni per ciascuna delle mie immagini nel collage:

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

Ecco le classi CSS che ho usato:

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

![Collage di foto con del testo sopra](images/photoCollageExample.png)

\--- /challenge \---