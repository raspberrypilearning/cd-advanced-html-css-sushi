## ಶೀರ್ಷಿಕೆಗಳು ಮತ್ತು ಅಡ್ಡ ಟಿಪ್ಪಣಿಗಳು

ಈ ಕಾರ್ಡ್‌ನಲ್ಲಿ ನೀವು ಇನ್ನೂ ಎರಡು ಬಗೆಯ **container** ಬಗ್ಗೆ ಕಲಿಯುವಿರಿ ಅಂಶ: ಚಿತ್ರಕ್ಕೆ ಶೀರ್ಷಿಕೆ (ಶೀರ್ಷಿಕೆ ಅಥವಾ ಸಣ್ಣ ವಿವರಣೆಯಂತಹ ಕೆಲವು ಪಠ್ಯ) ಸೇರಿಸಲು ನೀವು ಬಳಸಬಹುದಾದ ಒಂದು, ಮತ್ತು ಇನ್ನೊಂದು ಹೆಚ್ಚುವರಿ ವಿಷಯವನ್ನು ನೀವು ಹೊಂದಿರುವಾಗ ಅದು ಪುಟದಲ್ಲಿನ ಮುಖ್ಯ ಮಾಹಿತಿಯೊಂದಿಗೆ ನಿಜವಾಗಿಯೂ ಸೇರುವುದಿಲ್ಲ.

### ಶೀರ್ಷಿಕೆಗಳೊಂದಿಗೆ ಚಿತ್ರಗಳು

+ Find an `img` element where you have text above or below that goes with the picture. ನಾನು ಟಿಟೊ ಚಿತ್ರದೊಂದಿಗೆ `index.html`ನಲ್ಲಿ ಕೆಲಸ ಮಾಡುತ್ತಿದ್ದೇನೆ, ಆದರೆ ನಿಮ್ಮ ವೆಬ್‌ಸೈಟ್‌ನಲ್ಲಿರುವ ಯಾವುದನ್ನಾದರೂ ನೀವು ಹೋಗಬಹುದು. 

```html
  <img id="titoPicture" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />          
  <p>
    Tour guide Tito!
  </p>
```

+ ಕೋಡ್ ಮೇಲಿನ ಸಾಲಿನಲ್ಲಿ, ಆರಂಭಿಕ ಟ್ಯಾಗ್ `<figure>` ಅನ್ನು ಸೇರಿಸಿ. ಕೋಡ್ ಮೇಲಿನ ಸಾಲಿನಲ್ಲಿ, ಆರಂಭಿಕ ಟ್ಯಾಗ್ `</figure>` ಅನ್ನು ಸೇರಿಸಿ.

+ ಮುಂದೆ, `p` ಟ್ಯಾಗ್‌ಗಳನ್ನು ತೆಗೆದುಹಾಕಿ, ಅಥವಾ ಪಠ್ಯದ ಸುತ್ತಲೂ ನೀವು ಹೊಂದಿರುವ ಯಾವುದೇ ಟ್ಯಾಗ್‌ಗಳನ್ನು ತೆಗೆದುಹಾಕಿ (ಬಹುಶಃ ಇದು `h2`ನಂತಹ ಶೀರ್ಷಿಕೆಯಾಗಿದೆ?), ಮತ್ತು ಪಠ್ಯವನ್ನು `<figcaption> </figcaption>` ಬದಲಿಗೆ ಟ್ಯಾಗ್‌ಗಳು. ಇಡೀ ವಿಷಯವು ಈ ರೀತಿ ಕಾಣಬೇಕು:

```html
  <figure>
      <img id="titoPicture" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />          
      <figcaption>
      Tour guide Tito!
      </figcaption>
  </figure>
```

`figcaption` ಅಂಶವು ನಿಮ್ಮ **caption**. It can go either above the `img` element or below it.

![Picture of Tito with a caption](images/figureAndCaption.png)

## \--- collapse \---

## title: ಇದು ಏಕೆ ಉಪಯುಕ್ತವಾಗಿದೆ?

`figure` ಅಂಶವು ಒಂದು ರೀತಿಯ **container** ಕಾರ್ಯನಿರ್ವಹಿಸುತ್ತದೆ ನಿಮ್ಮ ಚಿತ್ರ ಮತ್ತು ಅದರ ಶೀರ್ಷಿಕೆಗಾಗಿ. ಶೈಲಿಗಳನ್ನು ವ್ಯಾಖ್ಯಾನಿಸುವಾಗ ಅವುಗಳನ್ನು ಒಂದು ಘಟಕವಾಗಿ ಪರಿಗಣಿಸಲು ಇದು ನಿಮ್ಮನ್ನು ಅನುಮತಿಸುತ್ತದೆ.

