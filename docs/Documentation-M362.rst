.. role:: raw-html-m2r(raw)
   :format: html


Module 362 : Mettre en service les systèmes vocaux et vidéo complexes
=====================================================================



:raw-html-m2r:`<img src="https://upload.wikimedia.org/wikipedia/commons/a/a2/3CX_Logo_-_Wiki.png" align="right" height="32px" />`

3CX
----------

Qu'est-ce que 3CX ?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

3CX est une **solution de communications virtuelle** qui permet aux entreprises de gérer leurs appels téléphoniques, leur messagerie instantanée, leur vidéoconférence ainsi que tous les services que pourrait proposer un PBX classique, grâce à différentes installations et forfaits.

12 millions d'utilisateurs l'utilisent chaque jour, le placant donc sans souci sur le podium des leaders mondiaux de la téléphonie !

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-paccueil.png" align="center"/>`

----

Licences
^^^^^^^^^^^^^^^^^^^^

Pour avoir une vue d'ensemble plus concrète de ce que propose 3CX en tant que service ou système, il est important de connaître les différentes licences proposées par l'entreprise du même nom.

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-licences.png" align="center"/>`

----

Différents types d'installation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

:raw-html-m2r:`<br>`

:raw-html-m2r:`<img src="https://imgs.search.brave.com/t5Gh4h12EKJUKsBYlQEidsH_O2SyxBPQABqSv3rnPxU/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9icmFu/ZHNsb2dvcy5jb20v/d3AtY29udGVudC91/cGxvYWRzL2ltYWdl/cy9kZWJpYW4tbG9n/by5wbmc" align="right" height="32px" />`

Linux
~~~~~~~~~~~~~~

:raw-html-m2r:`<br>`

Chez 3CX, le principal avantage de leur système est leur **OS basé sur Debian** qui est **optimisé pour leur PBX virtuel.**

L'installation s'avère simple si l'on est familiarisé avec le milieu de la virtualisation sous linux.

:raw-html-m2r:`<u>Voici les prérequis matériels pour l'installation de 3CX sur Debian : </u>`

**Votre machine a besoin d'au moins 1 cœur de processeur dédié et de 2Go de RAM. Si vous hébergez vous-même votre machine et que votre hébergeur utilise une unité centrale partagée, vous avez besoin de 2 cœurs !**

Passez en revue les spécifications matérielles suggérées afin d'allouer du temps d'unité centrale et des ressources de mémoire vive supplémentaires en fonction des critères suivants :


* Nombre d'appels simultanés gérés par le système.
* Nombre d'utilisateurs actifs - 100 sessions actives du client Web sont plus exigeantes que 100 appels occasionnels via des téléphones IP.
* L'utilisation de l'enregistrement des appels - le système est sollicité pour le mixage audio et le stockage des fichiers.

..

   3CX peut être installé sur n'importe quel système fonctionnant sous Debian 12. Si vous souhaitez faire une installation barebone, assurez-vous que le matériel fonctionne avec Debian 12 et que le fournisseur du matériel vous aidera en cas de problème. Nous ne pouvons pas vous aider à résoudre les problèmes liés à l'installation de Debian 10 sur du matériel " barebone ".

   Ne configurez pas de réseau virtuel, d'interface VPN ou d'option TeamViewer VPN sur l'hôte 3CX.


Pour les autres prérequis liés à la virtualisation, au réseau etc... Je vous invite à vous référer à leur documentation complète disponible avec le lien ci-dessous :

**https://www.3cx.fr/docs/manuel/installation-debian-linux-ipbx/**

Voici aussi le lien pour le téléchargement de l'iso linux de 3CX :

**https://downloads-global.3cx.com/downloads/debian10iso/debian-amd64-netinst-3cx.iso**

:raw-html-m2r:`<img src="https://lh7-us.googleusercontent.com/dnv4yC4v_g33UFLJcYGuXi3QmSsWkMeu_Iir9wF8EmmyCZTKqkXkgFiIYQfmL_WMYjxXJoSGsAFnsz2kkg3GRqR_GmU9pxCSW8YbKFS63S5mnrrJkDrqopNUzxvNp9oaYDly7gzf0vpt7Ug" style="display: block; margin: 0 auto;" />`

*Premier lancement de l'iso de 3CX*

Choisissez ce que vous préférez en fonction de vos habitudes d'installation de distributions Linux.

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-linux.png" style="display: block; margin: 0 auto;" height="470px"/>`

*Attendre que l'installation s'effectue et choisir les options correspondantes à vos besoins (FQDN...)*

----

:raw-html-m2r:`<br>`

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-CLI.png" style="display: block; margin: 0 auto;" />`

Lorsque votre VM aura redémarré et que vous aurez cette interface de disponible, je vous conseille d'installer 3CX avec votre navigateur web comme support visuel.

:raw-html-m2r:`<br>`

