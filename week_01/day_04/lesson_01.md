
# Le monde des failles de securités connues et les exploits.

## 1. Introduction
Aujourd'hui vous allez enfin obtenir votre diplôme de `script Kiddie`. Vous allez decouvrir le monde des hackers du dimanche. Ceux ci sont  très dénigré par les "pro" parce qu'il ne codent pas leurs outils ou exploit. Mais il n'y aucune honte à avoir. C'est un monde à connaitre et maitriser pour bien comprendre l'environnement.

## 2. Historique et Contexte
Commençons par une petite histoire.

### 2.1 the shadow browkers
![pere castor](http://bibliotheque-ville-montluel.fr/wp-content/uploads/2018/02/bibli-actu_perecastor-1140x620.jpg)
En 2017 on apprend qu’un petit groupe de hacker se faisant appelé `The shadow brokers`, qui dit avoir hacké le NSA en 2013, publient une liste d'outils qu’ils ont volé chez eux.
Parmi ceux-ci des programmes utilisant des failles informatiques inconnues à l’époque ou à peine patchés.
Parmi les outils “EternalBlue”, qui s'appuit sur une faille Windows, un programme qui permet de se connecter à n’importe quel ordinateur windows non mis à jour à distance et d’y faire ce qu’on veut.
Publié en avril 2O17 l’outil volé est obsolète puisque le patch de Microsoft est paru en Mars 2017.
Le patch est intervenu comme par hasard en mars 2017, un mois juste avant la publication de l'outil hacké, alors meme que le hack où l'outil a été volé date de 2013.
Ce qui veut dire que la NSA avait entre ses mains cet outil et connaissance de cette faille Microsoft depuis au moins 2013.

Pour la suite de l'histoire c'est simple. Oui le patch est parru avant le leak mais tout le monde ne met pas à jour ses ordinateurs et cette faille permet à **Wanna Cry**, le premier `ransomware` publiquement connu de faire un carnage dans le monde entier.
Soit la NSA n’avait rien dit à Microsoft, soit ils avaient un accord.
On y apprend surtout que la NSA exploite des failles non patchés (ou potentiellement ajoutées à leurs demandes) en dépit des citoyens americains et du monde entier que ça met en danger.

```Vous pouvez écouter le podcast “https://darknetdiaries.com/episode/53/” sur les shadow brokers```

### 2.2 Exploit Wednesday
Cette histoire ce complete bien avec celle de la tradition du "Exploit Wednesday".
Cette histoire commence le mardi. Avec le "patch tuesday" de Microsoft. Tous les 1er mardi du mois, Microsoft publie une mise à jours de sécurité de Windows.
Comme Microsoft n'explique pas ou tres peu ce que contient la mise à jour. Lorsque celle ci survient, il s'ensuit une course effrené pour la decouverte de ce que contient celle ci.
Quelles lignes de codes ont été modifié et pourquoi ? Ceux qui participe à cette course le font pour beaucoups de raison.
Sachez juste que l'objectif est soit de protégé, soit d'attaquer les Windows qui ne seront pas mis à jours.
Ainsi quand Microsoft publie une mise à jours, Microsoft revèle dans le même temps une faille de securité qui affecte tout les ordinateurs qui ne sont pas à jours. C'est une faille facile à trouver, il faut juste gratter un peu pour la decouvrir.
Et ça marche de la même manière pour toutes les mises à jours. Un hacker va chercher à savoir ce qui a été patch pour exploiter ceux qui n'ont pas mis à jours.

```Ce n'est pas parce qu'une faille est patché qu'un programme qui exploite cette faille est obsolète.``` C'est la 1ere idée que je veux vous faire comprendre.

### 2.3 O-day
Il existe des gens qui recherchent toute la journée des nouvelles failles de securité, sur tout type de programme. La chose à savoir c'est qu'une faille a une valeur. Quelle soit exploité, quelle soit vendu ou quelle soit rançonné.
Il existe un marché des failles de securité. Sur ce marché on vend des "exploits" c'est à dire des programmes qui font office de `POC` ou `proof of concept` qui exploitent ces nouvelles failles avec une documentations et des explications pour reproduire la faille.
Ce marché sert un peu de menace pour justifier une rançon aupres des grosses boites. Si Apple, Google, Microsoft and co n'achetent pas la faille quand on leurs proposent ils peuvent se retrouver avec un virus dans leurs réseaux et/machine qui pourrait couter extremement cher en terme d'image et/ou en réparation.

Pour donner une idée, une faille pas encore connue qui permet de prendre le controle d'un ordinateur à distance a beaucoup plus de valeur qu'une faille qui permet de rediriger vers une [video youtube](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

Une faille pas connue s'apelle une faille 0-day. C'est à dire qu'elle est connue par la firme qui publie le programme, celui qui est affecté par la faille, depuis 0 jour. En gros la firme ne connait pas l'existance de la faille.
Une faille peut tres bien être vendu plusieur fois sur le Dark Web pendant des années, utilisé par des agences de renseignements pendant plusieurs années. Tant que l'entreprise developpeuse n'est pas au courant de celle ci, elle est toujours appelé une 0-day.

Les 0-days peuvent se vendrent assez cher en fonction de ce que la faille permet de faire.
Pour le reste, une fois que la faille est connue, elle sera classé en fonction de sa dangeresité, de son type, de qui elle affecte, et de ses prerequis.
Chaque faille connue à un code qui la defini. Ce code est appelé `CVE`. ou `Common Vulnerabilities and Exposures`. Le score de dangereusité est le `CVSS` ou `Common Vulnerability Scoring System`


### 2.4 Les CVE
`
The mission of the CVE® Program is to identify, define, and catalog publicly disclosed cybersecurity vulnerabilities.
`
Un code CVE est assez simple. Par exemple [CVE-2021-41340](https://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2021-41340). Il contient l'année de la decouverte de la faille et son numéro dans l'ordre d'apparition. ça donne une indication chronologique.

Pour un hacker, c'est tout aussi intéressant de savoir trouver des failles que de savoir récuperer des exploits de failles connues pret à être utiliser tout de suite.
C'est ce boulot là que vous allez faire aujourd'hui. Vous allez chercher sur internet des failles connues et des exploits que vous pourrez utiliser.


### 2.5 Les programmes de bug bounty
C'est ainsi que sont né les programmes de `bug bounty`. C'est comme ça que s'appelle les offres de certaines boites pour acheter des failles de securité par encore connue. Ainsi Apple va publier une gamme de prix pour des types de failles de sécurité precises. Microsoft le fera aussi etc etc ..

Il existe des plateformes qui en publient et si demain vous êtes chercheurs en sécurité peut être pourrez vous en avoir besoin pour savoir chez qui il est plus interessant de rechercher si une faille existe. Par exemple [bugcrowd](https://bugcrowd.com/programs) ou encore [yeswehack](https://yeswehack.com/programs) et [hackerone](https://www.hackerone.com/)



## 3.  How to attack

Mais on ne s'y prend pas n'importe comment pour attaquer une entreprise ou une machine.
Il y a 7 étapes à respecter pour bien faire la chose je vous laisse [les decouvrirs](https://www.beyondtrust.com/blog/entry/7-steps-cyber-attack-can-protect-windows-privileged-accounts)


Je vais juste vous conseiller des outils pour reussir chaque partie de ce que vous allez avoir besoin de faire aujourd'hui.

### 3.1 Reconnaissance:
On va chercher à savoir de quoi la cible est composé, à cartographier notre cible.
Pour cela on peut tres bien rechercher dans le code à la main, utiliser des programmes qui le feront pour nous ou deviner.
Pour ce qui est de notre cas, on va cartographier à partir du navigateur internet. Vous ne pourrez pas decouvrir tout les programmes de mapping aujourd'hui.
Le plus performant pour notre cas d'usage est "Wappalyzer", c'est une extension de navigateur firefox ou chrome qui donne une liste de librairie et de programme que le site sur lequel vous vous baladez utilise pour se construire.  L'outil analyse juste le code source de la page et remonte les informations qu'il a trouvé.
Certains sites vous laisserons plus d'information que d'autres. C'est déjà un critère filtrant. Plus on a d'information sur une cible potentiel, plus on est capable de l'attaquer car on connait de vecteur potentiel d'attaque.

### 3.2 Scanner:
Ensuite nous allons rechercher des vulnerabilités connues, ou des failles techniques specifique (c'est à dire laissé par un developpeur distrait) qui serait sur le site internet ciblé ou des failles logiques.
  - Pour trouver des failles techniques specifique on utilise des scanners qui testent des failles typiques ( xss, csrf, sqli, lfi, etc... ), ou on teste nous meme, et souvent on mixe les deux.
  - Pour les failles logiques je vous laisse lire [cette article](https://www.vaadata.com/blog/fr/que-sont-les-failles-logiques-sur-les-applications-web/)
  - Puis vous pouvez chercher les failles connues qui affecte les logiciels et librairies utiliser par la cible. Pour cela plusieurs voie sont possible.
    Chercher sur twitter un post d'un hacker qui veut revendiquer la paternité d'une vulnerabilité, chercher sur github un exploit, chercher les CVE qui affecte un logiciel, fouiller [www.exploit-db.com/](https://www.exploit-db.com/). Parfois meme chercher "hack wordpress" sur Google donne de super resultat. Bref ce n'est pas ce qui manque. Mais il y a un vrai travail à effectuer entre trouver un exploit qui fonctionne sur la cible qu'on vise, le faire fonctionner et l'utiliser à son avantage.
Encore une fois, un systeme qui sera mis à jours seront donc moins vulnerable

### 3.3 Acces et élévation de privilège:
L'idée est de faire fonctionner les failles qu'on a trouvé et tourner à son avantage cette situation pour obtenir des droits qu'on est pas sencé avoir. Puis d'utiliser ces nouveaux droits pour s'elever de plus en plus haut dans la hierarchie des droits. Une fois qu'on a un niveau de droit suffisant on peut passez aux étapes suivantes. Pour y arriver on utilise des failles qui sont desormais accessible et exploitable. Souvent on peut apprendre de nouvelles informations qui vont vous permettre d'envisager d'autres types d'attaques.
Pour sécuriser ceci il faut d'abord être au courant de cette étape. Il va falloir se placer à la place d'un attaquant et d'imaginer pour chaque utilisateur et ses droits existant ce qui pourrait lui permettre d'élever ses privileges.
C'est à partir de là qu'on a crée la règle "zero trust / no one will be trusted" qui peut se traduire par la politique de la confiance 0. Il faut limiter les possibilités et les connaissances d'une personne à son stricte minimum nécessaire pour effectuer sa tache.
C'est pour cette raison qu'on cherche à limiter au maximum les possibilités d'administration d'un utilisateur et à fractionner celles ci en plusieurs niveaux et rôle different. Afin de compliquer la tache du hacker qui aurait reussi à se connecter avec ce compte. C'est ce qu'on appelle la défense en profondeur ou "defense in depth". Pour faire simple c'est chercher à sécuriser autant que possible, chaque processus et chaque machine qui le compose. Le problème de ce genre de manoeuvre c'est que ça peut se faire au detriment d'une fluidité d'utilisation.
C'est un difficile équilibre à maintenir, limiter au maximum les abus et donc les usages ; tout en permettant aux utilisateurs de travailler et d'utiliser l'outil avec satisfaction.
C'est à cause de ce fait que la sécurité en entreprise est souvent vu comme un ajouteur d'entropie. Que la sécurité va empecher les employés de travailler efficacement ensemble. Sachez qu'une bonne sécurité limite au maximum son empreinte sur l'utilisateur. Elle a vocation à le proteger pas à le contraindre. De toute façon si vous contraignez trop un utilisateur il va souvent chercher à contourner votre système pour réussir à travailler efficacement.
En bref c'est la partie qui est la plus compliqué à sécuriser.
C'est pour ceci qu'en tant qu'attaquant il est; soit toujours possible d'elever ses privileges, soit plus utile de convaincre un employé de vous aider. Parce qu'un employé connaitra les manoeuvres et les petits tricks pour parvenir à votre but et il peut y etre habitué.

## 4. A retenir
Il existe des failles de sécurité meme lorsqu'un logiciel ou un systeme est à jours. On en découvre tous les jours et vous pouvez soit etre vulnerable parce que vous n'avez pas mis à jours votre système. Soit parce que la personne qui vous cible à les moyens d'acceder à une faille que le monde ne connait pas encore. Si une personne utilise ce genre de faille contre vous c'est que vous n'etes pas n'importe qui.
La conclusion de ceci c'est que vous n'etes pas en sécurité, JAMAIS.
Une fois que vous le savez, que vous l'avez accepter, vous saurez vous proteger.

## 5. Pour aller plus loins

Vous pouvez explorer le modèle `0 trust`, qui se veut la réponse à la menace 0-day. C'est une methode qui part du principe que vous ne pouvez faire confiance à aucun des maillons de votre infrastructure humaine ou technique.

**Tout vas, un jour ou l'autre, défaillir.**

Vous pouvez aussi vous interesser au `chaos engineering` qui permet d'éprouver votre modèle 0 trust.
