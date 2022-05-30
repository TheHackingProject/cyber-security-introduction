# Sensibilitation à la cybersécurité

Bonjour à toutes et tous. Nous sommes tres content de vous acceuillir cette semaine pour notre cours **sensibilitation à la cybersecurité**.
Le programme va etre chargé et plutot relevé. Pour faire tres simple vous allez apprendre l'entiereté de [ce glossaire](https://www.ssi.gouv.fr/administration/glossaire/) de l'ANSSI.

En fin de semaine une bonne grosse interro et bisous.
fin du cours. Rideau. Tchao les amis.
ça nous a fait plaiz' de vous apprendre tout ça.

![bisous](https://www.francetvinfo.fr/pictures/QZsc0wdwsX8YfEaOL9IcxiKCi38/640x360/2017/12/06/eltVideoWs-265181-5a286eb80bd35.jpeg)


### Bref.
Cette semaine vous allez découvrir une certaine partie de la cybersécurité. Cette partie de la cybersécurité peut être réduite à la dénomination “Recherche en Source Ouverte” ou **OSINT** ( open source intelligence technique ). En réalité, le dernier jour ira un peu plus loin et nous verrons un peu d'ingénierie sociale ( social engineering ) mais OSEF.

L’objectif à travers ce cours c’est vous apprendre à quel point cela peut être facile de trouver un **vecteur d’attaque** envers vous ou votre entreprise. Comprenez bien que le but n'est pas de faire de vous des hackers, mais de vous montrer l'étendue des possibilités qu'une personne informé a. Comme toujours ; l'information c'est le pouvoir.
Et vous apprendrez ceci par l'experience en decouvrant avec quelle facilitée un hack peut être fait.
Libre à vous de chercher à mettre en pratique et d'approfondir les connaissances. Vous apprendrez surtout que la bonne posture en sécurité **n’est pas d'être unhackable** mais de **faire partie des plus pénibles à hacker**. C'est le seul objectif à atteindre. Le vilain trouve des signaux de vulnérabilités qui le font remonter jusqu'à vous car il sait que vous êtes vulnérable. Un peu comme un chien qui flaire une piste. (Un hacker ne vérifie pas que vous êtes vulnérable, il le sait déjà parce qu’il a remonté la piste jusqu'à vous.)
A moins que vous ne soyez une cible privilégiée c’est ainsi que ça se passe.

![chien](https://raw.githubusercontent.com/bafraikin/ressource_thp_cursus_secu/master/ressources/jour_01/dog.jpg)

Aussi, l'objectif de ce cours n'est pas de faire de vous des hackeurs éthiques complet.
Déjà parce qu'il n'y a pas le temps en une semaine. Ensuite parce que l'ambition de ce cours c'est de **vous sensibiliser à la cybersecurité**. Et pour cela rien de mieux que de se rendre compte du danger.  Plutot que de faire de vous un hackeur tres tres *technique*. Nous avons decidé de vous enseigner que **tout les moyens sont bons quand on est un attaquant**. Ainsi **l'important n'est pas le chemin mais l'arrivée**. Parfois ça peut etre tres tres simple, et c'est pour demontrer ceci que pour la plupart du cours nous allons nous limiter à l'utilisation d'un navigateur internet. Mais ce n'est pas pour ça que vous n'apprendrez pas à reperer et **exploiter des failles de sécurité**, ni à recuperer les mots de passes de votre papy ou d'autre encore.

Pour ce que nous attendons de vous pendant le cours, c'est surtout d'etre **independant**. N'hesitez pas à travailler en groupe et a partager avec les autres. ( sauf les reponses ). Les exercices pratiques sont conçus pour être résolu **en groupe**. Repartissez vous le travail et travaillez en équipe dès que vous sentez que c'est possible. C'est normal de bloquer parfois. Perserverez et/ou reflechir autrement peu vous aider. Tout ne vous sera pas donné clé en main.
Il n'est pas necessaire de coder quelque chose pour ce cours. Normalement vous saurez toujours trouver un outil tout fait pour vous. L'open source est un monde fantastique pour les hackers. Il faut juste savoir le chercher.

## Les precautions à prendre
- Faites attention à vous, vous pouvez tres bien **chercher et telecharger un virus et l'executer sans le savoir.**

![PIETE](https://www.memecreator.org/static/images/memes/4900025.jpg)

**Si** vous vous retrouvez dans la situation où vous avez telechargé un fichier.

***PITIE*** -> Avant de l'ouvrir, analysez le fichier sur [virustotal](https://www.virustotal.com/gui/home/upload) < <
Et si possible, lisez le code avant de l'executer.

![pitié](https://c.tenor.com/OBSd0JyDRbQAAAAC/what-he-said-regina-hall.gif)

- De preference travaillez sur un ordinateur qui peut etre reboot facilement et qui ne contient rien auquel vous tenez. Ou au pire faites un backup.
- Travaillez sur un PC un maximum à jours, avec un navigateur internet à jours. Faites y gaffe

**Le mieux pour le cours est un pc qui a un OS linux**. Nous conseillons Ubuntu, c'est le plus simple à installer et qui est le plus proche de Kali linux (OS de cybersecurité).
ça va vous permettre d'installer absolument tout les outils dont vous avez besoin sans la galère d'installer kali.

Parfois il vous sera demandé de rediger quelque chose pour expliquer votre processus, c'est tres important. En cyber securité il faut toujours ecrire un "write up"/rapport quand on découvre quelque chose. Pour que les gens qui vont devoir regler le problème par la suite puissent bien comprendre comment vous avez fait et surtout puissent s'approprier la faille, afin de la reproduire facilement et corriger d'eux meme. C'est le moment où vous partagerez vos connaissances et ce que vous avez appris.

Ce cours a aussi pour objectif de vous apprendre 2-3 bonnes pratiques et choses à observer pour vous protéger vous et vos proches.

**On va commencer avec le laïus réglementaire mais qui est très important**.
Sachez que ce que vous allez apprendre très bientôt est dangereux. De par la facilité avec laquelle cela peut être mis en œuvre et l’impact que cela peut avoir sur la vie d’une personne. Je vous demande donc de ne jamais utiliser ce que vous allez apprendre contre quelqu’un ou quelconque société sans en avoir recueilli son consentement averti et éclairé par écrit. Sachez que c’est illégal de le faire sans que la personne ait donné son accord au préalable.

Sachez aussi que pendant l'entièreté du cours, **certaines images pourraient cacher des indices**. ça peut vous débloquer si vous vous retrouvez devant quelque chose de trop retors, mais préférez demander des indices aux gens qui font le cours en même temps que vous.
Pour accéder à ces indices par vous même je vous recommande de vous renseigner sur les **métadonnées des images et EXIF**

*Vous devriez trouver un message dans les deux photos d'illustration de ce cours qui vous dit que ça fonctionne bien*

![hacker](https://raw.githubusercontent.com/bafraikin/ressource_thp_cursus_secu/master/ressources/jour_01/Hacker.jpg)

*J'espère que tout le monde a enfilé son meilleur hoodie de hacker, sa distro linux de prête, ça commence.*

