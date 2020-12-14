# Changelog kTwinkly

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de traduction ou de texte.



## ``BETA`` 14 Décembre 2020

Correction du script d'installation des dépendances pour les Raspberry Pi sous Debian 9/Strech à cause d'une incompatibilité entre le module cryptography installé via PyWheels et avec la version 1.1.0 de OpenSSL installée sur cet OS.



## ``BETA`` 12 Décembre 2020

Correction du script d'installation des dépendances pour installation python3.7 depuis les repos apt s'il est disponible



## ``BETA`` 11 Décembre 2020

Correction d'un bug sur le chargement des animations GEN2 hors playlist

Optimisation du changement d'animation (pas de rechargement en mémoire si l'animation est déjà présente dans le contrôleur)

Nouvelle optimisations et corrections des actions "supprimer playlist" et "vider mémoire"

Quelques corrections ergonomiques sur l'écran de gestion de playlists

Suppression temporaire de la page de configuration MQTT



## ``BETA`` 10 Décembre 2020

Ajout d'une popup de confirmation de suppression des animations

Première version pour la gestion des playlists pour les guirlandes qui supportent cette fonctionnalité

- Ajout d'un bouton **Créer une nouvelle playlist** sur l'écran des animations pour supprimer la playlist courante et ajouter uniquement les animations sélectionnées

- Ajout d'un bouton **Ajouter à la playlist courante** sur l'écran des animations pour ajouter les animations sélectionnées à la playlist courante

- Ajout d'un bouton **Supprimer la playlist** pour effacer la playlist courante

- Les éléments sont ajoutés dans l'ordre où sont affichées les animations dans l'écran de gestion. Il est possible de réordonner les lignes avant d'utiliser les boutons pour choisir l'ordre. Si le bouton **Sauvegarder** n'est pas utilisé, l'ordre ne sera pas conservé pour la liste déroulante des animations.

- Pour l'instant, la durée d'affichage n'est pas configurable, elle est de 30 secondes entre 2 animations

- Si une playlist est définie, la commande "On" va relancer la playlist, sinon, elle réutilise la dernière animation

  

## ``STABLE`` 09 Décembre 2020

Première version stable basée sur la beta du 9 Décembre 2020



## ``BETA`` 09 Décembre 2020

Changement du nom par défaut des animations capturées ou chargées

Simplification de la fenêtre de gestion des animations



## ``BETA`` 07 Décembre 2020

Mise à jour du script d'installation des dépendances :

- Installation de python 3.7.3 en mode “altinstall” pour Debian 9

- Nouveau process d’installation de mitmproxy via pip

Ajout d’une nouvelle option pour avoir des logs de mitmproxy (kTwinkly_mitm)

Image d’équipement par défaut si l’image n’est pas trouvée dans la librairie du plugin



## ``BETA`` 06 Décembre 2020

Renommage de la classe utilitaire de Twinkly en TwinklyString pour éviter les éventuels conflits avec l'autre plugin Twinkly.

Utilisation du mode "effect" au lieu du mode "movie" pour les guirlandes GEN2.

Correction du process de démarrage du proxy mitmdump.



## ``BETA`` 05 Décembre 2020

Publication de la première version beta

