## ಕ್ಲಿಕ್ ಮಾಡಬಹುದಾದ ಕಾರ್ಡ್‌ಗಳು

ಫೋಟೋ ಗ್ಯಾಲರಿ ಮಾಡಲು ಅಥವಾ ನಿಮ್ಮ ಪ್ರಾಜೆಕ್ಟ್‌ಗಳನ್ನು ತೋರಿಸುವ ಪೋರ್ಟ್ಫೋಲಿಯೋ ಪುಟವನ್ನು ಮಾಡಲು ನೀವು ಬಳಸಬಹುದಾದ ತಂತ್ರ ಇಲ್ಲಿದೆ: ಸ್ವಲ್ಪ **preview cards**.

![Preview card showing an image thumbnail and some text](images/cardsPreview.png)

+ ನಿಮ್ಮ ವೆಬ್‌ಸೈಟ್‌ಗೆ ಈ ಕೆಳಗಿನ HTML ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಿ, ನೀವು ಎಲ್ಲಿ ಬೇಕಾದರೂ. ನಾನು `index.html` ನಲ್ಲಿ ಗಣಿ ಮಾಡುತ್ತಿದ್ದೇನೆ. ನಿಮ್ಮ ಸ್ವಂತ ಪೂರ್ವವೀಕ್ಷಣೆ ಕಾರ್ಡ್‌ಗಳಿಗೆ ತಕ್ಕಂತೆ ನೀವು ಚಿತ್ರ ಮತ್ತು ಪಠ್ಯವನ್ನು ಬದಲಾಯಿಸಬಹುದು. ನಾನು ಐರ್ಲೆಂಡ್‌ನ ಪ್ರವಾಸಿ ಆಕರ್ಷಣೆಗಳ ಮುಖ್ಯಾಂಶಗಳನ್ನು ಮಾಡಲಿದ್ದೇನೆ.

```html
    <article class="card">
        <img src="monkey-2223271_640.jpg" class="tinyPicture">
        <h3>Fota Wildlife Park</h3>
        <p>Fota Island, County Cork</p>
    </article>
```

![Image and text before styles are applied](images/cardUnstyled.png)

+ ತರಗತಿಗಳು `card` ರಚಿಸಲು ಕೆಳಗಿನ CSS ಕೋಡ್ ಸೇರಿಸಿ ಮತ್ತು `tinyPicture`:

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

ಇಡೀ ಪೂರ್ವವೀಕ್ಷಣೆ ಕಾರ್ಡ್ ಅನ್ನು ಲಿಂಕ್ ಆಗಿ ಪರಿವರ್ತಿಸೋಣ ಆದ್ದರಿಂದ ಜನರು ಹೆಚ್ಚಿನ ಮಾಹಿತಿಯನ್ನು ನೋಡಲು ಕ್ಲಿಕ್ ಮಾಡಬಹುದು.

+ ಸಂಪೂರ್ಣ `article` ಇರಿಸಿ ಲಿಂಕ್ ಅಂಶದೊಳಗಿನ ಅಂಶ. ಮುಚ್ಚುವಿಕೆಯನ್ನು ಖಚಿತಪಡಿಸಿಕೊಳ್ಳಿ `</a>` ಟ್ಯಾಗ್ ಮುಚ್ಚಿದ ನಂತರ `</article>` ಟ್ಯಾಗ್! **URL** ಲಿಂಕ್ ಅನ್ನು ಬದಲಾಯಿಸಲು ಹಿಂಜರಿಯಬೇಡಿ ನೀವು ಲಿಂಕ್ ಮಾಡಲು ಬಯಸುವ ಯಾವುದಕ್ಕೂ. ಅದು ನಿಮ್ಮ ವೆಬ್‌ಸೈಟ್‌ನಲ್ಲಿ ಮತ್ತೊಂದು ಪುಟವಾಗಬಹುದು ಅಥವಾ ಅದು ಸಂಪೂರ್ಣವಾಗಿ ಮತ್ತೊಂದು ವೆಬ್‌ಸೈಟ್ ಆಗಿರಬಹುದು.

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

--- collapse ---
---
title: ಪುಟದ ನಿರ್ದಿಷ್ಟ ಭಾಗಕ್ಕೆ ಲಿಂಕ್ ಮಾಡಲಾಗುತ್ತಿದೆ
---

