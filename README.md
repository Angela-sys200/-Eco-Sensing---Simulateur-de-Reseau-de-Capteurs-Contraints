# -Eco-Sensing---Simulateur-de-Reseau-de-Capteurs-Contraints
Ce projet a pour objectif de simuler un réseau de capteurs agricoles autonomes (IoT) ayant des contraintes strictes de mémoire et d’énergie. Chaque capteur est capable de mesurer des données environnementales (température ou humidité), de les stocker temporairement dans une mémoire tampon (buffer) limitée à 5 paquets, et de les transmettre ensuite à une station de base située en (0,0).

Le projet met en œuvre des listes chaînées dynamiques pour gérer la mémoire de manière efficace, tout en respectant des contraintes "hardware" :  
- mémoire RAM très faible,  
- batterie limitée,  
- coût énergétique pour chaque transmission.

Le programme doit :
- produire et stocker des mesures dans un buffer dynamique,
- supprimer le plus ancien paquet avec free() quand le buffer est plein,
- afficher une alerte quand une suppression est nécessaire,
- simuler la consommation d’énergie à chaque envoi,
- enregistrer automatiquement un journal (log.txt) avec les données clés (temps, batterie, nombre de paquets).
- Ce projet intègre à la fois la gestion mémoire en C (pointeurs, malloc, free), la simulation de comportements physiques (distance, consommation), et la persistance des données via des fichiers.

