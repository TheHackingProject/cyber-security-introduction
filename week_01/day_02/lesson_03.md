# Le Fuzzing

## 1. Introduction
Parfois pour découvrir des sous domaine, pour découvrir des fichiers sur une cible ou juste des nouvelles pages sur un site internet. Il faut bruteforce.
Cette technique de reconnaissance par bruteforce s'apelle le fuzzing. 


## 2. Le fuzzing 
Un site est un outil, il sert un propos. Il doit donc pouvoir être mis à jours, et être intuitif un minimum. Le developpeur aussi cherche à rester intuitif, surtout dans la façon qu'il a de nommer ses fichiers. On doit pouvoir deviner ce que contient un fichier à son nom et son arborescence. On peut donc difficilement imaginer que des documents ou des urls d'un site soit généré aléatoirement. Pas impossible mais peu probable. 
Il est donc probable qu'utiliser un dictionnaire de mot les plus courramment utilisés sur un site web peu vous permettre d'augmenter votre surface d'attaque possible. 
Vous avez ici la raison d'être du fuzzing.


## 3. Les outils
Pour fuzz un website j'utilise géneralement dirbuster, gobuster ou encore wfuzz. Le tout est d'avoir un bon dictionnaire de mot ou autrement appelée **wordlist**.

La façon d'utiliser d'utiliser ces outils ressemble un peu à cela.

```
> ./outil --wordlist /path/wordlist --url https://example.com/FUZZ
```

Vous pouvez ensuite ajouter les filtres que vous voulez, pour choisir les réponses que vous voulez isoler ( par défaut la reponse HTTP avec un status egal à 200 ). 

Vous pouvez aussi rajouter une extension pour rechercher des fichiers et d'autres types d'url.

```
> ./outil --wordlist /path/wordlist --url https://example.com/FUZZ.txt
```


