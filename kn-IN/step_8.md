## ಫೋಟೋ ಕೊಲಾಜ್

ಈ ಕಾರ್ಡ್‌ನಲ್ಲಿ ನೀವು HTML ಅಂಶಗಳನ್ನು ನಿಖರವಾಗಿ ಇರಿಸಲು ಮತ್ತು ಫೋಟೋ ಕೊಲಾಜ್ ಮಾಡಲು CSS ಅನ್ನು ಬಳಸಲು ಕಲಿಯುವಿರಿ.

![](images/photoCollageWithText_wide.png)

+ `div` ಅನ್ನು ಸೇರಿಸಿ ನಿಮ್ಮ ಪುಟಕ್ಕೆ ಮತ್ತು ನೀವು ಇಷ್ಟಪಡುವಷ್ಟು ಚಿತ್ರಗಳನ್ನು ಅದರಲ್ಲಿ ಇರಿಸಿ. `div` ನೀಡಿ ಮತ್ತು `img` ಅಂಶಗಳು `id` ಮೌಲ್ಯಗಳನ್ನು.

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

ಫೋಟೋಗಳು ನಿಮ್ಮ ಕೋಡ್‌ನಲ್ಲಿ ಗೋಚರಿಸುವ ಕ್ರಮದಲ್ಲಿ ವೆಬ್ ಪುಟದಲ್ಲಿ ಒಂದರ ನಂತರ ಒಂದರಂತೆ ಕಾಣಿಸುತ್ತದೆ.

+ ನಿಮ್ಮ CSS ಫೈಲ್‌ನಲ್ಲಿ, `div` ಒಳಗೆ ಇರುವ ಅಂಶಗಳಿಗಾಗಿ ಈ ಕೆಳಗಿನ CSS ವರ್ಗವನ್ನು ಸೇರಿಸಿ: 

```css
    .absPos {
        position: absolute;
    }
```

+ ಮುಂದೆ, ನೀವು ಆಸ್ತಿಯನ್ನು ಸೇರಿಸುವ ಅಗತ್ಯವಿದೆ `position: relative;` ಕಂಟೇನರ್ಗೆ ಮತ್ತು ಅದಕ್ಕಾಗಿ ಗಾತ್ರವನ್ನು ವ್ಯಾಖ್ಯಾನಿಸಿ. ಇದು ಇತರ ಅಂಶಗಳ ಸ್ಥಾನಗಳನ್ನು **relative to** (ಅಂದರೆ, ಒಳಗೆ) ಧಾರಕಕ್ಕೆ ವ್ಯಾಖ್ಯಾನಿಸುತ್ತದೆ.

```css
    .relPos {
        position: relative;
    }

    #photoBox {
        width: 800px;
        height: 400px;
    }
```

+ ನಂತರ **id selectors** ಬಳಸಿಕೊಂಡು ಪ್ರತಿಯೊಂದು ಅಂಶಗಳಿಗೆ ಶೈಲಿಯ ನಿಯಮಗಳ ಗುಂಪನ್ನು ರಚಿಸಿ ಅವುಗಳ ಗಾತ್ರಗಳನ್ನು ಹೊಂದಿಸಲು (`width` ಮತ್ತು / ಅಥವಾ `height` ಗುಣಲಕ್ಷಣಗಳು) ಹಾಗೆಯೇ ಅವುಗಳ ನಿಖರವಾದ ಸ್ಥಾನಗಳು.

ಒಂದು ಅಂಶದ ಸ್ಥಾನವನ್ನು ವ್ಯಾಖ್ಯಾನಿಸಲು, ನೀವು ಬಳಸಬಹುದಾದ ನಾಲ್ಕು ಗುಣಲಕ್ಷಣಗಳಿವೆ: `left`, `right`, `top`, ಮತ್ತು `bottom`. ಪ್ರತಿಯೊಂದು ಅಂಚುಗಳು ಪೋಷಕರ ಅಂಚಿನಿಂದ ಎಷ್ಟು ದೂರವಿರಬೇಕು ಎಂಬುದನ್ನು ಅವು ಪ್ರತಿನಿಧಿಸುತ್ತವೆ. ಲಂಬ ಸ್ಥಾನಕ್ಕಾಗಿ `top` ಅಥವಾ `bottom` ಅನ್ನು ಬಳಸಿ, ಮತ್ತು ಸಮತಲ ಸ್ಥಾನಕ್ಕಾಗಿ `left` ಅಥವಾ `right` ಅನ್ನು ಬಳಸಿ.

