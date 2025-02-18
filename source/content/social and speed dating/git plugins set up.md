---
tags:
  - productivity/obsidian
  - coding/git
---
> **Instructions pour configurer le plugin Obsidian Git (à faire ==une seule fois)==**

Bienvenue sur le **vault partagé** ! 🎉  
Ces étapes doivent être faites **une seule fois** pour que tout fonctionne bien. **Pas besoin de comprendre Git, il suffit de suivre exactement ces instructions.**

---

## **1️⃣ Activer le plugin Obsidian Git**

1. Ouvrez **Obsidian**.
2. Allez dans **Paramètres (⚙️ en bas à gauche)**.
3. Allez dans **Plugins communautaires** → **Parcourir**.
4. Recherchez **"Obsidian Git"** et cliquez sur **Installer**.
5. Cliquez sur **Activer**.

---

## **2️⃣ Configurer les paramètres du plugin**
Retournez dans **Paramètres** → **Git**. **Modifiez les paramètres suivants** :
dans **Automatic**
- **Split timers for automatic commit and sync** ✅ **ACTIVÉ**
 - **"Auto commit and sync interval (min)"** → **5** ✅ **ACTIVÉ**
    - (Obsidian enregistre dans GIT toutes les modifications toutes les 5 minutes).
- **Auto push interval (minutes)** → **10** ✅ **ACTIVÉ**
- **Auto pull interval (minutes)** → **5** ✅ **ACTIVÉ

Résumé du fonctionnement après configuration **dans Automatic** :
- **Toutes les 5 minutes**, vos modifications sont **sauvegardées localement** (commit auto).
- **Toutes les 10 minutes**, elles sont **envoyées sur GitHub** (push auto).
- **Toutes les 5 minutes**, votre vault se met **automatiquement à jour** avec les modifications de l’équipe (pull auto).



dans **Pull**
- **Pull on startup**, **Push on commit & sync** et **Pull on commit and sync** -> ✅ **ACTIVÉ**


dans **Miscellenous**
- **Cochez "Show status bar"** → ✅ **ACTIVÉ** (permet de voir si tout est bien synchronisé).



📌 **IMPORTANT** :
- **Ne changez aucun autre réglage**, sinon il pourrait y avoir des erreurs pour l’équipe.
- Si vous avez un problème, demandez à [nom de l’admin Git] avant de modifier quoi que ce soit.

---

## **3️⃣ Tester si tout fonctionne** 🚀

1. Écrivez **n'importe quoi** dans une note.
2. Attendez **5 minutes** ou allez dans la **Palette de commandes (Ctrl + P / Cmd + P sur Mac)**.
3. Tapez **"Git: Commit-and-sync with specific message"** et sélectionnez-le.
4. Si tout va bien, **Obsidian a sauvegardé votre travail** et vous êtes **synchronisé avec l’équipe** ! 🎉

Si vous voyez une erreur, dites-le à [nom de l’admin Git].

---

✅ **C'est tout !** Vous n’avez plus rien à toucher, tout fonctionne automatiquement.  
**Écrivez vos notes normalement, et Obsidian Git s’occupe du reste.** ✨