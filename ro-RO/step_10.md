## Efecte speciale

Pe acest card veti invata cateva efecte benefice pe care le puteti obtine cu ajutorul CSS.

### Umbre și mișcare

Să adăugăm o mică mișcare atunci când plasați cursorul pe cărțile pe care le-ați făcut mai devreme.

+ Găsiți cartea `: mutați` clasă CSS de mai devreme și schimbați-o la următoarea:

```css
    .card: hover {box-shadow: 0px 2px 2px rgba (0,0,0,0,2); transformare: translateY (-2px); }
```

+ Încercați valori diferite în `traduce` funcție!

## \--- colaps \---

## titlu: Proprietatea `transformă`

Dacă ați finalizat cartelele Intermediate HTML / CSS Sushi, este posibil să vă amintiți folosirea proprietății `transform` în unele animații `cheie` cadre. Aici veți vedea că puteți utiliza proprietatea pe cont propriu într-un bloc CSS obișnuit.

Un fel de valoare pe care o puteți seta este `rotiți`, pentru a face un element de întoarcere. Altele sunt `translateY`, care mișcă ceva în sus sau în jos, și `translateX`, pentru mișcarea dintr-o parte în alta.

\--- / colaps \---

+ Redați-le cu valori ale pixelilor diferite în proprietatea `box-shadow` pentru a vedea ce fac. 

## \--- colaps \---

## titlu: Ce este `rgba`?

`rgba (0,0,0,0,2)` este un alt mod de definire a unei culori.

Are cele trei numere obișnuite (de la `0` până la `255`) pentru roșu, verde și albastru.

Al patrulea număr, numit valoarea **alfa** , definește modul în care este **transparent** (sau vizibil). Este un număr zecimal între `0` și `1`, cu `1` nefiind deloc vizibile, iar `0` fiind complet invizibil. Aceasta inseamna ca valoarea alfa a unui element este mai mica, cu atat mai mult este aceasta.

\--- / colaps \---

+ În cele din urmă, faceți mișcarea netedă prin adăugarea următoarei proprietăți la clasa `.card` de mai devreme: 

```css
    tranziție: toate 0,2 secunde;
```

O durată de `0.2S` înseamnă `tranziția` durează 0,2 secunde.

### Caseta de lumina

Un alt efect pe care l-ați văzut probabil pe o mulțime de site-uri web este **lightbox**: faceți clic pe ceva și site-ul se estompează, în timp ce altceva, ca o imagine mai mare sau o fereastră pop-up, apare în fața a tot.

![Efectul efectului lightbox în acțiune](images/lightboxLemur.png)

Pentru a obține acest efect, veți face două linkuri: una pentru caseta de lumină reală (bitul care apare) și una pentru lucrul pe care faceți clic pentru a face să apară caseta de lumină. O să fac a mea pe pagina Atracții a site-ului meu. Te duci cu orice pagina pe care ai poze!

+ Decideți ce doriți să apară când faceți clic și adăugați-le pe toate în pagină între un set de taguri `` pentru a crea un link. Asigurați-vă că dați link-ul `id`. Codul poate merge oriunde pe pagină: veți face elementele invizibile în pasul următor!

```html
    <a href="#_" class="lightbox" id="boxLemur">
        <h3>Lemur !!</h3>
        <img src="monkey-2223271_640.jpg" alt="Picture of a lemur" />
        <p>Un lemur care se bucură de o mică gustare</p>
    </a>
```

Puteți pune tot ce vă place între etichetele de legătură. Am o imagine mare, o rubrică și un text. Poate vrei doar o poză și nici un text!

+ Adăugați următorul cod CSS pentru caseta de lumină. Puteți să aflați ce fac unele dintre ele?

```css
    .lightbox {fundal: rgba (0,0,0,0,8); culoare: #ffffff; text-align: centru; text-decoration: nici unul; lățime: 100%; înălțime: 100%; top: 0; stânga: 0; poziție: fixă; vizibilitate: ascuns; z-index: 999; }
```

Notă: Setarea proprietății `poziția` la `fixe` înseamnă că poziția pe care o setați va fi relativă la fereastra browserului, astfel încât aceasta va rămâne pusă când derulați.

+ Apoi, decideți ce doriți să faceți pentru a crea caseta de lumină și adăugați o pereche de taguri `` jurul acelui element (în cazul meu este o imagine mai mică a unui lemur). **Ținta** din link - ul va fi lightbox, pe care ați setat folosind `id`. S-ar putea să recunoașteți această tehnică mai devreme!

```html
    <a href="#boxLemur">
        <img src="monkey-2223271_640.jpg" class="mediumPics">
    </a>
```

+ În final, adăugați următorul cod CSS. Rețineți că aceasta este o **pseudo-clasa**; ar trebui să meargă după codul pentru clasa `.lightbox` și nu înăuntru!

```css
    .lightbox: vizibilitate {vizibilitate: vizibil; }
```

Pseudo-clasa `: țintă` se aplică ori de câte ori caseta lightbox a fost ținta ultimului clic pe link. Deci , atunci când faceți clic oriunde, `vizibilitate` va fi restabilite la `ascunse`.

+ Încercați să faceți clic pe noul dvs. link pentru a vedea caseta de lumină care apare! Pentru ao face să dispară, faceți clic pe oriunde pe pagină.

Puteți adăuga cât mai multe casete luminoase pe care le doriți unei pagini. Toate acestea se pot folosi aceeași clasă CSS - doar asigurați - vă că fiecare are un alt `id`! Pentru fiecare, trebuie să faceți ceva pe pagina dvs. de Web într-un link pe care puteți face clic pentru a face să apară caseta de lumină și apoi utilizați `id` ca valoare `href` în acel link, așa cum ați făcut mai sus!