# Outil de capture des animations

[Retour à la documentation du plugin](index.md)

Ce package utilise l'outil opensource mitmproxy (mitmdump) pour capturer les échanges entre l'application Twinkly s'exécutant sur votre smartphone et le contrôleur de la guirlande lorsqu'une animation est téléchargée sur la guirlande. Les informations sur l'animation sont sauvegardées dans un fichier zip qu'il faut ensuite charger sur le plugin Jeedom. L'animation pourra ensuite être envoyée à la guirlande depuis Jeedom et intégrée dans une playlist.

## ``PRE-VERSION`` 12 Décembre 2012

Le package est disponible uniquement sur Windows. Il faut [dézipper le fichier](../ProxyTool/kTwinklyCapture_20221212-1.zip), lancer la commande kTwinklyCapture.exe et suivre les indications.

Après avoir saisi l'adresse IP de la guirlande (visible sur la page de de l'équipement dans Jeedom), et éventuellement changé le port du proxy (14233 par défaut), cliquer sur le bouton pour démarrer la capture.

Il faut paramétrer le proxy sur le smartphone, comme indiqué dans la documentation du plugin, puis lancer l'application Twinkly et télécharger les animations vers la guirlande depuis la gallerie (en utilisant ler bouton "Appliquer" depuis la prévisualisation de l'animation).

Si la capture s'est bien passée, les animations seront disponibles dans un sous-dossier "Movies" à coté de l'outil de capture.

Pour ajouter l'animation à Jeedom, accéder à la page "Gérer les animations" depuis l'équipement, et utiliser le bouton "Ajouter" (ou faire un glisser/déplacer du zip vers la fenêtre).

Attention : une animation n'est valable que pour la guirlande utilisée lors de la capture.
