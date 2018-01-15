## All in a row

On this card you will learn some tricks for arranging things **horizontally** on a page.

First, getting stuff centered! 

- By setting the left and right margins to `auto` you can make any element be in the middle instead of over to the left. Try it now on the `.card` class.

```css
    margin-left: auto;
    margin-right: auto;
```

That's one common problem solved! Another is arranging elements side by side in a row. 

- Put all of the card links you just made into a new container element. It's not going to be an `article` or a `section`, but one called `div`. It's a general purpose container you can use for grouping things and making nice layouts.

```html
    <div class="cardContainer">
```

- Add the following CSS in your stylesheet:

```css
    .cardContainer {
        display: flex;
        flex-wrap: wrap;
        justify-content: space-around;
        padding: 10px;
    }
```

Voilà! Thanks to **Flex** Your cards are now displayed side by side! Drag the vertical slider on Trinket's code pane and watch how the cards move around to fit the window size.

- Try deleting the `width` and `height` properties from the `.card` class and see what happens: **Flex** cleverly fits the cards together like a jigsaw puzzle, keeping an even height across everything that's in the same row.

If you have a navigation menu at the top of your page, that's another place you might use this trick. 

- Find the CSS rules for your menu. If you prefer, you can try it out with my website. 

- Delete `display: inline;` from the **list items** \(in my website, that's the `nav ul li` block.\). Then, in the list, `nav ul`, add in 

```css
    display: flex;
    justify-content: flex-start;
```
   
You end up with pretty much the same menu, right? The cool thing about Flex is you can control the layout with the property `justify-content`. 

- Change the value of `justify-content` to `flex-end` and see what happens. Or change it to `space-around` to make the menu items evenly spaced, just like you did for the cards.

A **responsive** website is one that adjusts itself to the screen size: so it always looks great whether you're looking at it on a computer, mobile phone or tablet. Let's make your menu responsive. Start with the regular styles: this will be your **default** behaviour.

- Add the following CSS rules to your menu. You probably have colours and borders defined as well; I've left them out to save space here! If you already have CSS rules defined for your menu, just add in or change the properties and values that you are missing.

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

With the CSS above you're going **mobile first**: the default style is good for small screens. You define different styles for bigger screens like this:

```css
    @media all and (min-width: 600px) {
        nav ul {
            flex-direction: row;
            justify-content: space-around;
        }
    }
```

Everything inside this block applies whenever the window is wider than **600 pixels**. 

- Can you add another block for screens bigger than **800 pixels**, with `flex-end` instead of `space-around`?

**Flex** is a pretty powerful layout tool that could fill a whole Sushi Series of it's own, but you can learn more at [dojo.soy/html3-flex](http://dojo.soy/html3-flex)

- Trinket's project window is quite small. To test out your website on a full size screen, download the project and open up the file `index.html` in a browser. Adjust the width of the window to see the menu change! You can put any CSS rules you like into these blocks, to define different styles for different screen sizes. It'll be especially useful when you do **CSS grid** layouts later!