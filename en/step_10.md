## Special effects

On this card you'll learn a few more nice effects that you can achieve with CSS.

### Shadows and movement

Let's add a little movement when you hover over the cards you made earlier. 


+ Find the `.card:hover` CSS class from earlier and change it to the following. Try out different values in the translate function!

```css
    .card:hover {
        box-shadow: 0px 2px 2px rgba(0,0,0,0.2); 
        transform: translateY(-2px);
    }
```
    
--- collapse ---
---
title: The transform property
---

If you completed the Intermediate Sushi Cards then you may remember using the `transform` property in some `@keyframes` animations.

Here you see you can also use the property on its own within a regular CSS block.

One kind of value you can set it to is `rotate`, to make something turn. Others are `translateY`, which moves something up or down, and `translateX`, for sideways movement.

--- /collapse ---
   
+ Play about with different pixel values in the `box-shadow` property to see what they do. 
     
--- collapse ---
---
title: What's rgba?
---

`rgba(0,0,0,0.2)` is another way of defining a colour. 

It's got the usual three numbers \(from `0` up to `255`\) for Red, Green and Blue. 

The fourth number, called the **alpha** value, defines how see-through something is. It is a decimal number between `0` and `1`, with `1` being not see-through at all and `0` being completely invisible. The lower the alpha value, the more see-through it is.

--- /collapse ---

+ Finally, make the movement smooth by adding the following property to the `.card` class from earlier: 

```css
    transition: all 0.2s ease-out;
``` 

A duration of `0.2s` means the transition lasts for `0.2 seconds`.

### Lightbox

Another effect you've probably seen on loads of websites is **lightbox**, where you click on something and the screen dims while something else, like a bigger picture or a popup box, appears in front of everything. 

![Lightbox effect in action](images/lightboxLemur.png)

To get this effect you will make two links: one for the actual lightbox (the bit that pops up), and one for the thing that you click to make the lightbox appear. I'm going to do mine on the Attractions page of my website. You go with whatever page you have pictures on!

+ Decide what things you want to appear when you click, and add them all to your page, in between a set of `a` tags to make a link. Make sure you give the link an `id`. The code can go anywhere on the page: you will be making the elements invisible in the next step!

```html
    <a href="#_" class="lightbox" id="boxLemur">
        <h3>Lemur!!</h3>
        <img src="monkey-2223271_640.jpg" alt="Picture of a lemur" class="bigPics"/>
        <p>A lemur enjoying a little snack</p>
    </a>
```

You can put anything you like in between the link tags. I've got a big picture, a heading and some text. Maybe you just want a picture and no text.

+ Add the following CSS for the lightbox. Can you work out what some of it does?
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

Note: Setting the `position` property to `fixed` means it stays put when you scroll.

+ Next, decide what thing you want to click to make the lightbox appear, and add add a pair of `a` tags around the element (in my case it's a smaller picture of a lemur). The **target** of the link will be the lightbox, which you set using the `id`. You might recognise this technique from earlier!

```html
    <a href="#boxLemur">
        <img src="monkey-2223271_640.jpg" class="smallPics">
    </a>
```

+ Finally add the following CSS. Note that this is a **pseudo-class**; it should go after the code for the `.lightbox` class and not inside it!

```css
    .lightbox:target {
        visibility: visible;
    }
```
    
The `:target` pseudo-class gets applied whenever the lightbox was the target of the last link clicked. So when you click anywhere the `visibility` will be set back to `hidden`.

+ Try clicking your new link to see the lightbox appear! To make it go away, you just click anywhere.

You can add as many lightboxes as you want to a page. They can all use the same CSS class. Just make sure each one has a different `id`! For each one, you need to make something on your webpage into a link that you can click to make the lightbox appear, and you use the `id` as the `href` value in that link; just as you've done above!