---
layout: post
title: 4 mai 2023, Principes de base des scripts Unity
---

## 🔍Introduction
Bienvenue dans la partie 4 du guide du débutant d'IceTheDev2 sur Unity !

## Création d'un Script
Il y a 2 façons de créer un script dans Unity.

Vous pouvez droit-cliquer dans un vide espace du doussier Assets dans l'onglet Project, sélectionner Create > C# Script...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855668248/in/dateposted-public/" title="99"><img src="https://live.staticflickr.com/65535/52855668248_a4f541723b_o.png"/></a>

...Nommez-le...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855399379/in/dateposted-public/" title="100"><img src="https://live.staticflickr.com/65535/52855399379_1982d3133b_o.png"/></a>

...et faites glisser dans le Cube. Enregistrez la scéne avec CTRL + S et cliquez une fois sur le Cube dans la Hierarchy pour ouvrir son Inspector:

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855401849/in/dateposted-public/" title="101"><img src="https://live.staticflickr.com/65535/52855401849_be89836592_o.png"></a>

Nous pouvons voir que « BasicScript» est attaché au Cube en tant que composant.

Pour supprimer un composant, droit-cliquer sur son titre dans l'Inspector...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855403849/in/dateposted-public/" title="102"><img src="https://live.staticflickr.com/65535/52855403849_eb9280fc29_o.png"/></a>

...et sélectionnez « Remove Component ».

Pour supprimer un composant parmi les actifs du projet, cliquez dessus une fois et appuyez sur la touche « DEL ».

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52854654252/in/dateposted-public/" title="103"><img src="https://live.staticflickr.com/65535/52854654252_070fde0632_o.png"/></a>

Cliquez sur « Delete » ou appuyez sur « Enter ».

Vous pouvez également droit-cliquer sur le script y cliquer sur « Delete ».

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855628730/in/dateposted-public/" title="104"><img src="https://live.staticflickr.com/65535/52855628730_401b8dce90_o.png"/></a>

L'autre façon de créer un script est d'ouvrir l'Inspector de l'objet...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52854657817/in/dateposted-public/" title="105"><img src="https://live.staticflickr.com/65535/52854657817_3cedcf4524_o.png"/></a>

...cliquez sur « Add Component », écrivez le nom du script et appuyez deux fois sur « Enter ».

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855242026/in/dateposted-public/" title="106"><img src="https://live.staticflickr.com/65535/52855242026_12208ac23c_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855687768/in/dateposted-public/" title="107"><img src="https://live.staticflickr.com/65535/52855687768_4d1713a0e8_o.png"/></a>

## Ouvrir un Script
Dans l'exemple suivant, j'utiliserai Visual Studio 2022. Cependant, vous pouvez utiliser n'importe quel éditeur de code que vous voulez.

Tout d'abord, assurons-nous d'avoir sélectionné le bone éditeur de code. Allez dans « Edit » en haut.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855422149/in/dateposted-public/" title="108"><img src="https://live.staticflickr.com/65535/52855422149_78b11072e2_o.png"/></a>

...sélectionnez « Preferences... » et assurez-vous que vous êtes sur l'onglet « External Tools ».

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855696403/in/dateposted-public/" title="109"><img src="https://live.staticflickr.com/65535/52855696403_2c23330019_o.png"/></a>

Regardez l'External Script Editor. Si ce n'est pas votre éditeur préféré, sélectionne-le et modifiez-le.

Pour ouvrir un script, vous avez 2 options similaires à celles de création du script. Vous pouvez soit double-cliquer sur le script dans les Assets du project soit dans l'Inspector de l'objet:

## Syntaxe des Scripts
Une fois le script ouvert, vous obtiendrez quelque chose de similaire à ceci:
```
using System.Collections;
using System.Collections.Generic;
using UnityEngine;

public class BasicScript : MonoBehaviour
{
    // Start is called before the first frame update
    void Start()
    {
        
    }

    // Update is called once per frame
    void Update()
    {
        
    }
}
```

Parlons de chaque section une par une.

### 'using'
En C# (C-Sharp, le langage de progrq,,qtion utilisé par Unity) « using » (« utiliser ») signifie que on importe, indiquant au programme que on utilisera une certaine classe.

System.Collections fournit des classes qui implément diverses collections d'objets; telles que des listes, des files d'qttente et des tables de hachage.

System.Collections.Generic fournit des classes de collections génériques, qui fournissent un moyen sûr et efficace de stocker et de manipuler des groupes d'objets.

