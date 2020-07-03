## क्लिक करने योग्य कार्ड

यहां एक तकनीक है जिसका उपयोग आप फोटो गैलरी या अपनी projects को दिखाने वाला एक portfolio page बनाने के लिए कर सकते हैं: little **preview cards**.

![Image thumbnail और कुछ text दिखाते हुए Preview card](images/cardsPreview.png)

+ अपनी पसंद के अनुसार, अपनी वेबसाइट में निम्न HTML कोड जोड़ें। मैं ` index.html ` पर अपना काम कर रहा हूँ | आप अपने स्वयं के पूर्वावलोकन कार्ड के अनुरूप चित्र और पाठ को बदल सकते हैं। मैं आयरलैंड में पर्यटकों के आकर्षण का एक समूह बनाने जा रहा हूँ।

```html
    <article class="card">
        <img src="monkey-2223271_640.jpg" class="tinyPicture">
        <h3>Fota Wildlife Park</h3>
        <p>Fota Island, County Cork</p>
    </article>
```

![शैलियों को लागू करने से पहले Image और text](images/cardUnstyled.png)

+ Classes बनाने के लिए निम्न CSS code जोड़ें: `card` और `tinyPicture`

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

![एक छोटे कार्ड प्रभाव बनाने के लिए स्टाइल के साथ Image और text.](images/cardStyled.png)

चलिए पूरे preview card को लिंक में बदलते हैं ताकि लोग अधिक जानकारी देखने के लिए क्लिक कर सकें।

+ पूरे `article` element को एक link element के अंदर रखें। बंद करना सुनिश्चित करें `</a>` टैग बंद होने के बाद `</article>` टैग है! लिंक ** URL** बदलने के लिए स्वतंत्र महसूस करें , जो भी आप करना चाहते हैं। यह आपकी वेबसाइट पर एक और पेज हो सकता है, या यह पूरी तरह से एक और वेबसाइट हो सकता है।

```html
    <a href="attractions.html#scFota">  
        <article class="card ">
            <img src="monkey-2223271_640.jpg" class="tinyPicture">
            <h3>Fota Wildlife Park</h3>
            <p>Fota Island, County Cork</p>
        </article>
    </a>
```

![Text और picture जिसे लिंक में बदल दिया गया है](images/cardLink.png)

## \--- collapse \---

## title: किसी पेज के विशिष्ट भाग से जोड़ना

ध्यान दें कि `href` का मान मेरे लिंक `#scFota` में कैसे समाप्त होता है ? यह एक साफ सुथरी चाल है जिसका उपयोग करके आप किसी पृष्ठ के किसी विशेष भाग में जा सकते हैं।

+ सबसे पहले, लिंक करने के लिए पेज का URL टाइप करें, उसके बाद `#` ।

+ जिस पेज को आप लिंक कर रहे हैं, उसके लिए कोड फ़ाइल में, उस भाग को ढूंढें जिसे आप कूदना चाहते हैं और उस element को आईडी दें `id` , उदाहरण के लिए, `<section id="scFota"`. `id` आईडी का मान = आपके लिंक में `#` के बाद आप क्या लिखते हैं |

\--- /collapse \---

## \--- collapse \---

## title: शैलियों को रीसेट करना

अब जबकि पूरा preview card कड़ी है, text font बदल गया हो सकता है।

+ यदि हां, तो आप इसे **CSS class** क्लास जोड़कर ठीक कर सकते हैं लिंक के लिए: `class="cardLink"`| अपनी स्टाइल शीट में डालने के लिए यहां CSS कोड दिया गया है:

```css
    .cardLink {
        color: inherit;
        text-decoration: none;
    }
```

किसी भी property का value `inherit` निर्धारित करना यह मान का उपयोग करता है कि **parent** element का value क्या है। तो इस मामले में, पाठ का रंग मुखपृष्ठ के बाकी पाठ से मेल खाएगा।

\--- /collapse \---

+ इनमें से कम से कम चार या पांच कार्ड बनाएं। यदि आप मेरी उदाहरण वेबसाइट से काम कर रहे हैं, तो आप आकर्षण पृष्ठ पर प्रत्येक अनुभाग के लिए एक कर सकते हैं। अगले सुशी कार्ड पर, आप सीखेंगे कि कार्ड को शांत चाल से कैसे व्यवस्थित किया जाए!