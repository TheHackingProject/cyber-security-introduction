# Chiffrement et encodage

## 1 Introduction
On va d'abord chercher à donner la différence entre chiffrement et encodage. Puis vous apprendrez que l'humain est incapable de générer de l'aléatoire et de le retenir de manière efficiente. Et donc qu'à partir d'une somme d'informations il est souvent possible de deviner le mot de passe de quelqu'un. Grâce à une attaque par dictionnaire.

## 2. Contexte
Les moldus font souvent la confusion entre un encodage et un algorithme de chiffrement. Ce qui fait qu'ils ne font pas la différence entre un QR code/code barre et un hash de mot de passe. Ce n'est pas un hasard si les deux 1ers ont "code" dans leurs noms.

## 3. Ressources
### 3.1 L'encodage
L’encodage est une opération de substitution grâce à un dictionnaire. Pour retrouver le texte original il faut juste connaitre le dictionnaire et comment il fonctionne. Pour rendre le message texte secret après encodage il faut cacher le dictionnaire et sa méthode d’utilisation.

Par exemple, c'est ce qu’on retrouve avec le “morse” ou encore le “braille” qui encodent le caractère par caractère. En informatique on retrouve le base64 ou encore les QR codes et les codes barres. Ceux-ci sont facilement décodables par n'importe qui. Donc n'importe qui peut les lire s’il sait comment décoder. N'hésitez pas à essayer et lire les codes barres autour de vous. Vous pourriez avoir des surprises et peut-être découvrir des failles de sécurité. En général le but d’un encodage est d’uniformiser un message ou de réduire la place qu’il prend. Pas de le rendre secret.

