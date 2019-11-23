## اجعل قائمتك قابلة للاستجابة

موقع الويب ** القابل للاستجابة ** هو موقع يتكيف مع حجم الشاشة بحيث يبدو رائعًا دومًا ، سواء كنت تنظر إليه على جهاز كمبيوتر أو هاتف محمول أو جهاز لوحي. دعنا نجعل قائمتك قابلة للاستجابة!

ستبدأ باستخدام الأنماط العادية: سيكون هذا هو سلوكك ** الافتراضي**.

## \--- collapse \---

## title: ماذا تعني كلمة "الافتراضي"؟

الأنماط الافتراضية هي مجموعة القواعد المعتادة الخاصة بك. يتم تطبيقها اولا ، قبل التحقق من أي شروط خاصة.

يمكنك إضافة كود برمجي يتحقق بعد ذلك من حجم الشاشة وإجراء بعض التعديلات إذا لزم الأمر.

\--- /collapse \---

+ أضف قواعد CSS التالية إلى قائمتك. ربما لديك ألوان وحدود محددة كذلك ؛ لقد تركتهم لتوفير المساحة هنا! إذا كان لديك بالفعل قواعد CSS محددة لقائمتك ، فما عليك سوى إضافة أو تغيير الخصائص والقيم أدناه.

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

مع تعليمات CSS أعلاه ، ستكون قائمتك أكثر ملاءمة للشاشات الصغيرة. وهذا ما يسمى بطريقة ** المحمول أولاً ** في البرمجة.

![Menu items stacked vertically on a small screen](images/responsiveMenuMobile.png)

## \--- collapse \---

## title: ماذا تعني كلمة "الافتراضي"؟

Quite often when coding a website, you will be using a computer screen, and you'll probably define your styles based on how it looks on that screen.

When you code for mobile first, you instead choose default styles that are suitable for small screens such as smartphones. You then add extra code to make adjustments for bigger screens.

Since more and more people browse the internet on their smartphones or tablets rather than on a computer, it's good practise to develop your website with this in mind.

\--- /collapse \---

+ Now add the following code to your style sheet:

```css
    @media all and (min-width: 1000px) {
        nav ul {
            flex-direction: row;
            justify-content: space-around;
        }
    }
```

The first line of code above checks what size the browser window is. If the window is **1000 pixels** wide or more, it will apply all the style rules inside the block.

![Menu items spaced evenly across one line on a wider screen](images/responsiveMenuMedium.png)

## \--- collapse \---

## title: How does it work?

The block contains new values for only some properties of the `nav ul` menu.

Whenever the window is wider than 1000 pixels, these new values will be applied instead of the ones you already defined for `nav ul`.

The rest of the properties you defined previously for `nav ul` will stay the same.

\--- /collapse \---

+ If you are using Trinket to write code, it might be helpful to download the project so you can test it out on a full-size screen.

\--- challenge \---

## Challenge: make your menu adjust itself for big screens

+ Can you add another block for screens bigger than **1600 pixels**, with `flex-end` instead of `space-around`?

![Menu items to the right on a wide screen](images/responsiveMenuWide.png)

\--- hints \---

\--- hint \---

The following code defines flex properties for menu items when the screen is bigger than 1600 pixels:

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

You can put any CSS rules you like into blocks like these to define different styles for different screen sizes. It’ll be especially useful when you do CSS grid layouts later!