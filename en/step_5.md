## All in a row

On this card you will learn some tricks for arranging things **horizontally** on a page. First, you'll see how to get stuff centered. Then you'll arrange elements side by side in a row. 

+ Add the following CSS properties to the `.card` class:

```css
    margin-left: auto;
    margin-right: auto;
```

By setting the left and right margins to `auto` you can make any element be in the middle instead of over to the left. 

+ Put all of the card links you just made into a new container element. It's not going to be an `article` or a `section`, but one called `div`. It's a general purpose container you can use for grouping things and making nice layouts.

```html
    <div class="cardContainer">
```

+ Add the following CSS in your stylesheet:

```css
    .cardContainer {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        padding: 10px;
    }
```

Voilà! Thanks to **Flex** Your cards are now displayed side by side! 

+ Drag the edge of your window to make the website wider and narrower and watch how the cards move around to fit the window size.

+ Try deleting the `width` and `height` properties from the `.card` class and see what happens: **Flex** cleverly fits the cards together like a jigsaw puzzle, keeping an even height across everything that's in the same row.

If you have a navigation menu at the top of your page, that's another place you might use this trick. 

+ Find the CSS rules for your menu. If you prefer, you can try it out with my website. 

+ Delete `display: inline;` from the **list items** \(in my website, that's the `nav ul li` block.\). Then, in the list, `nav ul`, add in 

```css
    display: flex;
    justify-content: flex-start;
```
   
You end up with pretty much the same menu, right? The cool thing about Flex is you can control the layout with the property `justify-content`. 

+ Change the value of `justify-content` to `flex-end` and see what happens. Or change it to `space-around` to make the menu items evenly spaced, just like you did for the cards.

**Flex** is a pretty powerful layout tool that could fill a whole Sushi Series of it's own, but you can learn more at [dojo.soy/html3-flex](http://dojo.soy/html3-flex)