- [ici l’explication comment décoder un QRcode pass sanitaire](https://twitter.com/MathisHammel/status/1418846453590544396?s=20)
- [ici ce qu’il contient](https://twitter.com/cyclOptimiste/status/1400752758098219014?s=20)

La méconnaissance de cette non-sécurité peut amener à la création d'articles de blog génialissime. Ainsi nous avons pu avoir **[le meilleur billet de blog du monde](https://mango.pdf.zone/finding-former-australian-prime-minister-tony-abbotts-passport-number-on-instagram)** L'histoire d'un homme qui a pu obtenir le numéro de passeport d'un 1er ministre.

Parfois certains systèmes informatiques vont directement se reposer sur le fait que les gens ignorent que le QR code n'est pas sécurisé. Comme le montre [cette vidéo où des gens rentrent dans les duty free des aéroports sans billet véritable](https://www.youtube.com/watch?v=qnq0UfOUTlM)

### 3.2 Le chiffrement
Pour le chiffrement c’est un processus un peu différent. Le plus important est de comprendre que toute opération de chiffrement cherche le plus possible à se rapprocher d'un processus qui génère de l'aléatoire. Il y a un algorithme qui donne une série d'instructions à respecter afin de transformer une data ( qu’on peut représenter sous forme de chaîne de caractère ) en une autre chaine de caractère. Cet algorithme a besoin d’une `clé` pour ***chiffrer*** et ***déchiffrer*** le message.

Le processus peut être publiquement connu, seule la clé a besoin d'être secrète. Ainsi rot13 est un algorithme de chiffrement, car  l'algo est connu publiquement. Sa sécurité repose sur le fait que sa clé, le nombre 13, est secrète. Le problème est que cette clé est vraiment très très réduite en possibilités. Et aussi que la clé se répète beaucoup trop souvent.



### 3.3 Le hashage
Le hashage est une opération cryptographique qui permet d'obtenir à partir d'une donnée un hash. Les caracteristiques d'un bon algorithme de hash sont 
- L'abscence de collision : deux données differentes ne sont pas censées donner le même hash  
- Le fait qu'il ne fonctionne que dans un sens : on ne peut pas obtenir la donnée original à partir du hash 
- Le fait qu'une même donné donnera toujours le même hash

ps: bonus pour les hashs les plus sécurisé - deux données très proches donnent deux hashs qui ne se ressemblent pas du tout.

Cette technologie est beaucoups utilisé pour pouvoir stocker des mots de passe. Le fonctionnement est assez simple. 
L'objectif est de vérifier qu'on possède le mot secret, celui qui genère un hash précis. Si le mot de passe est assez complexe il n'est pas bruteforçable. Seule la personne qui connait le mot d'origine peut génerer le hash en question. Donc la base de donnée peut stocker le hash qui à été generé à partir du mot de passe sans problème et sans crainte de divulger les mots de passe de ses utilisateurs. Lors de la demande de connexion de l'utilisateur on lui demande de soumettre un mot, et si le mot genère le même hash que celui stocké dans la base de donnée à coté du login soumis, alors c'est que ce doit être le bon utilisateur. 


Vous pouvez vous amusez avec ce [générateur de hash](https://hashes.com/en/generate/hash) pour essayer de comprendre à quoi cela ressemble.

### 3.4 Faiblesse de l'esprit humain
Vous ne savez pas créer spontanément des mots de passe ou des phrases de chiffrements complètement aléatoires et encore moins les retenir facilement. Ceci va entrainer la création de schémas connus, comme le rajout de ***123*** à la fin d'un mot de passe très utilisé comme ***password***. Pour les plus malins, le ***123*** peut être avant ***password***. Ou encore à l'écriture du mot de passe sur un post it accessible sur le bureau ou dans un [pastebin](pastebin.com) afin de le partager plus facilement. Il est aussi possible d'être encore plus ***malin*** en remplaçant les lettres par des chiffres. Par exemple **PA55W0RD**. Le genre de chose que personne ne peut deviner.

On observe donc qu'en général les contraintes que les sites rajoutent pour la création de mot de passe comme majuscule, minuscule, caractère spécial et chiffre ne solidifient pas forcément les mots de passe. Les utilisateurs sont bien trop tentés de contourner ces règles pour ne pas trop changer leur mot de passe préféré afin de réussir à le retenir.


### 3.5 Comment craquer des mots de passe aujourd'hui
L'une des faiblesses principales de l'être humain du côté cryptographie c'est son incapacité à créer de l'aléatoire et surtout à le retenir. Vous pouvez regarder [cette vidéo](https://www.youtube.com/watch?v=vVXbgbMp0oY) si vous avez besoin d'en être convaincu.

Craquer des mots de passe, ça veut dire, en pratique, qu'on va chercher à trouver l'origine d'un hash. Pour craquer des mots de passe, on va utiliser ce qu’on vient d’apprendre. Non pas en trouvant une backdoor dans des algorithmes de hachages, mais en utilisant le fait que les hommes sont incapables de générer de l'aléatoire par eux-mêmes.

Il existe alors 2 situations.

- Soit vous connaissez un mot de passe qui a appartenu à la même personne et donc vous espérez craquer le hash en utilisant un dérivé de ce mot de passe. `password` peut devenir `password123`, `Pa55w0rd!!` etc..
- Soit vous partez de 0 et vous utilisez les différentes banques de mot de passe tel que “rockyou.txt” qui contiennent les mots de passe de gens.

Parfois ces listes de mots de passe sont ordonnées en fonction du pourcentage d'utilisation d'un mot de passe. Oui il n’y a pas que vous qui ayez pensé à “password” comme mot de passe. [Comme le montre cet article de la Voix Du Nord](https://www.lavoixdunord.fr/1034831/article/2021-06-25/cybersecurite-doudou-ou-marseille-ces-mots-de-passe-les-plus-utilises-en-france). Vous aurez ainsi les mots de passe à checker en 1er pour cracker un mot de passe puisque les plus utilisés en pourcentage grâce à ce petit [classement de mot de passe](https://nordpass.com/json-data/top-worst-passwords/pdfs/worst-passwords-2020-fr.pdf). Cette attaque s'appelle l'attaque par dictionnaire.


## 4 Points importants à retenir
L'humain est incapable de générer de l'aléatoire et de le retenir facilement. Et si vous voulez avoir un mot de passe fort, il faut absolument le générer aléatoirement. Donc utiliser un gestionnaire de mot de passe et un générateur de mot de passe.
