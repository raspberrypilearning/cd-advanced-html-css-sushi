## आपला मेनू प्रतिसाद देणारा करा

एक**responsive** वेबसाइट म्हणजे जे स्वतःला स्क्रीनच्या आकारात समायोजित करते जेणेकरून ती संगणकावर, मोबाईल फोनवर किंवा टॅब्लेटवर पहात असली तरीही ती नेहमीच छान दिसेल. चला आपल्या मेनूला प्रतिसाद देणारा करू या!

आपण नेहमीच्या शैलीसह प्रारंभ कराल: हे आपले **default** वर्तन असेल.

## \--- collapse \---

## title: 'default' म्हणजे काय?

'default' शैली आपल्या शैलीच्या नियमांचा नेहमीचा संच असतो. कोणत्याही विशेष अटी तपासण्यापूर्वी त्यांना 'default' शैली लागू केले जाते.

आपण स्क्रीनचा आकार तपासणारा आणि आवश्यक असल्यास काही समायोजित करणारा कोड जोडू शकता.

\--- /collapse \---

+ आपल्या मेनूमध्ये खालील CSS नियम जोडा. आपल्याकडे कदाचित रंग आणि किनारी देखील परिभाषित केलेली असतील; मी त्यांना येथे जागा वाचवण्यासाठी दुर्लक्षिले आहे! आपल्याकडे आपल्या मेनूसाठी आधीपासूनच CSS नियम परिभाषित असल्यास, आपण गहाळ असलेले गुणधर्म आणि मूल्ये फक्त जोडा किंवा बदला.

```css
    nav ul {
        padding: 0.5em;
        display: flex;
        flex-direction: column;
    }
    nav ul li {
        text-align: center; 
        list-style-type: none;
        margin-right: 0.5em;
        margin-left: 0.5em;
    }
```

वरील CSS कोडसह, आपला मेनू छोट्या स्क्रीनसाठी अनुकूल असेल. याला ** mobile-first ** विकास असे म्हटले जाते.

![छोट्या स्क्रीनवर मेनू आयटम एकावर एक उभे केलेले](images/responsiveMenuMobile.png)

## \--- collapse \---

## title: 'mobile-first' म्हणजे काय?

बर्‍याचदा वेबसाइट कोडींग करताना आपण संगणक स्क्रीन वापरत असाल आणि कदाचित आपली शैली त्या स्क्रीनवर कशी दिसते या आधारावर आपण आपल्या शैली निश्चित कराल.

आपण प्रथम मोबाईलसाठी कोडिंग करता तेव्हा आपण त्याऐवजी स्मार्टफोनसारख्या छोट्या स्क्रीनसाठी योग्य असलेल्या डीफॉल्ट शैलीची निवड करता. नंतर आपण मोठ्या स्क्रीनसाठी समायोजित करण्यासाठी अतिरिक्त कोड जोडता.

जास्तीत जास्त लोक संगणकाऐवजी स्मार्टफोन किंवा टॅब्लेटवर इंटरनेट ब्राउझ करीत आहेत, हे लक्षात घेऊन आपले संकेतस्थळ विकसित करणे योग्य आहे.

\--- /collapse \---

+ आता आपल्या स्टाइल शीट मध्ये पुढील कोड जोडा:

```css
    @media all and (min-width: 1000px) {
        nav ul {
            flex-direction: row;
            justify-content: space-around;
        }
    }
```

वरील कोडची पहिली ओळ ब्राउझर विंडोचा आकार तपासते. विंडो **1000 pixels** इतकी विस्तृत किंवा अधिक असल्यास, हा कोड ब्लॉकमध्ये असणारे सर्व शैली नियम लागू करेल.

![विस्तृत स्क्रीनवरील मेनू आयटम एका ओळीवर समान रीतीने अंतरावर ठेवले](images/responsiveMenuMedium.png)

## \--- collapse \---

## title: हे कसे कार्य करते?

ब्लॉकमध्ये `nav ul` मेनूच्या काही गुणधर्मांसाठी नवीन मूल्ये आहेत.

जेव्हा जेव्हा विंडो 1000 पिक्सलपेक्षा विस्तृत असेल तेव्हा`nav ul` साठी आपण आधीपासून परिभाषित केलेल्याऐवजी ही नवीन मूल्ये लागू केली जातील.

आपण यापूर्वी `nav ul` साठी परिभाषित केलेले उर्वरित गुणधर्म तसेच राहतील.

\--- /collapse \---

+ आपण कोड लिहिण्यासाठी ट्रिन्केट वापरत असल्यास, प्रकल्प डाउनलोड करणे कदाचित उपयुक्त ठरेल जेणेकरून आपण त्यास एका पूर्ण-आकाराच्या स्क्रीनवर तपासू शकता.

\--- challenge \---

## Challenge: आपला मेनू मोठ्या स्क्रीनसाठी स्वतःस समायोजित करेल असे करा

+ `flex-end` च्या ऐवजी `space-around` सह आपण **1600 pixels**पेक्षा मोठ्या स्क्रीनसाठी दुसरा ब्लॉक जोडू शकता का?

![विस्तृत स्क्रीनवर उजवीकडे मेनू आयटम](images/responsiveMenuWide.png)

\--- hints \---

\--- hint \---

जेव्हा स्क्रीन 1600 पिक्सलपेक्षा मोठी असेल तेव्हा खालील कोड मेनू आयटमसाठी फ्लेक्स गुणधर्म ठरवतो:

```css
    @media all and (min-width: 1600px) {
        nav ul {
            flex-direction: row;
            justify-content: flex-end;
        }
    }  
```

\--- /hint \---

\--- /hints \---

\--- /challenge \---

वेगवेगळ्या स्क्रीन आकारांसाठी भिन्न शैली परिभाषित करण्यासाठी आपण अश्यासारख्या ब्लॉकमध्ये कोणतेही CSS नियम घालू शकता. आपण नंतर CSS ग्रीड लेआउट करता तेव्हा हे विशेषतः उपयुक्त ठरेल!