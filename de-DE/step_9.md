## Fotocollage

Auf dieser Karte lernen Sie, CSS zu verwenden, um HTML-Elemente exakt zu positionieren und eine Fotocollage zu erstellen.

![](images/photoCollageWithText_wide.png)

+ Fügen Sie Ihrer Seite ein `div` und fügen Sie so viele Bilder ein, wie Sie möchten. Gib den `div` und den `img` Elementen `id` Werte.

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

Die Fotos erscheinen auf der Webseite nacheinander in der Reihenfolge, in der sie in Ihrem Code erscheinen.

+ Fügen Sie in Ihrer CSS-Datei die folgende CSS-Klasse für die Elemente innerhalb von `div`: 

```css
    .absPos {Position: absolut; }
```

+ Als Nächstes müssen Sie die Eigenschaft `position: relative hinzufügen.` zu dem Container selbst und definieren Sie eine Größe für ihn. Dadurch ist es so , daß die Positionen der anderen Elemente definiert sind **bezogen auf** (das heißt, innerhalb) des Behälters.

```css
    .relPos {Position: relativ; } #photoBox {Breite: 800px; Höhe: 400px; }
```

+ Erstellen Sie dann für jedes der Elemente einen Satz von Stilregeln, indem Sie **ID-Selektoren** , um ihre Größen (`Breite` und / oder `Höhe` Eigenschaften) sowie ihre genauen Positionen festzulegen.

Um die Position eines Elements zu definieren, gibt es vier Eigenschaften, die Sie verwenden können: `links`, `rechts`, `oben`und `unten`. Sie stellen dar, wie weit jede der Kanten vom Rand des Elternteils entfernt sein sollte. Verwenden Sie entweder `oben` oder `unten` für die vertikale Position und entweder `links` oder `rechts` für die horizontale Position.

![Diagramm, das zeigt, wie sich die oberen, linken, unteren und rechten Eigenschaften auf den übergeordneten Container beziehen](images/cssPositionProperties.png)

+ Wählen Sie genaue Positionen für jedes Ihrer Bilder und verwenden Sie eine der Eigenschaften `links`, `rechts`, `oben`und `unten` , um diese Positionen in Ihren CSS-Regeln zu definieren. Beispielsweise platziert dieser Code das Katzenbild 100 Pixel von oben und 60 Pixel von links:

```css
    #imgTeaCat {Breite: 250px; oben: 100px; links: 60px; }
```

Hinweis: Die Positionswerte können auch negativ sein! Wenn Sie einen negativen Wert verwenden, wird das Element außerhalb des Containers über die angegebene Kante hinaus verschoben.

### Dinge überschneiden sich

Vielleicht möchten Sie, dass sich einige der Bilder überschneiden. Aber wie wählst du aus, welcher an der Spitze steht?

+ Wählen Sie zwei Bilder und geben Sie ihnen Positionen, die sie überlappen lassen.

+ Fügen Sie eine zusätzliche Eigenschaft hinzu, `z-index: 10;` zu einem von ihnen, und fügen Sie dann `Z-Index: 7;` zum anderen.

+ Sehen Sie sich das Ergebnis auf Ihrer Webseite an.

![](images/horse10Cat7.png)

+ Vertauschen Sie nun die `Z-Index` Werte, so dass die `7` und die `10` genau umgekehrt sind. Siehst du irgendeinen Unterschied auf deiner Webseite?

![](images/horse7Cat10.png)

## \--- Einsturz \---

## titel: Wie funktioniert der z-index?

Mit der Eigenschaft `z-index` können Sie entscheiden, wie sich zwei oder mehr Elemente überlappen sollen. Der Wert kann eine ganze Zahl sein.

Das Element mit der **höchsten** Nummer landet auf **oberen** des Stapels, oder anders gesagt auf den **vorderen**. Das Element mit der nächsthöheren Zahl steht dahinter und vor den anderen usw., bis Sie zu dem Element mit der niedrigsten Nummer kommen, das hinter allen anderen Elementen auf der Rückseite erscheint.

\--- / einklappen \---

Sie können beliebige HTML-Elemente auf diese Weise positionieren, nicht nur Bilder. Zum Beispiel könnten Sie ein `p` -Element verwenden, um Text über ein Foto hinzuzufügen.

\--- Herausforderung \---

## Herausforderung: Machen Sie eine Fotocollage

+ Versuchen Sie, Ihre eigene Collage von Fotos wie die unten gezeigte zu erstellen! Verwenden Sie die exakte Positionierung zusammen mit verschiedenen Werten für `z-index` , um den Überlappungseffekt so zu gestalten, wie Sie es möchten.

\--- Hinweise \---

\--- Hinweis \---

Im Folgenden finden Sie den HTML-Code für die Fotocollage auf meiner Irland-Website. Es gibt sechs Fotos und ein Stück Text in einem `div`.

```html
    <div id="photoBox" class="relPos">
        <img id="imgStreet" class="collagePhoto absPos" src="ireland-1474045_640.jpg" alt="Irish town" />
        <img id="imgTeaCat" class="collagePhoto absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
        <img id="imgCoast" class="collagePhoto absPos" src="cattle-2369463_640.jpg" alt="Cows at the coast" />
        <img id="imgTrees" class="collagePhoto absPos" src="ireland-2614852_640.jpg" alt="Tree tunnel" />
        <img id="imgSheep" class="collagePhoto absPos" src="sheep-456989_640.jpg" alt="Sheep on the road" />
        <img id="imgHorse" class="collagePhoto absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <p id="photoText" class="absPos">Irland</p>
    </div>
```

\--- /Hinweis \---

\--- Hinweis \---

Hier sind die CSS-Regeln, die die Positionen für jedes meiner Bilder in der Collage festlegen:

```css
    #imgPferd {width: 120px; oben: 200px; links: 390px; Z-Index: 10; } #imgSheep {Breite: 200px; oben: 100px; links: 20px; Z-Index: 8; } #imgCoast {Breite: 150px; oben: 250px; links: 10px; Z-Index: 5; } #imgTrees {Breite: 110px; oben: 65px; links: 205px; Z-Index: 9; } #imgTeaCat {Breite: 250px; oben: 210px; links: 160px; Z-Index: 7; } #imgStreet {Breite: 180px; oben: 90px; links: 310px; Z-Index: 6; } #photoText {font-family: "Pinsel-Skript MT"; Farbe: hellgrün; Schriftgröße: 4em; links: 35px; oben: 15px; Z-Index: 20; }
```

\--- /Hinweis \---

\--- Hinweis \---

Hier sind die CSS-Klassen, die ich verwendet habe:

```css
    .collagePhoto {Grenze: 1px durchgehend weiß; } .relPos {Position: relativ; } .absPos {Position: absolut; }
```

\--- /Hinweis \---

\--- / Hinweise \---

![Fotocollage mit Text über die Oberseite](images/photoCollageExample.png)

\--- /Herausforderung \---