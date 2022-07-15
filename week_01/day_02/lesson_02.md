# Google dorks et reconnaissance
L'utilisation pro de Google Dorks.

## 1. Introduction
Il est possible sur internet de faire des recherches grâce à des moteurs de recherches, mais savez-vous que vous pouvez aussi rechercher directement qui est vulnérable à votre faille préférée ?

Aujourd’hui vous allez apprendre à explorer le web et à utiliser Google comme vous ne l’avez jamais connu. C’est aujourd’hui que vous allez vraiment retourner le web entièrement pour retrouver le site web vulnérable de vos rêves. Vous utiliserez aussi les connaissances d’hier.

![image](https://media4.giphy.com/media/26n6WywJyh39n1pBu/giphy.gif)

## 2. Historique  et contexte

Les moteurs de recherche indexent d'eux-mêmes les informations et les sites disponibles sur le Net. Et surtout, ils permettent de rechercher dans cette masse d'information qu'ils possèdent. Ils permettent aussi de spécifier précisément quel type de contenu ou dans quelle zone vous voulez rechercher. Ce mécanisme peut être abusé et tourné à votre avantage.


## 3. Les googles dorks.
### 3.1 les opérateurs

Aujourd'hui, on va se concentrer sur Google.

Pour la recherche Google le concept est simple: la plupart des moldus utilisent la recherche dans un moteur de recherche de cette façon “recette flan” puis Google leur remonte les meilleurs liens en fonction de son algorithme. Mais il existe des façons de lui imposer certains trucs dans les recherches.


Je vous laisse faire la recherche ***google advanced search operators***
sinon ce [lien](https://ahrefs.com/blog/google-advanced-search-operators/).

Tout ça va vous permettre de faire des choses dingues avec Google comme :

```txt
intext: password inurl: pastebin.com
```

ou encore

```txt
inurl:thehackingproject.org intext:pares-feux
```
![power](https://pbs.twimg.com/media/Da-a-9SX0AAc_-C.jpg)


**Sachez que chaque moteur de recherche possède ce genre de règles. Il faut juste aller chercher les mots-clés magiques et reproduire les logiques.**



### 3.2 Comment l'utiliser

Si vous tapez dans Google :

```txt
intitle: robots.txt inurl: lemonde.fr
```

Cette recherche vous permet de trouver l’URL simplement du fichier robots.txt du site lemonde.fr Où on y voit que lemonde.fr ne veut pas que google indexe l’URL “/blog/\*/wp-login.php”. C’est l’URL de login des gens qui possèdent un blog sur le monde. Et c'est assez logique que *Le Monde* ne veuille pas que ça soit référencé dans Google. Ça ferait désordre. L'URL devient assez facilement retrouvable “https://www.lemonde.fr/blog/wp-login.php”. Ce genre de mécanisme peut permettre de découvrir et d’obtenir des informations sur une cible.

Parfois rechercher avec l'opérateur “filetype: pdf inurl:entreprise.com” va permettre de retrouver des fichiers PDF qui sont accessibles sans se connecter et
parfois l’entreprise qui l'héberge ne le sait pas elle-même. Vous allez parfois pouvoir trouver des mots de passe, des documents internes, des fichiers de
configurations … etc.

[Il existe des sites qui font la recherche pour vous en fonction de ce que vous voulez](https://twitter.com/hackermaderas/status/1466468417364496391?s=20)


## 4. Points importants à retenir.
C’est un outil très puissant. Il est important que vous en preniez la mesure.
Il existe même des sites qui compilent ces requêtes. [exploit-db](https://www.exploit-db.com/google-hacking-database) est le plus connu. Mais n'est pas forcement le meilleur.


### 5 Mais vous pouvez allez encore plus loin avec des regex

Visitez ce [blog](http://blog.k3170makan.com/2012/03/goodork-super-charging-your-google.html)
Ainsi nous pouvons effectuer la recherche suivante dans Google
```
-b "*.@thehackingproject.org"
```

C'est un truc un peu capricieux mais quand ça marche c'est fou

![too much power](https://ih1.redbubble.net/image.507832378.5398/pp,840x830-pad,1000x1000,f8f8f8.u2.jpg)

Cette petite recherche anodine va vous permettre de retrouver certains mails. Dont celui d'un Certain Charles Dacquay ou encore celui de Félix.

C’est très important que vous compreniez le potentiel de cet outil. C’est évidemment possible sur d’autres moteurs de recherche, mais chaque moteur de recherche possède ses propres variantes et ses propres mots clés.

