# Changelog kTwinkly

>**IMPORTANT**
>
>Pour rappel s'il n'y a pas d'information sur la mise à jour, c'est que celle-ci concerne uniquement de la mise à jour de traduction ou de texte.

## ``BETA`` 5 Décembre 2022

Mise à jour de la liste des produits depuis la dernière version de l'application Twinkly.

Corrections sur l'upload des animations et playlists par drag and drop.

Quelques corrections cosmétiques.

## ``BETA`` 22 Novembre 2022

Une action sur la luminosité permet d'allumer (luminosité > 0) ou d'éteindre (luminosité = 0) la guirlande.

## ``STABLE`` 5 Novembre 2022

Passage en stable de toutes les évolutions et corrections disponibles en beta.

**IMPORTANT : Si vous venez de la version stable, il est nécessaire de supprimer et recréer les équipements pour recréer les commandes et les identifiants internes.**
**La suppression des équipements efface également les animations liées à la guirlande. Si vous avez capturé des animations, pensez à les télécharger sur votre ordinateur pour pouvoir les remettre en suite.**
**Cette opération n'est pas nécessire si vous venez de la dernière beta**

## ``BETA`` 19 Octobre 2022

Modification de la page des commandes pour s'adapter aux nouveautés du core 4.3.

Correction du bouton Tester manquant sur les commandes actions.

## ``BETA`` 20 Décembre 2021

Suppression de la commande "Effacer mémoire" pour les guirlandes GEN1 (cette opération n'est pas supportée par le firmware)


## ``BETA`` 18 Décembre 2021

Possibilité d'ajouter des images pour les équipements qui n'en disposent pas.

Limitation de la taille d'une playlist à 15 animations maximum.


## ``BETA`` 14 Décembre 2021

Quelques corrections de bugs.

Indication de l'animation courante en mode playlist et movie (en GEN2 uniquement, non supporté en GEN1).

**IMPORTANT : Il y a eu quelques changements sur la création des commandes. Je conseille de supprimer et recréer les équipements. N'oubliez pas de sauvegarder vos animationset playlist localement pour pouvoir les recharger (en utilisant la fonction export/import).**


## ``BETA`` 12 Décembre 2021

Corrections diverses :
 - meilleure gestion d'erreur lors de la suppression des playlists et animations 
 - masquage des boutons import/export pour Twinkly Music (non applicable)
 - correction du bouton "Recherche" (détection des équipements) rendu inopérant suite à une modification sur la version précédente
 - téléchargement de plusieurs animations simultanément sous forme d'un zip (pour l'instant, il n'est pas possible de recharger ce zip directement, il faut charger chaque animation séparément)
 - ajout de plusieurs animations en même temps
 - quelques corrections de bugs coté interface graphique


## ``BETA`` 11 Décembre 2021

Un grand nombre de corrections sur la gestion des playlists qui devraient éviter beaucoup de problèmes (erreurs 1106).

Possibilité d'exporter/impoter les animations et playlist d'un équipement sous forme d'un fichier zip.

Modification des actions sur l'écran playlist :
 - la sauvegarde de la playlist ne la charge pas immédiatement sur la guirlande. Il faut utiliser l'action "Activer"
 - l'action "Effacer la playlist" ne vide pas la mémoire. IL faut utiliser l'action "Effacer la mémoire" pour cela
 - il est possible de télécharger une playlist puis de la recharger plus tard. La gestion de plusieurs playlists viendra (probablement) plus tard.


## ``STABLE`` 11 Décembre 2021

Passage en stable des modifications de la beta du 8 décembre.


## ``BETA`` 8 Décembre 2021

Corrections de bugs :
 - Correction d'un bug sur la gestion des playlists qui provoquait des erreurs 1106
 - Correction de l'option "vider la mémoire" qui n'avait pas d'effet. Si cette case est cochée la mémoire sera complétement vidée lors de l'envoi d'une animation ou l'enregistrement d'une playlist. Sinon, les animations déjà en mémoire seront conservées.

Ajout de nouvelles commandes :
 - Action pour vider la mémoire. Il est toujours possible de vider la mémoire par le bouton présent sur l'écran de la playlist
 - Utilisation basique du mode "couleur"


## ``STABLE`` 7 Décembre 2021

Correction du on/off sur les GEN1 qui n'ont aucune animation de chargée

Ajout de nouvelles commandes dans la classe de gestion TwinklyStrings, non encore implémentées dans le plugin (à venir pour une prochaine release)


## ``STABLE`` 2 Décembre 2021

Passage de toutes les modifications de la dernière ``BETA`` en ``STABLE``
 - Amélioration de la gestion des authentifications. Normalement, moins d'erreurs en cas d'utilisation simultanée de Jeedom et de l'app sur smartphone.
 - Gestion avancée des playlists sur les guirlande Gen II
 - Support minimal de Twinkly Music
 - Correction de l'installation de dépendances (Python 3.7+ et mitmproxy)

**IMPORTANT : Il est nécessaire de supprimer et recréer les équipements pour recréer les commandes et les identifiants internes.**
**La suppression des équipements efface également les animations liées à la guirlande. Si vous avez capturé des animations, pensez à les télécharger sur votre ordinateur pour pouvoir les remettre en suite.**


## ``BETA`` 27 Novembre 2021

Corrections pour Twinkly Music


## ``BETA`` 25 Novembre 2021

Changement impactant : il y a maintenant 2 commandes info différentes : Etat (on/off) et Mode Courant (movie/playlist/off) qui remplace la commande Etat des versions précédentes.

**IMPORTANT : Il est nécessaire de supprimer et recréer les équipements.**

Ajout de la gestion du Twinkly Music : découverte automatique des équipements et commandes basic on / off. A cause de ce changement, la découverte d'équipements est un peu plus longue.


## ``BETA`` 07 Novembre 2021

Mise à jour de la liste des produits et des images depuis la dernière version de l'application mobile. Ajoute notamment le support des gammes Flex et Line.


## ``STABLE`` 17 Octobre 2021

Ajoute d'une dépendance manquante.


## ``BETA`` 02 Février 2021

Correction pour permettre la désactivation d'un équipement injoignable. La réactivation reste impossible.


## ``BETA`` 28 Janvier 2021

Correction d'un bug lié au cache des tokens dans le cas de guirlandes multiples.


## ``BETA`` 26 Janvier 2021

Meilleure gestion des tokens d'authentification.

Ajout d'une option pour vider systématiquement la mémoire du contrôleur lors du chargement des playlists. A utiliser lors d'un changement "massif" de la playlist, ou lors du chargement d'une grosse playlist pour éviter de saturer la mémoire. A utiliser également en cas d'erreur de chargement de la playlist. A terme, un test de la mémoire disponible sera réalisé avant upload pour éviter de tenter de charger une liste trop grosse, mais ce n'est pas encore implémenté.


## ``BETA`` 16 Décembre 2020

Nouvel écran dédié de gestion de la playlist, avec possibilité de choisir la durée de chaque animation.


## ``STABLE`` 15 Décembre 2020

Gestion des playlists, sans possibilité de changer le timing pour l'instant (30 secondes entre chaque animation).


## ``BETA`` 14 Décembre 2020

Correction du script d'installation des dépendances pour les Raspberry Pi sous Debian 9/Strech à cause d'une incompatibilité entre le module *cryptography* installé via PyWheels avec la version 1.1.0 de OpenSSL installée sur cet OS.



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

