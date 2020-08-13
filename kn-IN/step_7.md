## ತಂಪಾದ ಪುಟ ವಿನ್ಯಾಸಗಳನ್ನು ವಿನ್ಯಾಸಗೊಳಿಸಿ

+ ಈ ಕಾರ್ಡ್‌ಗಾಗಿ ನೀವು ಒಳಗೆ ಮೂರು ಅಂಶಗಳೊಂದಿಗೆ `main` ಅಂಶವನ್ನು ಹೊಂದಿರುವ ಪುಟದೊಂದಿಗೆ ಕೆಲಸ ಮಾಡಬೇಕು: ಒಂದು `article` ಮತ್ತು ಎರಡು `aside` ಗಳು. ನಿಮಗೆ ಅಗತ್ಯವಿದ್ದರೆ ಮುಂದುವರಿಯಿರಿ ಮತ್ತು ಮೊದಲು ಇವುಗಳನ್ನು ರಚಿಸಿ. ನೀವು ನನ್ನ ವೆಬ್‌ಸೈಟ್‌ನೊಂದಿಗೆ ಕೆಲಸ ಮಾಡಲು ಬಯಸಿದರೆ, ಅನ್ನು `aside` ಸೇರಿಸಿ ಹಿಂದಿನ ಸುಶಿ ಕಾರ್ಡ್‌ನಿಂದ ಆಕರ್ಷಣೆಗಳ ಪುಟಕ್ಕೆ ಕೋಡ್. 

ನೀವು ಅನ್ವಯಿಸುವ ಮೂರು ವಿಭಿನ್ನ ಪುಟ ವಿನ್ಯಾಸಗಳು ಇಲ್ಲಿವೆ:

![](images/cssGridLayouts.png)

+ `main` ಹೊಸ CSS ತರಗತಿಗಳನ್ನು ಸೇರಿಸಿ ಮತ್ತು ಅದರೊಳಗಿನ ಮೂರು ಅಂಶಗಳು.

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

ನೀವು ವಿನ್ಯಾಸವನ್ನು ಬದಲಾಯಿಸುವ ಕಂಟೇನರ್ `main`, ಆದರೆ ನೀವು ಇದನ್ನು `div` ನಂತಹ ಯಾವುದೇ ರೀತಿಯ ಕಂಟೇನರ್‌ನೊಂದಿಗೆ ಮಾಡಬಹುದು ಅಥವಾ `article`, ಅಥವಾ ಇಡೀ ಪುಟ `boby`. ನೀವು ಬಳಸಲು ಹೊರಟಿರುವ ತಂತ್ರವನ್ನು **CSS grid** ಎಂದು ಕರೆಯಲಾಗುತ್ತದೆ.

ಈ ಉದಾಹರಣೆಯಲ್ಲಿ, `header` ಮತ್ತು `footer` ವಿನ್ಯಾಸದಿಂದ ಹೊರಗುಳಿಯಲಾಗುವುದು, ಆದರೆ ಅವುಗಳನ್ನು ಗ್ರಿಡ್‌ನಲ್ಲಿ ಸೇರಿಸುವುದು ತುಂಬಾ ಸಾಮಾನ್ಯವಾಗಿದೆ.

+ `display`ನವನ್ನು ಹೊಂದಿಸಿ `grid`‌ಗೆ ಆಸ್ತಿ ಒಟ್ಟಾರೆ ಪಾತ್ರೆಯಲ್ಲಿ:

```css
    .attPageLayoutGrid {
        display: grid;
        grid-column-gap: 0.5em;
        grid-row-gap: 1em;
    }
```

`grid-column-gap` ಏನು ಎಂದು ನೀವು ಯೋಚಿಸುತ್ತೀರಿ ಮತ್ತು `grid-row-gap` ಗುಣಲಕ್ಷಣಗಳು ಮಾಡುತ್ತವೆ?

+ ಮುಂದೆ, ನೀವು `grid-area` ವನ್ನು ಹೆಸರಿಸಿ ಪ್ರತಿ ಅಂಶಕ್ಕೆ: 

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

