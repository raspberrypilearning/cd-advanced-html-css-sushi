## Cartonașe de accesat

Iată o metodă pe care o poți folosi pentru a creea un album foto, sau o pagina de portofoliu care să arate proiectele tale: little **preview cards**.

![Previzulalizează cartonașul afișând o imagine în miniatura si ceva text](images/cardsPreview.png)

+ Adaugă următoarea comanda site-ului tău, unde dorești. O voi face pe `index.html`. Poți modifica poza și textul în funcție de cartonașele tale precedente. Am de gând să adaug o serie de atracții turistice din Irlanda.

```html
    <article class="card">
        <img src="monkey-2223271_640.jpg" class="tinyPicture">
        <h3>Fota Wildlife Park</h3>
        <p>Fota Island, County Cork</p>
    </article>
```

![Imaginea si textul inaintea aplicării modelelor](images/cardUnstyled.png)

+ Adauga urmatoarea comanda CSS pentru a creea grupele `card` și `tinyPicture`:

```css
    .tinyPicture {
        height: 60px;
        border-radius: 10px;
    }
    .card {
        width: 200px;
        height: 200px;
        border: 2px solid #F0FFFF;
        border-radius: 10px;
        box-sizing: border-box;
        padding: 10px;
        margin-top: 10px;
        font-family: "Trebuchet MS", sans-serif;
    }
    .card:hover {
        border-color: #1E90FF;
    }
```

![Imaginea si textul modelate pentru a da un efect de cartonaș](images/cardStyled.png)

Hai să transformăm cartonașul într-ul link, pentru ca ceilalți să-l poată accesa, pentru mai multe informații.

+ Pune toate elementele `article` în interiorul unui compoziției link-ului. Asigură-te că eticheta de sfârșit `</a>` se afla înaintea etichetei `</article>` tag! Poți să schimbi adresa **URL** cu orice adresa vrei tu. Poate să fie o altă pagina din site-ul tău, sau poate să fie, în totalitate, un alt site.

```html
    <a href="attractions.html#scFota">  
        <article class="card ">
            <img src="monkey-2223271_640.jpg" class="tinyPicture">
            <h3>Fota Wildlife Park</h3>
            <p>Fota Island, County Cork</p>
        </article>
    </a>
```

![Textul si imaginea transformate intr-o adresa](images/cardLink.png)

## \--- collapse \---

## titlu: Legaturile spre o parte anume a paginii

Ai observat cum se termină valoarea `href` din adresa mea, în `#scFota`? Este un truc mic, pe care-l poți folosi, pentru a sări la o anumită parte a paginii.

+ Mai întâi, introdu adresa URL a paginii în link, urmat de `#`.

+ În codul paginii, pentru pagina catre care faci legătura, caută porțiunea la care vrei să sari, și dăi acelui element un `id`, spre exemplu, `<section id="scFota"`. Valoarea `id` este aceea pe care o tastezi dupa `#` din adresa ta.

\--- /collapse \---

## \--- collapse \---

## titlu: Resetarea tipurilor

Acum întregul cartonaș este o adresă, iar fontul textului apare modificat.

+ Dacă e așa, atunci îl poti corecta adăugând **CSS class** adresei: `class="cardLink"`. Aici e codul CSS pe care trebuie să o adaugi modelului tău:

```css
    .cardLink {
        color: inherit;
        text-decoration: none;
    }
```

Setarea valorii unei proprietăți la `inherit` ajunge să utilizeze valoarea pe care o are elementul **parent**. Deci in acest caz, culoarea textului va fi identica cu cea a textului din pagina principala.

\--- /collapse \---

+ Creează cel puțin patru sau cinci astfel de cartonașe. Dacă lucrezi de pe exemplu meu de site, poți face câte un cartonaș pentru fiecare sectiune din pagina Atracții. În cartonașul următor, vei învăța cum să aranjezi cartonașele folosind un truc atractiv!