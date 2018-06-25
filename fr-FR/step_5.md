## Tous dans une rangée

Sur cette carte, vous apprendrez quelques astuces pour organiser les choses **horizontalement** sur une page. D'abord, vous verrez comment centrer les choses. Ensuite, vous organiserez les éléments côte à côte dans une rangée.

+ Ajoutez les propriétés CSS suivantes à la classe `.card`:

```css
    marge-gauche: auto; marge-droite: auto;
```

Vous devriez voir les cartes se déplacer au centre de la page. En définissant les marges gauche et droite sur `auto`, vous pouvez faire en sorte que n'importe quel élément soit au milieu plutôt qu'à gauche.

![Les cartes apparaissent au milieu plutôt qu'à gauche](images/marginAuto.png)

+ Faites glisser le bord de la fenêtre du navigateur pour rendre la page plus étroite et plus large. Notez que les cartes restent centrées.

+ Mettez tous les liens de carte que vous venez de créer dans un nouvel élément de conteneur. Ce ne sera pas un `article` ou un `section`, mais un appelé `div`. Ceci est un conteneur polyvalent que vous pouvez utiliser pour regrouper des choses et faire de belles mises en page.

```html
    <div class="cardContainer">
```

+ Ajoutez le code CSS suivant dans votre feuille de style:

```css
    .cardContainer {display: flex; flex-wrap: envelopper justify-content: espace-autour; rembourrage: 10px; }
```

Voilà! Grâce à **Flex**, vos cartes sont maintenant affichées côte à côte!

+ Faites glisser le bord de votre fenêtre pour rendre le site Web plus large et plus étroit, et observez comment les cartes se déplacent pour s'adapter à la taille de la fenêtre, parfois jusqu'à la ligne suivante.

![Cartes disposées en deux rangées espacées régulièrement pour s'adapter à la largeur du navigateur](images/flexSideBySide.png)

+ Essayez de supprimer les propriétés `largeur` et `hauteur` de la classe `.card` et voyez ce qui se passe: `flex` assemble intelligemment les cartes comme un puzzle, gardant une hauteur uniforme sur tout ce qui est dans la même rangée.

![Cartes disposées côte à côte avec largeur automatique](images/flexAutoWidths.png)

Si vous avez un menu de navigation en haut de votre page, c'est un autre endroit où vous pouvez utiliser cette astuce. Votre menu doit être composé d'éléments de liste ((`li`) pour ce bit suivant. Si vous préférez, vous pouvez l'essayer avec mon site Web.

+ Trouvez les règles CSS pour le menu. Dans mon site Web, ce sont les blocs `nav ul`, `nav ul li`et `nav ul li a`.

+ Supprimer l'affichage de la propriété `: inline;` parmi les éléments de la liste. Ensuite, dans la liste `nav ul`, ajoutez:

```css
    affichage: flex; justify-content: flex-start;
```

![Menu avec éléments alignés à gauche](images/flexMenuStart.png)

Vous vous retrouvez avec à peu près le même menu, non? La chose cool à propos de `flex` est que vous pouvez contrôler la mise en page avec la propriété `justify-content`.

+ Changez la valeur de `justify-content` en `flex-end` et voyez ce qui se passe. Ou modifiez-le à `espace autour de` pour que les éléments du menu soient espacés régulièrement, comme vous l'avez fait pour les cartes.

![Menu avec des éléments espacés uniformément](images/flexMenuSpace.png)

![Menu avec les éléments alignés sur la droite](images/flexMenuEnd.png)

**`flex`** est un outil de mise en page assez puissant qui pourrait remplir toute une série de cartes Sushi - vous pouvez en apprendre plus à ce sujet au [dojo.soy/html3-flex](http://dojo.soy/html3-flex).