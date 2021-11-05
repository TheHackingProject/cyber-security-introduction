# GUIDELINES DE RÉDACTION RESSOURCES ET PROJETS

## 1.Objectifs
### 1.1. Introduction
The Hacking Project est une formation se basant sur un principe simple : nous donnons des projets concrets et quotidiens à nos élèves, avec des ressources les aidant à effectuer ces projets. Les projets font réfléchir et encouragent la discussion entre élèves.

Voici quelques exemples de couples projets ressources donnés aux élèves :

- découvrir le HTML/CSS grâce à la première moitié du célèbre cours de Mathieu Nebra, puis recréer le site [bettermotherfuckingwebsite](http://bettermotherfuckingwebsite.com/)
- suivre un tuto simple expliquant une library de scrapping, puis aller sur le site [CoinMarketCap](https://coinmarketcap.com/all/views/all/) pour récupérer toutes les valeurs de cryptomonnaies et les stocker dans un hash
- lire une ressource à propos d'une library d'authentification puis installer cette dernière dans une app rails pour avoir un système d'authentification

Le fait de proposer des projets concrets sans (trop) tenir les élèves par la main leur permet d'apprendre à chercher, ce que nous encourageons beaucoup.

De une à deux fois par semaine, nous imposons aux élèves des "projets validants". Ce sont des projets qu'ils devront rendre sur notre plateforme via un lien vers leur GitHub. Le lendemain dans la matinée, les élèves vont se corriger entre eux : chaque élève devra corriger deux personnes, puis sera corrigée par deux personnes, selon des critères de correction définis par nous.

### 1.2. Ce que l'on retrouve dans une journée d'apprentissage
Chaque jour, des projets seront donnés aux élèves. Pour les réaliser, des ressources seront données. Plusieurs fois par semaine, des projets seront à rendre. Ceci est en général le mardi et le jeudi. Jamais le mercredi, ni le vendredi. Certaines semaines peuvent avoir qu'un seul projet validant.

Pour chaque journée validante, il faut rédiger entre 10 et 15 guidelines de correction. Les guidelines permettent :

- aux étudiants de se corriger entre eux et de s'assurer qu'ils travaillent un minimum
- aux étudiants de se poser les bonnes questions ("ah tiens tu as fait comme ça, c'est malin")
- aux étudiants de former un esprit de groupe et de rencontrer des gens intéressants

Les guidelines sont à répondre par `oui` ou par `non` et posent très peu de doute quant à la réponse :

- `Est-ce qu'il y a bien un fichier index.html ?`
- `Est-ce qu'il y a bien un fichier style.css ?`
- `Est-ce que le fichier de CSS est bien branché depuis le fichier HTML ?`
- etc

Enfin, les guidelines sont réparties équitablement dans le travail à faire du projet : 3-4 questions pour s'assurer que l'élève a travaillé un minimum, 4-5 questions pour s'assurer qu'il a fait la première moitié du projet, 4-5 questions pour être allé aux 3/4, puis 4-5 questions pour finaliser le projet.

Cela va en général assez vite :)

## 2. Sur le fond
### 2.1. Les projets
Les projets sont le nerf de la guerre à The Hacking Project. Ces derniers doivent être challengeants sans être impossibles.

À The Hacking Project les élèves apprennent via la pratique. Les élèves passent plus de temps à plancher sur des projets concrets que de suivre des cours au fond de la classe près du radiateur. Ainsi, la meilleure façon pour enseigner OmniAuth est de l'installer sur son application, grâce à un petit cours qui explique l'intérêt de la technologie avec (si besoin) un petit tutoriel sur son branchement à une application.

Nous sommes donc "project driven". Il faut penser chaque journée comme un projet à réaliser. Les ressources sont là en guise de soutien à la réalisation du projet. En général il vaut mieux passer beaucoup de temps à penser et écrire un projet que de rédiger les ressources.

### 2.1.1. Deux types de projets

Il y a principalement deux types de projets :

- les projets normaux (ex: faire une todo list en AJAX, ajouter une interface admin à son site, recréer en HTML/CSS la page d'accueil de google.com). Ces projets ont des consignes claires et un objectif réalisable. Ils demandent aux élèves de résoudre des problèmes concrets et ces derniers apprendrons beaucoup du fait de ne pas être tenus par la main
- les projets pas à pas (assez rares) (ex: découvrir un framework avec un pas à pas). Ces projets sont un peu plus qu'un tuto Udemy : l'objectif est de faire un pas à pas où nous ne donnons pas tout le code. C'est notamment très pratique pour découvrir un univers très nouveau aux élèves avec plein de concepts en tout genre

### 2.1.2. Un double enjeu

Les projets de The Hacking Project doivent répondre à un double enjeu :

- enseigner une notion importante aux élèves.
- être amusants et concrets. Cette notion importante est trop souvent oubliée des écoles qui vont enseigner la POO en déclarant une classe chien qui va aboyer. Oui on apprend, mais on peine à voir l'intérêt.

Les meilleurs projets sont ceux arrivants à conjuguer ces deux aspects.


### 2.1.3. De la liberté mais pas trop
Il arrive dans des formations en informatique d'avoir comme projet "aujourd'hui reproduisez votre CV en HTML, faites-le comme vous voulez". Ces sujets sont malheureusement trop libres et en donnant cette liberté les gens ne sauront pas quoi faire. Un peu comme si je disais "pour apprendre à faire un jeu vidéo, fais un jeu vidéo". En soit c'est pas faux, mais trop permissif : est-ce qu'une page en HTML basique faite en 5 minute est acceptée en guise de projet ? Comment je gère le design de la page, si je n'y connais rien ?

Pour reprendre l'exemple du CV en HTML/CSS, nous demandons aux élèves de reproduire le plus fidèlement possible la page d'accueil de Google. Ces derniers auront un but précis à atteindre ce qui a un effet "cap".

Ainsi, nous ne donnons que très rarement des projets "aujourd'hui faites [_quelque chose de vague_], comme vous voulez".

Il est tout à fait possible (et recommandé) de laisser les élèves la liberté de choisir telle ou telle techno, mais il faut leur donner un cap précis. Le choix du chemin qu'ils prendront leur appartient.


### 2.1.4. Inscrit dans une vision plus large
C'est parfait de penser les projets comme des entités à part entière, mais il ne faut oublier que ces derniers sont inscrits dans un plus grand contexte : l'apprentissage à la compétence choisie par le parcours.

Ainsi certains projets peuvent sembler ne pas répondre à nos différents enjeux, mais s'inscrivent dans notre vision. Par exemple nous aimons bien faire faire aux élèves une chose un peu relou à faire bas-niveau, afin de leur montrer la magie de tel techno qui leur mâche le travail. Cela permet de faire deux choses :

- la première est de démontrer par la pratique comment telle techno fait gagner du temps
- la seconde est d'enlever une partie de l'effet "magie noire sous le capot" : en voyant le modèle bas-niveau, ceci permettra de démystifier une bonne partie de la bibliothèque haut niveau

### 2.1.5. L'humour est une arme redoutable
Il arrive souvent qu'il faut passer par des projets classiques. En effet, c'est dur d'apprendre l'algorithmie sans faire un bon vieux bubble sort. Pour ceci, afin d'agrémenter notre cursus, nous n'hésitons pas à utiliser l'humour dans nos projets. C'est un humour qui est basé sur le pince-sans-rire et sur les blagues dramatisant des situations simples.



### 2.1.6. Structure d'un projet
Voici la structure type d'un projet :

```markdown
# Titre du projet
Description du projet au format texte et en 1 paragraphe max (pas plus)

## 1. Introduction
Introduction qui leur explique dans les grandes lignes le projet.

## 2. Le projet
### 2.1. Première étape du projet
Ici expliquer la première étape du projet.

### 2.2. Seconde étape du projet
Ici expliquer la seconde étape du projet.

etc..

## 3. Rendu attendu
 Un récapitulatif de ce que nous attendons du projet.
```

Nous avons donné dans le dossier `assets/` un bon exemple de projet.


## 2.2. Les ressources
Les ressources permettent de réaliser les projets. Nous y expliquons les concepts importants tout en apportant un recul nécessaire pour donner aux élèves un pragmatisme qui permet de peser le pour et le contre de chaque solution. Le but est de leur expliquer un concept, tout en leur apportant un maximum de contexte sur le pourquoi de ce concept. Cela leur donnera des bases qui leur permettront de survivre en territoire hostile.



### 2.2.1. Comment expliquer ?
Une ressource va expliquer le pourquoi d'une technologie, puis donner un petit tutoriel sur comment obtenir les bases de la dite technologie. Généralement cela suffit.

Il arrive très régulièrement que certaines ressources en ligne soient excellentes ou que la documentation suffise. Dans ces cas là, pas besoin de réinventier la roue : il suffit de rediriger les étudiants vers cette ressource et la contextualiser.

#### 2.2.1.1. Ressources externes
Voici généralement les ressources externes que l'on retrouve dans un cours THP :

- Une vidéo explicative : c'est un excellent format de ressource très apprécié par les élèves. N'hésitez pas à chercher sur Youtube en priorité
- Un article de blog tuto : rien ne vaut un bon vieux pas à pas avec les étapes à copier-coller
- La page Wikipedia : un bon moyen d'aller plus loin. Attention, une page Wikipedia est en générale très sèche et ne convient que très rarement si vous cherchez à expliquer un concept

### 2.2.2. Structure d'une bonne ressource
Voici la structure type d'une ressource :

```markdown
# Titre de la ressource
Description de la ressource au format texte et en 1 paragraphe max (pas plus)

## 1. Introduction
Une introduction sur la ressource.

## 2.Historique et contexte
Cette partie peut être plus ou moins longue. Elle explique l'histoire ou le contexte sur la notion que l'on veut enseigner.

## 3. La ressource
Cette partie est le nerf de la ressource, elle expliquera les notions de cette ressource.

### 3.1. Première sous partie
blabla

### 3.2. Deuxième sous partie
blabla

## 4. Points importants à retenir
La ressource en quelques points importants.

## 5. Pour aller plus loin
Quelques éléments en ligne pour aller plus loin
```

Nous avons donné dans le dossier `assets/` un bon exemple de ressource.

## 3. Sur la forme
Nous utilisons le format markdown. Les fautes et coquilles sont à proscrire : relisez-vous et/ou utilisez un correcteur orthographique. THP possède [Antidote](https://www.antidote.info/fr) donc il est possible de demander à l'équipe de faire une repasse pour éviter le gros des fautes.

### 3.1. Quelques éléments de markdown
#### 3.1.1. Les images
Il est tout à fait possible d'intégrer une image dans le cours. Au format markdown cela donnera cela :

```markdown
![](https://i.imgur.com/uIozOrU.jpg)
```

⚠️ Afin d'éviter de les perdre, les images devront être importées sur [Imgur](https://imgur.com/). Pour avoir le lien, il faudra faire : clic droit -> `Copier le lien de l'image`. Cette dernière sera au format : `https://i.imgur.com/CODE.EXT` et non pas au format `https://imgur.com/gallery/CODE`.

___
⚠️ **ALERTE ERREUR COMMUNE** ⚠️

Les images importées dans ce répository et intégrées via `![](../images/truc.png)` (ou équivalent) ne marcheront pas dans notre cours. Veuillez donc les intégrer sur Imgur et récupérer le lien.
___

#### 3.1.2. :smiley: et emojis
Il est possible de mettre des smileys pour agrémenter le cours. Cependant, notre convertisseur ne convertira pas `:smiley:` en 😀. Pour avoir des smileys au format 😊☺️😄 garanti, il faut les écrire au format unicode. Grosso modo, prenez un éditeur de texte ultra basique (bloc-notes par exemple) et mettez-y votre emoji. Si ce dernier se met au format 😊☺️😄 c'est le bon format, s'il se met au format `:smiley:`, ce n'est pas bon.

[Voilà une page](https://www.iemoji.com/emoji-cheat-sheet/all) qui permet la recherche des unicode ou des emoji en toutes lettres et qui permet de copier-coller directement l'unicode (première colonne):


### 3.2. Erreurs communes et conseils de rédaction
Voici quelques erreurs et conseils que nous allons vous donner :

#### 3.2.1. Inclusion
THP a été historiquement fondée sur des cours à l'informatique. Dans ce domaine, nous nous devons montrer une certaine inclusivité quant à notre style rédactionnel. De plus, [la science a l'air de montrer qu'un style inclusif a ses vertus](https://www.bunkerd.fr/ecriture-inclusive/). Cependant, nous refusons d'utiliser le point médian qui est souvent employé à tord et à travers.

Voici les quelques techniques que nous utilisons pour écrire de manière inclusive.

##### 3.2.1.1. Mots épicènes
Les mots épicènes sont les mots qui peuvent être utilisés pour les deux sexes : personne, élève, dév (on a inventé ce terme pour remplacer développeur/développeuse), collègue, individu, etc.

Ne dites pas :

> Tu es curieux

Dites plutôt :

> Tu es une personne curieuse

##### 3.2.1.2. Paraphrases
Rien ne vaut une bonne paragraphe qui permet d'éviter d'avoir à interpeller la personne qui va vous lire.

Ne dites pas :

> Alors, tu es partant ?

Dites plutôt :

> Alors, tu es en pleine forme ?

#### 3.2.2. "Du coup"
"Du coup" [n'existe pas](https://www.lefigaro.fr/langue-francaise/expressions-francaises/2017/09/22/37003-20170922ARTFIG00008-du-coup-ne-faites-plus-la-faute.php) en langue française. Enfin, pas dans l'utilisation que les gens en font. Cette expression est à proscrire.


#### 3.2.3. Ponctuation et espaces
En français, il faut toujours mettre un espace insécable avant `:`. Écrire "voici une liste: liste" n'est pas correct.

📚👓 **Astuce** : si un caractère de ponctuation s'écrit sans lever le stylo (`.`, `,`), il faut mettre un espace après uniquement. Si un caractère s'écrit en levant le stylo une fois (`:`, `;`, `?`, `!`), il faut un espace avant **et** après.

#### 3.2.4. Style trop parlé
Le style du cours de THP est à la limite du familier : on s'adresse à la personne comme si l'on s'adressait à un ami. Cependant, il ne faut pas tomber dans les écueils d'utiliser un langage trop "parlé".

Ne dites pas :
> T'as pas compris ? Bah c'est normal ! Je vais te montrer un exemple (pour que tu comprennes mieux hein 😉)

Dites plutôt :
> Tu ne comprends pas ? Pas de soucis ! Je vais te montrer un exemple pour que tu comprennes mieux ☺️


(_Il est à noter que cet exemple est là juste pour montrer une bonne et mauvaise forme dans langage familier. Dans le fond, utiliser trois phrases pour dire que l'on va donner un exemple est contraire à notre volonté d'aller droit au but_)

#### 3.2.5. Majuscules accentuées
En français, contrairement à ce que laissent penser les gens qui ne savaient pas comment écrire au clavier `À`, la casse ne prime pas sur l'orthographe. En gros, les majuscules doivent être accentuées si accent il faut mettre.

[Sinon, cela peut donner des résultats inattendus](https://i.redd.it/nz1wi9lckm461.jpg).

## 4. Comment c'est organisé
Voici à quoi ressembre l'arborescence d'un dossier de cours :

```
.
├── assets
│   ├── lesson_example_01.md
│   └── project_example_01.md
├── week_01
│   ├── day_01
│   │   ├── day_presentation.txt
│   │   ├── day_title.txt
│   │   ├── lesson_01.md
│   │   ├── lesson_02.md
│   │   ├── project_01.md
│   │   └── project_02.md
│   ├── day_02
│   │   ├── day_presentation.txt
│   │   ├── day_title.txt
│   │   ├── correction_guidelines.txt
│   │   ├── lesson_01.md
│   │   ├── lesson_02.md
│   │   ├── project_01.md
│   │   └── project_02.md
│   ├── day_03
│   ├── day_04
│   ├── day_05
│   ├── week_presentation.txt
│   └── week_title.txt
├── week_02
├── week_03
├── week_04
├── week_05
├── week_06
├── week_07
├── week_08
├── week_09
├── week_10
├── week_11
├── week_12
└── README.md
```

Chaque semaine sera un dossier à la racine :

- `week_01/` pour la semaine 1
- `week_02/` pour la semaine 2
- `week_06/` pour la semaine 6
- `week_10/` pour la semaine 10
- and so on

Chaque semaine aura :

 - Un fichier `week_title.txt` qui aura le `title` de la semaine (Ex : "Introduction à l'algorithmie")
 - Un fichier `week_presentation.txt` qui aura la `presentation` de la semaine (Ex: "Cette semaine tu vas apprendre à faire de l'algorithmie en faisant notamment de la récursion, des algorithmes de tri, des structures de données. Tu finiras par une intelligence artificielle imbattable au morpion !")
 - 5 jours qui auront chacun 1 dossier :
  - `day_01/` pour le jour 1
  - `day_02/` pour le jour 2
  - `day_03/` pour le jour 3
  - `day_04/` pour le jour 4
  - `day_05/` pour le jour 5

Chaque jour aura au moins :

 - Un fichier `day_title.txt` qui aura le `title` du jour (Ex : "Faire ta première page web")
 - Un fichier `day_presentation.txt` qui aura la `presentation` du jour (Ex: "Tu vas apprendre HTML et CSS, deux langages qui te permettront de réaliser ta première page web").

S'il y a des ressources, mettre les fichiers `lesson_XX.md`. S'il y a des projets, mettre les fichiers `project_XX.md`.

Enfin, les corrections (s'il y a besoin) sont mises dans un fichier `correction_guidelines.txt`. ⚠️ Les corrections sont mises au jour du projet validant, non pas au jour des corrections. Ainsi, si la journée de mardi est validante, les corrections seront faites le mercredi, et le fichier `correction_guidelines.txt` sera mis dans le dossier `day_02/`.
