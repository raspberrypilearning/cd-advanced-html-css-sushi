## مؤثرات خاصة

في هذه البطاقة ، ستتعرف على بعض التأثيرات اللطيفة التي يمكنك انجازها باستخدام CSS.

### الظلال والحركة

دعنا نضيف حركة صغيرة عندما تمرر مؤشر الماوس فوق البطاقات التي قمت بإنشائها مسبقًا.

+ ابحث عن `.card: hover ` فئة CSS من ماسبق وقم بتغييرها إلى ما يلي:

```css
    .card:hover {
        box-shadow: 0px 2px 2px rgba(0,0,0,0.2); 
        transform: translateY(-2px);
    }
```

+ جرب قيمًا مختلفة في ` دالة ` الترجمة!

## \--- collapse \---

## title: `خاصية` التحويل

إذا قمت بإكمال بطاقات سوشي HTML / CSS ، فقد تتذكر استخدام خاصية التحويل ` transform` في بعض الإطارات المفتاحية للرسوم المتحركة ` @keyframes `. هنا ترى أنه يمكنك أيضًا استخدام الخاصية وحدها داخل كتلة CSS اعتيادية.

نوع من القيم التي يمكنك تعيينها هي ` rotate ` ، لجعل عنصر يدور. الخاصية الآخرى ` translate Y ` ، التي تحرك شيئًا ما لأعلى أو لأسفل ، و ` translateX ` ، للحركة من جانب إلى آخر.

\--- /collapse \---

+ حاول التلاعب بقيم بكسل مختلفة في خاصية ` box-shadow` لمعرفة ماذا تفعل. 

## \--- collapse \---

## title: ماهي ` rgba ` ؟

`rgba(0,0,0,0.2)` هي طريقة أخرى لتحديد اللون.

تحتوي على الأرقام الثلاثة المعتادة (من ` 0 ` حتى ` 255 `) للأحمر والأخضر والأزرق.

الرقم الرابع ، يدعي قيمة الفا ** alpha ** ، وتحدد الشفافية ** transparent ** (أو النظر من خلال) شيء ما. وهو رقم عشري بين ` 0 ` و ` 1 ` ، حيث ` 1 ` تمثل معتم تماما و ` 0 ` شفاف تماما. هذا يعني أنه كلما انخفضت قيمة ألفا لعنصر ما ، زادت درجة شفافيته.

\--- /collapse \---

+ أخيرًا ، اجعل الحركة سلسة عن طريق إضافة الخاصية التالية إلى `.card` من ما سبق: 

```css
    transition: all 0.2s ease-out;
```

مدة ` 0.2 ثانية ` تعني الانتقال ` transition` يستمر لمدة 0.2 ثانية.

### الصندوق المضئ Lightbox

من التأثيرات الأخرى التي ربما تراها على الكثير من مواقع الويب هو ** lightbox **: حيث تنقر على شيء ما فيظلم موقع الويب بينما يظهر شيء آخر ، مثل صورة أكبر أو مربع منبثق ، يظهر في المقدمة.

![Lightbox effect in action](images/lightboxLemur.png)

للحصول على هذا التأثير ، ستقوم بإنشاء رابطين: واحد لصندوق الضوء الفعلي (الشيء الذي ينبثق) ، وواحد للشيء الذي تنقر عليه لإظهار صندوق الضوء. سأقوم بعمل التأثير في صفحة "الجذب السياحي" على موقعي. تستطيع العمل مع أي صفحة لديك فيها صور!

+ Decide what things you want to appear when you click, and add them all to your page in between a set of `a` tags to make a link. Make sure you give the link an `id`. The code can go anywhere on the page: you will be making the elements invisible in the next step!

```html
    <a href="#_" class="lightbox" id="boxLemur">
        <h3>Lemur!!</h3>
        <img src="monkey-2223271_640.jpg" alt="Picture of a lemur" />
        <p>A lemur enjoying a little snack</p>
    </a>
```

You can put anything you like in between the link tags. I've got a big picture, a heading, and some text. Maybe you just want a picture and no text!

+ Add the following CSS code for the lightbox. Can you work out what some of it does?

```css
    .lightbox{
        background: rgba(0,0,0,0.8);
        color: #ffffff;
        text-align: center;
        text-decoration: none;
        width: 100%;
        height: 100%;
        top: 0;
        left: 0;
        position: fixed;
        visibility: hidden;
        z-index: 999;
    }
```

Note: Setting the `position` property to `fixed` means the position you set will be relative to the browser window, so it will stay put when you scroll.

+ Next, decide what thing you want to click to make the lightbox appear, and add add a pair of `a` tags around that element (in my case it's a smaller picture of a lemur). The **target** of the link will be the lightbox, which you set using the `id`. You might recognise this technique from earlier!

```html
    <a href="#boxLemur">
        <img src="monkey-2223271_640.jpg" class="mediumPics">
    </a>
```

+ Finally add the following CSS code. Note that this is a **pseudo-class**; it should go after the code for the `.lightbox` class and not inside it!

```css
    .lightbox:target {
        visibility: visible;
    }
```

The `:target` pseudo-class gets applied whenever the lightbox was the target of the last link clicked. So when you click anywhere, the `visibility` will be set back to `hidden`.

+ Try clicking your new link to see the lightbox appear! To make it go away, just click anywhere on the page.

You can add as many lightboxes as you want to a page. They can all use the same CSS class — just make sure each one has a different `id`! For each one, you need to make something on your webpage into a link that you can click to make the lightbox appear, and then use the `id` as the `href` value in that link, just as you've done above!