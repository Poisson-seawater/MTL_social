---
tags:
  - productivity/obsidian
---
> [!info] Tour rapide de présentation d'Obsidian

#### Sommaire
- Gestion de la connaissance: Wiki et Zettelkasken
- 1er pas sur Obsidian
- Structurer sa vault 
- Adapter Obsidian - plugins communautaires
- Adapter Obsidian - plugins interne
	- Template
	- Daily note

## Ressource
- [Home - Obsidian Help](https://help.obsidian.md/Home)

## Gestion de la connaissance: Wiki et Zettelkasken

**Objectif:** organiser et interconnecter des informations pour mieux les exploiter.
- **Zettelkasten** : Une méthode de prise de notes basée sur des liens entre idées uniques, comme des neurones connectés.
- **Wiki** : Un outil pour créer et naviguer dans des pages interconnectées, idéal pour un travail collaboratif ou une base de connaissances.
- **Obsidian** : Une application qui combine la structure du Zettelkasten avec la flexibilité des wikis, en utilisant des notes Markdown reliées entre elles.
	- la version payante, permet de synchroniser ta Vault (gros set de dossier) sur plusieurs plateforme


###### Obsidian en soi
[About - Obsidian, 5 phrases pour comprendre l'ojectif](https://obsidian.md/about)

Obsidian a trois caractéristiques fondamentales :
- **Plain text** (avec support Markdown) comme format par défaut.
- **Liens** (y compris les backlinks bidirectionnels) comme élément central.
- Conçu pour être **hautement extensible** (plugins, thèmes, etc.) et personnalisable.


###### Avantage VS n'importe quel autre plateforme
Un avantage majeur d'Obsidian utilisant des fichiers Markdown plutôt que des formats propriétaires est que toute base de connaissances personnelle est [future proof](https://www.elizabethbutlermd.com/how-to-take-future-proof-notes/). Vos notes Markdown peuvent être déplacées vers un autre éditeur, consultées et modifiées comme du texte brut. Elles sont compatibles avec Windows, Mac, et Linux.


### **Wiki**
**What** : Système hypertexte collaboratif permettant de créer, modifier et interconnecter des pages.  
**When** : Introduit en 1995 avec le premier WikiWikiWeb.  
**Where** : Utilisé en ligne, dans des organisations, ou pour des projets communautaires (ex. Wikipedia).  
**Why** : Centraliser et structurer la connaissance pour un accès rapide et une mise à jour facile.

### **Zettelkasten**

**Who** : Popularisé par Niklas Luhmann, sociologue allemand. Il a écris plus de 70 livres et 400 articles scientifique avant les ordinateurs 
**What** : Méthode de prise de notes basée sur des fiches interconnectées, chacune représentant une idée unique.  
**When** : Développée dans les années 1950-1970 pour la recherche académique.  
**Why** : Favoriser la pensée associative, stimuler la créativité et construire une base de connaissances évolutive.


----

## 1er pas sur Obsidian
> [!info] honnêtement, la suite de ce pdf est inutile. Juste commence a l'utiliser et prend des notes c'est le mieux.
> Mais si tu continues a lire, c'est plus un step by step des concepts de base de Obsidian

***IMPORTANT:*** chaque "titre" de note doit être ==unique.== Cela inclus aussi les "aliases" (*notion plus avancé*).

#### Obsidian comme éditeur de texte
1. **Titres :** `#` pour les titres de niveau 1, `##` pour les sous-titres, jusqu'à `######` pour le niveau 6.
2. **Texte en gras :** `**Texte**` ou `__Texte__`.
3. **Texte en italique :** `*Texte*` ou `_Texte_`.
4. **Listes :**
    - Listes à puces : `- Élément` ou `* Élément`.
    - Listes numérotées : `1. Élément`.
5. **Liens :** `[Texte](URL)` pour insérer un lien cliquable.
6. **Images :** `![Description](URL)` pour afficher une image.
	1. permet d'afficher une image en ligne!
7. **Blocs de code :** Utiliser des backticks triples pour insérer des blocs de code.
9. **Blocs de citation :** `> Citation`.
	1. "\> \[!texte]" pour que la 1ère ligne sois en gras
10. **Lien vers des documents externe:** comme une vidéo ou un excel !
11. **View**: editing VS reading

Aussi TOUT est customisable dans [Obsidian] !!! Et Obsidian possède assez de raccourcis clavier pour ne jamais devoir toucher à la souris !! *Contrairement à [[_Notion]]*

###### Rendre les notes plus esthétique ou complexe
Juste pour ton information, c'est un sujet très avancé:
- **CSS :** Obsidian permet d’ajouter des thèmes personnalisés ou des styles CSS via des fichiers `.css`. Ces personnalisations modifient l’apparence des notes et de l’interface.
- **JavaScript et HTML :** Les plugins personnalisés et les snippets HTML permettent d’ajouter des interactions ou des fonctionnalités avancées.
- **Formules mathématiques :** Intégrées avec LaTeX, les formules s’écrivent entre `$...$` pour inline ou `$$...$$` pour un affichage en bloc. Exemple : `$$E=mc^2$$` rend une équation formatée proprement.


### Rangement et Lien au sien de la Vault.
3 techniques utilisable en synergie - on y reviens plus tard:
- **Rangement par dossier** 
	- c'est comme utiliser son bureau et l'explorateur de fichier de window.
- **Les Tags**
	- c'est des étiquettes qu'on met à nos notes. Cela permet de les ranger, trier, filtrer par ce mot clé. 
- **Les liens**
	- même principe que l'on retrouve dans [[_Notion]] MAIS ici on peut utiliser des raccourcis clavier !

La règle non-dite et d'utiliser une seul Vault pour tout ton wiki (perso, école, travail ...) et 1 vault comme environnement de test (essayer les plugins communautaire). 
- personnellement, j'ai rajouté une 3e Vault, celle qui synchronisé a mon ordi et mon cell. 
- n'ayant pas explorer la collaboration sur Obsidian je ne sais pas dans quel mesure tout mélanger complique la tâches. 


*note: en regardant d'autre tuto, tu rencontreras certains qui prône une approche plus qu'un autre. Certain on des milliers de fiche et 0 dossiers. C'est faisable (avec le CTR+G et Dataview)!!*



###### Dataview
Un langage intégré à Obsidian pour générer des vues dynamiques à partir des métadonnées de vos notes.
On en reviendra quand on parlera de la structure de la vault et des plugins. 

### liens internes et externes
Les liens internes pour l’interconnexion des idées, tandis et les liens externes pour des ressources complémentaires. 
*Dans un manuel scolaire tu fais des exercices, puis te regardes la correction en fin de page. C'est des liens internes. Tu va sur Wikipédia pour confirmer une informations et tu met la page en favoris, c'est un liens externes.*

#### Liens internes
1. **Création de liens internes :**
    - Utilisez `[[Nom de la note]]` pour relier une note existante.
    - Utilisez `[[Nom de la note|Texte affiché]]` pour personnaliser le texte du lien.
2. **Navigation rapide :**
    - Cliquer sur un lien interne ouvre instantanément la note associée.
2. **Backlinks :**
    - Visualisez tous les liens pointant vers une note via le panneau des backlinks.

###### Création de liens vers le web :
- Syntaxe : `[Texte affiché](URL)`. Exemple : `[Obsidian](https://obsidian.md)`.
- *La majorité de mes onglet en favoris sont uniquement sur Obsidian*

##### Navigation entre note
- **Outlink :** Liens sortants créés depuis une note vers une autre note ou une ressource externe. Exemple : `[[Nom de la note]]` ou `[Texte](URL)`.
- **Backlink :** Liens entrants qui montrent quelles autres notes pointent vers une note donnée.
	- Visualisés dans le panneau des backlinks, ils aident à comprendre les connexions dans votre réseau de notes.

**Relation :** Les outlinks construisent les connexions, les backlinks les révèlent et les centralisent.

###### Graph view
Pour visualiser les relations entre vos notes sous forme de réseau. Chaque nœud représente une note, et chaque lien illustre une connexion (outlink).

**Paramètres principaux :**
1. **Filtres :** Affichez des notes spécifiques en filtrant par tags, dossiers, ou texte.
2. **Nœuds isolés :** Option pour afficher ou masquer les notes sans lien.
3. **Groupe par couleur :** Groupez les nœuds en fonction des tags, dossiers ou autres critères.
4. **Distance des liens :** Ajustez la portée visible des connexions (profondeur).
5. **Clusters :** Détectez des groupes de notes fortement interconnectées.

Assez de théories, revenons comment utiliser Obsidian.

### Les raccourcis clavier
> Le niveau supérieur c'est intégrer VIM 

Aller dans les paramètres. Les raccourcis classiques y sont déjà par défault.

Je recommande te créer et te familiariser avec les raccourcis suivant dès le début:
 - ouvrir la "sidebar" de gauche et de droite
 - ouvrir la palette de commande
 - passer d'une note a l'autre 
 - ouvrir les paramètres

### Écrire dans Obsidian 
Tu peux modifier l'interface avec:
- Group tab
- ouvrir dans une nouvelle fenêtre 

Tuto: [Obsidian Rocks - Exploring knowledge management with Obsidian.](https://obsidian.rocks/)

"*Group tab*", un exemple vaut mille mots, ici 3 notes ouverte en même temps
![](https://publish-01.obsidian.md/access/186a0d1b800fa85e50d49cb464898e4c/assets/ui-stacked-tabs.png)


## Structurer sa vault 
Tel qu'on l'a vue plus haut
1. **Hiérarchie par dossiers :**
    - Les notes sont rangées dans des dossiers et sous-dossiers selon leur thème ou catégorie.
    - Exemple : `Projets/Projet A/Notes`.
2. **Tagging :**
    - Utilisez des tags (`#tag`) pour catégoriser sans contraindre les notes dans une structure fixe.
    - Exemple : Une note peut avoir `#Lecture` et `#ProjetA`.
3. **Liens et réseau :**
    - Reliez les notes entre elles grâce aux liens internes (`[[Note]]`) pour construire un graphe d’idées.


###### Recommandation
- Utilisez des dossiers pour des projets spécifiques (`Projets/ProjetA`).
- Ajoutez des tags pour des thèmes transversaux (`#Idées`, `#Références`).
	- et utiliser des nested-tag (*ou tag enfant*): ```#Cuisine/platPrincipale```
- Reliez les idées grâce à des liens internes pour renforcer les connexions.
	- NE jamais avoir de note "orpheline"


#### Approches courantes 

###### Zettelkasten
1. **Approche Zettelkasten** (Atomicité et réseau)
    - Chaque note représente une idée unique et autonome, appelée "note atomique".
    - Les notes sont reliées entre elles par des liens internes (`[[Nom de la note]]`).
    - Les idées s’organisent en réseau, favorisant les connexions émergentes.
    - **Exemple :** Une note "Théorie X" pointe vers des idées connexes comme "Critiques de la Théorie X" ou "Applications pratiques".
    - **Avantages :** Favorise la créativité et la pensée associative.
    - **Limites :** Nécessite une discipline stricte pour nommer et relier les notes.

La méthode a 100% demande que tes notes commences toute par la date du jour (afin que chaque titre reste unique !). C'est aussi fort utile si tu veux analyser ton Obsidian aussi comme un journal !

###### Johnny Decimal
2. **Approche Johnny Decimal** (Structure numérique)
    - Le contenu est organisé par un système de numérotation à deux niveaux :
        - **Domaines principaux** : ex. 10-19 pour "Projets".
        - **Sous-catégories** : ex. 11.01 pour "Projet A".
    - Chaque note est associée à une catégorie numérique, facilitant la recherche et l’organisation.
    - **Exemple :**
        
        ```
        10-19 Projets
          ├── 11.01 Recherche sur X
          ├── 12.01 Analyse de Y
        ```
        
    - **Avantages :** Clair et méthodique, parfait pour des projets ou bases volumineuses.
    - **Limites :** Moins flexible pour des liens dynamiques.

###### PARA
3. **Approche PARA** (Projets, Zones, Ressources, Archives)
    - Les notes sont classées dans quatre grandes catégories :
        - **Projets :** Actions à réaliser (ex. "Planification d’un voyage").
        - **Zones :** Thèmes récurrents (ex. "Santé", "Apprentissage").
        - **Ressources :** Informations de référence (ex. "Articles lus").
        - **Archives :** Contenus terminés ou inactifs.
    - **Exemple :**
        ```
        📂 Projets
        📂 Zones
            ├── Santé
            ├── Finance
        📂 Ressources
            ├── Livres
            ├── Articles
        📂 Archives
        ```
        
    - **Avantages :** Simple et intuitif pour une gestion personnelle ou professionnelle.
    - **Limites :** Moins adapté à la pensée associative ou exploratoire.


#### **Approche mixte**
Comme le dis le [[culte of done manifesto]], faut commencer.  Et au fur est a mesure de ton aventure tu vas développer ta propres méthodes. Puis comme tout le monde tu auras plein de vieille note dans un dossier "bordel a ranger plus tard". Ainsi qu'une collection de vieux tag d'ancien projet ou passion, qui sont eux aussi mal ranger. 

Mon point est que commencer c'est le plus important et ta méthode va se créer avec le temps et n'en perd pas a vouloir ranger tes anciennes notes. Cela se fera a mesure (si jamais) tu reviends dessus.

Juste assure toi que chaque note est
- lié a une autres
- a un tag 
	- met le dans les **propriétés**
- et essaye de respecter le principe d'atomiticité pour profiter du plein pouvoir d'Obsidian. 

Et je te recommande de mettre la vue par défaut en "READ ONLY". 

###### Dataview
C'est un plugins et un language intégré dans Obsidian pour traiter ta Vault comme une base de donnée. J'ai pas encore joué avec mais j'ai conscience que c'est le niveau supérieur. 


#### Conclusion sur l'intro a Obsidian
Ta capacité a bien écrire tes notes est le plus important ! La n'est pas mon champ d'expertise tho. 


Voici 2 exemple de comment j'utilise le principe d'atomiticité:

**Comme un sommaire** (kind of obvious)
![[_note de cours Marketing#Le plan marketing]]

**Au sien d'un texte afin de l'épurer** (*exemple de wikipédia*)
The [national flag](https://en.wikipedia.org/wiki/National_flag "National flag") of [Mozambique](https://en.wikipedia.org/wiki/Mozambique "Mozambique") is a horizontal [tricolour](https://en.wikipedia.org/wiki/Tricolour_(flag) "Tricolour (flag)") of green, black, and gold with white [fimbriations](https://en.wikipedia.org/wiki/Fimbriation "Fimbriation") and a red [isosceles triangle](https://en.wikipedia.org/wiki/Isosceles_triangle "Isosceles triangle") at the [hoist](https://en.wikipedia.org/wiki/Hoist_(flag) "Hoist (flag)"). The triangle is [charged](https://en.wikipedia.org/wiki/Charge_(heraldry) "Charge (heraldry)") with a [five-pointed](https://en.wikipedia.org/wiki/Five-pointed_star "Five-pointed star") gold star in its center, above which there is a [bayonet](https://en.wikipedia.org/wiki/Bayonet "Bayonet")-equipped [AK-47](https://en.wikipedia.org/wiki/AK-47 "AK-47") crossed by a [hoe](https://en.wikipedia.org/wiki/Hoe_(tool) "Hoe (tool)"), superimposed on an open book. The colours and symbols of the flag represent different aspects of the [Mozambican people](https://en.wikipedia.org/wiki/Demographics_of_Mozambique "Demographics of Mozambique") and their [war of independence](https://en.wikipedia.org/wiki/Mozambican_War_of_Independence "Mozambican War of Independence").


##### Obsidian et d'autre collaborateur
Jamais essayer, mais possible
- [Collaborate on a Publish site - Obsidian Help](https://help.obsidian.md/Obsidian+Publish/Collaborate+on+a+Publish+site)
- [Collaborate on a shared vault - Obsidian Help](https://help.obsidian.md/Obsidian+Sync/Collaborate+on+a+shared+vault)
- [Commercial license - if for profit compagnie(https://help.obsidian.md/teams/license)

Après de par la nature de **Markdown** de tes fiches, tu peux les mettre dans le drive et n'importe qui ayant l'application Obsidian.md peux les modifier.
Utilise [[GitHub]] est une autre option que je ne maitrise pas. 


##### To Hype you
Avec le pouvoir du open source, et un peu de volonté a mettre les mains dans la technologie. Tu peux être GARANTI qu'Obsidian sera toujours la solution la PLUS a la pointe de la technologie et de l'agréabilité !

## Adapter Obsidian - plugins interne
La liste est dans les paramètre sous "core plugins". 

Après avoir commencer a créer quelque fiches et pris la mains avec Obsidian. Regarde en 1 a chaque jour et essaye les. Certains sont "niches" d'autre vital. 


Ceux "vitaux", qui sont plus ou moins nécessaire au fonctionnement de Obsidian selon son design
- command palette
- file recovery
- file
- graph view

Mes must use
- Template
- Workspaces
- Tags view

Bref il y en a plusieurs à explorer !


### Template
Le plugin **Templates** d’Obsidian automatise la création de notes standardisées grâce à des modèles prédéfinis. 


## Adapter Obsidian - plugins communautaires
###### My MUST plugins 
Pour tout usage
- [Local Backup](https://www.obsidianstats.com/plugins/local-backup)
	- pour backup ma vault dans un .Zip !
- [Kanban](https://www.obsidianstats.com/plugins/obsidian-kanban)
- [Excalidraw](https://www.obsidianstats.com/plugins/obsidian-excalidraw-plugin) c'est un tableau blanc
	- *mon PC étant vieux, ce plugins peux être lents*
- [Project](https://www.obsidianstats.com/plugins/obsidian-projects)
	- gérer ses projets ET me sert aussi de CRM, il a beaucoup de potentiel.
	- Version plus User friendly que [Dataview](https://www.obsidianstats.com/plugins/dataview)
- [Tag Wrangler](https://www.obsidianstats.com/plugins/tag-wrangler)
	- 1er plugin pour maximiser l'usage des Tag
- [Reminder](https://www.obsidianstats.com/plugins/obsidian-reminder-plugin)
	- mettre des deadlines a ses todo

Il y a plus de 2000 plugins, je suis sur que tout problème que tu vas rencontrer est déjà répondu. Sinon rien t'empêche de profiter des joies de l'open source et de mettre les mains dans la pâtes !

# Ressource
Pour plus d'information et aller plus loins, commence par regarder la documentation officiel, elle est épuré, concise et no-bullshit: [Home - Obsidian Help.](https://help.obsidian.md/Home)
- Le [forum officiel](https://forum.obsidian.md/) 


##### Youtube tuto
- [Obsidian for Beginners - YouTube](https://www.youtube.com/playlist?list=PL3NaIVgSlAVLHty1-NuvPa9V0b0UwbzBd)
- [Obsidian Tutorials For Personal & Professional Productivity - YouTube](https://www.youtube.com/playlist?list=PLAHdNALkfDl4BEn_iCmmkAZDxaO98QATl) ses vidéos sont plus longue que nécessaire. 
###### Blogs
- [Obsidian Rocks - Exploring knowledge management with Obsidian.](https://obsidian.rocks/)

##### Plugins
[Explore New, Updated, Trending, Most Downloaded, and Top Rated Obsidian Plugins](https://www.obsidianstats.com/)

