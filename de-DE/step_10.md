## Spezialeffekte

Auf dieser Karte lernst du ein paar nette Effekte, die du mit CSS erreichen kannst.

### Schatten und Bewegung

Lassen Sie uns eine kleine Bewegung hinzufügen, wenn Sie den Mauszeiger über die Karten bewegen, die Sie zuvor erstellt haben.

+ Suchen Sie die CSS-Klasse `.card: hover` von früher, und ändern Sie sie wie folgt:

```css
    .card: Hover {Box-Schatten: 0px 2px 2px rgba (0,0,0,0,2); transform: translateY (-2px); }
```

+ Probieren Sie verschiedene Werte in der Funktion `translate` aus!

--- Einsturz ---

## title: Die Eigenschaft `transformiere`

Wenn Sie die Intermediate HTML / CSS Sushi Cards fertiggestellt haben, erinnern Sie sich vielleicht daran, die Eigenschaft `transform` in einigen `@keyframes` Animationen zu verwenden. Hier sehen Sie, dass Sie die Eigenschaft auch eigenständig in einem regulären CSS-Block verwenden können.

Eine Art von Wert, auf die Sie sie setzen können, ist `rotiere`, um ein Element zu drehen. Andere sind `translateY`, das etwas nach oben oder unten bewegt, und `translateX`, um sich von Seite zu Seite zu bewegen.

--- / einklappen ---

+ Spielen Sie mit verschiedenen Pixelwerten in der Eigenschaft `box-shadow` herum, um zu sehen, was sie tun. 

--- Einsturz ---

## Titel: Was ist `rgba`?

`rgba (0,0,0,0.2)` ist eine weitere Möglichkeit, eine Farbe zu definieren.

Es hat die üblichen drei Zahlen (von `0` bis `255`) für Rot, Grün und Blau.

Die vierte Zahl, der Wert **Alpha** , definiert, wie **transparente** (oder durchsichtig) etwas ist. Es ist eine Dezimalzahl zwischen `0` und `1`, wobei `1` überhaupt nicht durchsichtig ist und `0` vollständig unsichtbar ist. Dies bedeutet, je niedriger der Alpha-Wert eines Elements ist, desto durchsichtiger ist es.

--- / einklappen ---

+ Schließe die Bewegung schließlich ab, indem du der Klasse `.card` von früher die folgende Eigenschaft hinzufügst: 

```css
    Übergang: alle 0,2s erleichtern;
```

Eine Dauer von `0,2 s` bedeutet, dass der `Übergang` 0,2 Sekunden dauert.

### Leuchtkasten

Ein weiterer Effekt , den Sie wahrscheinlich auf viele Websites gesehen haben , ist **Leuchtkasten**: Sie klicken auf etwas und die Website dimmt während etwas anderes, wie ein größeres Bild oder ein Popup - Fenster, erscheint vor allem.

![Lightbox-Effekt in Aktion](images/lightboxLemur.png)

Um diesen Effekt zu erhalten, werden Sie zwei Links machen: einen für den eigentlichen Leuchtkasten (das Bit, das erscheint) und einen für die Sache, auf die Sie klicken, um den Leuchtkasten zu sehen. Ich mache meinen auf der Seite "Attraktionen" meiner Website. Sie gehen mit welcher Seite Sie Bilder haben!

+ Entscheiden Sie, welche Dinge angezeigt werden sollen, wenn Sie auf klicken, und fügen Sie sie alle zwischen `` Tags zu Ihrer Seite hinzu, um einen Link zu erstellen. Stellen Sie sicher, dass Sie dem Link eine `ID`. Der Code kann überall auf der Seite erscheinen: Sie werden die Elemente im nächsten Schritt unsichtbar machen!

```html
    <a href="#_" class="lightbox" id="boxLemur">
        <h3>Lemur !!</h3>
        <img src="monkey-2223271_640.jpg" alt="Picture of a lemur" />
        <p>Ein Lemur, der einen kleinen Snack genießt</p>
    </a>
```

Sie können alles, was Sie möchten, zwischen den Link-Tags einfügen. Ich habe ein großes Bild, eine Überschrift und etwas Text. Vielleicht möchten Sie nur ein Bild und keinen Text!

+ Fügen Sie den folgenden CSS-Code für den Leuchtkasten hinzu. Können Sie herausfinden, was einige davon tun?

```css
    .lightbox {Hintergrund: rgba (0,0,0,0,8); Farbe: #ffffff; Textausrichtung: Mitte; Textdekoration: keine; Breite: 100%; Höhe: 100%; oben: 0; links: 0; Position: fixiert; Sichtbarkeit: versteckt; Z-Index: 999; }
```

Hinweis: Wenn Sie die Eigenschaft `position` auf `fixed` bedeutet dies, dass die von Ihnen festgelegte Position relativ zum Browserfenster ist und beim Scrollen beibehalten wird.

+ Als nächstes entscheiden Sie, welche Sache Sie klicken möchten, um den Leuchtkasten erscheinen zu lassen, und fügen Sie ein Paar `a` Tags um dieses Element hinzu (in meinem Fall ist es ein kleineres Bild eines Lemurs). Das **Ziel** des Links ist der Leuchtkasten, den Sie mit den `ID`. Sie können diese Technik von früher erkennen!

```html
    <a href="#boxLemur">
        <img src="monkey-2223271_640.jpg" class="mediumPics">
    </a>
```

+ Fügen Sie abschließend den folgenden CSS-Code hinzu. Beachten Sie, dass dies eine **-Pseudoklasse**; Es sollte nach dem Code für die `.lightbox` Klasse gehen und nicht darin!

```css
    .lightbox: target {Sichtbarkeit: sichtbar; }
```

Die Pseudo-Klasse `: Ziel` wird immer dann angewendet, wenn der Leuchtkasten das Ziel des letzten angeklickten Links war. Wenn Sie also irgendwo klicken, wird die `Sichtbarkeit` auf `versteckte`.

+ Versuchen Sie, auf Ihren neuen Link zu klicken, um den Leuchtkasten zu sehen! Um es zu entfernen, klicken Sie einfach irgendwo auf die Seite.

Sie können einer Seite beliebig viele Leuchtkästen hinzufügen. Sie können alle die gleiche CSS-Klasse verwenden - stellen Sie nur sicher, dass jede eine andere `ID`! Für jeden einzelnen musst du etwas auf deiner Webseite zu einem Link machen, auf den du klicken kannst, um den Leuchtkasten zu sehen, und dann die `ID` als `href` Wert in diesem Link zu verwenden, genau wie du es oben getan hast!