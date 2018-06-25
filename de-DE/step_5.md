## Alle in einer Reihe

Auf dieser Karte lernst du einige Tricks, um Dinge **horizontal** auf einer Seite anzuordnen. Zuerst wirst du sehen, wie man Dinge zentriert bekommt. Dann ordnen Sie Elemente nebeneinander in einer Reihe an.

+ Fügen Sie der Klasse `.card` die folgenden CSS-Eigenschaften hinzu:

```css
    Rand links: Auto; Rand rechts: Auto;
```

Sie sollten sehen, dass sich die Karten in die Mitte der Seite bewegen. Wenn Sie den linken und rechten Rand auf `auto`, können Sie jedes Element in der Mitte anstatt links platzieren.

![Die Karten erscheinen in der Mitte statt links](images/marginAuto.png)

+ Ziehen Sie den Rand des Browserfensters, um die Seite schmaler und breiter zu machen. Beachten Sie, dass die Karten zentriert bleiben.

+ Setzen Sie alle gerade erstellten Kartenlinks in ein neues Containerelement. Es wird kein `Artikel` oder `Abschnitt`, sondern einer mit `Div`. Dies ist ein universeller Container, mit dem Sie Objekte gruppieren und schöne Layouts erstellen können.

```html
    <div class="cardContainer">
```

+ Fügen Sie den folgenden CSS-Code in Ihr Stylesheet ein:

```css
    .cardContainer {Anzeige: flex; Flex-Wrap: wickeln; justify-content: räumlicher Raum; Auffüllen: 10px; }
```

Voilà! Dank **Flex**werden deine Karten nun nebeneinander angezeigt!

+ Ziehen Sie den Rand Ihres Fensters, um die Website breiter und schmaler zu machen, und beobachten Sie, wie sich die Karten bewegen, um an die Fenstergröße angepasst zu werden. Manchmal wird die nächste Zeile umbrochen.

![Die Karten sind in zwei Reihen angeordnet, die gleichmäßig auf die Browserbreite verteilt sind](images/flexSideBySide.png)

+ Versuchen Sie, die Eigenschaften `width` und `height` aus der Klasse `.card` löschen und sehen Sie, was passiert: `flex` fügt die Karten geschickt wie ein Puzzle zusammen und behält eine gleichmäßige Höhe über alles in der gleichen Reihe.

![Karten nebeneinander mit automatischer Breite angeordnet](images/flexAutoWidths.png)

Wenn Sie oben auf Ihrer Seite ein Navigationsmenü haben, können Sie diesen Trick verwenden. Ihr Menü muss aus Listenelementen ((`li`) für dieses nächste Bit bestehen. Wenn Sie möchten, können Sie es mit meiner Website ausprobieren.

+ Suchen Sie die CSS-Regeln für das Menü. In meiner Website sind das die Blöcke `nav ul`, `nav ul li`und `nav ul li a`.

+ Löschen Sie die Eigenschaft `display: inline;` aus den Listenelementen. Fügen Sie dann in der Liste `nav ul`Folgendes hinzu:

```css
    Anzeige: flex; justify-content: Flexstart;
```

![Menü mit Elementen, die nach links ausgerichtet sind](images/flexMenuStart.png)

Sie haben am Ende fast die gleiche Speisekarte, oder? Das Tolle an `flex` ist, dass Sie das Layout mit der Eigenschaft `justify-content`steuern können.

+ Ändern Sie den Wert von `justify-content` in `flex-end` und sehen Sie, was passiert. Oder ändern Sie es in `Leerzeichen um` herum, um die Menüelemente gleichmäßig zu verteilen, genau wie bei den Karten.

![Menü mit gleichmäßig verteilten Objekten](images/flexMenuSpace.png)

![Menü mit Elementen, die nach rechts ausgerichtet sind](images/flexMenuEnd.png)

**`flex`** ist ein ziemlich leistungsfähiges Layout - Tool , das eine ganze Sushi - Karte Reihe von selbst füllen könnte - Sie mehr darüber erfahren , kann [dojo.soy/html3-flex](http://dojo.soy/html3-flex).