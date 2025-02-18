---
tags:
  - art/photographie
  - blog
---
[Tout comprendre des capteurs de vos appareils photo et smartphones](https://www.frandroid.com/produits-android/photo/appareil-photo/894453_tout-comprendre-des-capteurs-de-vos-appareils-photo-et-smartphones)

[Pixel binning, HDR, capteurs, mode IA... on vous explique tout sur la photo sur smartphone](https://www.frandroid.com/comment-faire/comment-fonctionne-la-technologie/578741_tout-savoir-photo-smartphone)
- [ ] #_ToDo_/someday/cellphone  A LIRE !!
- [ ] rendre plus concis et MindMap pour comprendre les termes 
###### Les  capteur
Le capteur photo est un composant électronique à base de silicium, de cuivre et de verre chargé de collecter la lumière issue de l’objectif et de la convertir en information électrique.

 Pour collecter la lumière, le capteur est divisé en de multiples petits puits de lumière, appelés **photosites**, généralement carrés, dont la taille est exprimée en microns (µm) voire en nanomètres (nm).

Le tout recouvert par de multiples couches de verre aux rôles bien distincts. De l’extérieur vers l’intérieur :

1. La première a une fonction de barrière physique protectrice, contre les poussières, les projections de lubrifiant, les gouttelettes d’eau (et de salive, mais vous n’êtes pas censés cracher sur vos capteurs).
2. La deuxième couche a pour mission de **filtrer les rayons infrarouges** (IR) à cause desquels vos images pourraient prendre une teinte violette désagréable. Certains photographes choisissent cependant de supprimer ce filtre IR pour, justement, s’adonner aux joies de la photographie infrarouge — notamment en astrophotographie — comme au temps de l’argentique où on utilisait des pellicules dédiées. Il va sans dire que la garantie saute en même temps que le filtre IR.
3. La troisième couche dite _« **filtre passe-bas »**_ ou _« filtre anti-aliasing »_ permet d’ajouter du flou pour minimiser l’artefact d’_aliasing_, ou crénelage en bon français. Ce filtre a tendance à disparaître sur les capteurs récents à très haute définition.
4. La quatrième couche est généralement un **réseau de micro-lentilles** qui permet d’orienter correctement les rayons de lumière vers les photosites (et pas entre les deux). Au centre du capteur photo, ces rayons incidents sont presque perpendiculaires au capteur, puis ils deviennent de plus en plus inclinés au fur et à mesure que l’on se rapproche de la périphérie, compliquant le travail des micro-lentilles et donc leur conception. Cela est d’autant plus vrai sur les appareils photo hybrides que sur les reflex, puisque l’arrière de l’objectif est deux fois plus proche du capteur.
5.  Cinquième et ultime couche : les filtres colorés. Ceux-ci peuvent être de l’une des trois couleurs primaires de la lumière : rouge, vert ou bleu. Ils permettent à chaque photosite de ne capter qu’une seule couleur à la fois, le processeur se chargeant ensuite de reconstituer les deux informations chromatiques manquantes à partir de celles des photosites adjacents (avec parfois quelques erreurs d’estimation). Ce damier coloré forme une matrice qui peut soit être dite de **type Bayer** (du nom de son inventeur) dans l’écrasante majorité des cas, soit de **type X-Trans** (exclusif à Fujifilm), soit un dérivé de la matrice de Bayer (généralement par adjonction de filtres blancs, ou jaunes, ou magenta, ce qui arrive dans certains smartphones). Il peut aussi ne pas du tout y avoir de filtre coloré dans le cas d’un capteur monochrome capable de photographier uniquement en noir et blanc. Cas le plus rare, et exclusif aux APN Sigma, les **capteurs Foveon** se dispensent de filtre coloré. La séparation des couleurs selon leur longueur d’onde se fait alors dans la profondeur du photosite, exploitant pour cela une propriété quantique du silicium (une histoire de potentielle énergie et d’électronvolt).


Matrice de Bayer et matrice Hybride => Pour l'autofocus

Technologie de capteurs CMOS. 


###### BSI CMOS ou FSI CMOS, quelle différence pour quel bénéfice ?

Nous l’avons vu, un capteur photo est constitué de diverses couches et de pistes électriques. Celles-ci peuvent se situer à deux endroits différents : soit devant les photosites (les photons doivent traverser les circuits électriques avant de tomber au fond du puit de lumière), soit derrière (le circuit électrique se trouve tout en bas du capteur, donc n’interfère pas avec le parcours des photons). Dans le premier cas, on parle de capteur **FSI CMOS** (_FrontSide Illuminated_) et dans le second de **BSI CMOS** (_BackSide Illimunated_, souvent traduit par _« rétroéclairé »_). La quasi-totalité des capteurs de smartphones sont de type BSI CMOS depuis l’[iPhone 4s](https://www.frandroid.com/produits/apple/smartphones/252-apple-iphone-4s). Du côté des appareils photo numériques, les BSI CMOS demeurent l’apanage des modèles hybrides et reflex haut de gamme, ce qui leur permet de monter plus haut en sensibilité sans générer de bruit numérique.

![FSI vs BSI - CMOS](https://images.frandroid.com/wp-content/uploads/2021/04/frandroid-fsi-vs-bsicmos.jpg)


Les FSI CMOS restent cependant majoritaires, car, proportionnellement à la taille des capteurs photo, la surface occupée par les pistes électriques demeure acceptable et le coût supplémentaire d’un BSI CMOS ne justifie pas forcément le gain qualitatif. Par défaut, si la fiche mentionne uniquement _« CMOS »_, il est sous-entendu qu’il est de type FSI.


#### La taille, la définition et la résolution : le triangle magique

Maintenant que vous avez décidé quelle technologie de capteur adopter (même si, dans les faits, vous n’avez pas vraiment le choix), reste à déterminer quelle taille et quelle définition correspond le mieux à vos besoins.

###### la taille
Héritage de l’argentique, le format _« 24 x 36 mm »_ est celui à partir duquel tout est calculé et évalué. Les anglophones l’appellent _« Full Format »_, qui ne doit pas être confondu avec un autre FF, qui lui est l’acronyme de _« Full Frame »_.

un capteur photo _« Full Frame »_ est un capteur dont 100 % de la surface disponible est dédiée à la captation de lumière, ce qui est incompatible avec l’architecture des CMOS. Ainsi, un capteur CMOS de 24 x 36 mm de dimension est Full Format, mais pas Full Frame, alors qu’un capteur CCD plus petit peut être Full Frame, mais n’est pas considéré comme Full Format.


La taille du capteur photo a un impact direct sur les focales perçues avec tel ou tel [objectif photo](https://www.frandroid.com/produits-android/photo/appareil-photo/1389315_objectifs-photo-tout-comprendre-aux-differents-types-dobjectifs-pour-bien-choisir), mais le terme _« **focale équivalente »**_ est utilisé. La formulation complète devrait être _« focale équivalente à un objectif de même focale monté sur un capteur 24 x 36 mm »_.

En utilisant un appareil photo doté d’un capteur plus petit que le 24 x 36 mm (et a fortiori un smartphone), il faut donc tenir compte du **facteur de conversion** (ou _« crop factor »_) par lequel multiplier la focale réelle pour obtenir la focale équivalente, ou, au contraire par lequel diviser la focale équivalente (généralement celle donnée par les fiches techniques des smartphones). Ce facteur de conversion est facile à calculer, puisqu’il s’agit de la division de la diagonale d’un capteur 24 x 36 mm (environ 43,27 mm) par la diagonale du capteur considéré.

- [ ] voir tableau des différents fournisseur


###### Définition VS résolution d'un capteur
- La définition d’un capteur correspond au nombre de photosites présents sur ce capteur. Elle est exprimée en pixels (px), mégapixels (1 Mpx = 1 000 000 px) voire gigapixels (1 Gpx = 1 000 000 000 px).
- La résolution d’un capteur correspond à la définition rapportée à la taille du capteur. Elle devrait normalement être exprimée en pixels/cm², mais, par commodité, il est souvent question de pixels par pouce (« _pixel per inch »_ ou _ppi_ ), qui est une densité linéaire exprimée dans une unité impériale.

En d’autres termes, la définition est toujours une population et la résolution est une densité de population rapportée à une surface donnée. Ainsi, à taille de capteur égale, plus la définition est élevée, plus la résolution est élevée. Par contre, à définition égale, un capteur photo plus grand aura une résolution plus faible que le capteur plus petit. La résolution seule, quant à elle, ne vous dira rien de la taille ni de la définition du capteur.

![](https://images.frandroid.com/wp-content/uploads/2021/04/frandroid-tailledefinitionresolution.jpg)
Imaginez que ces schémas représentent quatre capteurs (A, B, C, et D) et leurs photosites. Alors :  
– Les capteurs A et D ont la même taille, mais pas la même définition donc pas la même résolution. Idem pour les capteurs B et C.  
– Les capteurs C et D ont la même définition, mais, ne faisant pas la même taille, n’ont pas la même résolution. Idem pour les capteurs A et B.  
– Les capteurs A et C ont la même résolution, mais n’ont ni la même taille, ni la même définition.



Dans les faits, la résolution sert surtout à déduire la **taille des photosites**, exprimée en micron (µm), information plus souvent utilisée pour les modules photographiques des smartphones que pour les capteurs des APN.


#### gros capteur photo
plus grand est le capteur, plus grands seront les photosites (à définition égale), ce qui permet de [monter plus haut en sensibilité](https://www.frandroid.com/produits-android/photo/758940_triangle-dexposition-comment-gerer-louverture-la-vitesse-et-la-sensibilite-de-vos-photos) ou, du moins, à sensibilité égale, d’obtenir des résultats plus propres. L’autre avantage d’un grand capteur photo est d’obtenir une profondeur de champ plus courte : à ouverture, focale et distance au sujet égale, ce dernier se détachera mieux de l’arrière-plan flou. Idéal si vous êtes amateur de portraits !

#### petit capteur photo
Un capteur plus petit permet de faire des appareils photo plus petits. Plus faciles à stabiliser, chauffant moins, ces capteurs du fait de leur physique transportent également les signaux électriques plus rapidement, d’où des rafales et des cadences vidéo plus élevées. Autres avantages, les objectifs compatibles peuvent être plus petits et, surtout, le _« crop factor »_ permet d’atteindre plus aisément de longues focales sans sacrifier les ouvertures, ce qui est particulièrement pratique en photo de sport, animalière ou d’action.


Revers de la médaille, ce facteur de conversion rend plus compliquée l’obtention de très grands angles et, parallèlement, à focale équivalente et ouverture identique, la profondeur de champ est plus importante sur un petit capteur. Pour beaucoup, cela peut sembler un inconvénient, mais, dans les faits, c’est plutôt pratique, surtout en vidéo.


#### avantages et inconvénients des hautes définitions ?
Un capteur photo plus défini est, théoriquement, plus précis puisqu’à taille de capteur égale, vous gagnez en pouvoir résolvant (c’est l’aptitude à discerner les détails les plus en plus fins). Avec cette augmentation, vous pouvez vous passer d’un filtre passe-bas (celui dont nous parlions au tout début), mais, pour autant, le risque zéro n’existe pas en ce qui concerne le crénelage ou le moirage (_aliasing_ et _moiré_ en anglais).

Une plus grande définition, cela autorise aussi une plus grande souplesse de travail en post-traitement : recadrage, correction des perspectives, travail plus détaillé, plus grandes possibilités d’impressions, etc. En augmentant la définition en photo, vous augmentez également celle en vidéo. Si la Full HD est le minimum syndical, la 4K (UHD ou DCI) est aujourd’hui la norme, mais il faudra au minimum 33 Mpx (sur un capteur 16:9) ou 45 Mpx (sur un capteur 3:2) pour espérer filmer en 8K (UHD ou DCI). Enfin, dans le cas des smartphones, augmenter la définition du capteur photo permet d’obtenir un zoom numérique (par recadrage) plus convaincant.


En contrepartie, en optant pour un capteur photo plus défini, vous gagnez aussi le droit d’acheter des [cartes mémoires](https://www.frandroid.com/produits-android/photo/appareil-photo/1344337_carte-sd-microsd-sdxc-sdhc-tout-savoir-sur-les-normes-de-cartes-memoires) plus grosses et des disques durs (ou SSD) plus volumineux

> les photosites doivent mesurer au moins 0,75 micron pour être en mesure de capturer les rouges les plus extrêmes

Néanmoins, le plus gros problème des hautes définitions, et donc de fortes résolutions, est rarement évoqué. À taille de capteur équivalent, la taille des photosites diminue de manière proportionnellement inverse à la hausse de la résolution. Or la photographie telle que nous la connaissons a besoin de lumière pour fonctionner, et plus spécifiquement le spectre visible de la lumière. Pour rappel, il s’étend de 400 nm de longueur d’onde pour le bleu proche ultra-violet (UV) et jusqu’à environ 750 nm pour le rouge proche infrarouge (IR). Cela implique que les photosites doivent, au plus petit, mesurer 750 nanomètres (soit 0,75 micron) de large pour être en mesure de capturer les nuances de rouges les plus extrêmes.



# Conseil pour choisir 
Conseil généraux car avec Deep-learning et les algorithmes, sa change un peu la donne.
### Si vous photographiez essentiellement avec votre smartphone

- Ne prêtez pas d’attention ni à la taille ni à la définition de votre capteur.
- Fuyez les sirènes des très hautes définitions.
- Privilégiez un modèle récent couplé à un objectif lumineux et/ou proposant des focales dont vous serez susceptibles d’avoir besoin.
- Évitez de débrayer les automatismes et réglages appliqués par défaut, ceux-ci participant pour beaucoup de la qualité du rendu final.
- Faites-vous plaisir, en vous rappelant que les meilleures photos sont faites avec l’appareil que vous avez toujours sur vous.

### Si vous souhaitez un APN pour la photographie généraliste « en amateur »

- Un capteur photo de 20 à 24 Mpx suffit amplement, quelle que soit sa taille.
- Préférez, si possible, un APN avec capteur stabilisé.
- L’offre optique disponible et l’ergonomie des boîtiers sont plus importantes que la taille et la définition du capteur.
- Investissez dans des objectifs nouveaux ou, dans le cas des hybrides, des adaptateurs pour redécouvrir les joies des optiques « _vintage_ ».

### Si vous pratiquez la photographie d’action/de sport/d’animaux/de mariages ou pour photographier vos enfants (c’est pareil)

- Un capteur photo de 20 à 24 Mpx suffit.
- Optez, si possible, pour un capteur BSI CMOS et stabilisé.
- Préférez les capteurs plus petits (APS-C, 4/3 ») pour obtenir des focales longues, légères et lumineuses.
- Si vous optez pour un capteur 24 x 36 mm, optez pour un modèle de plus de 40 Mpx afin de bénéficier d’une marge de recadrage supplémentaire.
- Mettez surtout l’accent sur la rapidité et la précision de l’autofocus.

### Si vous êtes un adepte du portrait

- Un capteur photo de 20 à 24 Mpx suffit. Un capteur plus défini sera plus détaillé… vous verrez donc mieux les défauts de la peau.
- Les capteurs 24 x 36 mm permettent d’obtenir de plus faibles profondeurs de champ, mais les résultats seront tout aussi bons avec de [l’APS-C](https://www.frandroid.com/produits/appareils-photo/appareil-photo-aps-c) et du Micro 4/3.
- 75 % du rendu final sera conditionné par l’objectif, bien plus que le boîtier et son capteur. Cherchez d’abord un objectif dont le rendu vous plaît, puis choisissez votre boîtier en conséquence.
- Un autofocus avec détection des yeux efficace est un plus non négligeable.

### Si vous êtes passionné de photographie de rue

- Un capteur photo de 20 à 24 Mpx suffit, mais il n’y a pas de restriction à vouloir plus.
- Préférez, si possible, un capteur BSI CMOS plus à l’aise en haute sensibilité pour éviter l’utilisation du flash (histoire de rester discret).
- Optez si possible pour un capteur stabilisé.
- Quelle que soit la taille de votre capteur, vérifiez qu’il existe des objectifs 28, 35, 50 ou 85 mm (ou équivalents) lumineux dans la monture pour laquelle vous avez opté.
- Un autofocus réactif est un plus.

### Si vous êtes fasciné par les paysages ou l’architecture

- Plus haute sera la définition, mieux ce sera.
- La stabilisation n’est pas indispensable, surtout si vous travaillez régulièrement sur trépied.
- Les capteurs plus petits permettront des boîtiers plus légers donc plus faciles à transporter.
- Choisissez surtout un boîtier bien protégé contre la poussière et les infiltrations d’eau, pour résister aux conditions climatiques variées.
- Portez une attention particulière à l’autonomie et à la possibilité de recharger en USB, notamment pour les poses longues de nuit.
- C’est l’un des rares cas où les capteurs Foveon prennent tout leur sens.