## ಎಲ್ಲಾ ಸತತವಾಗಿ

ಈ ಕಾರ್ಡ್‌ನಲ್ಲಿ ನೀವು ವಿಷಯಗಳನ್ನು **horizontally**ಗಾಗೀ ಜೋಡಿಸಲು ಕೆಲವು ತಂತ್ರಗಳನ್ನು ಕಲಿಯುವಿರಿ ಒಂದು ಪುಟದಲ್ಲಿ. ಮೊದಲಿಗೆ, ವಿಷಯವನ್ನು ಕೇಂದ್ರೀಕರಿಸುವುದು ಹೇಗೆ ಎಂದು ನೀವು ನೋಡುತ್ತೀರಿ. ನಂತರ ನೀವು ಸತತವಾಗಿ ಅಂಶಗಳನ್ನು ಅಕ್ಕಪಕ್ಕದಲ್ಲಿ ಜೋಡಿಸುತ್ತೀರಿ.

+ `.card`‌ಗೆ ಕೆಳಗಿನ CSS ಗುಣಲಕ್ಷಣಗಳನ್ನು ಸೇರಿಸಿ ವರ್ಗ:

```css
    margin-left: auto;
    margin-right: auto;
```

ಕಾರ್ಡ್‌ಗಳು ಪುಟದ ಮಧ್ಯಭಾಗಕ್ಕೆ ಚಲಿಸುವುದನ್ನು ನೀವು ನೋಡಬೇಕು. ಎಡ ಮತ್ತು ಬಲ ಅಂಚುಗಳನ್ನು `auto`ಗೆ ಹೊಂದಿಸುವ ಮೂಲಕ, ನೀವು ಯಾವುದೇ ಅಂಶವನ್ನು ಎಡಕ್ಕೆ ಬದಲಾಗಿ ಮಧ್ಯದಲ್ಲಿ ಮಾಡುವಂತೆ ಮಾಡಬಹುದು.

![ಕಾರ್ಡ್‌ಗಳು ಎಡಕ್ಕೆ ಬದಲಾಗಿ ಮಧ್ಯದಲ್ಲಿ ಗೋಚರಿಸುತ್ತವೆ](images/marginAuto.png)

+ ಪುಟವನ್ನು ಕಿರಿದಾದ ಮತ್ತು ಅಗಲವಾಗಿಸಲು browser windowದ ಅಂಚನ್ನು ಎಳೆಯಿರಿ - ಕಾರ್ಡ್‌ಗಳು ಕೇಂದ್ರೀಕೃತವಾಗಿರುವುದನ್ನು ಗಮನಿಸಿ.

+ ನೀವು ಮಾಡಿದ ಎಲ್ಲಾ ಕಾರ್ಡ್ ಲಿಂಕ್‌ಗಳನ್ನು ಹೊಸ ಕಂಟೇನರ್ ಅಂಶವಾಗಿ ಇರಿಸಿ. ಇದು `article` ಅಥವಾ `section` ಆಗುವುದಿಲ್ಲ, ಆದರೆ `div` ಎಂದು ಕರೆಯಲ್ಪಡುತ್ತದೆ. ಇದು ಸಾಮಾನ್ಯ ಉದ್ದೇಶದ ಕಂಟೇನರ್ ಆಗಿದ್ದು, ನೀವು ವಿಷಯಗಳನ್ನು ಗುಂಪು ಮಾಡಲು ಮತ್ತು ಉತ್ತಮ ವಿನ್ಯಾಸಗಳನ್ನು ಮಾಡಲು ಬಳಸಬಹುದು.

```html
    <div class="cardContainer">
```

+ ನಿಮ್ಮ style sheet‌ನಲ್ಲಿ ಈ ಕೆಳಗಿನ CSS ಕೋಡ್ ಸೇರಿಸಿ:

```css
    .cardContainer {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        padding: 10px;
    }
```

Voilà! **Flex**ಗೆ ಧನ್ಯವಾದಗಳು, ನಿಮ್ಮ ಕಾರ್ಡ್‌ಗಳನ್ನು ಈಗ ಅಕ್ಕಪಕ್ಕದಲ್ಲಿ ಪ್ರದರ್ಶಿಸಲಾಗುತ್ತದೆ!

