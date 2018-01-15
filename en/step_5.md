## Sidenotes and captions

If you want to add a **caption** to a picture, that is, some text that goes with it like a title or short description, then you could make use of two elements designed just for that purpose: `figure` and `figcaption`!

- Find an `img` element where you have text above or below that goes with the picture. I'm working with the Tito picture on `index.html`, but you can go with whatever is on your website.  

```html
  <img id="imgTito" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />  		
  <p>
    Tour guide Tito!
  </p>
```

- On the line above the code, add the tag `<figure>`. Place the closing tag `<\figure>` on a new line after the code.

- Next, remove the `p` tags, or whatever tags you have around the text \(maybe it's a heading, like `h2`?\) and put the text in between `<figcaption> <\figcaption>` tags instead. The whole thing should look something like this:

```html
  <figure>
      <img id="imgTito" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />  		
      <figcaption>
      Tour guide Tito!
      </figcaption>
  </figure>
```
   
The `figcaption` element is your `caption`. It can go either above the `img` element or below it.

When your web page updates, the picture and text might have changed position. Maybe you were happy with the original positioning of the elements and don't want this. Simply define CSS rules for the `figure` and set the margin properties to zero, or values that suit you. You can style both `figure` and `figcaption` as you would any other element, with background colour, borders, and everything else.

```css
  figure { 
      margin-top: 0px;
      margin-bottom: 0px;
      margin-left: 0px;
      margin-right: 0px;
  }
```

The `figure` element acts as a sort of **container** for your picture and its caption. As well as allowing you to treat them as one unit when defining styles, grouping them together logically helps to maintain a good structure to your website.
   
Another useful container is `aside`. You use it when you have extra stuff that doesn't really belong with the main information on a page. For example, the Attractions page on my website is a list of places to visit. I want to add some notes about weather and how to get around. That information doesn't really belong in the `article` element with all the attractions.

- Outside of the `article` element, add one or more pairs of `<aside> <\aside>` tags containing your extra stuff.

```html  
  <aside class="lightPurpleBackground">
      <h2>Getting around</h2>
      <h3>Train and bus</h3>
      <p>You can get to most of the major towns by train from Dublin. There are many buses that do tours to popular locations and tourist attractions.</p>
      <h3>Car</h3>
      <p>The easiest way to get around outside of the cities is by car.</p>
    </aside>
    <aside class="lightPurpleBackground">
      <h2>Weather</h2>
      <p>The weather in Ireland is <span class="specialText">very unpredictable!</span> It's best to <span class="specialText">be prepared</span> for any kind of weather, even if it's a nice day!</p>
  </aside>
```

The `aside`, `article` and other containers are similar. The only real difference is in the **meaning**, that is, what you use them for. It's important to use meaningful HTML elements whenever you can. It gives your website better structure and is especially helpful for people using **screen readers**.
  
You can write some CSS rules to make the `aside` elements look different or stand out if you want to. 

Did you spot the bonus element in there, `span`? It's a special tag you can use just for adding extra CSS! You can put anything in between a pair of `span` tags. It's useful for things like styling a **part** of the text in a paragraph.

```css
  .lightPurpleBackground {
    background-color: #CFBFFF;
  }
  .specialText {
      color: #FF4500;
      font-size: larger;
  }
```

On the next card you're going to learn how to make the layout more interesting! 

- To get ready, make a page that has one `article` and two `aside` elements inside the `<main> </main>` tags. Or if you prefer, you can work with the Attractions page on my website.

   