## Cartes cliquables

Voici une technique que vous pouvez utiliser pour faire une galerie photo ou une page de portefeuille montrant vos projets: peu **cartes aperçu**.

![Carte de prévisualisation montrant une vignette d'image et du texte](images/cardsPreview.png)

+ Ajoutez le code HTML suivant à votre site Web, où vous voulez. Je fais le mien sur `index.html`. Vous pouvez changer l'image et le texte en fonction de vos propres cartes de prévisualisation. Je vais faire un tas de points forts des attractions touristiques en Irlande.

```html
    <article class="card">
        <img src="monkey-2223271_640.jpg" class="tinyPicture">
        <h3>Fota Wildlife Park</h3>
        <p>Île Fota, comté de Cork</p>
    </article>
```

![Image et texte avant l'application des styles](images/cardUnstyled.png)

+ Ajouter le code CSS suivant pour créer les classes `carte` et `tinyPicture`:

```css
    .tinyPicture {hauteur: 60px; border-radius: 10px; } .card {width: 200px; hauteur: 200px; bordure: 2px solide # F0FFFF; border-radius: 10px; taille de boîte: border-box; rembourrage: 10px; marge supérieure: 10px; famille de polices: "Trebuchet MS", sans-serif; } .card: hover {border-color: # 1E90FF; }
```

![Image et texte avec style pour créer un petit effet de carte](images/cardStyled.png)

Transformons toute la carte de prévisualisation en un lien afin que les gens puissent cliquer pour voir plus d'informations.

+ Placez l'élément entier `article` intérieur d'un élément de lien. Assurez-vous que l'étiquette de fermeture `</a>` est postérieure à l'étiquette de fermeture `</article>`! N'hésitez pas à changer le lien **URL** à tout ce que vous voulez lier. Cela pourrait être une autre page sur votre site Web, ou il pourrait s'agir d'un autre site entièrement.

```html
    <a href="attractions.html#scFota">  
        <article class="card ">
            <img src="monkey-2223271_640.jpg" class="tinyPicture">
            <h3>Fota Wildlife Park</h3>
            <p>Île de Fota, comté de Cork</p>
        </article>
    </a>
```

![Texte et image transformés en lien](images/cardLink.png)

## \--- effondrer \---

## title: Lien vers une partie spécifique d'une page

Remarquez comment la valeur de `href` dans mon lien se termine par `#scFota`? C'est une astuce que vous pouvez utiliser pour accéder à une partie spécifique d'une page.

+ Tout d'abord, tapez l'URL de la page à lier, suivie de `#`.

+ Dans le fichier de code de la page à laquelle vous vous connectez, recherchez la partie à laquelle vous souhaitez accéder et attribuez à cet élément un `id`, par exemple, `<section id = "scFota"`. La valeur du `id` est ce que vous tapez après le `#` dans votre lien.

\--- /effondrer \---

## \--- effondrer \---

## title: Réinitialisation des styles

Maintenant que la totalité de la carte de prévisualisation est un lien, la police de texte peut avoir changé.

+ Si c'est le cas, vous pouvez le corriger en ajoutant un **CSS class** au lien: `class = "cardLink"`. Voici le code CSS à mettre dans votre feuille de style:

```css
    .cardLink {color: inherit; text-decoration: aucun; }
```

Définir la valeur de n'importe quelle propriété à `hérite de` fait utiliser la valeur que l'élément **parent** a. Dans ce cas, la couleur du texte correspondra au reste du texte sur la page d'accueil.

\--- /effondrer \---

+ Faites au moins quatre ou cinq de ces cartes. Si vous travaillez à partir de mon exemple de site Web, vous pouvez en créer un pour chacune des sections de la page "Attractions". Sur la prochaine carte de sushi, vous apprendrez comment organiser les cartes avec un truc cool!