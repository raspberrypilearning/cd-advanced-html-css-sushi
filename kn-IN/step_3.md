## Clickable cards

Here's a technique you could use to make a photo gallery, or a portfolio page showing off your projects: little **preview cards**.

![Preview card showing an image thumbnail and some text](images/cardsPreview.png)

+ Add the following HTML code to your website, anywhere you like. I'm doing mine on `index.html`. You can change the picture and text to suit your own preview cards. I'm going to do a bunch of highlights of the tourist attractions in Ireland.

```html
    <article class="card">
        <img src="monkey-2223271_640.jpg" class="tinyPicture">
        <h3>Fota Wildlife Park</h3>
        <p>Fota Island, County Cork</p>
    </article>
```

![Image and text before styles are applied](images/cardUnstyled.png)

+ Add the following CSS code to create the classes `card` and `tinyPicture`:

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

![Image and text with styling to create a small card effect](images/cardStyled.png)

Let's turn the whole preview card into a link so people can click to see more information.

+ Place the whole `article` element inside a link element. Make sure the closing `</a>` tag is after the closing `</article>` tag! Feel free to change the link **URL** to whatever you want to link to. That could be another page on your website, or it could be another website entirely.

```html
    <a href="attractions.html#scFota">  
        <article class="card ">
            <img src="monkey-2223271_640.jpg" class="tinyPicture">
            <h3>Fota Wildlife Park</h3>
            <p>Fota Island, County Cork</p>
        </article>
    </a>
```

![Text and picture that has been turned into a link](images/cardLink.png)

## \--- collapse \---

## title: Linking to a specific part of a page

`href`ನ ಮೌಲ್ಯ ಹೇಗೆ ಎಂಬುದನ್ನು ಗಮನಿಸಿ ನನ್ನ ಲಿಂಕ್‌ನಲ್ಲಿ `#scFota` ನಲ್ಲಿ ಕೊನೆಗೊಳ್ಳುತ್ತದೆ? ಇದು ಪುಟದ ನಿರ್ದಿಷ್ಟ ಭಾಗಕ್ಕೆ ಹೋಗಲು ನೀವು ಬಳಸಬಹುದಾದ ಅಚ್ಚುಕಟ್ಟಾಗಿ ಟ್ರಿಕ್ ಆಗಿದೆ.

+ ಮೊದಲಿಗೆ, ಲಿಂಕ್ ಮಾಡಲು ಪುಟದ URL ಅನ್ನು ಟೈಪ್ ಮಾಡಿ, ನಂತರ `#`.

+ ನೀವು ಲಿಂಕ್ ಮಾಡುತ್ತಿರುವ ಪುಟದ ಕೋಡ್ ಫೈಲ್‌ನಲ್ಲಿ, ನೀವು ಹೋಗಲು ಬಯಸುವ ಭಾಗವನ್ನು ಹುಡುಕಿ ಮತ್ತು ಆ ಅಂಶಕ್ಕೆ `id`ನೀಡಿ, ಉದಾಹರಣೆಗೆ, `<section id="scFota"`. `id`ಯ ಮೌಲ್ಯ `#`ನಂತರ ನೀವು ಟೈಪ್ ಮಾಡುವುದು ನಿಮ್ಮ ಲಿಂಕ್‌ನಲ್ಲಿ.

\--- /collapse \---

## \--- collapse \---

## title: ಶೈಲಿಗಳನ್ನು ಮರುಹೊಂದಿಸಲಾಗುತ್ತಿದೆ

ಈಗ ಇಡೀ ಪೂರ್ವವೀಕ್ಷಣೆ ಕಾರ್ಡ್ ಲಿಂಕ್ ಆಗಿರುವುದರಿಂದ, ಪಠ್ಯ ಫಾಂಟ್ ಬದಲಾಗಿರಬಹುದು.

+ ಹಾಗಿದ್ದಲ್ಲಿ, ನೀವು **CSS class** ವನ್ನು ಸೇರಿಸುವ ಮೂಲಕ ಅದನ್ನು ಸರಿಪಡಿಸಬಹುದು ಲಿಂಕ್‌ಗೆ: `class="cardLink"`. ನಿಮ್ಮ style sheet‌ನಲ್ಲಿ ಹಾಕಲು CSS ಕೋಡ್ ಇಲ್ಲಿದೆ:

```css
    .cardLink {
        color: inherit;
        text-decoration: none;
    }
```

ಯಾವುದೇ ಆಸ್ತಿಯ ಮೌಲ್ಯವನ್ನು `inherit`ಹೊಂದಿಸುವುದು **parent** ಮೌಲ್ಯವನ್ನು ಬಳಸುವಂತೆ ಮಾಡುತ್ತದೆ ಅಂಶ ಹೊಂದಿದೆ. ಆದ್ದರಿಂದ ಈ ಸಂದರ್ಭದಲ್ಲಿ, ಪಠ್ಯದ ಬಣ್ಣವು ಮುಖಪುಟದಲ್ಲಿನ ಉಳಿದ ಪಠ್ಯಕ್ಕೆ ಹೊಂದಿಕೆಯಾಗುತ್ತದೆ.

\--- /collapse \---

+ ಈ ಕಾರ್ಡ್‌ಗಳಲ್ಲಿ ಕನಿಷ್ಠ ನಾಲ್ಕು ಅಥವಾ ಐದು ಕಾರ್ಡ್‌ಗಳನ್ನು ಮಾಡಿ. ನೀವು ನನ್ನ ಉದಾಹರಣೆ ವೆಬ್‌ಸೈಟ್‌ನಿಂದ ಕೆಲಸ ಮಾಡುತ್ತಿದ್ದರೆ, ಆಕರ್ಷಣೆಗಳ ಪುಟದಲ್ಲಿನ ಪ್ರತಿಯೊಂದು ವಿಭಾಗಗಳಿಗೆ ನೀವು ಒಂದನ್ನು ಮಾಡಬಹುದು. ಮುಂದಿನ ಸುಶಿ ಕಾರ್ಡ್‌ನಲ್ಲಿ, ಕಾರ್ಡ್‌ಗಳನ್ನು ತಂಪಾದ ಟ್ರಿಕ್‌ನೊಂದಿಗೆ ಹೇಗೆ ಜೋಡಿಸುವುದು ಎಂದು ನೀವು ಕಲಿಯುವಿರಿ!