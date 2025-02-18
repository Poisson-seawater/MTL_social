---
tags:
  - coding/website
---
Une **Single Page Application (SPA)** est une application web qui charge **une seule page HTML** et met à jour dynamiquement son contenu sans recharger complètement la page. Cela offre une expérience utilisateur fluide, similaire à celle d'une application native.


### **Fonctionnement d'une SPA**

1. Lorsqu’un utilisateur accède à une SPA, une seule page HTML est chargée (souvent **`index.html`**).
2. Ensuite, le **JavaScript** de l'application prend le contrôle :
    - Il gère la navigation entre les pages (sans rechargement complet).
    - Il met à jour dynamiquement certaines parties de la page en fonction des actions de l'utilisateur.
3. Les ressources comme le CSS, JS, et les données sont chargées une fois, puis mises en cache.

### **Avantages des SPAs**

1. **Rapidité** : Une fois la page initiale chargée, les transitions entre les sections sont instantanées.
2. **Expérience utilisateur améliorée** : Pas de rechargement complet = navigation fluide.
3. **Moins de charge sur le serveur** : Le serveur envoie uniquement les données nécessaires, et non une nouvelle page HTML entière.
4. **Utilisable comme une PWA** : Les SPAs peuvent facilement devenir des Progressive Web Apps (installables sur mobile).


# Set up avec [[Firebase]]
### **Quand Répondre "Yes" ?**

Réponds **"Yes"** si :

- Ton site est développé avec **React**, **Vue**, **Angular**, **Svelte**, ou tout autre framework SPA.
- La navigation est gérée côté client.

Réponds **"No"** si :

- Tu as un site statique classique avec plusieurs fichiers HTML séparés.
