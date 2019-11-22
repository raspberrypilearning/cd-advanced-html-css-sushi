## Toate pe un rând

În acest cartonaș vei învăța câteva trucuri pentru aranjarea lucrurilor pe **horizontally**, într-o pagina. Prima data, vei vedea cum se pot așeza lucrurile pe centru. Apoi vei aranja elementele unul lângă altul pe un rând.

+ Adaugă următoarele proprietăți clasei `.card`:

```css
    margin-left: auto;
    margin-right: auto;
```

Ar trebui sa vezi cartonașele mutându-se în centrul paginii. Prin setarea marginilor, stânga și dreapta pe `auto`, poți face ca fiecare element să fie în partea din mijloc, nu în partea cea mai din stânga.

![Cartonașe ce apar în mijloc în loc să apară mai la stânga](images/marginAuto.png)

+ Trage de margine ferestrei pentru a face pagina mai îngustă sau mai largă - observă cum cartonașul rămâne centrat.

+ Pune toate adresele care le-ai creat intr-o nouă casetă de elemente. Nu va fi una `article` sau o `section`, ci una numită `div`. Aceasta este o casetă de uz general pe care o vei putea folosi atunci cand ordonezi lucrurile si când creezi suprafete draguțe.

```html
    <div class="cardContainer">
```

+ Adaugă următorul cod CSS in fila de modelare:

```css
    .cardContainer {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        padding: 10px;
    }
```

Voilà! Mulțumită lui **Flex**, cartonașele tale sunt acum afișate unul lângă altul!

+ Trage de marginea ferestrei pentru a o face mai lată sau mai îngustă, și observă cum cartonașele se mișcă în jur pentru a se putea potrivi cu mărimea selectată a ferestrei, câteodata înfășurându-se la linia următoare.

![Catonașe aranjate în două rânduri depărtate egal pentru a se putea potrivi cu lățimea ecranului](images/flexSideBySide.png)

+ Încearcă să ștergi proprietățile de `width` și `height` din clasa de cartonașe `.card` și vezi ce se întâmplă: `flex` va aranja ingenios cartonașele exact ca un puzzle tăiat, menținând înălțimea egală peste toate lucrurile de pe același rând.

![Cartonașe aranjate unul lângă altul cu lățime automată](images/flexAutoWidths.png)

Dacă există un meniu de bare în partea de sus a paginii, atunci acolo este un alt loc unde vei putea folosi acest truc. Meniul tău trebuie să fie alcătuit din losta de elemente( (`li`) pentru părticica următoare. Dacă vrei, poți testa site-ul meu.

+ Găsește regulile CSS pentru meniu. În aite-ul meu, acesta e blocul `nav ul`, `nav ul li`, și `nav ul li a`.

+ Șterge proprietățile `display: inline;` din lista de obiecte. Mai apoi, în lista `nav ul`, adaugă:

```css
    display: flex;
    justify-content: flex-start;
```

![Meniu cu elemente aliniate la stânga](images/flexMenuStart.png)

Vei ajunge la exact aproape același meniu, așa-i? Partea tare a `flex` e că tu controlezi suprafața prin proprietatea `justify-content`.

+ Schimbă valaoarea `justify-content` în `flex-end` și veI ce se întamplă. Sau schimb-o în `space-around` pentru a face obiectele din meniu și mai departate, exact cum ai procedat și cu cartonașele.

![Meniu cu elemente departate egal](images/flexMenuSpace.png)

![Meniu cu elemente aliniate la dreapta](images/flexMenuEnd.png)

**`flex`** este un sculă de aranjare destul de puternică capabilă să umple toată seria de cartonașe Sushi, independent - poți învăța mai multe despre asta la [dojo.soy/html3-flex](http://dojo.soy/html3-flex).