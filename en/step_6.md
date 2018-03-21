## Make your menu responsive

A **responsive** website is one that adjusts itself to the screen size: so it always looks great whether you're looking at it on a computer, mobile phone or tablet. Let's make your menu responsive. Start with the regular styles: this will be your **default** behaviour.

+ Add the following CSS rules to your menu. You probably have colours and borders defined as well; I've left them out to save space here! If you already have CSS rules defined for your menu, just add in or change the properties and values that you are missing.

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

+ Can you add another block for screens bigger than **800 pixels**, with `flex-end` instead of `space-around`?

**Flex** is a pretty powerful layout tool that could fill a whole Sushi Series of it's own, but you can learn more at [dojo.soy/html3-flex](http://dojo.soy/html3-flex)

+ Trinket's project window is quite small. To test out your website on a full size screen, download the project and open up the file `index.html` in a browser. Adjust the width of the window to see the menu change! You can put any CSS rules you like into these blocks, to define different styles for different screen sizes. It'll be especially useful when you do **CSS grid** layouts later!