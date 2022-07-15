# DNS crawling/discovery
Une ressource sur le DNS Crawling.

## 1. Introduction
Sur internet vous connaissez tous et toutes des noms de domaines. Un nom de domaine ça ressemble à ça 'Google.com' ou 'Yahoo.fr'.  Mais savez-vous que **wifi.google.com** existe ? Si vous allez sur cette URL, vous aurez une erreur 404, mais vous noterez qu'en utilisant **fddggg.google.com** vous n'avez pas la même erreur. Ce qui signifie que le nom de domaine wifi.google.com existe bien. C'est juste que vous n'utilisez pas bien l'adresse. Quand je dis que vous ne l'utilisez pas bien cela veut dire que vous n'utilisez pas le bon protocole (puisque par défaut votre navigateur envoie une requête HTTP aux serveurs) ou le bon port
(par défaut votre navigateur envoie une requête sur le port 80 ou 443 ).


## 2. Historique et contexte
Pour une exploration plus en profondeur, on va parler du DNS et partir à la recherche des sous-domaines d’un domaine donné. Le DNS ou Domain Name System c’est le concept roi que tout le monde utilise sans vraiment le connaître. Pour faire simple, un enregistrement DNS c’est par exemple “thehackingproject.org” 'TheHackingProject' est un nom de domaine qui a été enregistré dans le registre “.org” qui est géré par “PIR” ( Public Interest Registry). C'est un service que quelqu'un a payé et qu'il renouvelle annuellement. Une fois que cette personne a acquis cet enregistrement, vous pouvez dire que **thehackingproject.org** va être un raccourci ou un alias vers le serveur web qui héberge un site.

Ainsi un nom de domaine va être une ligne dans un registre qui va faire correspondre un nom avec une adresse IP. Cet enregistrement fonctionne comme cela: quand on demande d'accéder à un nom de domaine, une requête est faite au registre qui stocke l'information de ce nom de domaine afin de récupérer l'adresse IP du serveur avec lequel on veut communiquer. Une fois l'adresse IP récupérée, on va envoyer une seconde requête au serveur web grâce à cette adresse IP.

L'avantage de fonctionner comme ça permet aux utilisateurs de ne pas avoir à retenir l’adresse IP exacte. Et cela permet de changer d’adresse IP et aussi de serveur quand on le veut sans avoir à apprendre à tout le monde une nouvelle adresse IP. Ce que je vous ai décrit ici est le type d'enregistrement DNS de type A ou AAA.
Il existe d’autres types d’enregistrement DNS, mais je vous laisse explorer ça par vous-même si le cœur vous en dit. https://www.techtarget.com/searchnetworking/definition/domain-name-system.

Une fois que vous avez acquis un nom de domaine, vous pourrez enregistrer autant de sous-domaines que vous le voudrez. Ainsi thehackingproject a enregistré 'formation.thehackingproject', 'www.thehackingproject', 'student.thehackingproject' et bien d'autres.

**Si vous avez la flemme de lire ou que vous n'avez pas très bien compris vous pouvez regardez cette [video](https://www.youtube.com/watch?v=QHVK666TFUI) qui est bien plus complète et expliqué par quelqu'un de beaucoup plus compétent en la matière que moi.**

## 3 Le crawling DNS

### 3.1 Google Dorks
Le crawling DNS qu'est-ce que c'est ? Quel est son objectif ?
Son objectif est de découvrir un maximum de noms de domaine et sous-domaines que peut regrouper une organisation ou une cible. Normalement c'est impossible de découvrir un enregistrement DNS qu'on ne nous communique pas. Il n'existe pas de façon de consulter la liste de tous les sites en `.fr`
Vous pouvez toujours brute force en utilisant des mots courants comme `table.fr` et voir si ça redirige vers une adresse IP, mais c'est très limité. Ce qui nous intéresse c'est d'utiliser des techniques un peu plus stables. Il existe beaucoup de façon de faire du crawling. Sachez qu'il faut toujours ruser. Chercher les traces de l'existence de sous-domaine sur le net.
Une des plus simple c'est de demander à Google quels sous-domaines il connait.

Par exemple  avec la requête suivante:

```txt
site:*.@thehackingproject.org -www
```

Cette query permet de découvrir des sous-domaines de THP. Elle va vous permettre de découvrir qu’il a existé un sous-domaine `secu` à THP. Mais vous n’aurez pas tout. Google ne sait pas tout non plus.

## 3.2 Crt.sh

Une autre façon c'est d'utiliser les certificats ssl/tls qui sont connus sur internet. Je ne vais pas vous expliquer ce que c'est aujourd'hui, mais sachez que c'est ce qui permet de rajouter le 'S' a HTTPS. Un site qui vous permet de le faire pour vous c'est [crt.sh](https://crt.sh). Un site très pratique qui va retrouver tous les domaine et sous-domaine de THP pour lequel un **certificat tls** existe et a été vu sur internet.

Sur crt.sh on apprend qu’il a existé des sous-domaines à thp comme “**lp.thehackingproject.org**” ou **blog.thehackingproject** “formation” ou encore “student”, etc. ça permet de faire de l'archéologie aussi.

## 4 Points à retenir
Ce genre d’outil, il en existe beaucoup et ils fonctionnent tous avec des systèmes particuliers. L’objectif c’est de découvrir des sous-domaines, mais aussi d’obtenir des informations sur ce que l’entreprise fait ou est en train de construire ou a abandonné. Souvent ces portes dérobées sont moins bien gardées, plus mises à jour depuis longtemps ou juste intéressantes pour en apprendre plus.

Chaque sous-domaine peut être un serveur différent, codé dans des langages différents, avec des failles de sécurité différentes. Des failles qui n’attendent que vous. Le plus juteux c’est quand un sous-domaine a été oublié depuis longtemps et qu’il est très facile de le hacker parce qu’il existe plein de failles connues dessus et ce sous-domaine devient alors un vecteur d’attaque assez simple, ou une façon d’obtenir des informations en plus.

## 5 Pour aller plus loin
Vous pouvez aussi faire du scan DNS avec [DNSdumpster](https://dnsdumpster.com)
et obtenir des [graphs trop cool](https://dnsdumpster.com/static/graph/google.com-202111181635.html).

J’aime aussi beaucoup Amass qui est un super projet OWASP qui compile plusieurs méthodes à la fois pour obtenir un maximum de domaine et sous-domaine.

Parfois vous trouverez des sous-domaines qui ont été supprimés. Comme par exemple **blog.thehackingproject.org**, qui a été supprimé ou déplacé. Par contre si vous voulez voir à quoi il ressemblait vous pouvez très bien regarder avec le **cache google** ou dans la [waybackmachine](https://archive.org/web/)