UnityEngine fournit toutes les classes et fonctions spécifiques au développement du moteur de jeu Unity. Il comprend des classes pour créer des objets de jeu, manipuler leurs propriétés, contrôler leur comportement et rendre des graphiques.

### public class BasicScript : MonoBehaviour ???
1. public - Cet mot-clé spécifie que la classe est accessible à partir de tout autre code du projet.

2. class - Cet mot-clé est utilisé por définir une classe, qui est un plan de création d'objets.

3. BasicScript - C'est le nom de la classe. Vous pouvez choisir n'importe quel nom pour votre classe, tant qu'il respecte les [conventions de dénomination C#](https://learn.microsoft.com/en-us/dotnet/csharp/fundamentals/coding-style/coding-conventions).

4. : MonoBehaviour - Il s'agit de la classe de base dont la classe BasicScript hérite. MonoBehaviour est une classe fournie par Unity qui vous permet d'attacher des scripts à des objets de jeu et d'interagir avec eux lors de l'exécution. En héritant de MonoBehaviour, la classe BasicScript accède à toutes les méthodes intégrées de MonoBehaviour, telles que Start(), Update(), FixedUpdate(), etc.

### void Start()? void Update??
`void` est un mot clé en C# utilisé pour indiquer qu'une méthode (telle que `Start()` et `Update()`) ne renvoie pas de valeur.

`Start()` est appelé lorsque la scène est chargée pour la première fois. Il peut être utilisé pour établir des références à d'autres objets, initialiser des variables, etc.

`Update()` est appelé à chaque image. Il peut être utilisé pour mettre à jour la position, la rotation ou l'échelle des objets en fonction de l'entrée de l'utilisateur, de la physique, répondre à l'entrée de l'utilisateur, vérifier les collisions, animer l'objet, mettre à jour les variables, etc.

### Commentaires
Un commentaire est un morceau de texte qui est ignoré par le compilateur. Utilisez-les pour expliquer pourquoi quelque chose est fait, et non ce que fait le code. Le code doit être explicite.

Dans l'exemple ci-dessus, les commentaires expliquent aux nouveaux utilisateurs quand `Start()` et `Update()` sont appelés.

Généralement, le code est écrit et lu par des personnes qui connaissent le langage et n'ont pas besoin de ce genre de commentaires.

Pour déclarer un commentaire, utilisez deux barres obliques (//).

## Tester un Script
Pour tester un script, `Debug.Log()` est couramment utilisé. Cette méthode écrit un message dans la console.

Essayez d'écrire `Debug.Log("Hello, World!");` dans la méthode `Start()`. N'oubliez pas d'utiliser les guillemets doubles (""), qui sont nécessaires en C#. "Bonjour le monde!" est une chaîne (morceau de texte) qui est un argument dans la méthode. N'oubliez pas de terminer par un point-virgule (;), comme cela est requis en C#.

N'oubliez pas de sauvegarder le script (CTRL + S) et lancez le jeu en cliquant sur le bouton de lecture en haut.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855717808/in/dateposted-public/" title="110"><img src="https://live.staticflickr.com/65535/52855717808_92f9ee8fca_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855666990/in/dateposted-public/" title="111"><img src="https://live.staticflickr.com/65535/52855666990_f5989cf3c4_o.png"/></a>

(Votre Unity ne sera pas rouge. Je montrerai dans un prochain article comment passer au rouge en mode jeu.)

Vous pouvez également essayer d'écrire `Debug.Log("Hello, World!");` dans la méthode `Update()`.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52855666990/in/dateposted-public/" title="111"><img src="https://live.staticflickr.com/65535/52855666990_f5989cf3c4_o.png"/></a>

Au fait, CTRL + P est le raccourci pour entrer en mode lecture.

## Conclusion
Les scripts sont une partie essentielle du développement de jeux. Ils peuvent être utilisés pour manipuler les positions, les rotations et les échelles des objets, et ils seront plus cool avec [variables](https://mammothinteractive.com/variables-in-c-unity-tutorial/) et [loops](https ://learn.unity.com/tutorial/loops-z2b#).

Unity est un excellent moyen de se lancer dans le développement de jeux. La meilleure façon d'apprendre n'importe quel langage de programmation ou moteur de jeu est de créer quelque chose qui vous passionne vraiment avec une grande cohérence.

([ChatGPT, un modèle de langage formé par OpenAI](https://chat.openai.com/) a aidé à rédiger ce message)

Merci beaucoup d'avoir consulté mon blog, j'espère sincèrement que vous avez apprécié cet article et attendez-en plus le jeudi après 15h00 UTC.
