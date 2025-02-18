---
tags:
  - IA/test
  - health/alimentation
---
-> [[_ Alimentation]]
-> [[créer une application web sans code]]


- [ ] ranger les excel de proteine ?
- [ ] brainstorm fonctionnalité 
- [ ] avec Chat puis Claude 
- [ ] créer une app avec [[bolt.new]]

Puis:
- code [[app de suivi des objectifs]]


###### hébergement
[Welcome to Firebase Hosting](https://bolt---prot-comparateur.web.app/) -> [Firebase Hosting](https://firebase.google.com/docs/hosting?hl=fr)

[Connexion : comptes Google](https://console.firebase.google.com/project/bolt---prot-comparateur/overview)
###### code
Sur
- [[bolt.new]]: 
	- ~~[bolt.new/\~/sb1-tzpkrqbg](https://bolt.new/~/sb1-tzpkrqbg)~~
	- [last version avec Authentification et Firebase](https://bolt.new/~/sb1-ydeb7rg8)
	- La version "jet_2" est host dans "*protein-comparateur*" sur Firebase. 
- [[websim.ai]]: 
	- [Protein Price Comparator](https://websim.ai/p/g68826s0n463danr_1nl)
	- Issues:
		- discount deal ne fonctionne pas !
		- après avoir remplis un produit, que les champs disparaissent le on dit "bravo, *new produit* upload" et un bouton "new produit" pour regénérer les champs
		- "on sale" button au milieux et plus esthétique
		- search product donne le nombre de produit,
			- ET propose de lister par magasin
		- rajouter "fruit sec" a la liste des produits en best deal
			- et les autre "cheese" et "vegan" sont choisi par button (au lieux d'une liste) dans "Calculator"
- [[_Claude IA]]: 
	- [claude.site/artifacts/09ffc16e-c833-4b60-8f4a-6094cf91e716](https://claude.site/artifacts/09ffc16e-c833-4b60-8f4a-6094cf91e716) (le site publier)
	- sinon le code est répartie en plusieurs chat !!

# Ou j'en suis
- [ ] finir de prompter l'app 
- [ ] la déployer sur une plateforme et la rendre utilisable

###### note sur le déploiement
Comment / Ou sont **stocker les donnée** ??
- dans son cache internet ?

###### au 2024-12-12
essayer de publier mon site depuis GitHub dans Firebase. Pas réussis, donc j'ai rééssayer depuis [[bolt.new]]. Plus assez de token, donc je vais attendre demain. 
Sur [[Replit.com]], faut payer pour déployer. 
Donc demain
-  on va focus sur les [[_ Skool IA francophone]] pour apprendre un max les outils sans code, et ensuite on se remettre a coder. 
- 1h de tuto sur [[Firebase]] et [[GitHub]]
	- 1er terminer OpenClassroom tuto


----
###### Publication sur: 
- [[GitHub]]: pour mettre du code, mais le code doit être héberger sur mon ordi !! donc doit apprendre (*rapidement*) à utiliser GitHub et Git
- [[Replit.com]] : faut payer
- [[Netfly]]: connection avec [[bolt.new]] a explorer

###### Firebase ID
198280463050


const firebaseConfig = {  apiKey: "AIzaSyBdpqfNKz5Iy-slKtqS5t9yendRCmPAKxA",  authDomain: "test-prot-comparateur.firebaseapp.com",  projectId: "test-prot-comparateur",  storageBucket: "test-prot-comparateur.firebasestorage.app",  messagingSenderId: "1092168330398",  appId: "1:1092168330398:web:a953928eb88b46fac51f8f",  measurementId: "G-35FVGBM9PN"
};

Démarrer en mode test







----
# Fonctionnalité
2 data base auquel on a accès. 
- la sienne
- celle des autres usagé que l'on suit !!
	- *éviter de ce faire spam par des merde d'une épicerie*


plus tard
 - Daily Protein accounting
**pourquoi différence avec vegan et Cheese:**
Car si l'usage est vegan ou vegetalien, le top ce fera de lui-même. Par contre, pour un usager régulier avoir cheese et comparer les bon deals en pois chiche rapidement c'est utile !!

###### Les onglets:
- top protéine deal
- Calculator
- Search

###### top protéine deal
- vegan
- all deals
- cheese
- en spécial


###### Calculator
Remplir les cases
- product name
- store
	- list déroulante pour aider a remplir plus rapidement, 
	- list basé sur les réponses précédente
- Prix / 100g
	- radio bouton a côté pour changer la case en 2 case: prix régulier et weight (grams)
- bouton "en spécial": 
	- si click, alors s'affiche le prix / 100g en spécial.
	- Permet de constuire le top 7 des deals en spéciales 
		- ou de comparer les spéciaux a l'épicerie
- Protéine, deux unités en % ou en gramme
	- le gramme est par défault pour 100g, cependant on peut le modifier manuellement (pour 30, 50, 75 ... n'importe)

Bouton "calculate value": quand appuyer, rajoute le produit dans la base de donnée.

Puis s'affiche le meilleur deals régulier en $/gramme de protéine. 


###### Search
permet de chercher un produit, de l'afficher, de le supprimer, ou de le modifier. 

###### Daily Protein accounting



## Cahier des Charges Chat GPT

#### Objectif

Développer une application mobile ergonomique et hautement fonctionnelle permettant aux utilisateurs de comparer de manière précise et rapide des options de viandes disponibles sur le marché. L’application vise à optimiser la prise de décision basée sur des critères quantitatifs tels que le prix, le poids, et la teneur nutritionnelle, tout en intégrant la gestion des promotions.

---

### Fonctionnalités Clés

#### 1. **Module "Top 7 Deals"**

- Présentation des 7 meilleures offres disponibles, classées par rapport à leur rapport qualité/prix.
- Inclusion d’un classement parallèle des 7 meilleures promotions ou offres spéciales, en fonction des entrées utilisateurs concernant les produits.
- Informations clés affichées pour chaque deal :
  - Nom du produit
  - Prix total ou prix par 100g (selon le format d’entrée choisi par l’utilisateur).
  - Poids total.
  - Prix par kilogramme.
  - Pourcentage de protéines.
  - Provenance (magasin ou fournisseur).

#### 2. **Module d’Entrée Manuelle**

- Fonctionnalité permettant la saisie personnalisée de données produits, notamment :
  - Nom du produit.
  - Prix total ou prix par 100g (avec une option pour basculer entre les deux formats).
  - Si l’utilisateur choisit le prix total :
    - Poids total.
    - Prix total.
  - Pourcentage de protéines.
  - Provenance (magasin ou fournisseur), avec auto-complétion des choix récurrents.
  - Prix en promotion, lorsqu’applicable, permettant l’analyse spécifique des produits spéciaux.
- Vérification automatique pour assurer l’unicité du nom du produit et de sa provenance dans la base de données.

#### 3. **Module de Recherche et Gestion des Données**

- Fonction de recherche avancée pour retrouver rapidement un produit enregistré par son nom ou ses caractéristiques clés.
- Interface intuitive permettant de :
  - Modifier des informations préexistantes (prix, poids, provenance, etc.).
  - Supprimer des entrées obsolètes ou incorrectes.
- Système d’alerte pour éviter les duplications lors de la création ou l’édition des données.

#### 4. **Interface Minimaliste et Performante**

- Conception adaptée à une utilisation rapide et fluide en magasin.
- Disponibilité hors ligne pour garantir l’accessibilité des fonctionnalités principales même sans connexion internet.
- Navigation intuitive avec des options clairement organisées en onglets distincts, facilitant l’accès à chaque module.

---

### Conclusion

Cette application se distingue par son approche centrée sur l’utilisateur, combinant la simplicité d’utilisation à des fonctionnalités avancées pour la comparaison de viandes. Elle vise à rationaliser la prise de décision lors des courses tout en offrant une expérience intuitive et adaptée aux besoins variés des utilisateurs.



# prompt par claud
###### Application de comparaison de prix des protéines
Je souhaite créer une application web pour comparer les prix des différentes sources de protéines. L'application permet aux utilisateurs de trouver les meilleures offres et de calculer le prix en dollar par gramme de protéine.

## Fonctionnalités principales

### Navigation
- Interface avec 3 onglets principaux : "Best Deals", "Calculator" et "Search"
- Navigation fluide entre les sections

### Onglet "Best Deals"
- Affichage des meilleures offres de protéines
- Filtres pour :
  - Tous les produits
  - Produits végans
  - Fromages
  - Produits en promotion
- Tri par prix/gramme de protéine
- Affichage du top 7 des meilleures offres

### Onglet "Calculator"
- Formulaire d'ajout de produit avec :
  - Nom du produit
  - Magasin (avec autocomplétion basée sur les entrées précédentes)
  - Prix par 100g
    - Option pour basculer entre prix/100g et prix total + poids
  - Contenu en protéines (g/100g ou %)
  - Switch pour indiquer si le produit est en promotion
- Bouton de calcul qui :
  - Ajoute le produit à la base de données
  - Affiche le classement des meilleurs rapports qualité/prix

### Onglet "Search"
- Barre de recherche pour trouver les produits existants
- Affichage des résultats avec :
  - Nom du produit
  - Magasin
  - Prix régulier
  - Prix par gramme de protéine
- Boutons pour modifier ou supprimer chaque produit

## Spécifications techniques
- Interface utilisateur responsive
- Composants React modernes
- Design épuré et professionnel
- Utilisation de Tailwind CSS pour le style
- Gestion d'état avec React Hooks
