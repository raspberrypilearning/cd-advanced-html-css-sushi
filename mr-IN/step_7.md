## छान पृष्ठ (पेज) लेआउट डिझाइन करा

+ या कार्डासाठी आपण अश्या पृष्ठावर काम केले पाहिजे ज्यात एक `article` आणि दोन `aside` अश्या तीन घटकांसह `main` घटक आहे. पुढे जा आणि आपल्याला आवश्यक असल्यास हे आधी तयार करा. आपण माझ्या वेबसाइटवर काम करू इच्छित असल्यास, मागील सुशी कार्डवरून `aside` कोड आकर्षण पृष्ठावर जोडा. 

येथे आपण तीन भिन्न पृष्ठ लेआउट्स लागू करत आहातः:

![](images/cssGridLayouts.png)

+ `main` वर नवीन CSS वर्ग जोडा आणि त्यातील प्रत्येकात तीनही घटक.

```html
    <main class="attPageLayoutGrid">
        <article class="attGridArticle">
            <!--other stuff here-->
        </article>
        <aside class="attGridAside1">
            <!--other stuff here-->
        </aside>
        <aside class="attGridAside2">
            <!--other stuff here-->
        </aside>
    </main>
```

ज्या कंटेनरचे लेआउटआपण बदलत आहात ते `main` आहे, परंतु आपण हे `div` किंवा `article` कोणत्याही प्रकारच्या कंटेनरबाबत किंवा अगदी संपूर्ण पान `body` च्या बाबतसुद्धा करू शकता. आपण वापरत असलेल्या टेकनीकला **CSS grid** असे म्हणतात.

या उदाहरणात, `header` आणि `footer` डिझाइनमधून वगळले जाईल परंतु त्यांना ग्रीडमध्ये समाविष्ट करणे अगदी नेहमीचे आहे.

+ एकूणच कंटेनर वर `grid` साठी `display` ही प्रॉपर्टी सेट करा:

```css
    .attPageLayoutGrid {
        display: grid;
        grid-column-gap: 0.5em;
        grid-row-gap: 1em;
    }
```

`grid-column-gap` and `grid-row-gap` गुणधर्म काय करतात असे आपणास वाटते?

+ पुढे, आपण प्रत्येक घटकासाठी `grid-area` नाव द्या: 

```css
    .attGridArticle {
        grid-area: agArticle;
    }
    .attGridAside1 {
        grid-area: agAside1;
    }
    .attGridAside2 {
        grid-area: agAside2;
    }
```

मग आपण आपले लेआउट डिझाइन करा! चला पृष्ठाच्या तळाशी दोन `aside` घटक आजूबाजूला ठेवू या. यासाठी आपल्याला दोन समान रुंदीचे **columns** आवश्यक आहेत. आपण **row** चीउंची स्वयंचलित ठेवू शकता.

+ `.attPageLayoutGrid`CSS नियम मध्ये खालील कोड ठेवा:

```css
    grid-template-rows: auto;
    grid-template-columns: 1fr 1fr;
    grid-template-areas: 
        "agArticle agArticle"
        "agAside1 agAside2";
```

`fr` म्हणजे **fraction**. आपण दोन स्तंभांवरील सर्व जागा घेणारा `article` कसा बनवाल ते पहा </0>.

## \--- collapse \---

## title: मदत! मला चुका आणि चेतावणी मिळाली!

आपण वरील कोड अगदी अचूक टाइप केले तरीही आपण ट्रिंकेट वापरत असल्यास, आपल्यास काही त्रुटी आणि चेतावण्या दिसतील. याचे कारण असे की ट्रिंकेट अद्याप CSS ग्रीड गुणधर्म ओळखत नाही. तथापि, कोड तरीही कार्य करेल.

जर सीएसएस ग्रीड कोड आपल्याला ''unknown property ' चेतावणी किंवा ''unexpected token 1fr' सारखी चूक दाखवत असेल तर आपण त्याकडे दुर्लक्ष करू शकता.

\--- /collapse \---

![Asides तळाशी शेजारी शेजारी आहेत](images/cssGridAsidesAtBottom.png)

चला आपण `aside` घटक उजव्या बाजूला ठेवूया आणि त्यांना `article`च्या अर्ध्या रूंदीचे बनवू या.

+ `grid-template-columns` आणि `grid-template-areas`-स्तंभांची मूल्ये अशी बदला:

```css
    grid-template-columns: 2fr 1fr;
    grid-template-areas: 
        "agArticle agAside1"
        "agArticle agAside2";
```

![Asides उजव्या बाजूला खाली आहेत](images/cssGridAsidesOnRight.png)

+ आपणास `aside`घटक तळापर्यंत पसरेल असा नको असल्यास आपण बिन्दु वापरुन रिक्त जागा जोडू शकता: 

```css
    grid-template-areas: 
        "agArticle agAside1"
        "agArticle agAside2"
        "agArticle . ";
```

![Asides उजवीकडे आणि खाली ताणले गेलेले नाहीत](images/cssGridAsidesTopRight.png)

\--- challenge \---

## आव्हान: भिन्न स्क्रीन आकारांसाठी भिन्न लेआउट बनवा

+ स्क्रीन किती रुंद आहे यावर अवलंबून आपण लेआउट बदलण्यासाठी आधी जोडलेल्या स्क्रीन आकार तपासणीचा वापर करू शकता? टीप: प्रत्येक स्क्रीन आकारासाठी आधीपासून CSS ब्लॉक तयार केलेले असल्यास आपण नवीन ब्लॉक बनवण्याऐवजी त्याच ब्लॉकमध्ये नवीन CSS कोड जोडू शकता.

\--- hints \---

\--- hint \---

जेव्हा स्क्रीन 1000 पिक्सलपेक्षा मोठी असेल तेव्हा खालील कोड वरील CSS वर्गासाठी एक लेआउट परिभाषित करते:

```css
    @media all and (min-width: 1000px) {
        .attPageLayoutGrid {
            grid-template-columns: 1fr 1fr;
            grid-template-areas: 
                "agArticle agArticle"
                "agAside1 agAside2";
        }
    }  
```

\--- /hint \---

\--- hint \---

जेव्हा स्क्रीन 1600 पिक्सलपेक्षा मोठी असेल तेव्हा खालील कोड वरील सीएसएस वर्गासाठी एक लेआउट परिभाषित करते:

```css
    @media all and (min-width: 1600px) {
        .attPageLayoutGrid {
            grid-template-columns: 1fr 1fr;
            grid-template-areas: 
                "agArticle agAside1"
                "agArticle agAside2"
                "agArticle .";
        }
    }  
```

\--- /hint \---

\--- /hints \---

\--- /challenge \---

**CSS grid** वापरुन, आपण आपल्यास आवडत असलेले जवळजवळ कोणतेही लेआउट बनवू शकता. आपण अधिक जाणून घेऊ इच्छित असल्यास [dojo.soy/html3-css-grid](http://dojo.soy/html3-css-grid){:target="_blank"} वर जा