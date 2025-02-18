---
tags:
  - outils/firebase
---
#### **Récupérer les clés et identifiants nécessaires**

##### **1. Accéder aux paramètres du projet Firebase**

Je me rends dans la [console Firebase](https://console.firebase.google.com/) et sélectionne le projet. Dans le menu à gauche, je clique sur **Paramètres du projet** (icône ⚙️ en bas à gauche).

##### **2. Obtenir la configuration Firebase pour l’application**

Je récupère les clés nécessaires selon le type de projet :

- **Web** : Dans l’onglet **Général**, section **Vos applications**, je copie le script de configuration (clé `apiKey`, `authDomain`, `projectId`, etc.).
- **Android/iOS** : Si l'application mobile utilise Firebase, je télécharge les fichiers nécessaires :
    - **Android** : le fichier `google-services.json` dans **Outils pour Android**.
    - **iOS** : le fichier `GoogleService-Info.plist` dans **Outils pour iOS**.

##### **3. Vérifier les accès API et service**

Je m’assure que les services Firebase nécessaires (Firestore, Auth, etc.) sont activés. Si des accès API sont requis, je vérifie les autorisations depuis **Google Cloud Console** → **IAM et Administration**.

##### **4. Générer des clés de service (si nécessaire)**

Si le projet utilise des scripts ou un backend nécessitant des accès **admin** :

- Je vais dans **Comptes de service** → **Clés privées**.
- Je clique sur **Générer une clé privée** pour récupérer un fichier JSON.

##### **5. Partager les informations de manière sécurisée**

Une fois les clés récupérées, je m’assure de ne pas les exposer dans le code. Je les stocke dans un fichier `.env` ou dans un gestionnaire sécurisé comme **GitHub Secrets** ou **Vault**.

---

Je laisse tout prêt sur le PC avec une note claire pour le stagiaire : les identifiants sont sécurisés, les fichiers nécessaires sont ajoutés au projet, et tout est prêt pour continuer.