..

   L'installation en CLI étant réservée aux utilisateurs aguerris de 3CX, je ne le vous recommanderais seulement si vous nécessitez de paramètres spéciaux/avancés.


:raw-html-m2r:`<br>`

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/conf-3cx1.png

:raw-html-m2r:`<u>Ici, 3 options sont disponibles : </u>`


* *Upload a new configuration file create on 3CX*
* *Restore a backup*
* *Install without config file (legacy, not recommended)*

Nous utiliserons la 3ème option pour cette installation.

:raw-html-m2r:`<br>`

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/conf-3cx2.png

:raw-html-m2r:`<br>`

Cette étape nous permet de configurer les différents ports utilisés par les services de 3CX.

..

   Si seulement votre instance 3CX tourne sur votre VM, je vous conseille de laiser les ports par défaut proposer par le wizard d'installation.

   Dans le cas contraire, utilisez des ports qui ne sont pas utilisés par d'autres services!


----

.. image:: https://upload.wikimedia.org/wikipedia/commons/2/2a/Windows_Logo_2012-2015.png
    :align: right
    :height: 32px


Windows
~~~~~~~

Il est aussi possible d'héberger votre PBX 3CX sous l'OS Windows.

:warning: **DISCLAIMER** :warning:

Cependant, cela nécessitera des connaissances avancées, car vous vous retrouverez face à des contraintes plus récurrentes que sur Linux.

Par exemple, lors des MàJ Windows, il est possible que l'état du Firewall Windows Defender se réinitialise et donc efface les règles de traffics entrants/sortants permettant au 3CX et aux téléphones liés de fonctionner correctement.

De plus, Windows est par défaut plus vulnérable que Linux, de par son architecture et car il est l'OS le plus répandu !

Lorsque l'installation est terminée, on peut remarquer dans le fichier hosts de notre OS Windows que 3CX a rajouté cette ligne :

  ``127.0.0.1 arthur.3cx.ch``

Cette dernière permet, lorsque nous tapons l'URL en question dans notre navigateur, que notre ordinateur pointe vers notre adresse loopback.

Attention, cela se produit seulement si ... config préalable dns non

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-hosts.png

----

Interface
^^^^^^^^^^^^^^^^^^^^^^

Après avoir terminé la configuration du 3CX, vous pourrez accéder à l'URL correspondante à l'installation de votre 3CX (\ *ici arthur.3cx.ch:5001*\ ), et ainsi vous logger avec les identifiants administrateur précédemment choisis.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-login.png

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/dashboard.png

Après s'être identifiés, nous débarquons sur l'interface admin.

----

Exercice 1
^^^^^^^^^^^^^^^^^

Demande
~~~~~~~~~~~~~~~~~~~

**Exercice 1: Création d’un numéro d’assistance**

L’accessibilité téléphonique du service clientèle de Cardinal Bier Import AG doit être améliorée. À l’heure actuelle, le numéro principal n’est desservi que par une seule personne. Récemment, une application de Customer Releationship Management a été installée. Désormais, les commandes, réclamations ou autres demandes des clients sont enregistrées électroniquement. Une équipe de 4 collaboratrices a été formée. La répartition des appels au sein de cette équipe doit être définie. Créez une solution de téléphonie pour le service clientèle de Cardinal Bier Import AG. Vous disposez d’une instance vPBX de Peoplefone ou d’autres installations. Lisez les exigences de l’entreprise et établissez une configuration.

**Besoins en téléphonie du service clientèle**

:raw-html-m2r:`<u>Exigences auxquelles doit satisfaire le numéro principal:</u>`


* Horaires d’ouverture du lundi au vendredi de 8h00 à 18h00 et le samedi de 8h00 à 17h00
* Saisie de tous les jours fériés catholiques légaux pour le site de Fribourg, pour les 12 prochains mois.
* IVR pour allemand, français et anglais en amont

Formez des groupes pertinents. Les appels doivent être répartis de manière séquentielle au sein du groupe. Il doit y avoir passage d’un groupe à un autre, si personne ne répond ou si la ligne est occupée. L’appel passera sur messagerie et signalera qu’aucun collaborateur n’est libre, seulement aucune personne ne répond. Les équipes parlant les langues officielles du canton reçoivent un numéro d’appel externe et les collaboratrices peuvent passer des appels externes sur lle téléphone IP avec ce numéro ou avec le numéro principal.

Les textes de message suivants peuvent être repris dans le fichier ZIP ou vous pouvez en enregistrer vous-même:


* HPN_AB_FeiertagFerien.wav
* HPN_AB_keinMitarbeiterFrei.wav
* HPN_AB_Oefffnungszeiten.wav
* IVR_Ansage.wav

Fichiers WAV
Le texte parlé des fichiers WAV ne doit pas correspondre à 100% à la problématique de cet exercice.
Les utilisateurs suivants doivent être enregistrés:


* Meier Anna, parle allemand, français
* Müller Janine, parle allemand, anglais
* Angeloz Marie, parle français
* Ducrest Sophie, parle français, anglais

Mission par groupe de 2 ou 4:


* Tracez le Call Flow pour le numéro principal (modèles disponibles dans le chapitre 10 du module 361)
* Configurez l’installation en fonction des exigences

Testez l’installation et consignez les tests dans un protocole

Workflow :
~~~~~~~~~~~~~~~~~~~~~~

La chose la plus importante à faire dans un exercice tel quel, est de dessiner un schéma de principe très simple, à la main de préférence.

Cela permet de visualiser au mieux la demande et de pouvoir poser des questions au client si les indications ne sont pas claires !

.. image:: "https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/sch%C3%A9ma-ex1.png

La demande est désormais plus compréhensible, nous allons donc maintenant procéder à la configuration de notre PBX virtuel !

Commencons par les utilisateurs :

:raw-html-m2r:`<u> Disclaimer : Pour l'exercice, seuls 2 téléphones IP Yealink étaient à disposition ; ils seront configurés pour les utilisateurs 100 et 101. </u>`

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/users1.png

Configuration Janine :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/janine.png

Les champs obligatoires à remplir lors de la création de l'utilisateur sont les suivants :


* Extension
* Prénom
* Nom
* Adresse Mail

----

Exigences réseau
^^^^^^^^^^^^^^^^^

Ce chapitre se base sur le cours 07-Exigences Réseau du cockpitprofessionnel.ch

**Latence**

La durée d’exécution des paquets vocaux est un critère essentiel pour la qualité vocale. On s’intéresse ici au délai total entre la parole de l’émetteur et l’écoute du récepteur (délai de bout en bout).

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/jitter.png

**Perte de paquets**

Un paquet vocal contient seulement 20 à 30 ms de paroles, ce qui correspond environ à une syllabe. Un codec doit pouvoir compenser jusqu’à 5% de perte de données, ce qui n’est pas entendu lors d’une conversation téléphonique.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/pertedepaquets.png


----


Exercice 2
^^^^^^^^^^^^^^^^^

1. NAT / PAT avec installation app natel externe
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Workflow de l'exercice :

Dépannage 3CX

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/depannage-3cx.png


Vous avez la possibilité à travers ce menu de définir si oui ou non le serveur 3CX agit en tant qu'intermédiaire pour les appels.
Ici, cela nous sera utile afin de nous simplifier la tâche, au lieu de configurer un port de mirroring sur le switch.

2. 1 App + 1 Webclient en interne avec Wireshark
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

3. 2 Téléphones SIP avec Wireshark (comparaison G711/G722/G729 )
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

G711
********

Les caractéristiques du codec G.711 sont les suivantes :

- Bande de fréquences : 300-3400Hz
- Fréquence d’achantillonnage de 8 khz
- Débit fixe de 64 kbits/s (échantillons de 8 bits x 8 kHz)
- Délai de compression de 0,125 ms (sans aucun délai d’anticipation)

MOS :

- Mesure de qualité en conditions idéales : MOS 4,45 en G.711 Loi-µ et 4,45 en G.711 Loi-A
- Mesure de qualité en condition dégradées : MOS 4,13 en G.711 Loi-µ et 4,11 en G.711 Loi-A


Capture wireshark d'une conversation en G711 :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/rtp-conf-payload-G711.png

Comme escompté, nous remarquons que la discussion transite du téléphone 192.168.1.122 en passant par le serveur 3CX 192.168.1.120 .

La première chose qui est importante à souligner, est que les paquets utilisent le protocole de transport UDP (couche OSI 4) pour naviguer à travers le réseau, réduisant donc la latence potentielle de la conversation.

Étant donné que le trafic est d'interne à interne, il n'est par défaut pas chiffré, laissant le payload contenu dans le RTP visible en clair.
Il est donc tout à fait possible à partir d'un fichier d'un logiciel tel que Wireshark, d'écouter une conversation à partir de la conversation RTP !

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/i2i-call-RTP-voice-recording.png 





G722
********

Les caractéristiques du codec G.722 sont les suivantes :

- Bande de fréquences : 50-7000Hz
- Fréquence d'échantillonnage : 16 kHz
- Débit fixe : 64 kbps
- Délai de compression : Non spécifié

MOS :

- Mesure de qualité en conditions idéales : MOS (Mean Opinion Score) similaire pour G.722 et G.711
- Mesure de qualité en conditions dégradées : MOS (Mean Opinion Score) similaire pour G.722 et G.711

Voici un graphique comparatif pour les bandes de fréquence du G711 et du G722 :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/g711-g722-frequency-response.jpg
    :alt: graph-g711-g722

G729
********


Parler de la MOS pour la qualité audio