+ ವೆಬ್‌ಸೈಟ್ ಅನ್ನು ವಿಶಾಲವಾಗಿ ಮತ್ತು ಕಿರಿದಾಗಿಸಲು ನಿಮ್ಮ ವಿಂಡೋದ ಅಂಚನ್ನು ಎಳೆಯಿರಿ ಮತ್ತು ವಿಂಡೋ ಗಾತ್ರಕ್ಕೆ ಸರಿಹೊಂದುವಂತೆ ಕಾರ್ಡ್‌ಗಳು ಹೇಗೆ ಚಲಿಸುತ್ತವೆ ಎಂಬುದನ್ನು ನೋಡಿ, ಕೆಲವೊಮ್ಮೆ ಮುಂದಿನ ಸಾಲಿಗೆ ಸುತ್ತಿಕೊಳ್ಳುತ್ತದೆ.

![ಎರಡು ಸಾಲುಗಳಲ್ಲಿ ಜೋಡಿಸಲಾದ ಕಾರ್ಡ್‌ಗಳು ಬ್ರೌಸರ್ ಅಗಲಕ್ಕೆ ಸರಿಹೊಂದುವಂತೆ ಸಮನಾಗಿರುತ್ತವೆ](images/flexSideBySide.png)

+ `width` ಅಳಿಸಲು ಪ್ರಯತ್ನಿಸಿ ಮತ್ತು `height` `.card`‌ನಿಂದ ಗುಣಲಕ್ಷಣಗಳು ವರ್ಗ ಮತ್ತು ಏನಾಗುತ್ತದೆ ನೋಡಿ: `flex` ಜಿಗ್ಸಾ ಪಜಲ್ನಂತೆ ಜಾಣತನದಿಂದ ಕಾರ್ಡ್‌ಗಳನ್ನು ಒಟ್ಟಿಗೆ ಹೊಂದಿಸುತ್ತದೆ, ಒಂದೇ ಸಾಲಿನಲ್ಲಿರುವ ಎಲ್ಲದರಲ್ಲೂ ಇನ್ನೂ ಎತ್ತರವನ್ನು ಇರಿಸುತ್ತದೆ.

![ಕಾರ್ಡ್‌ಗಳು ಸ್ವಯಂಚಾಲಿತ ಅಗಲದೊಂದಿಗೆ ಅಕ್ಕಪಕ್ಕದಲ್ಲಿ ಜೋಡಿಸಲ್ಪಟ್ಟಿವೆ](images/flexAutoWidths.png)

ನಿಮ್ಮ ಪುಟದ ಮೇಲ್ಭಾಗದಲ್ಲಿ ನೀವು ನ್ಯಾವಿಗೇಷನ್ ಮೆನು ಹೊಂದಿದ್ದರೆ, ನೀವು ಈ ಟ್ರಿಕ್ ಅನ್ನು ಬಳಸಬಹುದಾದ ಮತ್ತೊಂದು ಸ್ಥಳವಾಗಿದೆ. ನಿಮ್ಮ ಮೆನು ಪಟ್ಟಿ ಅಂಶಗಳಿಂದ ಕೂಡಿದೆ ( (`li`) ಈ ಮುಂದಿನ ಬಿಟ್‌ಗಾಗಿ. ನೀವು ಬಯಸಿದರೆ, ನೀವು ಅದನ್ನು ನನ್ನ ವೆಬ್‌ಸೈಟ್‌ನೊಂದಿಗೆ ಪ್ರಯತ್ನಿಸಬಹುದು.

+ ಮೆನುಗಾಗಿ CSS ನಿಯಮಗಳನ್ನು ಹುಡುಕಿ. ನನ್ನ ವೆಬ್‌ಸೈಟ್‌ನಲ್ಲಿ, ಅದು ಬ್ಲಾಕ್‌ಗಳು `nav ul`, `nav ul li`, ಮತ್ತು `nav ul li a`.

+ ಆಸ್ತಿಯನ್ನು ಅಳಿಸಿ `display: inline;` ಪಟ್ಟಿ ಐಟಂಗಳಿಂದ. ನಂತರ, `nav ul` ಪಟ್ಟಿಯಲ್ಲಿ, ಸೇರಿಸಿ:

```css
    display: flex;
    justify-content: flex-start;
```

![Menu with items aligned to the left](images/flexMenuStart.png)

You end up with pretty much the same menu, right? The cool thing about `flex` is you can control the layout with the property `justify-content`.

+ Change the value of `justify-content` to `flex-end` and see what happens. Or change it to `space-around` to make the menu items evenly spaced, just like you did for the cards.

![Menu with items evenly spaced](images/flexMenuSpace.png)

![Menu with items aligned to the right](images/flexMenuEnd.png)

**`flex`** is a pretty powerful layout tool that could fill a whole Sushi Card series of its own — you can learn more about it at [dojo.soy/html3-flex](http://dojo.soy/html3-flex).