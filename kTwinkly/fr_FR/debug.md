# Capture des requêtes de l'application smartphone

La procédure suivante peut être utilisée pour capturer les échanges entre l'application smartphone Twinkly et les guirlandes, pour du diagnostic, ou pour permettre d'implémenter de nouvelles fonctionnalités.

La procédure est décrite pour Windows, mais elle est transposable facilement sur MacOS.

L'installation des dépendances du plugin kTwinkly ajoute également l'outil mitmproxy sur la machine Jeedom. Au lieu de l'installer sur une autre machine, il est possible de lancer l'outil mitmdump comme indiqué ci-dessousn se connectant en SSH au serveur Jeedom. 
Il faudra ensuite tranférer le fichier de dump vers une autre machine.

## Installation du mitmproxy/mitmdump

On utilisera la version zip plutôt que l'outil d'installation.

Télécharger le package zip de mitmproxy : https://snapshots.mitmproxy.org/7.0.4/mitmproxy-7.0.4-windows.zip
Le décompresser dans un dossier c:\mitmproxy. Si un sous dossier a été créé lors de l'extraction, déplacer les fichiers directement dans c:\mitmproxy

## Démarrage du proxy de capture

Ouvrir une invite de commande et se placer dans le dosssier d'installation (```cd c:\mitmproxy```)
Lancer le proxy avec la commande ```mitmdump -w twinkly.txt "~u xled|xmusic"```  Accepter  l'accès au travers du firewall si c'est demandé.
Si le port 8080 utilisé par défaut par mitmdump est déjà pris, utiliser l'option ```-p xxx``` pour utiliser un autre port (xxx = numéro de port, utiliser une valeur > 1024)

L'écran suivant doit s'afficher:
(screenshot)

## Configurer le proxy sur le smartphone

Configurer le proxy sur le smartphone en utilisant la procédure décrite dans la documentation du plugin : https://kimagurefr.github.io/jeedom_docs/kTwinkly/fr_FR/#etape-3---configuration-du-smartphone-sur-des-mobiles-apple

Utiliser l'adresse IP de la machine où s'exécute mitmdump, et le port (8080 par défaut, ou la valeur spécifiée par l'option -p)

## Capturer les appels à l'API depuis le smartphone

Lancer l'application Twinkly sur le smartphone, puis lancer les diverses commandes à capturer vers les différentes guirlandes.

Si le proxy fonctionne, on doit voir du texte défiler dans l'écran mitmdump.
Si ce n'est pas le cas, ou si l'application Twinkly ne marche pas, c'est que le proxy n'est pas configuré correctement ou n'est pas joignable.

## Terminer la capture

Fermer l'application mitmdump en utilisant la combinaison de touches Ctrl-C.
Le fichier indiqué sur la ligne de comamnde après l'option w (twinkly.txt dans l'exemple) contient tous les échanges HTTP entre le smartphone et les guirlandes.
C'est ce fichier qu'il faudra communiquer au développeur.

