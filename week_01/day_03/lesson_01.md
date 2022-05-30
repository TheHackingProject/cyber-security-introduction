# La cryptographie et la cryptologie

## 1. Introduction
Aujourd’hui on va voir un domaine un peu compliqué.
L’objectif du jour n’est pas de faire de vous des cryptographes pro.
C’est de vous faire entrevoir le domaine et surtout de vous convaincre que c’est une affaire de professionnel et que vous ne devriez pas essayer
d'être cette personne qui se croit plus malin que le monde entier en choisissant son secret de manière “astucieuse” ou en choisissant de chiffrer soit
même ses messages.
La cryptologie est la science des secrets. La cryptographie c'est l'art de rendre secret une information, en permettant aux personnes qui y ont le droit de quand même obtenir l'information.

## 2 Historique et Contexte.
De nos jours, si rien n'était un chiffre vous pourriez facilement lire tous les messages qu'envoie toute votre famille sur le réseau wifi de la maison ou sur le réseau de votre travail ou encore les réseaux publics du macdo ou dans le train. Vous pourriez aussi connaitre les messages envoye par des inconnus autour de vous avec leurs smartphones. Bref ça changerait radicalement la vie. 
Depuis l'Empire romain au moins, on a cherche a camoufler des messages avec des astuces diverses. Aujourd'hui nos algorithmes de chiffrements doivent s'adapter au fait qu'un ordinateur peut tenter des milliers de combinaison par seconde. Ceux-ci doivent donc être beaucoup plus performant qu'à une époque ou cet effort devait être à la main.

## 3 les bases de la cryptographie
### 3.1 Le code cesar


  La base de la base c'est vraiment la rotation ou le code César (c'est la même chose). Le plus connue étant le rot13 qui veut dire une rotation de 13 lettres sur l'alphabet. L’objectif est de cacher le message à transmettre en appliquant une rotation sur les lettres du message original. 
 Si on choisit une rotation de 1 ou de lettre `a` ( 1 ou `a` c’est la même chose vu que `a` c’est la 1re lettre de l’alphabet ) 
 La rotation est appliquée sur chaque lettre du message de la même manière. `a` devient `b` et `ab` devient `bc` etc.. 
 Donc si on choisit une rotation de 13

`a` devient alors `n` et `coucou les amis` devient `pbhpbh yrf nzvf`.

Le nombre qui sert a la rotation est appele la cle. C'est une notion universelle en cryptographie.

Du point de vue du moldu, le code César, c'est une bonne manière de se protéger. Le message semble indéchiffrable et va décourager les curieux.
En plus le seul secret à transmettre finalement c’est le nombre de rotations , ici `13`, et le message, lui, peut voyager publiquement et son message restera secret. Seulement si aujourd'hui `HTTPS` et vos messageries chiffrés ne fonctionnent pas sur ce principe c'est parce qu'il existe deux possibilités très simples pour le cracker. Deux options qui sont au final très abordables. 
- Finalement il n’y a que 26 rotations possibles. (l’alphabet)donc on peut assez vite toutes les tester et trouver le message. 
- - Chaque langage a une empreinte, et même à travers une rotation, l’empreinte peut être retrouvée. 

Une empreinte c’est la fréquence d’apparition d’une lettre dans la langue. En français la lettre “E” est très largement la plus utilisée. 

Voici le spectre de la langue française vu par fréquence d’apparition.

![analysis_frequency_french](https://raw.githubusercontent.com/bafraikin/ressource_thp_cursus_secu/master/ressources/jour_03/french_frequency_analysis.gif)


## 4. A Retenir

Si vous avez un texte que vous suspectez d’être en Français et que l'empreinte ressemble à celle que nous avons vue dans ce cours, mais que les lettres ne sont pas celles attendues, on va facilement pouvoir retrouver le sens du message original. 
Ainsi si la lettre la plus utilisée dans le message est très clairement le `r` alors on peut s'imaginer que le `r` a remplacé le `e` et donc que la rotation est de 13 car `r - e = m` ou encore `18 - 5 = 13`. 
À partir de la le message est déchiffrable. Simplement.

## 5. Pour aller plus loins

Vous allez peut-être vous dire, oui, mais si au lieu d’un seul chiffre j’utilise une suite de chiffres que je répète.
Du genre `123` que j’applique sur `abc` ça donnerait `bdf` 
Ici chaque chiffre de la suite de chiffre est appliqué séparément. Donc avec `123` sur `abc` on applique une rotation de `1` sur `a`, de `2` sur `b` et `3` sur `c`. 
Si on voulait continuer à chiffrer le message on recommencerait à partir de 1. Donc sur la string "abcd", ce serait une rotation de `1` qui serait appliquée sur la lettre `d` Ce système de chiffrage s'appelle le code `vigenere` 

Ainsi avec `123`, le message suivant:

```Du fait de la baisse de confiance présente, il convient d arrêter de stigmatiser les principales alternatives imaginables, à long terme.```

devient :

```Dv hajv df na ccitue eg cppfjcndg psgsfptf, kl dqnwkeov d btrfves fe tvihoauksft lfu pskndkpbnet clugroctjxet kmbiiocbmgs, b nooi tftmf.```

Ce texte a une empreinte qui ressemble à ça

![message_chiffre_analysis](https://raw.githubusercontent.com/bafraikin/ressource_thp_cursus_secu/master/ressources/jour_03/Screen%20Shot%202021-11-03%20at%201.27.12%20PM.png)


alors que l’empreinte du message original ressemble à ça

![message_analysis](https://raw.githubusercontent.com/bafraikin/ressource_thp_cursus_secu/master/ressources/jour_03/Screen%20Shot%202021-11-03%20at%201.26.41%20PM.png)

On voit ici que l'empreinte a été modifiée. C'est bien mieux en effet, mais ce n’est toujours pas infaillible. 
Puisque la clé que vous utilisez pour chiffrer est “ABC”. C’est une clé de longueur 3. Ce qui fait que tous les 3 caractères la clé se répète. 
Et donc tous les 3 caractères c’est la même rotation qui est effectuée, et donc tous les 3 caractères on retrouve l'empreinte de la langue originale. 
C’est le test de `Kasiski` ( vous pourrez vous la péter en soirée ) 

Si le texte est assez long, vous pourrez facilement déchiffrer le message original.