![ಮೇಲಿನ, ಎಡ, ಕೆಳಗಿನ ಮತ್ತು ಬಲ ಗುಣಲಕ್ಷಣಗಳು ಮೂಲ ಧಾರಕಕ್ಕೆ ಹೇಗೆ ಸಂಬಂಧಿಸಿವೆ ಎಂಬುದನ್ನು ತೋರಿಸುವ ರೇಖಾಚಿತ್ರ](images/cssPositionProperties.png)

+ ನಿಮ್ಮ ಪ್ರತಿಯೊಂದು ಚಿತ್ರಕ್ಕೂ ನಿಖರವಾದ ಸ್ಥಾನಗಳನ್ನು ಆರಿಸಿ, ಮತ್ತು ಯಾವುದೇ ಗುಣಲಕ್ಷಣಗಳನ್ನು ಬಳಸಿ `left`, `right`, `top`, ಮತ್ತು `bottom` ನಿಮ್ಮ ಸಿಎಸ್ಎಸ್ ನಿಯಮಗಳಲ್ಲಿ ಆ ಸ್ಥಾನಗಳನ್ನು ವ್ಯಾಖ್ಯಾನಿಸಲು. ಉದಾಹರಣೆಗೆ, ಈ ಕೋಡ್ ಬೆಕ್ಕಿನ ಚಿತ್ರವನ್ನು ಮೇಲಿನಿಂದ 100 pixel‌ಗಳನ್ನು ಮತ್ತು ಎಡದಿಂದ 60 ಪಿಕ್ಸೆಲ್‌ಗಳನ್ನು ಇರಿಸುತ್ತದೆ:

```css
    #imgTeaCat {
        width: 250px;
        top: 100px;
        left: 60px;
    }
```

ಗಮನಿಸಿ: ಸ್ಥಾನದ ಮೌಲ್ಯಗಳು ಸಹ negative ಣಾತ್ಮಕವಾಗಬಹುದು! ನೀವು negative ಣಾತ್ಮಕ ಮೌಲ್ಯವನ್ನು ಬಳಸಿದರೆ, ಅದು ನೀವು ನಿರ್ದಿಷ್ಟಪಡಿಸಿದ ಯಾವುದೇ ಅಂಚಿನಲ್ಲಿರುವ ಅಂಶವನ್ನು ಧಾರಕದ ಹೊರಗೆ ತಳ್ಳುತ್ತದೆ.

### ವಿಷಯಗಳನ್ನು ಅತಿಕ್ರಮಿಸುತ್ತದೆ

ಕೆಲವು ಚಿತ್ರಗಳನ್ನು ಅತಿಕ್ರಮಿಸಲು ನೀವು ಬಯಸಬಹುದು. ಆದರೆ ಯಾವುದನ್ನು ಮೇಲಕ್ಕೆ ಹೋಗಬೇಕೆಂದು ನೀವು ಹೇಗೆ ಆರಿಸುತ್ತೀರಿ?

+ ಎರಡು ಚಿತ್ರಗಳನ್ನು ಆರಿಸಿ ಮತ್ತು ಅವುಗಳನ್ನು ಅತಿಕ್ರಮಿಸಲು ಕಾರಣವಾಗುವ ಸ್ಥಾನಗಳನ್ನು ನೀಡಿ.

+ ಹೆಚ್ಚುವರಿ ಆಸ್ತಿಯನ್ನು ಸೇರಿಸಿ, `z-index: 10;` ಅವುಗಳಲ್ಲಿ ಒಂದಕ್ಕೆ, ತದನಂತರ `z-index: 7` ಇನ್ನೊಂದಕ್ಕೆ.

+ ನಿಮ್ಮwebpage ಫಲಿತಾಂಶವನ್ನು ನೋಡೋಣ.

![](images/horse10Cat7.png)

+ ಈಗ `z-index` ವಿನಿಮಯ ಮಾಡಿಕೊಳ್ಳಿ ಮೌಲ್ಯಗಳು, ಆದ್ದರಿಂದ `7` ಮತ್ತು `10` ಇತರ ಮಾರ್ಗಗಳು. ನಿಮ್ಮ ವೆಬ್ ಪುಟದಲ್ಲಿ ನೀವು ಏನಾದರೂ ವ್ಯತ್ಯಾಸವನ್ನು ನೋಡುತ್ತೀರಾ?

![](images/horse7Cat10.png)