ನಂತರ ನೀವು ನಿಮ್ಮ ವಿನ್ಯಾಸವನ್ನು ವಿನ್ಯಾಸಗೊಳಿಸುತ್ತೀರಿ! ಎರಡು ಅನ್ನು `aside` ಇಡೋಣ ಅಂಶಗಳು ಪುಟದ ಕೆಳಭಾಗದಲ್ಲಿ ಅಕ್ಕಪಕ್ಕದಲ್ಲಿರುತ್ತವೆ. ಇದಕ್ಕಾಗಿ ನಿಮಗೆ ಎರಡು **columns** ಬೇಕಾಗುತ್ತವೆ ಸಮಾನ ಅಗಲ. ನೀವು **row** ಇರಿಸಬಹುದು ಎತ್ತರ ಸ್ವಯಂಚಾಲಿತ.

+ ಕೆಳಗಿನ ಕೋಡ್ ಅನ್ನು `.attPageLayoutGrid` ಒಳಗೆ ಇರಿಸಿ CSS ನಿಯಮಗಳು:

```css
    grid-template-rows: auto;
    grid-template-columns: 1fr 1fr;
    grid-template-areas: 
        "agArticle agArticle"
        "agAside1 agAside2";
```

`fr` **fraction** ಸೂಚಿಸುತ್ತದೆ. ನೀವು `article` ವನ್ನು ಹೇಗೆ ಮಾಡುತ್ತೀರಿ ಎಂಬುದನ್ನು ಗಮನಿಸಿ ಎರಡು ಕಾಲಮ್‌ಗಳ ಮೇಲೆ ಎಲ್ಲಾ ಜಾಗವನ್ನು ತೆಗೆದುಕೊಳ್ಳಿ.

--- collapse ---
---
title: ಸಹಾಯ! ನನಗೆ ದೋಷಗಳು ಮತ್ತು ಎಚ್ಚರಿಕೆಗಳು ಸಿಕ್ಕಿವೆ!
---

ನೀವು Trinket ಬಳಸುತ್ತಿದ್ದರೆ, ನೀವು ಕೋಡ್ ಅನ್ನು ನಿಖರವಾಗಿ ಮೇಲಿನಂತೆ ಟೈಪ್ ಮಾಡಿದರೂ ಸಹ, ಕೆಲವು ದೋಷಗಳು ಮತ್ತು ಎಚ್ಚರಿಕೆಗಳು ಗೋಚರಿಸುವುದನ್ನು ನೀವು ಗಮನಿಸಬಹುದು. CSS ಗ್ರಿಡ್ ಗುಣಲಕ್ಷಣಗಳನ್ನು Trinket ಇನ್ನೂ ಗುರುತಿಸದಿರುವುದು ಇದಕ್ಕೆ ಕಾರಣ. ಆದಾಗ್ಯೂ, ಕೋಡ್ ಇನ್ನೂ ಕಾರ್ಯನಿರ್ವಹಿಸುತ್ತದೆ.

CSS ಗ್ರಿಡ್ ಕೋಡ್ ನಿಮಗೆ 'ಅಜ್ಞಾತ ಆಸ್ತಿ' ಎಚ್ಚರಿಕೆಗಳನ್ನು ಅಥವಾ 'ಅನಿರೀಕ್ಷಿತ ಟೋಕನ್ 1fr' ನಂತಹ ದೋಷವನ್ನು ನೀಡಿದರೆ, ನೀವು ಇವುಗಳನ್ನು ನಿರ್ಲಕ್ಷಿಸಬಹುದು.

--- /collapse ---

![ಪಕ್ಕದಲ್ಲಿ ಕೆಳಭಾಗದಲ್ಲಿ ಅಕ್ಕಪಕ್ಕವಿದೆ](images/cssGridAsidesAtBottom.png)

ಅನ್ನು `aside` ಇಡೋಣ ಅಂಶಗಳು ಬಲಭಾಗದಲ್ಲಿವೆ ಮತ್ತು ಅವುಗಳನ್ನು `article` ಅರ್ಧ ಅಗಲವನ್ನಾಗಿ ಮಾಡಿ.

