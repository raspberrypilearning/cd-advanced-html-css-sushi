## Rendi il tuo menu reattivo

Un sito Web **reattivo** è uno che si adatta alle dimensioni dello schermo in modo che sia sempre eccezionale, sia che lo si guardi su un computer, un cellulare o un tablet. Rendiamo il tuo menu reattivo!

Inizierete con gli stili regolari: questa sarà la vostra **di default** comportamento.

## \--- chiudi \---

## titolo: cosa significa "default"?

Gli stili di default sono il tuo normale set di regole di stile. Sono applicati a prescindere da cosa, prima di verificare eventuali condizioni speciali.

È possibile aggiungere codice che poi controlla la dimensione dello schermo e apporta alcune modifiche se necessario.

\--- / chiudi \---

+ Aggiungi le seguenti regole CSS al tuo menu. Probabilmente hai definito anche i colori e i bordi; Li ho lasciati fuori per risparmiare spazio qui! Se hai già definito le regole CSS per il tuo menu, aggiungi o modifica le proprietà e i valori sottostanti che ti mancano.

```css
    nav ul {padding: 0.5em; display: flex; direzione della flessione: colonna; } nav ul li {text-align: center; list-style-type: none; margin-right: 0.5em; margin-left: 0.5em; }
```

Con il codice CSS sopra, il tuo menu sarà più adatto a schermi piccoli. Questo si chiama **mobile-first** development.

![Elementi del menu impilati verticalmente su un piccolo schermo](images/responsiveMenuMobile.png)

## \--- chiudi \---

## titolo: cosa significa 'mobile-first'?

Molto spesso quando codi un sito web, utilizzerai lo schermo di un computer e probabilmente definirai i tuoi stili in base a come appare su quello schermo.

Quando prepari prima il codice per dispositivi mobili, scegli invece gli stili predefiniti adatti per schermi di piccole dimensioni come gli smartphone. Quindi aggiungi del codice extra per apportare modifiche agli schermi più grandi.

Dal momento che sempre più persone navigano in Internet sui propri smartphone o tablet anziché su un computer, è buona norma sviluppare il sito Web tenendo conto di ciò.

\--- / chiudi \---

+ Ora aggiungi il seguente codice al tuo foglio di stile:

```css
    @media all e (min-width: 1000px) {nav ul {flex-direction: row; justify-content: space-around; }}
```

La prima riga di codice sopra controlla quali sono le dimensioni della finestra del browser. Se la finestra è **1000 pixel** larga o più, applicherà tutte le regole di stile all'interno del blocco.

![Le voci del menu sono distribuite uniformemente su una riga su uno schermo più ampio](images/responsiveMenuMedium.png)

## \--- chiudi \---

## titolo: come funziona?

Il blocco contiene nuovi valori solo per alcune proprietà del menu `nav ul`.

Ogni volta che la finestra è più larga di 1000 pixel, questi nuovi valori verranno applicati al posto di quelli già definiti per `nav ul`.

Il resto delle proprietà che hai definito precedentemente per `nav ul` rimarrà lo stesso.

\--- / chiudi \---

+ Se si utilizza Trinket per scrivere codice, potrebbe essere utile scaricare il progetto in modo da poterlo testare su uno schermo a schermo intero.

\--- sfida \---

## Sfida: fai in modo che il tuo menu si aggiusti automaticamente per i grandi schermi

+ Puoi aggiungere un altro blocco per schermi più grandi di **1600 pixel**, con `flex-end` invece di `space-around`?

![Voci del menu a destra su un ampio schermo](images/responsiveMenuWide.png)

\--- suggerimenti \---

\--- suggerimento \---

Il seguente codice definisce le proprietà flessibili per le voci di menu quando lo schermo è più grande di 1600 pixel:

```css
    @media all e (min-width: 1600px) {nav ul {flex-direction: row; justify-content: flex-end; }}  
```

\--- / suggerimento \---

\--- / suggerimenti \---

\--- / challenge \---

Puoi mettere qualsiasi regola CSS che ti piace in blocchi come questi per definire stili diversi per le diverse dimensioni dello schermo. Sarà particolarmente utile quando si eseguono i layout griglia CSS in un secondo momento!