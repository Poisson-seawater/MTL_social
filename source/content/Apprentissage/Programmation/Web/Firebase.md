---
tags:
  - IA/4/database
  - outils/firebase
---
> [!nf] [Firebase](https://firebase.google.com/), comment utiliser l'outils


**Firebase est une plateforme de développement d’applications web et mobiles.** Elle propose des services comme l’hébergement de sites web, l’authentification des utilisateurs et des bases de données cloud pour stocker des données. Le code peut être déployé depuis un ordinateur ou via GitHub. Firebase permet aussi de créer une base de données pour enregistrer et gérer les utilisateurs, ainsi que d’autres informations liées à l’application.




---

A chaque fois, on envoie le code sur [[Firebase]] qui le sauvegarde dans ses serveurs. 

-> [[alternative Firebase]]

----
###### Documentation complète Firebase CLI
[Documentation de référence de la CLI Firebase  |  Firebase Documentation](https://firebase.google.com/docs/cli?hl=fr)

### todo

### Sommaire
- [[basic launch website sur Firebase]]
- 

### Lien
- [[GitHub]]


### Processus général Firebase
#### **1. Coder un site web**
- Développer l'application avec HTML/CSS/JS ou un framework comme React, Vue, Angular.
	- [[bolt.new]], [[lovable]] ...

#### **2. Stocker le code**
- L'enregistrer **localement sur l’ordinateur** ou sur **GitHub** pour un suivi versionné.

#### **3. Déployer sur Firebase**
- Créer - [[Firebase database]] 
- **[[initialiser Firebase]] (`firebase init`)
- **Déployer** le site (`firebase deploy`)

#### **4. Ajouter des services Firebase (si nécessaire)**
- **Auth** : Connexion des utilisateurs (Google, email...)
- **Firestore / Realtime Database** : Stockage des données
- **Cloud Functions** : Exécuter du code backend
- **Storage** : Héberger des fichiers (images, vidéos...)
- **IDX**

#### **Automatiser le déploiement avec GitHub (optionnel)**

- Lier Firebase à GitHub pour un déploiement automatique après un `git push`.

### IDX
[[IDX]] est un espace de travail basé sur un navigateur permettant de créer, déployer et gérer des applications full stack multiplate-formes.
-> comme celui de [[Replit.com]]

### Utilisation de Firebase
Dans toutes les étapes de la création.
##### **1. Créer des meilleurs apps**
- **Auth**
- **Hosting**
- **Cloud Functions**
- **ML Kit**
- **Cloud Firestore**
- **Realtime Database**
- **Cloud Storage**


##### **2. Améliorer la qualité de l’app**
- **Crashlytics**
- **Performance Monitoring**
- **Test Lab**

##### **3. Faire grandir votre app**
- **Analytics**
- **Remote Config**
- **Predictions**
- **A/B Testing**
- **Cloud Messaging**
- **Dynamic Links**
- **In-app Messaging**

## SDK firebase
Avec JavaScript. 


# First step to launch website
[Premiers pas avec Firebase Hosting  |  Firebase Hosting](https://firebase.google.com/docs/hosting/quickstart?hl=fr)

# tuto
[Les bases de Firebase #1 Qu'est ce que Firebase en français facile | Tuto FR - YouTube](https://www.youtube.com/watch?v=YM8mV1ptuUY&list=PLT2KSPhMMiqp0jwqSCKaOjJHjl8ZFS2tI), va avec un code GitHub pour s'entrainer: [Les-bases-de-Firebase/Initial at master · drcmind/Les-bases-de-Firebase · GitHub](https://github.com/drcmind/Les-bases-de-Firebase/tree/master/Initial)

[Firebase Documentation](https://firebase.google.com/docs?authuser=0)