## छायाचित्रांचा कोलाज

या कार्डवर आपण HTML घटकांना अचूक स्थितीत ठेवण्यासाठी आणि फोटो कोलाज बनविण्यासाठी CSS वापरण्यास शिकाल.

![](images/photoCollageWithText_wide.png)

+ एक `div` आपल्या पृष्ठावर जोडा आणि आपल्याला पाहिजे तितक्या प्रतिमा त्यात टाका. `div` आणि `img` या घटकांना `id` मूल्ये द्या.

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

आपल्या कोडमध्ये फोटो ज्या क्रमाने आहेत त्याच क्रमाने एकापाठोपाठ एक असे वेबपृष्ठावर दिसतील.

+ आपल्या CSS फाइलमध्ये, खालील CSS वर्ग `div` मधील घटकांसाठी जोडा: 

```css
    .absPos {
        position: absolute;
    }
```

+ पुढे, आपल्याला कंटेनर आणि त्याचा आकार ठरवण्यासाठी `position: relative;` ही प्रोपर्टी जोडण्याची आवश्यकता आहे. यामुळे इतर घटकांची पोझिशन कंटेनरच्या तुलनेत **relative to** (म्हणजेच, आत) ठरवली जाते.

```css
    .relPos {
        position: relative;
    }

    #photoBox {
        width: 800px;
        height: 400px;
    }
```

+ त्या नंतर प्रत्येक घटकाचा आकार सेट करण्यासाठी (`width` and/or `height` properties) तसेच त्यांची अचूक स्थिती ठरवण्यासाठी **id selectors** वापर करून शैली नियमांचा एक संच तयार करा.

घटकांची स्थिती ठरवण्यासाठी, आपण चार गुणधर्म वापरू शकता: `left`, `right`, `top`, and `bottom`. ते पेरेंटच्या काठावरुन प्रत्येक कड किती लांब असावी हे दर्शवितात. उभ्या स्थितीसाठी एकतर `top` किंवा `bottom` वापरा, आणि आडव्या स्थितीसाठी `left` किंवा `right` वापरा.

![Top, left, bottom आणि right गुणधर्म त्यांच्या मूळ कंटेनरशी कसे संबंधित आहेत हे दर्शविणारे रेखाचित्र](images/cssPositionProperties.png)

+ आपल्या प्रत्येक चित्रासाठी अचूक स्थिती निवडा आणि आपल्या CSS नियमांमध्ये त्या स्थानांची व्याख्या करण्यासाठी `left`, `right`, `top`, आणि `bottom` यापैकी कोणत्याही गुणधर्मांचा वापर करा. उदाहरणार्थ, या कोडमध्ये मांजरीचे चित्र शीर्षस्थानी 100 पिक्सेल आणि डावीकडून 60 पिक्सेलअसे ठेवले जाईल:

```css
    #imgTeaCat {
        width: 250px;
        top: 100px;
        left: 60px;
    }
```

टीपः स्थान मूल्ये नकारात्मक (negative) देखील असू शकतात! आपण नेगेटीव्ह मूल्य वापरल्यास ते आपण निर्दिष्ट केलेल्या कोणत्याही काठावर कंटेनरच्या बाहेरच्या भागाला ढकलले जाईल.

### गोष्टी आच्छादित करणे

आपल्याला कदाचित काही चित्रे आच्छादित करू इच्छित असाल. परंतु कुठले चित्र सर्वात वर दिसावे हे आपण कसे निवडाल?

+ दोन images निवडा आणि त्यांना अशी स्थिती द्या की ज्यामुळे ते आच्छादित (एकावर एक) होऊ शकतात.

+ त्यापैकी एकाला `z-index: 10;`अतिरिक्त गुणधर्म जोडा,, आणि नंतर दुसर्‍याला `z-index: 7;` जोडा.

+ आता आपल्या वेबपृष्ठा वरती याचा परिणाम पहा.

![](images/horse10Cat7.png)

+ आता `z-index` मूल्यांची अदलाबदली करा, जेणेकरून `7` आणि `10` हे उलट पद्धतीने दिसतील. आपल्या वेबपृष्ठावर काही फरक दिसतो आहे का?

![](images/horse7Cat10.png)

## \--- collapse \---

## title: z-index कसे काम करतो?

दोन किंवा अधिक घटक कसे आच्छादित करावे हे `z-index` गुणधर्म आपल्याला ठरवू देते. हे मूल्य म्हणजे कोणतीही पूर्ण संख्या असू शकते.

**highest** संख्या **top** स्थानी असेल किंवा दुसर्‍या शब्दात सांगायचे तर अगदी **front**ला असेल. सर्वात जास्त संख्येसह असणारा घटक सर्वात पुढे आणि त्या मागे कमी संख्या असणारे घटक असे होत अगदी सर्वात कमी संख्या असणारा घटक इतर सर्व घटकांच्या पार्श्वभूमीवर असेल.

\--- /collapse \---

अशा प्रकारे, आपण केवळ images च नव्हे तर कोणत्याही HTML घटकांना स्थान देऊ शकता. उदाहरणार्थ, फोटोवर काही मजकूर जोडण्यासाठी आपण `p` घटक वापरू शकता.

\--- challenge \---

## Challenge: फोटो कोलाज बनवा

+ खाली दर्शविलेल्या फोटोसारखे आपले स्वत: चे फोटोंचे कोलाज तयार करण्याचा प्रयत्न करा! आपल्याला अगदी हवा तसा आच्छादित परिणाम मिळविण्यासाठी भिन्न `z-index` मूल्ये वापरा.

\--- hints \---

\--- hint \---

माझ्या आयर्लँड वेबसाइटवर फोटो कोलाजसाठी HTML code खालील प्रमाणे आहे. `div` मध्ये सहा images आणि मजकूर आहे.

```html
    <div id="photoBox" class="relPos">
        <img id="imgStreet" class="collagePhoto absPos" src="ireland-1474045_640.jpg" alt="Irish town" />
        <img id="imgTeaCat" class="collagePhoto absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
        <img id="imgCoast" class="collagePhoto absPos" src="cattle-2369463_640.jpg" alt="Cows at the coast" />
        <img id="imgTrees" class="collagePhoto absPos" src="ireland-2614852_640.jpg" alt="Tree tunnel" />
        <img id="imgSheep" class="collagePhoto absPos" src="sheep-456989_640.jpg" alt="Sheep on the road" />
        <img id="imgHorse" class="collagePhoto absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <p id="photoText" class="absPos">Ireland</p>
    </div>
```

\--- /hint \---

\--- hint \---

कोलाजमधील माझ्या प्रत्येक चित्रासाठी पोझिशन्स सेट करतात असे CSS नियम येथे आहेत:

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

येथे मी वापरलेले CSS वर्ग आहेतः:

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

![शीर्षस्थानी मजकूरासह फोटो कोलाज](images/photoCollageExample.png)

\--- /challenge \---