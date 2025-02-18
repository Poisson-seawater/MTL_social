---
tags:
  - outils/firebase
---
> [!info] Rappel des questions et leur significations !!

###### Sommaire
- are you ready to proceed: **YES**
- Which Firebase features do you want to set up for this directory? 
	- *demander a chat des conseil*
- Choisir si on prend un projet firebase deja existant ou on en créer un
- **Public directory** : mets `dist` si tu utilises **Vit
-   **[[Single Page App (SPA)]]** : réponds **Yes**.


autre:
 - "Set up the workflow to run a build script before every deploy? (y/N)" -> y

----
2. **Lors des prompts :**
    - Sélectionne **Hosting** pour déployer le site.
    - Ignore Firestore si tu n'as pas besoin de créer de nouvelles règles.
    - **Public directory** : mets `dist` si tu utilises **Vite** (ou un autre dossier de build).


### Firestore setup
- **`firestore.rules`** est le nom standard utilisé par Firebase pour les règles de sécurité Firestore.
- => **DONC:** juste appuyer sur "Entré"


###### personalisation au besoin
```shell
rules_version = '2';
service cloud.firestore {
  match /databases/{database}/documents {
    match /{document=**} {
      allow read, write: if request.auth != null;
    }
  }
}
```

Puis déployer dans [[git]]: `firebase deploy --only firestore`


