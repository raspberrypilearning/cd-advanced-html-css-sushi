## Légendes et notes de côté

Sur cette carte, vous découvrirez deux autres types d'élément **container** : un que vous pouvez utiliser pour ajouter une légende (un texte comme un titre ou une courte description) à une image, et un autre pour quand vous avez des choses supplémentaires qui ne le sont pas n'appartient pas vraiment à l'information principale sur une page.

### Photos avec légendes

+ Trouver un `img` élément où vous avez du texte ci-dessus ou ci-dessous qui va avec l'image. Je travaille avec l'image de Tito sur `index.html`, mais vous pouvez aller avec tout ce qui est sur votre site Web. 

```html
  <img id="titoPicture" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />          
  <p>
    Guide touristique Tito!
  </p>
```

+ Sur la ligne au-dessus du code, ajoutez la balise d'ouverture `<figure>`. Sur une nouvelle ligne sous le code, placez la balise de fermeture `<\ figure>`.

+ Ensuite, supprimez les balises `p` , ou les balises que vous avez autour du texte (c'est peut-être un en-tête, comme `h2`?), Et placez le texte entre `<figcaption> <\ figcaption>` balises à la place. Le tout devrait ressembler à ceci:

```html
  <figure>
      <img id="titoPicture" class="solidRoundBorders" src="tito.png" alt="Tito the dog" />          
      <figcaption>
      Guide touristique Tito!
      </figcaption>
  </figure>
```

L'élément `figcaption` est votre **légende**. Il peut aller au-dessus de l'élément `img` ou en dessous.

![Image de Tito avec une légende](images/figureAndCaption.png)

## \--- effondrer \---

## title: Pourquoi est-ce utile?

L'élément `figure` agit comme une sorte de **conteneur** pour votre photo et sa légende. Cela vous permet de les traiter comme une unité lors de la définition des styles.

Les regrouper logiquement contribue également à maintenir une bonne structure dans le code de votre site Web.

\--- /effondrer \---

Vous pouvez utiliser le code CSS pour le style `figure` et `figcaption` comme tout autre élément en utilisant des classes, ID, ou sélecteurs d'éléments. J'ajoute les règles suivantes pour supprimer l'espacement supplémentaire ajouté par le nouveau conteneur:

```css
  figure {margin-top: 0px; marge inférieure: 0px; marge gauche: 0px; marge-droite: 0px; }
```

### Notes secondaires

La page des attractions sur mon site Web est une liste de lieux à visiter. Je veux ajouter quelques notes sur la météo et comment se déplacer. Cette information n'appartient pas vraiment à l'élément `article` avec toutes les attractions. Ceci est un exemple de quand vous pouvez utiliser l'élément `aside`.

+ Aller à une page de votre site Web qui a un élément `article` dessus - J'utilise `attractions.html`.

+ **Outside** du `article` éléments, ajouter une ou plusieurs paires de `<aside> <\ de côté>` étiquettes contenant votre substance supplémentaire.

```html
  <aside class="sideNoteStyle">
      <h2>Se déplacer</h2>
      <h3>Train et bus</h3>
      <p>Vous pouvez vous rendre à la plupart des grandes villes en train depuis Dublin. Il y a beaucoup de bus qui font des excursions vers des endroits populaires et des attractions touristiques.</p>
      <h3>Car</h3>
      <p>La meilleure façon de se déplacer en dehors des villes est en voiture.</p>
    </aside>
    <aside class="sideNoteStyle">
      <h2>Météo</h2>
      <p>Le temps en Irlande est <span class="specialText">très imprévisible!</span> Il est préférable de <span class="specialText">préparer</span> pour tout type de temps, même si elle est une belle journée!</p>
  </aside>
```

## \--- effondrer \---

## title: Pourquoi est-ce utile?

Le ``, `article`, et d'autres conteneurs sont tous similaires. La seule vraie différence est dans le **signifiant**, c'est-à-dire, pour quoi les utilise-t-on.

Il est important d'utiliser des éléments HTML significatifs chaque fois que vous le pouvez. Il donne à votre site Web une meilleure structure et est particulièrement utile pour les personnes utilisant **lecteurs d'écran**.

\--- /effondrer \---

Avez-vous repéré l'autre élément là, `span`? C'est un tag spécial que vous pouvez utiliser juste pour ajouter du code CSS supplémentaire! Vous pouvez mettre n'importe quoi entre une paire de balises `span`. Il est utile pour des choses comme du style d' une **partie** du texte dans un paragraphe.

+ Ajoutez le code CSS suivant à votre feuille de style pour compléter le style pour le code HTML ci-dessus.

```css
  .sideNoteStyle {border: pointillé 1px violet; background-color: # c1ebec; rembourrage: 0,5em; marge: 0,5em; } .specialText {color: # FF4500; taille de police: plus grande; }
```

![Notes supplémentaires avec leur propre style](images/asidesStyled.png)

Sur la prochaine carte, vous allez apprendre à rendre la mise en page de votre site Web plus intéressante!

+ Pour vous préparer, créez une page qui contient un `article` et 2 `` éléments à l'intérieur des tags `<main> </main>`. Ou si vous préférez, vous pouvez travailler avec la page Attractions sur mon site Web.