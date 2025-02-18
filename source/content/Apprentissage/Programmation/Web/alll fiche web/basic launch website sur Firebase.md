---
tags:
  - outils/firebase
---
### **Le processus de déploiement sur Firebase**
- **Côté [[Firebase]]** : Vérifier le projet, activer les services nécessaires, récupérer les clés.
- **Côté PC** : Vérifier Node.js/Firebase CLI, initialiser Firebase, build le projet, tester en local, puis déployer.

##### **Actions côté Firebase** (sur la plateforme)

1. **Vérifier l’existence du projet Firebase** :
    
    - J’ouvre la [console Firebase](https://console.firebase.google.com/).
    - Je m’assure que le projet existe et qu’il est configuré correctement.
    - Je vérifie que **Firebase Hosting** est activé.
2. **Vérifier les services nécessaires** :
    
    - Je m’assure que les services nécessaires (ex. : **Hosting**, **Firestore**, **Authentication**) sont activés.
    - Si un domaine personnalisé est prévu, 
	    - ALORS je vérifie qu’il est configuré ou que les DNS sont prêts.
1. **[[Récupérer les clés et identifiants nécessaires - Firebase]]** :
    - Je m’assure que les paramètres d’accès au projet Firebase sont disponibles.
    - Si besoin, je récupère la configuration (fichier `firebase.json` ou clé de service).

---

### **Actions sur le PC du stagiaire**

#### **1. Vérifier l’environnement de développement**
-> [[Git]]
- **Node.js** : Je m’assure que Node.js est installé en tapant :
    
    ```bash
    node -v
    //puis
    npm -v
    //et 
    vite -v
    ```
    
- **Firebase CLI** : Je vérifie que Firebase CLI est installé avec :
    
    ```bash
    firebase --version
    ```
    
    - Si Firebase CLI manque, je l’installe :
        
        ```bash
        npm install -g firebase-tools
        ```
        

---

#### **2. Me connecter au projet Firebase**

- Je vérifie si Firebase CLI est déjà connecté : (*PAS COMPRIS PK JE FAIS SA !!*)
    
    ```bash
    firebase login:list
    ```
    
- Si besoin, je connecte mon compte :
    
    ```bash
    firebase login
    ```
    

---

#### **3. Vérifier et initialiser le projet localement**

- Je me place dans le dossier du projet du stagiaire :
    
    ```bash
    cd /chemin/vers/le/projet
    ```
    
- Je vérifie si Firebase est déjà initialisé (présence d’un `firebase.json`).
    - **S’il manque**, j’[[initialiser Firebase]] :
        
        ```bash
        firebase init
        ```
        
        - Je choisis **Hosting** dans la liste.
        - Je définis le dossier public (ex. : `build` ou `public`).
        - Je configure pour une **Single Page Application (SPA)** si nécessaire.

---

#### **4. Construire l’application**

- Si le projet utilise un framework moderne (React, Vue, etc.), je build l’application :
    - Exemple pour React :
        
        ```bash
        npm run build
        ```
        
- Je vérifie que le dossier **build** ou **dist** est créé.

---

#### **5. Tester le projet en local**

- Je teste l’application localement pour m’assurer que tout fonctionne :
    
    ```bash
    firebase serve
    ```
    
- Je vérifie que l’application s’affiche correctement à l’URL locale (`http://localhost:5000`).

---

#### **6. Déployer sur Firebase Hosting**

- Une fois prêt, je déploie l’application en production :
    
    ```bash
    firebase deploy
    ```
    
- Je copie et teste l’URL fournie par Firebase pour vérifier que tout fonctionne.

---

### **Résumé rapide**

- **Côté Firebase** : Vérifier le projet, activer les services nécessaires, récupérer les clés.
- **Côté PC** : Vérifier Node.js/Firebase CLI, initialiser Firebase, build le projet, tester en local, puis déployer.

Je laisse un message au stagiaire avec l’URL déployée pour qu’il vérifie tout en revenant. 🚀


#### dans 1 autre ordre
```shell
cd /chemin/vers/jet_3
git init
firebase init
npm install
npm run build
firebase serve
firebase deploy
```

-> [[initialiser Firebase]]
###### Puis GitHub et Git
```shell
git add .
git commit -m "Version du site"

git remote add origin https://github.com/ton-utilisateur/ton-repo.git
git push -u origin master
```

	
## suite
#### **5. Vérification & Configuration**

- Après le déploiement, Firebase CLI te fournit deux types d’URLs :
    
    - **Version live** : accessible publiquement (ex : `https://nom-projet.firebaseapp.com`).
    - **Preview URL** : si tu as utilisé une version temporaire avec `firebase hosting:channel`.
- **Configurer le domaine personnalisé** (optionnel) :
    
    - Depuis la [console Firebase Hosting](https://console.firebase.google.com/), ajoute ton domaine et vérifie le DNS avec Firebase.

---

### **Résumé des commandes principales**

|Commande|Action|
|---|---|
|`firebase login`|Se connecter à Firebase.|
|`firebase init`|Initialiser Firebase dans le projet.|
|`firebase serve`|Tester le site localement.|
|`firebase deploy`|Déployer les fichiers sur Firebase.|
|`firebase logout`|Se déconnecter de Firebase CLI.|

---

### **Bonnes pratiques**

- **Utilise le fichier `.firebaserc`** pour gérer plusieurs projets Firebase dans un même répertoire.
- **Vérifie toujours les logs** après un déploiement pour détecter d’éventuelles erreurs.
- **Active le HTTPS** par défaut (Firebase le gère automatiquement pour Hosting).

En suivant ce processus, ton projet sera correctement déployé sur Firebase et accessible en ligne rapidement.