`href`ನ ಮೌಲ್ಯ ಹೇಗೆ ಎಂಬುದನ್ನು ಗಮನಿಸಿ ನನ್ನ ಲಿಂಕ್‌ನಲ್ಲಿ `#scFota` ನಲ್ಲಿ ಕೊನೆಗೊಳ್ಳುತ್ತದೆ? ಇದು ಪುಟದ ನಿರ್ದಿಷ್ಟ ಭಾಗಕ್ಕೆ ಹೋಗಲು ನೀವು ಬಳಸಬಹುದಾದ ಅಚ್ಚುಕಟ್ಟಾಗಿ ಟ್ರಿಕ್ ಆಗಿದೆ.

+ ಮೊದಲಿಗೆ, ಲಿಂಕ್ ಮಾಡಲು ಪುಟದ URL ಅನ್ನು ಟೈಪ್ ಮಾಡಿ, ನಂತರ `#`.

+ ನೀವು ಲಿಂಕ್ ಮಾಡುತ್ತಿರುವ ಪುಟದ ಕೋಡ್ ಫೈಲ್‌ನಲ್ಲಿ, ನೀವು ಹೋಗಲು ಬಯಸುವ ಭಾಗವನ್ನು ಹುಡುಕಿ ಮತ್ತು ಆ ಅಂಶಕ್ಕೆ `id`ನೀಡಿ, ಉದಾಹರಣೆಗೆ, `<section id="scFota"`. `id` ಯ ಮೌಲ್ಯ `#` ನಂತರ ನೀವು ಟೈಪ್ ಮಾಡುವುದು ನಿಮ್ಮ ಲಿಂಕ್‌ನಲ್ಲಿ.

--- /collapse ---

--- collapse ---
---
title: ಶೈಲಿಗಳನ್ನು ಮರುಹೊಂದಿಸಲಾಗುತ್ತಿದೆ
---

ಈಗ ಇಡೀ ಪೂರ್ವವೀಕ್ಷಣೆ ಕಾರ್ಡ್ ಲಿಂಕ್ ಆಗಿರುವುದರಿಂದ, ಪಠ್ಯ ಫಾಂಟ್ ಬದಲಾಗಿರಬಹುದು.

+ ಹಾಗಿದ್ದಲ್ಲಿ, ನೀವು **CSS class** ವನ್ನು ಸೇರಿಸುವ ಮೂಲಕ ಅದನ್ನು ಸರಿಪಡಿಸಬಹುದು ಲಿಂಕ್‌ಗೆ: `class="cardLink"`. ನಿಮ್ಮ style sheet‌ನಲ್ಲಿ ಹಾಕಲು CSS ಕೋಡ್ ಇಲ್ಲಿದೆ:

```css
    .cardLink {
        color: inherit;
        text-decoration: none;
    }
```

ಯಾವುದೇ ಆಸ್ತಿಯ ಮೌಲ್ಯವನ್ನು `inherit` ಹೊಂದಿಸುವುದು **parent** ಮೌಲ್ಯವನ್ನು ಬಳಸುವಂತೆ ಮಾಡುತ್ತದೆ ಅಂಶ ಹೊಂದಿದೆ. ಆದ್ದರಿಂದ ಈ ಸಂದರ್ಭದಲ್ಲಿ, ಪಠ್ಯದ ಬಣ್ಣವು ಮುಖಪುಟದಲ್ಲಿನ ಉಳಿದ ಪಠ್ಯಕ್ಕೆ ಹೊಂದಿಕೆಯಾಗುತ್ತದೆ.

--- /collapse ---

+ ಈ ಕಾರ್ಡ್‌ಗಳಲ್ಲಿ ಕನಿಷ್ಠ ನಾಲ್ಕು ಅಥವಾ ಐದು ಕಾರ್ಡ್‌ಗಳನ್ನು ಮಾಡಿ. ನೀವು ನನ್ನ ಉದಾಹರಣೆ ವೆಬ್‌ಸೈಟ್‌ನಿಂದ ಕೆಲಸ ಮಾಡುತ್ತಿದ್ದರೆ, ಆಕರ್ಷಣೆಗಳ ಪುಟದಲ್ಲಿನ ಪ್ರತಿಯೊಂದು ವಿಭಾಗಗಳಿಗೆ ನೀವು ಒಂದನ್ನು ಮಾಡಬಹುದು. ಮುಂದಿನ ಸುಶಿ ಕಾರ್ಡ್‌ನಲ್ಲಿ, ಕಾರ್ಡ್‌ಗಳನ್ನು ತಂಪಾದ ಟ್ರಿಕ್‌ನೊಂದಿಗೆ ಹೇಗೆ ಜೋಡಿಸುವುದು ಎಂದು ನೀವು ಕಲಿಯುವಿರಿ!