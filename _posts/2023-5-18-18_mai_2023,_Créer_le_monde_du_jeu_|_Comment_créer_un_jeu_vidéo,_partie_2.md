---
layout: post
title: 18 mai 2023, Créer le monde du jeu | Comment créer un jeu vidéo, partie 2
---

Pour ce tutoriel, j'utiliserai le moteur de jeu Unity. Consultez [ce](https://icethedev2.github.io/(13_April_2023)_How_to_Get_Started_with_the_Unity_Game_Engine-_Scene_and_Game_View/) tutoriel pour installer Unity et configurer un projet.

Je vais faire un Maze Runner dans cette série de tutoriels. Commençons!

## Le sol
Pour construire un sol sur lequel le joueur peut se tenir, nous pouvons utiliser un plan. Cliquez-droit dans la Hierarchy -> 3D Object -> Plane.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877734850/in/dateposted-public/" title="113"><img src="https://live.staticflickr.com/65535/52877734850_3dfc93559d_o.png"/></a>

Faisons-le gris avant de créer d'autres éléments afin que nous puissions le distinguer.

Pour colorer un objet dans Unity, nous avons besoin d'un matériau. Cliquez-droit dans l'onglet Project -> Create -> Meaterial.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877806903/in/dateposted-public/" title="114"><img src="https://live.staticflickr.com/65535/52877806903_a6cdc88afa_o.png"/></a>

Nommez le.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52876781842/in/dateposted-public/" title="115"><img src="https://live.staticflickr.com/65535/52876781842_2b0c12c77a_o.png"/></a>

Et changez son couleur (Albedo - le terme « Albedo » est un terme scientifique utilisé dans le domaine de la physique pour décrire le rapport entre la quantité de lumière réfléchie par une surface et la quantité de lumière qui tombe dessus).

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877748085/in/dateposted-public/" title="116"><img src="https://live.staticflickr.com/65535/52877748085_1f7d128939_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877528749/in/dateposted-public/" title="117"><img src="https://live.staticflickr.com/65535/52877528749_9d3a5a5a70_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877819013/in/dateposted-public/" title="118"><img src="https://live.staticflickr.com/65535/52877819013_f181fd61a4_o.png"/></a>

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877755840/in/dateposted-public/" title="119"><img src="https://live.staticflickr.com/65535/52877755840_06d8e2b073_o.png"/></a>

Enfin, glissez le matériau...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52876795597/in/dateposted-public/" title="120"><img src="https://live.staticflickr.com/65535/52876795597_f837193712_o.png" width="75" height="89" alt="120"/></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

...sur le plan dans la vue de la scène.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52876798087/in/dateposted-public/" title="121"><img src="https://live.staticflickr.com/65535/52876798087_0c8e1876c7_o.png" width="1123" height="642" alt="121"/></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

Et enregistrez vos modifications avec CTRL + S.

Réinitialisez également la transformation sur le plan pour la centrer sur les coordonnées 0, 0, 0.

Droit-cliquez sur le composant Transformer...

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877837083/in/dateposted-public/" title="122"><img src="https://live.staticflickr.com/65535/52877837083_b8d9ea4e52_o.png"/></a>

...et cliquez sur « Reset ».

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52876813212/in/dateposted-public/" title="123"><img src="https://live.staticflickr.com/65535/52876813212_027f3ed7ce_o.png" width="603" height="90" alt="123"/></a><script async src="//embedr.flickr.com/assets/client-code.js" charset="utf-8"></script>

## Le joueur
Créons une capsule pour le joueur.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877822950/in/dateposted-public/" title="124"><img src="https://live.staticflickr.com/65535/52877822950_6a0145e025_o.png"/></a>

Réinitialisez sa Transform.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877892613/in/dateposted-public/" title="125"><img src="https://live.staticflickr.com/65535/52877892613_65b9c81e06_o.png"/></a>

Tirez-le un peu vers le haut.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877828685/in/dateposted-public/" title="126"><img src="https://live.staticflickr.com/65535/52877828685_eae9459e22_o.png"/></a>

Et appliquez-y un matériau rouge.

<a data-flickr-embed="true" href="https://www.flickr.com/photos/197764307@N08/52877452051/in/dateposted-public/" title="127"><img src="https://live.staticflickr.com/65535/52877452051_511424ed82_o.png"/></a>

## Conclusion
Développer un jeu vidéo nécessite beaucoup d'efforts et de dévouement, mais avec les bons outils, les bons conseils et la motivation pour être cohérent (la cohérence est la chose la plus importante dans l'apprentissage de toute compétence), c'est un objectif réalisable. Dans les prochains articles, je vous expliquerai tout le processus, de la création du monde du jeu à la programmation du mouvement du joueur, en passant par l'ajout d'ennemis et d'obstacles et la mise en œuvre de la logique du jeu.

Unity est un excellent moyen de se lancer dans le développement de jeux. La meilleure façon d'apprendre n'importe quel langage de programmation ou moteur de jeu est de créer quelque chose qui vous passionne vraiment avec une grande cohérence.

([ChatGPT, un modèle de langage formé par OpenAI](https://chat.openai.com/) a aidé à écrire ce post)

Merci beaucoup d'avoir consulté mon blog, j'espère sincèrement que vous avez apprécié cet article, et attendez-vous à plus les jeudis après 15h00 UTC !
