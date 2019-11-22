## Rendre ton menu adaptable

Un site Web **adaptable** s'adapte à la taille de l'écran pour qu'il soit toujours beau, que tu le regardes sur un ordinateur, un téléphone portable ou une tablette. Faisons en sorte que ton menu soit adaptable!

Tu commenceras avec les styles habituels: ce sera ton comportement **par défaut**.

## \--- collapse \---

## title: Que signifie "par défaut" ?

Les styles par défaut sont ton ensemble normal de règles de style. Ils sont appliqués quoi qu'il arrive, avant de vérifier des conditions particulières.

Tu peux ajouter du code qui vérifie ensuite la taille de l'écran et apporte des ajustements si nécessaire.

\--- /collapse \---

+ Ajoute les règles CSS suivantes à ton menu. Tu as probablement défini des couleurs et des bordures également; Je les ai laissés de côté pour économiser de l'espace ici! Si tu as déjà défini des règles CSS pour ton menu, ajoute ou modifie simplement les propriétés et les valeurs ci-dessous qui te manquent.

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

Avec le code CSS ci-dessus, ton menu conviendra mieux aux petits écrans. Ceci s'appelle développement **mobile-first**.

![Éléments de menu empilés verticalement sur un petit écran](images/responsiveMenuMobile.png)

## \--- collapse \---

## title: Que signifie "mobile-first" ?

Très souvent, lors de la programmation d'un site Web, tu utiliseras un écran d'ordinateur et tu définiras probablement tes styles en fonction de leur apparence sur cet écran.

Lorsque tu codes pour mobile first, tu choisis plutôt les styles par défaut adaptés aux petits écrans tels que les smartphones. Tu ajoutes ensuite du code supplémentaire pour effectuer des réglages pour des écrans plus grands.

Étant donné que de plus en plus de personnes naviguent sur Internet avec leur smartphone ou leur tablette plutôt que sur un ordinateur, il est recommandé de développer ton site Web dans cet esprit.

\--- /collapse \---

+ Ajoute maintenant le code suivant à ta feuille de style:

```css
    @media all and (min-width: 1000px) {
        nav ul {
            flex-direction: row;
            justify-content: space-around;
        }
    }
```

La première ligne de code ci-dessus vérifie la taille de la fenêtre du navigateur. Si la fenêtre est de **1000 pixels** de large ou plus, il appliquera toutes les règles de style à l'intérieur du bloc.

![Éléments de menu répartis uniformément sur une ligne sur un écran plus large](images/responsiveMenuMedium.png)

## \--- collapse \---

## title: Comment ça marche?

Le bloc contient de nouvelles valeurs pour seulement certaines propriétés du menu `nav ul`.

Lorsque la largeur de la fenêtre dépasse 1 000 pixels, ces nouvelles valeurs seront appliquées à la place de celles que tu as déjà définies pour `nav ul`.

Le reste des propriétés que tu as définies précédemment pour `nav ul` restera le même.

\--- /collapse \---

+ Si tu utilises Trinket pour écrire du code, il peut être utile de télécharger le projet afin de pouvoir le tester sur un écran de taille normale.

\--- challenge \---

## Défi: faire en sorte que ton menu s'adapte aux grands écrans

+ Peux-tu ajouter un autre bloc pour les écrans plus grands que **1600 pixels** , avec `flex-end` au lieu de `space-around` ?

![Éléments de menu à droite sur un écran large](images/responsiveMenuWide.png)

\--- hints \---

\--- hint \---

Le code suivant définit les propriétés flex pour les éléments de menu lorsque l'écran est supérieur à 1600 pixels:

```css
    @media all and (min-width: 1600px) {
        nav ul {
            flex-direction: row;
            justify-content: flex-end;
        }
    }  
```

\--- /hint \---

\--- /hints \---

\--- /challenge \---

Tu peux placer les règles CSS de ton choix dans des blocs tels que ceux-ci pour définir différents styles pour différentes tailles d'écran. Ce sera particulièrement utile lorsque tu feras plus tard des dispositions de grille CSS!