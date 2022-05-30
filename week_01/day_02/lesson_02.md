#Jour 2 Google dorks et reconnaissance

## 1. Introduction
Il est possible sur internet de faire des recherche grace a des moteurs de recherches, mais savez vous que vous pouvez aussi rechercher directement qui est vulnerable a votre faille prefere ?

Aujourd’hui vous allez apprendre à explorer le web et à utiliser google comme vous ne l’avez jamais connu.
C’est aujourd’hui que vous allez vraiment retourner le web entièrement pour retrouver le site web vulnérable de vos rêves.
Vous utiliserez aussi les connaissances d’hier.

![image](https://media4.giphy.com/media/26n6WywJyh39n1pBu/giphy.gif)

## 2. Historique  et contexte
Les moteurs de recherche indexent d'eux meme les informations et les sites disponible sur le net. Et surtout, ils permettent de rechercher dans cette masse d'information qu'il possedent. Il permettent aussi de specifier precisement qu'elle type de contenu ou dans quelle zone vous voulez rechercher.
Ce mecanisme peut etre abuse et tourne a votre avantage.

## 3. Les googles dorks.
### 3.1 les operateurs
Aujourd'hui on va se concentrer sur Google.
Pour la recherche google le concept est simple:
La plupart des moldus utilisent la recherche dans un moteur de recherche de cette façon “recette flan” puis google leur remonte les meilleurs liens en fonction de son algorithme. Mais il existe des façons de lui imposer certains trucs dans les recherches.


Je vous laisse faire la recherche ***google advanced search operators***
sinon ce [lien](https://ahrefs.com/blog/google-advanced-search-operators/).

Tout ça va vous permettre de faire des choses dingues comme
```
intext: password inurl: pastebin.com
```
dans google
ou encore
```
inurl:thehackingproject.org intext:pares-feux
```
![power](https://pbs.twimg.com/media/Da-a-9SX0AAc_-C.jpg)



#### Sachez que chaque moteur de recherche possede ce genre de regle. Il faut juste aller chercher les mots cles magique et reproduire les logiques.



### 3.2 Comment l'utiliser

Si vous tapez
```
intitle: robots.txt inurl: lemonde.fr
```
dans Google.

Cette recherche vous permet de trouver l’url simplement du fichier robots.txt du site lemonde.fr
Où on y voit que lemonde.fr ne veut pas que google index l’url “/blog/\*/wp-login.php”.
C’est l’url de login des gens qui possèdent un blog sur le monde.  Et c'est assez logique que *Le Monde* ne veuille pas que ça soit referencé dans google. ça ferait desordre. L'url devient assez facilement retrouvable “https://www.lemonde.fr/blog/wp-login.php”.
Ce genre de mécanisme peut permettre de découvrir et d’obtenir des informations sur une cible.

Parfois rechercher avec l'opérateur “filetype: pdf inurl:entreprise.com” va permettre de retrouver des fichiers pdf qui sont accessibles sans se connecter et
parfois l’entreprise qui l'héberge ne le sait pas elle-même. Vous allez parfois pouvoir trouver des mots de passes, des documents interne, des fichiers de
configurations … etc.

[Il existe des sites qui font la recherche pour vous en fonction de ce que vous voulez](https://twitter.com/hackermaderas/status/1466468417364496391?s=20)


## 4. Points important a retenir.
C’est un outil très puissant. Il est important que vous en preniez la mesure.
Il existe même des sites qui compilent ces requêtes. [exploit-db](https://www.exploit-db.com/google-hacking-database) est le plus connu. Mais n'est pas forcement le meilleur.


### 5 Mais vous pouvez allez encore plus loins avec des regex

Visitez ce [blog](http://blog.k3170makan.com/2012/03/goodork-super-charging-your-google.html)
Ainsi nous pouvons effectuer la recherche suivante dans Google
```
-b "*.@thehackingproject.org"
```

C'est un truc un peu capricieux mais quand ça marche c'est fou

![too much power](https://ih1.redbubble.net/image.507832378.5398/pp,840x830-pad,1000x1000,f8f8f8.u2.jpg)

Cette petite recherche anodine va vous permettre de retrouver certains mail. Dont celui d'un Certain Charles Dacquay ou encore celui de Felix.

C’est très important que vous compreniez le potentiel de cet outil. C’est évidemment possible sur d’autres moteurs de recherche, mais chaque moteur de recherche possède ses propres variantes et ses propres mots clés.

