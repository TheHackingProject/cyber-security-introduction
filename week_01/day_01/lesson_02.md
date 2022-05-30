
# Jour 1 Breached database

## 1. Introduction
Vous savez sans aucun doute qu’il faut utiliser un mot de passe **différent et fort sur chaque compte** que vous créez. SPOILER: très très peu de personnes le font. Et ce pour plusieurs raisons que vous connaissez sûrement.
Il arrive parfois qu’un site web sur lequel vous vous êtes inscrit soit hacké et que la base de donnée où vos identifiants de connexion sont rangés soit volées.
Aujourd'hui nous allons apprendre a reperer et denicher les mots de passes exposes.

## 2. Historique et Contexte
En théorie votre mot de passe est protégé par un algorithme de hachage ([explication](https://fr.wikipedia.org/wiki/Fonction_de_hachage_cryptographique)) qui le rend impossible à deviner quand il se trouve dans une base de donnee.
Seulement parfois ce n’est pas le cas; parce que le site est codé avec le cul, d’autres fois votre mot de passe est trop simple (ex: *coucou123*) et il est très rapide de tester toutes les possibilités pour trouver votre mot de passe une fois que le hacker a le hash. Ou parfois encore vous utilisez sans le savoir un mot de passe que quelqu’un d’autre utilise ( ex: *password* ) celui-ci va donc donner le même hash, hash qui aura peut être déjà leak ailleurs, sera déjà connu et aura déja été cracké et publié. Ce qui permettra de retrouver votre mot de passe sans effort.

Sachant cela, on arrive parfois a des ecosystemes un peu cocasse. ![compte_revendu](https://github.com/bafraikin/ressource_thp_cursus_secu/blob/master/ressources/jour_01/vente_password.png?raw=true)

Ici un compte disney+ à été volé puis les identifiants ont été revendu sur aliexpress.
Donc pour 2 balles environs vous pouvez avoir acces à un compte disney+ à vie si le compte que vous avez acheté continue de payer et bien sur ne change jamais de mot de passe. Ici le payeur a change son mot de passe.

Ici faut comprendre que le mot "volé" est un peu fort. Il est plus probable qu'en réalité le vendeur d'aliexpress a eu acces à une base de donnée d'identifiant volée. A fait tourner un programme qui teste chaque identifiant sur une batterie de site ( disney+, spotify, etc ..). Et apparement se permet de revendre les identifiants qui fonctionne encore.

Vous êtes libre de lire cet article de blog qui illustre assez bien une autre façon de se servir de ces comptes volés. Ici des concours like/follow twitter et de la revente de compte twitter avec beaucoup de follower. [-> article passionnant <-](https://medium.com/@klakinoumi/comment-en-participant-%C3%A0-9500-concours-en-trois-mois-sur-twitter-jai-d%C3%A9couvert-un-trafic-de-3355795b0783).

Bref votre mot de passe est peut-être dans la nature.

## 3. Ressources

### 3.1. Hashes.com
Il existe un site qui peut aider un peu pour dechiffrer les hashs les plus connus ou les plus faibles. Donc si un mot de passe est tres utilise, il vous suffira de soumettre son hash dans ce site. J'ai nomme [Hashes.com](https://hashes.com)
Par exemple si vous rentrez le hash **a109e36947ad56de1dca1cc49f0ef8ac9ad9a7b1aa0df41fb3c4cb73c1ff01ea** dans [cette partie du site](https://hashes.com/en/tools/hash_identifier) vous decouvrirez instantanemment d'ou il vient.
Je vous conseille d’ailleurs de garder ce site sous le coude et **d’explorer ses possibilités**, il vous sera peut être utile aujourd’hui ou cette semaine.

### 3.2. HAVEIBEENPWNED
Pour savoir si un ou plusiseur mot de passe relie a une adresse mail voyez sur le site [Have I Been Pwned](https://haveibeenpwned.com/).
C'est un site tres pratique car il permet de savoir si un mot de passe a leak et de savoir sur quelle base de donnee il etait. Ainsi votre hypotethique mail `exemple@exemple.com` a ete reporte comme faisant partie du leak de la base de donne `Army Force Online` de 2016. Il y a donc cette base de donnee quelque part dans la nature. Et cette base de donnee inclus notre mail exemple@exemple.com et surement un mot de passe qui lui est associe. Voila tout ce que Have I Been Pwnd nous apprend.


## 4. Points important a retenir.
Certains mot de passes sont accessible sur internet assez facilement si on fait l'effort d'aller les cherchers. Il est donc ensuite possible d'essayer de hacker les comptes d'une personne a partir de ceux ci si cette personne utilise le meme mot de passe partout.
Il y a d’autres sites qui fonctionnent sur le système de Have I Been Pwned, qui collectent les bases de données hackée et vous laisse rechercher à partir d'un mail.  Vous pourrez en retrouver  dans l’**OSINT FRAMEWORK**. (site que je vous invite à chercher vous même ). Ceux-ci sont souvent payants mais donnent ici le mot de passe en clair directement ( c’est à dire non hashé). Il existe bien évidemment le même genre de site sur le Dark Web; parfois même des gratuits. Vous pouvez alors en utilisant le mot de passe et l’email correspondant essayer de vous connecter aux comptes associés à ce couple login/mdp.
( paypal, gmail, spotify, netflix etc … ).

Sachez aussi aue vous n'etes pas obligé de passer par ces services pour trouver le mot de passe de quelqu’un. **Vous pouvez tres bien aller rechercher la base de donnée qui a fuité le mot de passe directement**, et c'est souvent plus facile de la retrouver gratuitement. Vous pouvez très bien vous reposer sur Have I Been Pwned, puis faire une recherche google et obtenir le mot de passe désiré en cherchant un peu. Comprenez bien que c’est le mot de passe tel qu’il était à l'époque où la base de données
a été divulguée. **Le mot de passe n’est jamais mis à jour et peut très bien être obsolète.**


## 5. Pour aller plus loins
Sachez aussi que ces gigantesques bases de données permettent d'identifier les comptes secrets d'une personne qui a le même mot de passe. si deux comptes ont un mot de passe assez complexe de type "dfQ$b3WS6*4@KG%Lvpmqx9iix!3cR*fv3kHXg%" il est tres probable que ce soit la meme personne. ça peut vous permettre de decouvrir d'autres adresse mail ou identité utilisé par une même personne.