+ `grid-template-columns` ಮೌಲ್ಯಗಳನ್ನು ಬದಲಾಯಿಸಿ ಮತ್ತು `grid-template-areas` ಗೆ:

```css
    grid-template-columns: 2fr 1fr;
    grid-template-areas: 
        "agArticle agAside1"
        "agArticle agAside2";
```

![Asides are down the right hand side](images/cssGridAsidesOnRight.png)

+ ನಿಮಗೆ `aside` ಬೇಡವಾದರೆ ಎಲ್ಲಾ ರೀತಿಯಲ್ಲಿ ಕೆಳಕ್ಕೆ ವಿಸ್ತರಿಸುವ ಅಂಶಗಳು, ನೀವು ಡಾಟ್ ಬಳಸಿ ಖಾಲಿ ಜಾಗವನ್ನು ಸೇರಿಸಬಹುದು: 

```css
    grid-template-areas: 
        "agArticle agAside1"
        "agArticle agAside2"
        "agArticle . ";
```

![ಬಲಭಾಗದಲ್ಲಿ ಮತ್ತು ಕೆಳಗೆ ವಿಸ್ತರಿಸಿಲ್ಲ](images/cssGridAsidesTopRight.png)

--- challenge ---

## ಸವಾಲು: ವಿಭಿನ್ನ ಪರದೆಯ ಗಾತ್ರಗಳಿಗಾಗಿ ವಿಭಿನ್ನ ವಿನ್ಯಾಸಗಳನ್ನು ಮಾಡಿ

+ ಪರದೆಯು ಎಷ್ಟು ಅಗಲವಿದೆ ಎಂಬುದರ ಆಧಾರದ ಮೇಲೆ ವಿನ್ಯಾಸವನ್ನು ಬದಲಾಯಿಸಲು ನೀವು ಮೊದಲು ಸೇರಿಸಿದ ಪರದೆಯ ಗಾತ್ರದ ಪರಿಶೀಲನೆಗಳನ್ನು ಬಳಸಬಹುದೇ? ಗಮನಿಸಿ: ಪ್ರತಿ ಪರದೆಯ ಗಾತ್ರಕ್ಕೆ ನೀವು ಈಗಾಗಲೇ CSS ಬ್ಲಾಕ್ಗಳನ್ನು ರಚಿಸಿದ್ದರೆ, ಹೊಸದನ್ನು ರಚಿಸುವ ಬದಲು ನೀವು ಆ ಬ್ಲಾಕ್ಗಳಿಗೆ ಹೊಸ CSS ಕೋಡ್ ಅನ್ನು ಸೇರಿಸಬಹುದು.

--- hints ---


--- hint ---

ಪರದೆಯು 1000 pixel‌ಗಳಿಗಿಂತ ದೊಡ್ಡದಾದಾಗ ಮೇಲಿನ CSS ವರ್ಗದ ವಿನ್ಯಾಸವನ್ನು ಈ ಕೆಳಗಿನ ಕೋಡ್ ವ್ಯಾಖ್ಯಾನಿಸುತ್ತದೆ:

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

--- /hint ---

--- hint ---

ಪರದೆಯು 1600 pixel‌ಗಳಿಗಿಂತ ದೊಡ್ಡದಾದಾಗ ಮೇಲಿನ CSS ವರ್ಗದ ವಿನ್ಯಾಸವನ್ನು ಈ ಕೆಳಗಿನ ಕೋಡ್ ವ್ಯಾಖ್ಯಾನಿಸುತ್ತದೆ:

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

--- /hint ---

--- /hints ---

--- /challenge ---

**CSS grid** ನೊಂದಿಗೆ, ನೀವು ಇಷ್ಟಪಡುವ ಯಾವುದೇ ವಿನ್ಯಾಸವನ್ನು ನೀವು ಮಾಡಬಹುದು. ನೀವು ಇನ್ನಷ್ಟು ತಿಳಿದುಕೊಳ್ಳಲು ಬಯಸಿದರೆ, [dojo.soy/html3-css-grid](http://dojo.soy/html3-css-grid){:target="_blank"} ಗೆ ಹೋಗಿ.