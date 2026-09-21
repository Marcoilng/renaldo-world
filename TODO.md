# Plan d'Optimisation de la Vitesse de Chargement de index.html

## Informations Recueillies
- Le fichier HTML charge de nombreuses ressources externes : Tailwind CSS, Google Fonts, icônes Lucide, Font Awesome, styles.css personnalisés, et de nombreuses images.
- Les images sont chargées de manière avide par défaut, causant un chargement initial lent.
- Aucun indice de ressource comme preconnect ou preload n'est présent.
- Les polices et scripts sont chargés sans indices d'optimisation.

## Plan
- Ajouter des liens preconnect pour les domaines externes (fonts.googleapis.com, fonts.gstatic.com, unpkg.com, cdnjs.cloudflare.com, images.unsplash.com) pour réduire le temps de recherche DNS.
- Précharger les ressources critiques : favicon et image de fond du héros.
- Ajouter loading="lazy" aux images en dessous du pli (sections bio, services, événements) pour différer le chargement jusqu'à ce qu'elles soient nécessaires.
- S'assurer que les images ont des attributs alt appropriés et envisager d'ajouter width/height si possible.

## Fichiers Dépendants à Modifier
- index.html (seul fichier à modifier)

## Tâches Terminées
- [x] Ajouté des liens preconnect pour les domaines externes
- [x] Préchargé les ressources critiques (favicon et image du héros)
- [x] Ajouté loading="lazy" aux images dans la section bio
- [x] Ajouté loading="lazy" aux images dans la section services
- [x] Ajouté loading="lazy" aux images dans la section événements

## Étapes de Suivi
- Tester le temps de chargement du site web en utilisant les outils de développement du navigateur ou des testeurs en ligne.
- Vérifier que les images chargées paresseusement se chargent lors du défilement.
- Vérifier les liens cassés ou les ressources manquantes.
