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

في كثير من الأحيان عند برمجة موقع ويب ، سوف تستخدم شاشة كمبيوتر ، وربما ستحدد أنماطك استنادًا إلى كيفية ظهورها على تلك الشاشة.

عندما البرمجة للجوال أولاً ، فإنك تختار بدلاً من ذلك الأنماط الافتراضية المناسبة للشاشات الصغيرة مثل الهواتف الذكية. ثم تضيف اكواد برمجية إضافية لإجراء تعديلات للشاشات الأكبر حجمًا.

نظرًا لأن المزيد والمزيد من الناس يتصفحون الإنترنت على هواتفهم الذكية أو أجهزة الكمبيوتر اللوحية بدلاً من استخدامها على جهاز كمبيوتر ، فمن الممارسات الجيدة تطوير موقع الويب الخاص بك مع وضع ذلك في الاعتبار.

\--- /collapse \---

+ أضف الكود التالي الى ملف الأنماط الخاص بك:

```css
    @media all and (min-width: 1000px) {
        nav ul {
            flex-direction: row;
            justify-content: space-around;
        }
    }
```

يتحقق السطر الأول من الشفرة أعلاه من حجم نافذة المتصفح. إذا كانت النافذة بعرض ** 1000 بكسل ** أو أكثر ، سيتم تطبيق جميع قواعد النمط داخل الكتلة.

![Menu items spaced evenly across one line on a wider screen](images/responsiveMenuMedium.png)

## \--- collapse \---

## title: كيف يعمل؟

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