ತಾರ್ಕಿಕವಾಗಿ ಅವುಗಳನ್ನು ಒಟ್ಟಿಗೆ ಗುಂಪು ಮಾಡುವುದು ನಿಮ್ಮ ವೆಬ್‌ಸೈಟ್ ಕೋಡ್‌ನಲ್ಲಿ ಉತ್ತಮ ರಚನೆಯನ್ನು ಕಾಪಾಡಿಕೊಳ್ಳಲು ಸಹಾಯ ಮಾಡುತ್ತದೆ.

\--- /collapse \---

ನೀವು ಸಿಎಸ್ಎಸ್ ಕೋಡ್ ಅನ್ನು ಸ್ಟೈಲ್ `figure`ಗೆ ಬಳಸಬಹುದು ಮತ್ತು `figcaption` ನೀವು ತರಗತಿಗಳು, IDಗಳು ಅಥವಾ ಎಲಿಮೆಂಟ್ ಸೆಲೆಕ್ಟರ್‌ಗಳನ್ನು ಬಳಸುವ ಯಾವುದೇ ಅಂಶದಂತೆ. ಹೊಸ ಪಾತ್ರೆಯಿಂದ ಸೇರಿಸಲಾದ ಹೆಚ್ಚುವರಿ ಅಂತರವನ್ನು ತೆಗೆದುಹಾಕಲು ನಾನು ಈ ಕೆಳಗಿನ ನಿಯಮಗಳನ್ನು ಸೇರಿಸುತ್ತಿದ್ದೇನೆ:

```css
  figure { 
      margin-top: 0px;
      margin-bottom: 0px;
      margin-left: 0px;
      margin-right: 0px;
  }
```

### ಅಡ್ಡ ಟಿಪ್ಪಣಿಗಳು

ನನ್ನ ವೆಬ್‌ಸೈಟ್‌ನಲ್ಲಿನ ಆಕರ್ಷಣೆಗಳ ಪುಟವು ಭೇಟಿ ನೀಡಬೇಕಾದ ಸ್ಥಳಗಳ ಪಟ್ಟಿಯಾಗಿದೆ. ಹವಾಮಾನದ ಬಗ್ಗೆ ಕೆಲವು ಟಿಪ್ಪಣಿಗಳನ್ನು ಸೇರಿಸಲು ನಾನು ಬಯಸುತ್ತೇನೆ. ಆ ಮಾಹಿತಿಯು ನಿಜವಾಗಿಯೂ `article` ಸೇರಿಲ್ಲಎಲ್ಲಾ ಆಕರ್ಷಣೆಗಳೊಂದಿಗೆ ಅಂಶ. ನೀವು ಯಾವಾಗ ಅನ್ನು `aside` ಬಳಸಬಹುದು ಎಂಬುದಕ್ಕೆ ಇದು ಒಂದು ಉದಾಹರಣೆಯಾಗಿದೆ ಅಂಶ.

+ `article` ಹೊಂದಿರುವ ನಿಮ್ಮ ವೆಬ್‌ಸೈಟ್‌ನ ಪುಟಕ್ಕೆ ಹೋಗಿ ಅದರ ಮೇಲಿನ ಅಂಶ — ನಾನು `attractions.html` ಅನ್ನು ಬಳಸುತ್ತಿದ್ದೇನೆ.

+ **Outside** `article` ಅಂಶದ, ಒಂದು ಅಥವಾ ಹೆಚ್ಚಿನ ಜೋಡಿಗಳನ್ನು `<aside> </aside>` ನಿಮ್ಮ ಹೆಚ್ಚುವರಿ ವಿಷಯವನ್ನು ಹೊಂದಿರುವ ಟ್ಯಾಗ್‌ಗಳು.

```html
  <aside class="sideNoteStyle">
      <h2>Getting around</h2>
      <h3>Train and bus</h3>
      <p>You can get to most of the major towns by train from Dublin. There are many buses that do tours to popular locations and tourist attractions.</p>
      <h3>Car</h3>
      <p>The easiest way to get around outside of the cities is by car.</p>
    </aside>
    <aside class="sideNoteStyle">
      <h2>Weather</h2>
      <p>The weather in Ireland is <span class="specialText">very unpredictable!</span> It's best to <span class="specialText">be prepared</span> for any kind of weather, even if it's a nice day!</p>
  </aside>
```

