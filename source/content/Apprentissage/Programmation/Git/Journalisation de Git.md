---
tags:
  - coding/git
---




### Journalisation de Git
> Log en anglais

Par défaut,    `git log`    **énumère en ordre chronologique inversé** les commits réalisés (*commits les plus récents apparaissent en premier*); affiche chaque commit avec 
- son **identifiant SHA**, l'auteur du commit, la date et le message du commit

###### git reflog
`git reflog`  va loguer les commits ainsi que toutes les autres actions que vous avez pu faire en local : vos modifications de messages, vos merges, vos resets ...

Comme    `git log`   ,   `git reflog`  affiche un identifiant SHA-1 pour chaque action. Il est donc très facile de revenir à une action donnée grâce au SHA. 
Pour revenir à une action donnée, on prend les 8 premiers caractères de son SHA et on fait : `git checkout e789e7c`