## collage de photos

Sur cette carte, vous apprendrez à utiliser CSS pour positionner exactement les éléments HTML et faire un collage photo.

![](images/photoCollageWithText_wide.png)

+ Ajoutez un `div` à votre page et mettez-y autant d'images que vous le souhaitez. Donnez les valeurs `div` et `img` elements `id`.

```html
    <div id="photoBox" class="relPos">
        <img id="imgHorse" class="absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <img id="imgTeaCat" class="absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
    </div>
```

Les photos apparaîtront les unes après les autres sur la page Web, dans l'ordre où elles apparaissent dans votre code.

+ Dans votre fichier CSS, ajoutez la classe CSS suivante pour les éléments dans le `div`: 

```css
    .absPos {position: absolue; }
```

+ Ensuite, vous devez ajouter la propriété `position: relative;` au conteneur lui-même et définissez une taille pour cela. Cela fait en sorte que les positions des autres éléments sont définies **rapport à** (c'est-à-dire, à l'intérieur) du conteneur.

```css
    .relPos {position: relative; } #photoBox {largeur: 800px; hauteur: 400px; }
```

+ Créez ensuite un ensemble de règles de style pour chacun des éléments en utilisant **sélecteurs id** pour définir leurs tailles (`propriétés width` et / ou `height` ) ainsi que leurs positions exactes.

Pour définir la position d'un élément, vous pouvez utiliser quatre propriétés: `gauche`, `droite`, `top`et `bas`. Ils représentent à quelle distance chacun des bords devrait être du bord du parent. Utilisez soit `top` ou `bottom` pour la position verticale, et soit `left` ou `right` pour la position horizontale.

![Diagramme montrant comment les propriétés haut, gauche, bas et droite se rapportent au conteneur parent](images/cssPositionProperties.png)

+ Choisissez des positions exactes pour chacune de vos images et utilisez l'une des propriétés `left`, `right`, `top`et `bottom` pour définir ces positions dans vos règles CSS. Par exemple, ce code place l'image du chat à 100 pixels du haut et 60 pixels de la gauche:

```css
    #imgTeaCat {width: 250px; haut: 100px; à gauche: 60px; }
```

Remarque: Les valeurs de position peuvent également être négatives! Si vous utilisez une valeur négative, elle repoussera l'élément à l'extérieur du conteneur, quel que soit le bord que vous avez spécifié.

### Faire chevaucher les choses

Vous voudrez peut-être faire chevaucher certaines images. Mais comment choisissez-vous celui qui va en haut?

+ Choisissez deux images et donnez-leur des positions qui les font se chevaucher.

+ Ajouter une propriété supplémentaire, `z-index: 10;` à l'un d'entre eux, puis ajoutez `z-index: 7;` à l'autre.

+ Jetez un oeil sur le résultat sur votre page Web.

![](images/horse10Cat7.png)

+ Échangez maintenant les valeurs de `z-index` , de sorte que `7` et `10` soient l'inverse. Voyez-vous une différence sur votre page Web?

![](images/horse7Cat10.png)

## \--- effondrer \---

## title: Comment fonctionne z-index?

La propriété `z-index` vous permet de décider comment deux ou plusieurs éléments doivent se chevaucher. La valeur peut être n'importe quel nombre entier.

L'élément avec le **la plus élevée** nombre se termine sur **top** de la pile, ou, autrement dit , à tout le **avant**. L'élément avec le nombre le plus élevé suivant est derrière cela, et devant les autres, et ainsi de suite, jusqu'à ce que vous arriviez à l'élément avec le nombre le plus bas, qui apparaît à l'arrière derrière tous les autres éléments.

\--- /effondrer \---

Vous pouvez positionner n'importe quel élément HTML de cette manière, pas seulement des images. Par exemple, vous pouvez utiliser un élément `p` pour ajouter du texte sur une photo.

\--- défi \---

## Défi: faire un collage de photos

+ Essayez de créer votre propre collage de photos comme celui ci-dessous! Utilisez le positionnement exact avec différentes valeurs de `z-index` pour obtenir l'effet de chevauchement comme vous le souhaitez.

\--- astuces \---

\--- indice \---

Ci-dessous le code HTML pour le collage de photos sur mon site Web en Irlande. Il y a six photos et un texte à l'intérieur d'un `div`.

```html
    <div id="photoBox" class="relPos">
        <img id="imgStreet" class="collagePhoto absPos" src="ireland-1474045_640.jpg" alt="Irish town" />
        <img id="imgTeaCat" class="collagePhoto absPos" src="ireland-2360846_640.jpg" alt="Even cats drink tea in Ireland!" />
        <img id="imgCoast" class="collagePhoto absPos" src="cattle-2369463_640.jpg" alt="Cows at the coast" />
        <img id="imgTrees" class="collagePhoto absPos" src="ireland-2614852_640.jpg" alt="Tree tunnel" />
        <img id="imgSheep" class="collagePhoto absPos" src="sheep-456989_640.jpg" alt="Sheep on the road" />
        <img id="imgHorse" class="collagePhoto absPos" src="connemara-pony-512028_640.jpg" alt="Connemara pony" />
        <p id="photoText" class="absPos">Irlande</p>
    </div>
```

\--- / indice \---

\--- indice \---

Voici les règles CSS qui définissent les positions de chacune de mes images dans le collage:

```css
    #imgHorse {width: 120px; haut: 200px; à gauche: 390px; indice z: 10; } #imgSheep {width: 200px; haut: 100px; à gauche: 20px; indice z: 8; } #imgCoast {width: 150px; haut: 250px; à gauche: 10px; indice z: 5; } #imgTrees {width: 110px; haut: 65px; à gauche: 205px; indice z: 9; } #imgTeaCat {width: 250px; haut: 210px; à gauche: 160px; indice z: 7; } #imgStreet {width: 180px; haut: 90px; à gauche: 310px; indice z: 6; } #photoText {font-famille: "brush script MT"; couleur: vert clair; taille de police: 4em; à gauche: 35px; haut: 15px; indice z: 20; }
```

\--- / indice \---

\--- indice \---

Voici les classes CSS que j'ai utilisées:

```css
    .collagePhoto {bordure: 1px blanc uni; } .relPos {position: relative; } .absPos {position: absolue; }
```

\--- / indice \---

\--- /astuces \---

![Collage de photos avec du texte sur le dessus](images/photoCollageExample.png)

\--- /défi \---