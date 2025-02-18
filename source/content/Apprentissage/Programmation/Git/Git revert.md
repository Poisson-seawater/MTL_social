---
tags:
  - coding/git
---
La commande **git revert** vous permet de revenir à l'état précédent, tout en faisant un deuxième commit.  Au lieu de supprimer le commit de l'historique du projet, elle détermine comment **annuler les changements** introduits par le commit et ajoute un nouveau commit avec le contenu ainsi obtenu.

###### différence entre git reset et git revert
`git reset`  va revenir à l'état précédent sans créer un nouveau commit, alors que  `git revert`  va créer un nouveau commit.