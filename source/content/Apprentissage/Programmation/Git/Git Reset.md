---
tags:
  - coding/git
---




### Git Reset
  `git reset` est un outil complexe et polyvalent pour **annuler les changements**;  trois façons différentes, qui correspondent aux arguments de ligne de commande **--soft, --mixed et --hard**.


######  --hard
permet de **revenir à n'importe quel commit** mais en oubliant absolument tout ce qu'il s'est passé après !!

C'est une manière simple d'annuler des changements qui n'ont pas encore été partagés. Cette commande est incontournable lorsque vous commencez à travailler sur une fonctionnalité, que vous vous êtes trompé et que vous voulez recommencer de zéro.

######  --mixed
Pour revenir juste après votre dernier commit ou le commit spécifié, sans supprimer vos modifications en cours. 
Il permet aussi, dans le cas de fichiers indexés mais pas encore commités, de désindexer les fichiers

> Si rien n'est spécifié après    `git reset` , par défaut il exécutera un    `git reset --mixed HEAD~` .

>[!info] Le **HEAD** est un pointeur, une référence sur votre position actuelle dans votre répertoire de travail Git.

###### soft
Permet de se placer sur un commit spécifique afin de voir le code à un instant donné, ou de créer une branche partant d'un ancien commit. Elle ne supprime aucun fichier, aucun commit, et ne crée pas de HEAD détaché.