## Entwerfen Sie coole Seitenlayouts

+ Für diese Karte sollten Sie mit einer Seite arbeiten, die ein `Haupt` Element mit drei Elementen im Inneren enthält: 1 `Artikel` und 2 `Seiten`s. Gehen Sie voran und erstellen Sie diese zuerst, wenn Sie müssen. Wenn Sie mit meiner Website arbeiten möchten, fügen Sie den Code " `beiseite` der vorherigen Sushi-Karte zur Seite "Attraktionen" hinzu. 

Hier sind drei verschiedene Seitenlayouts, die Sie anwenden werden:

![](images/cssGridLayouts.png)

+ Fügen Sie zu `Haupt-` und jedem der drei darin enthaltenen Elemente neue CSS-Klassen hinzu.

```html
    <main class="attPageLayoutGrid">
        <article class="attGridArticle">
            <! - andere Sachen hier-->
        </article>
        <aside class="attGridAside1">
            <! - andere Sachen hier-->
        </aside>
        <aside class="attGridAside2">
            <! - andere Sachen hier-->
        </aside>
    </main>
```

Der Container, den Sie ändern werden, ist `Haupt`, aber Sie könnten dies mit jeder Art von Container tun, wie ein `Div` oder `Artikel`oder sogar die ganze Seite `Körper`. Die Technik, die Sie verwenden werden, heißt **CSS-Gitter**.

In diesem Beispiel werden die `Kopfzeile` und `Fußzeile` aus dem Design weggelassen, aber es ist durchaus üblich, sie auch in das Raster aufzunehmen.

+ Setzen Sie die Eigenschaft `display` auf `grid` auf dem Gesamtcontainer:

```css
    .attPageLayoutGrid {Anzeige: Gitter; Gitter-Spalten-Abstand: 0.5em; Raster-Zeilenabstand: 1em; }
```

Was denken Sie , die `Raster-Spalt Spalt` und `Raster-Reihe-Lücke` Eigenschaften tun?

+ Als Nächstes benennen Sie für jedes Element einen Rasterbereich</code> `: </li>
</ul>

<pre><code class="css">    .attGridArticle {grid-area: agArticle; } .attGridAside1 {Gitterbereich: agAside1; } .attGridAside2 {Gitterbereich: agAside2; }
`</pre> 
    Dann gestalten Sie Ihr Layout! Lassen Sie uns die beiden setzen `beiseite` am unteren Rand der Seite an Seite Elemente Seite. Dazu benötigen Sie zwei **Spalten** gleicher Breite. Sie können die halten **Zeile** automatische Höhen.
    
    + Fügen Sie den folgenden Code in die CSS-Regeln `.attPageLayoutGrid`:
    ```css
        grid-template-rows: auto; Raster-Vorlage-Spalten: 1fr 1fr; Raster-Template-Bereiche: "agArticle agArticle" "agAside1 agAside2";
    ```
    
    `fr` steht für **Bruch**. Beachten Sie, wie Sie den `Artikel` den gesamten Platz über den zwei Spalten einnehmen.
    
    ## \--- Einsturz \---
    
    ## Titel: Hilfe! Ich habe Fehler und Warnungen!
    
    Wenn Sie Schmuck verwenden, werden möglicherweise einige Fehler und Warnungen angezeigt, auch wenn Sie den Code genau wie oben eingegeben haben. Dies liegt daran, dass Trinket die CSS-Gittereigenschaften noch nicht erkennt. Der Code wird jedoch weiterhin funktionieren.
    
    Wenn der CSS-Grid-Code Warnungen zu unbekannten Eigenschaften oder einen Fehler wie "Unerwartetes Token 1fr" enthält, können Sie diese ignorieren.
    
    \--- / einklappen \---
    
    ![Asides sind nebeneinander an der Unterseite](images/cssGridAsidesAtBottom.png)
    
    Lassen Sie uns die setzen `beiseite` Elemente über auf der rechten Seite und machen sie die Hälfte der Breite des `Artikel`.
    
    + Verändern Sie die Werte von `Grid-Template-Spalten` und `Grid-Template-Areas` zu:
    ```css
        Raster-Vorlage-Spalten: 2fr 1fr; Raster-Vorlagen-Bereiche: "agArticle agAside1" "agArticle agAside2";
    ```
    
    ![Die Seiten sind auf der rechten Seite](images/cssGridAsidesOnRight.png)
    
    + Wenn Sie nicht möchten, dass sich die `` Seite- </code> Elemente bis ganz nach unten erstrecken, können Sie mit einem Punkt ein Leerzeichen hinzufügen: 
    ```css
        Raster-Vorlagen-Bereiche: "agArticle agAside1" "agArticle agAside2" "agArticle. ";
    ```
    
    ![Wie rechts und nicht gestreckt](images/cssGridAsidesTopRight.png)
    
    \--- Herausforderung \---
    
    ## Herausforderung: Erstellen Sie verschiedene Layouts für verschiedene Bildschirmgrößen
    
    + Können Sie die zuvor hinzugefügten Bildschirmgrößenüberprüfungen verwenden, um das Layout abhängig von der Breite des Bildschirms zu ändern? Hinweis: Wenn Sie bereits CSS-Blöcke für jede Bildschirmgröße erstellt haben, können Sie diesen Blöcken den neuen CSS-Code hinzufügen, anstatt neue zu erstellen.
    
    \--- Hinweise \---
    
    \--- Hinweis \---
    
    Der folgende Code definiert ein Layout für die obige CSS-Klasse, wenn der Bildschirm größer als 1000 Pixel ist:
    
    ```css
        @media all and (Mindestbreite: 1000px) {.attPageLayoutGrid {grid-template-columns: 1fr 1fr; Raster-Template-Bereiche: "agArticle agArticle" "agAside1 agAside2"; }}  
    ```
    
    \--- /Hinweis \---
    
    \--- Hinweis \---
    
    Der folgende Code definiert ein Layout für die obige CSS-Klasse, wenn der Bildschirm größer als 1600 Pixel ist:
    
    ```css
        @media all and (Mindestbreite: 1600px) {.attPageLayoutGrid {grid-template-columns: 1fr 1fr; Raster-Template-Bereiche: "agArticle agAside1" "agArticle agAside2" "agArticle."; }}  
    ```
    
    \--- /Hinweis \---
    
    \--- / Hinweise \---
    
    \--- /Herausforderung \---
    
    Mit **CSS Grid**können Sie fast jedes beliebige Layout erstellen. Wenn Sie mehr erfahren möchten, gehen Sie zu [dojo.soy/html3-css-grid](http://dojo.soy/html3-css-grid){: target = "_ blank"}