# Le pair programming
Le pair programming est une technique de développement informatique où vous serez 2 personnes à coder sur le même ordinateur.

## 1. Introduction

Le pair programming est une technique qui permet de bien s'améliorer en code, utilisée par de nombreuses startups. Le concept est simple : deux personnes sont sur un seul ordinateur, l'une d'entre elles tient le clavier et tape, l'autre lui donne son avis. **Au final les deux codent et prennent les décisions ensemble**. Ensuite, elles alternent régulièrement (à chaque exercice ou commit par exemple).

Nous allons voir quelques guidelines pour faire du pair programming à The Hacking Project.

## 2. Historique

Le pair programming est une technique assez récente pour faire du code, utilisée principalement en entreprise agile (le code sera plus propre) et en école (génial pour apprendre).

## 3. La ressource

### 3.1. Les bases du pair programming

#### 3.1.1. Prendre 2 moussaillons

Idéalement, il faut mettre en pair-programming des personnes de niveau proche afin qu'elles aient plus de probabilité de bloquer sur les mêmes sujets : **c'est en bloquant puis en trouvant soi-même la solution qu'on apprend** !

Il y a généralement à The Hacking Project trois types de niveau :

-   Le code c'est nul / PLS absolue / déprime totale
-   Pas facile, mais je survis
-   Je me débrouille

Nous t'invitons à estimer ton niveau et à trouver une personne de ton niveau.

En cas de pair de programmation réunissant une personne très à l'aise et une personne en PLS, gardez en tête que :

1.  Il est préférable que le meilleur des deux évite d'avoir le clavier. Sinon il risque de taper les solutions trop vite et de larguer l'autre.
2.  Il faut que la personne la plus à l'aise laisse à l'autre quelques minutes pour chercher chaque solution. Si on offre la solution sur un plateau systématiquement, le débutant aura l'impression de comprendre mais ne pratiquera pas réellement : il ne va pas progresser.
3.  Faites preuve de patience et prennez bien le temps d'expliquer ce que vous faites. L'un comme l'autre !

#### 3.1.2. Créer un repo Github commun

Le repo GitHub va te permettre de basculer le code d'un ordi à l'autre. Pour cela, il va falloir que tu fasses des `git clone`, `git push`, `git pull`. N'hésite pas à revenir au cours de Git qui explique cela plus en détails.

#### 3.1.3. Utiliser un seul ordinateur pour 2

Une personne va taper le code sur son ordinateur en fonction de ce que les deux décident de faire. L'échange est au cœur de cet exercice ! Il faut discuter de votre compréhension des problèmes, débattre des meilleures façons de le résoudre, être attentif aux fautes de l'autre et au final produire du code à deux.

#### 3.1.4. Alterner

Il est important d'alterner d'ordinateur et donc de personne qui tape. Celui qui écrivait peut alors `git push` son code, et son partenaire fait un `git pull` pour récupérer les modifications. Vous alternez et changez d'ordinateur.

### 3.2. Des outils pour faire du pair-programming

Le pair-programming peut être fait à distance, grâce aux nombreux outils de télétravail. Pour la partie audio, nous te conseillons de passer par ton outil vocal préféré : Discord, téléphone, Zoom, etc.

Pour la partie partage d'ordinateur, il existe plein d'extensions pour les éditeurs de texte qui permettent de partager du travail. Joel Falconer les a recensés [dans un article sur SitePoint](https://www.sitepoint.com/collaborative-coding-tools-for-remote-pair-programming/). Nous te conseillons vivement d'un installer un pour la formation.

## 4. Points importants à retenir

Pour faire du pair programming efficace, il faut deux personnes de niveau similaire qui travaillent sur un seul ordinateur, en alternant entre celui qui écrit et celui qui dicte.

Cette technique est au cœur de la méthodologie THP d'apprentissage en groupe : essayez de vous y tenir autant que possible. **L'ensemble des projets validants doivent être faits en pair-programming.**

___
⚠️ ALERTE ERREUR COMMUNE

Les personnes ayant un bon niveau de code ont tendance à ne pas voir l'intérêt du pair-programming : on file le clavier à quelqu'un de moins à l'aise et alors qu'on sait exactement quoi taper, lui met trois plombes à trouver où sont les accolades "{ }" … 😤

Pourtant c'est une erreur ! Ne pas coder dans son coin, c'est l'occasion d'aider son camarade à comprendre mais surtout de s'aider soi-même en se forçant à expliquer ce qu'on fait et pourquoi on le fait. **C'est une méthode très efficace pour comprendre en profondeur un concept et surtout le retenir !** Ça porte même un nom : [la méthode Feynman](https://blog.pandanote.com/fr/methode-feynman-apprendre-comprendre-memoriser/).

___

## 5. Pour aller plus loin

[L'article Wikipédia](https://en.wikipedia.org/wiki/Pair_programming?oldformat=true) explique pas mal les avantages et défauts du pair-programming, ainsi que les différents types de pair-programming.