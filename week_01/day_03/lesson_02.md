
## 1 Introduction
On va d'abord chercher a donner la difference entre chiffrement et encodage. Puis vous apprendrez que l'humain est incapable de generer de l'aleatoire et de le retenir de maniere efficiente. Et donc qu'a partir d'une somme d'informations il est souvent possible de deviner le mot de passe de quelqu'un. Grace a une attque par dictionnaire.


## 2. Contexte
Les moldus font souvent la confusion entre un encodage et un algorithme de chiffrement.
Ce qui fait qu'ils ne font pas la difference entre un QR code/code barre et un hash de mot de passe.
Ce n'est pas un hasard si les deux 1ers ont "code" dans leurs noms.

## 3. Ressources
### 3.1 L'encodage
L’encodage est une operation de substitution grâce à un dictionnaire. Pour retrouver le texte original il faut juste connaitre le dictionnaire et comment il fonctionne. Pour rendre le message texte secret après encodage il faut cacher le dictionnaire et sa méthode d’utilisation.

Par exemple, c'est ce qu’on retrouve avec le “morse” ou encore le “braille” qui encodent caractère par caractère.
En informatique on retrouve le base64 ou encore les QR code et les codes barres. Ceux ci sont facilement decodable par n'importe qui. Donc n'importe qui peut les lire si il sait comment decoder. N'hesitez pas a essayer et lire les codes barres autour de vous. Vous pourriez avoir des surprises et peut etre decouvrir des failles de securite.
En general le but d’un encodage est d’uniformiser un message ou de réduire la place qu’il prend. Pas de le rendre secret.

- ici l’explication comment decoder un QRcode pass sanitaire
https://twitter.com/MathisHammel/status/1418846453590544396?s=20
- ici ce qu’il contient
https://twitter.com/cyclOptimiste/status/1400752758098219014?s=20

La meconnaissance de cette non securité peut amener à la creation d'article de blog genialissime. Ainsi nous avons pu avoir **[le meilleur billet de blog du monde](https://mango.pdf.zone/finding-former-australian-prime-minister-tony-abbotts-passport-number-on-instagram)** L'histoire d'un homme qui a pu obtenir le numero de passport d'un 1er ministre.

Parfois certains systeme informatique vont directement se reposer sur le fait que les gens ignorent que le QR code n'est pas sécurisé.
Comme le montre [cette video où des gens rentrent dans les duty free des aéroports sans billet veritable](https://www.youtube.com/watch?v=qnq0UfOUTlM)

### 3.2 Le chiffrement
Pour le chiffrement c’est un processus un peu différent.
Le plus important est de comprendre que toute operation de chiffrement cherche le plus possible a se rapprocher d'un processus qui genere de l'aleatoire.
Il y a un algorithme qui donne une série d'instructions à respecter afin de transformer une data ( qu’on peut représenter sous forme de chaîne de caractère )  en une autre chaine de caractère. Cet algorithme a besoin d’une `clé` pour ***chiffrer*** et ***déchiffrer*** le message.
Le processus peut être publiquement connu, seul la clé a besoin d'être secrète.
Ainsi rot13 est un algorithme de chiffrement car il l'algo est connue publiquement. Sa securite repose sur le fait que sa cle, le nombre 13, est secrete.
Le probleme est que cette cle est vraiment tres tres reduite en possibilite. Et aussi que la cle se repete beaucoup trop souvent.

L'une des faiblesses principales de l'être humain du coté cryptographie c'est son incapacité à créer de l'aleatoire et surtout à le retenir.
Vous pouvez regarder [cette video](https://www.youtube.com/watch?v=vVXbgbMp0oY) si vous avez besoin d'en etre convaincu.

Vous ne savez pas créer spontanemment des mots de passes ou des phrases de chiffrements completements aleatoires et encore moins les retenirs facilement.
Ceci va entrainer la creation de schemas connues, comme le rajout de ***123*** à la fin d'un mot de passe très utilisé comme ***password***. Pour les plus malins le ***123*** peut etre au dessus. Ou encore à l'écriture du mot de passe sur un post it accessible sur le bureau ou dans un [pastebin](pastebin.com) afin de le partager plus facilement. Il est aussi possible d'etre encore plus ***malin*** en remplaçant les lettres pas des chiffres. Par exemple **PA55W0RD**. Le genre de chose que personne ne peut deviner.
On observe donc qu'en general les contraintes que les sites rajoutent pour la création de mot de passe comme majuscule, minuscule, caractere special et chiffre ne
solidifient pas forcement les mots de passes. Les utilisateurs sont bien trop tenté de contourner ces regles pour ne pas trop changer leur mot de passe preferé
afin de réussir à le retenir.


## 3.3 Comment craquer des mots de passes aujourd'hui.

Craquer des mots de passes ça veut dire, en pratique, qu'on va chercher à trouver l'origine d'un hash.

Pour craquer des mots de passe on va utiliser ce qu’on vient d’apprendre. Non pas en trouvant une backdoor dans des algorithmes de hachages mais en utilisant le fait que les hommes sont incapables de générer de l'aléatoire par eux-même

Il existe alors 2 situations.
- Soit vous connaissez un mot de passe qui a appartenu à la même personne et donc vous espérez craquer le hash en utilisant un dérivé de ce mot de passe.
`password` peut devenir `password123`, `Pa55w0rd!!` etc..
- Soit vous partez de 0 et vous utilisez les différentes banques de mot de passe tel que “rockyou.txt” qui contiennent les mots de passe de gens.
Parfois ces listes de mots de passes sont ordonnés en fonction du pourcentage d'utilisation d'un mot de passe. Oui il n’y a pas que vous qui ait pensé à “password” comme mot de passe. [Comme le montre cet article de la Voix Du Nord](https://www.lavoixdunord.fr/1034831/article/2021-06-25/cybersecurite-doudou-ou-marseille-ces-mots-de-passe-les-plus-utilises-en-france).
Vous aurez ainsi les mots de passes à checker en 1er pour cracker un mot de passe puisque les plus utilisés en pourcentage grace à ce petit [classement de mot de passe](https://nordpass.com/json-data/top-worst-passwords/pdfs/worst-passwords-2020-fr.pdf).
Cette attaque s'apelle l'attaque par dictionnaire.



## 4 A Retenir

L'humain est incapable de generer de l'aleatoire et de le retenir facilement. Et si vous voulez avoir un mot de passe fort il faut absolument le generer aleatoirement. Donc utiliser un gestionnaire de mot de passe et un generateur de mot de passe.