--- collapse ---
---
title: z-index ಹೇಗೆ ಕಾರ್ಯನಿರ್ವಹಿಸುತ್ತದೆ?
---

`z-index` ಎರಡು ಅಥವಾ ಹೆಚ್ಚಿನ ಅಂಶಗಳು ಹೇಗೆ ಅತಿಕ್ರಮಿಸಬೇಕು ಎಂಬುದನ್ನು ನಿರ್ಧರಿಸಲು ಆಸ್ತಿ ನಿಮಗೆ ಅನುಮತಿಸುತ್ತದೆ. ಮೌಲ್ಯವು ಯಾವುದೇ ಸಂಪೂರ್ಣ ಸಂಖ್ಯೆಯಾಗಿರಬಹುದು.

**highest** ಸಂಖ್ಯೆ **top** ಕೊನೆಗೊಳ್ಳುತ್ತದೆ ರಾಶಿಯ, ಅಥವಾ ಬೇರೆ ರೀತಿಯಲ್ಲಿ ಹೇಳುವುದಾದರೆ **front**. ಮುಂದಿನ ಅತ್ಯಧಿಕ ಸಂಖ್ಯೆಯ ಅಂಶವು ಅದರ ಹಿಂದೆ, ಮತ್ತು ಇತರರ ಮುಂದೆ, ಮತ್ತು ಹೀಗೆ, ನೀವು ಕಡಿಮೆ ಸಂಖ್ಯೆಯೊಂದಿಗೆ ಅಂಶವನ್ನು ಪಡೆಯುವವರೆಗೆ, ಅದು ಇತರ ಎಲ್ಲ ಅಂಶಗಳ ಹಿಂದೆ ಹಿಂಭಾಗದಲ್ಲಿ ಗೋಚರಿಸುತ್ತದೆ.

--- /collapse ---

ನೀವು ಯಾವುದೇ HTML ಅಂಶಗಳನ್ನು ಈ ರೀತಿ ಇರಿಸಬಹುದು, ಕೇವಲ ಚಿತ್ರಗಳಲ್ಲ. ಉದಾಹರಣೆಗೆ, ನೀವು `p` ಬಳಸಬಹುದು ಫೋಟೋದ ಮೇಲೆ ಕೆಲವು ಪಠ್ಯವನ್ನು ಸೇರಿಸುವ ಅಂಶ.

--- challenge ---

## ಸವಾಲು: ಫೋಟೋ ಕೊಲಾಜ್ ಮಾಡಿ

+ ಕೆಳಗೆ ತೋರಿಸಿರುವಂತೆ ನಿಮ್ಮ ಸ್ವಂತ ಫೋಟೋಗಳ ಕೊಲಾಜ್ ರಚಿಸಲು ಪ್ರಯತ್ನಿಸಿ! ವಿಭಿನ್ನ `z-index` ದೊಂದಿಗೆ ನಿಖರವಾದ ಸ್ಥಾನೀಕರಣವನ್ನು ಬಳಸಿ ಅತಿಕ್ರಮಣ ಪರಿಣಾಮವನ್ನು ನೀವು ಬಯಸಿದ ರೀತಿಯಲ್ಲಿ ಪಡೆಯಲು ಮೌಲ್ಯಗಳು.

--- hints ---


--- hint ---

ನನ್ನ ಐರ್ಲೆಂಡ್ ವೆಬ್‌ಸೈಟ್‌ನಲ್ಲಿ ಫೋಟೋ ಕೊಲಾಜ್‌ಗಾಗಿ HTML ಕೋಡ್ ಕೆಳಗೆ ಇದೆ. `div` ಒಳಗೆ ಆರು ಫೋಟೋಗಳು ಮತ್ತು ಪಠ್ಯದ ತುಣುಕುಗಳಿವೆ.

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

--- /hint ---

--- hint ---

ಅಂಟು ಚಿತ್ರಣದಲ್ಲಿನ ನನ್ನ ಪ್ರತಿಯೊಂದು ಚಿತ್ರಗಳ ಸ್ಥಾನಗಳನ್ನು ಹೊಂದಿಸುವ CSS ನಿಯಮಗಳು ಇಲ್ಲಿವೆ:

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

--- /hint ---

--- hint ---

ನಾನು ಬಳಸಿದ CSS ತರಗತಿಗಳು ಇಲ್ಲಿವೆ:

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

--- /hint ---

--- /hints ---

![Photo collage with text over the top](images/photoCollageExample.png)

--- /challenge ---