## \--- collapse \---

## title: ಇದು ಏಕೆ ಉಪಯುಕ್ತವಾಗಿದೆ?

`aside`, `article`, ಮತ್ತು ಇತರ ಪಾತ್ರೆಗಳು ಎಲ್ಲಾ ಹೋಲುತ್ತವೆ. ನಿಜವಾದ ವ್ಯತ್ಯಾಸವೆಂದರೆ **meaning**, ಅಂದರೆ, ನೀವು ಅವುಗಳನ್ನು ಏನು ಬಳಸುತ್ತೀರಿ.

ನಿಮಗೆ ಸಾಧ್ಯವಾದಾಗಲೆಲ್ಲಾ ಅರ್ಥಪೂರ್ಣ HTML ಅಂಶಗಳನ್ನು ಬಳಸುವುದು ಮುಖ್ಯ. ಇದು ನಿಮ್ಮ ವೆಬ್‌ಸೈಟ್‌ಗೆ ಉತ್ತಮ ರಚನೆಯನ್ನು ನೀಡುತ್ತದೆ ಮತ್ತು **screen readers** ಬಳಸುವ ಜನರಿಗೆ ವಿಶೇಷವಾಗಿ ಸಹಾಯಕವಾಗುತ್ತದೆ.

\--- /collapse \---

ನೀವು ಅಲ್ಲಿ ಇತರ ಅಂಶವನ್ನು ಗುರುತಿಸಿದ್ದೀರಾ, `span`? ಹೆಚ್ಚುವರಿ CSS ಕೋಡ್ ಸೇರಿಸಲು ನೀವು ಬಳಸಬಹುದಾದ ವಿಶೇಷ ಟ್ಯಾಗ್ ಇದಾಗಿದೆ! ನೀವು `span` ಜೋಡಿ ನಡುವೆ ಏನು ಬೇಕಾದರೂ ಹಾಕಬಹುದು ಟ್ಯಾಗ್‌ಗಳು. **part** ಸ್ಟೈಲಿಂಗ್ ಮಾಡುವಂತಹ ವಿಷಯಗಳಿಗೆ ಇದು ಉಪಯುಕ್ತವಾಗಿದೆ ಪ್ಯಾರಾಗ್ರಾಫ್ನಲ್ಲಿನ ಪಠ್ಯದ.

+ ಮೇಲಿನ HTML ಕೋಡ್‌ಗಾಗಿ ಸ್ಟೈಲಿಂಗ್ ಅನ್ನು ಪೂರ್ಣಗೊಳಿಸಲು ಈ ಕೆಳಗಿನ CSS ಕೋಡ್ ಅನ್ನು ನಿಮ್ಮ style sheet‌ಗೆ ಸೇರಿಸಿ.

```css
  .sideNoteStyle {
    border: dotted 1px purple;
    background-color: #c1ebec;
    padding: 0.5em;
    margin: 0.5em;
  }
  .specialText {
      color: #FF4500;
      font-size: larger;
  }
```

![ತಮ್ಮದೇ ಆದ ಸ್ಟೈಲಿಂಗ್‌ನೊಂದಿಗೆ ಹೆಚ್ಚುವರಿ ಟಿಪ್ಪಣಿಗಳು](images/asidesStyled.png)

ಮುಂದಿನ ಕಾರ್ಡ್‌ನಲ್ಲಿ, ನಿಮ್ಮ ವೆಬ್‌ಸೈಟ್‌ನ ವಿನ್ಯಾಸವನ್ನು ಹೆಚ್ಚು ಆಸಕ್ತಿಕರಗೊಳಿಸುವುದು ಹೇಗೆ ಎಂದು ನೀವು ಕಲಿಯಲಿದ್ದೀರಿ!

+ ತಯಾರಾಗಲು, ಒಂದು `article` ಮತ್ತು ಎರಡು ಅನ್ನು ಹೊಂದಿರುವ ಪುಟವನ್ನು`aside` ಮಾಡಿ `<main> </main>`ಒಳಗೆ ಅಂಶಗಳು ಟ್ಯಾಗ್‌ಗಳು. ಅಥವಾ ನೀವು ಬಯಸಿದರೆ, ನೀವು ನನ್ನ ವೆಬ್‌ಸೈಟ್‌ನಲ್ಲಿ ಆಕರ್ಷಣೆಗಳ ಪುಟದೊಂದಿಗೆ ಕೆಲಸ ಮಾಡಬಹುದು.