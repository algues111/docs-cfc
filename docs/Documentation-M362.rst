.. role:: raw-m2r(raw)
   :format:


Module 362 : Mettre en service les systèmes vocaux et vidéo complexes
=====================================================================



.. image:: https://upload.wikimedia.org/wikipedia/commons/a/a2/3CX_Logo_-_Wiki.png
   :align: right
   :height: 32px

3CX
----------

Qu'est-ce que 3CX ?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

3CX est une **solution de communications virtuelle** qui permet aux entreprises de gérer leurs appels téléphoniques, leur messagerie instantanée, leur vidéoconférence ainsi que tous les services que pourrait proposer un PBX classique, grâce à différentes installations et forfaits.

12 millions d'utilisateurs l'utilisent chaque jour, le placant donc sans souci sur le podium des leaders mondiaux de la téléphonie !

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/3cx-paccueil.png
   :align: center

----

Licences
^^^^^^^^^^^^^^^^^^^^

Pour avoir une vue d'ensemble plus concrète de ce que propose 3CX en tant que service ou système, il est important de connaître les différentes licences proposées par l'entreprise du même nom.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/3cx-licences.png
   :align: center

----

Différents types d'installation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

:raw-m2r:`<br>`

.. image:: https://imgs.search.brave.com/t5Gh4h12EKJUKsBYlQEidsH_O2SyxBPQABqSv3rnPxU/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9icmFu/ZHNsb2dvcy5jb20v/d3AtY29udGVudC91/cGxvYWRzL2ltYWdl/cy9kZWJpYW4tbG9n/by5wbmc
   :align: right
   :height: 32px

Linux
~~~~~~~~~~~~~~

:raw-m2r:`<br>`

Chez 3CX, le principal avantage de leur système est leur **OS basé sur Debian** qui est **optimisé pour leur PBX virtuel.**

L'installation s'avère simple si l'on est familiarisé avec le milieu de la virtualisation sous linux.

:raw-m2r:`<u>Voici les prérequis matériels pour l'installation de 3CX sur Debian : </u>`

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

.. image:: https://lh7-us.googleusercontent.com/dnv4yC4v_g33UFLJcYGuXi3QmSsWkMeu_Iir9wF8EmmyCZTKqkXkgFiIYQfmL_WMYjxXJoSGsAFnsz2kkg3GRqR_GmU9pxCSW8YbKFS63S5mnrrJkDrqopNUzxvNp9oaYDly7gzf0vpt7Ug
   :align: center

*Premier lancement de l'iso de 3CX*

Choisissez ce que vous préférez en fonction de vos habitudes d'installation de distributions Linux.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/3cx-linux.png
    :align: center
    :height: 470px

*Attendre que l'installation s'effectue et choisir les options correspondantes à vos besoins (FQDN...)*

----

:raw-m2r:`<br>`

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/3cx-CLI.png
    :align: center

Lorsque votre VM aura redémarré et que vous aurez cette interface de disponible, je vous conseille d'installer 3CX avec votre navigateur web comme support visuel.

:raw-m2r:`<br>`

..

   L'installation en CLI étant réservée aux utilisateurs aguerris de 3CX, je ne le vous recommanderais seulement si vous nécessitez de paramètres spéciaux/avancés.


:raw-m2r:`<br>`

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/conf-3cx1.png

:raw-m2r:`<u>Ici, 3 options sont disponibles : </u>`


* *Upload a new configuration file create on 3CX*
* *Restore a backup*
* *Install without config file (legacy, not recommended)*

Nous utiliserons la 3ème option pour cette installation.

:raw-m2r:`<br>`

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/conf-3cx2.png

:raw-m2r:`<br>`

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


.. warning::

   Cependant, cela nécessitera des connaissances avancées, car vous vous retrouverez face à des contraintes plus récurrentes que sur Linux.

   Par exemple, lors des MàJ Windows, il est possible que l'état du Firewall Windows Defender se réinitialise et donc efface les règles de traffics entrants/sortants permettant au 3CX et aux téléphones liés de fonctionner correctement.

De plus, Windows est par défaut plus vulnérable que Linux, de par son architecture et car il est l'OS le plus répandu !

Lorsque l'installation est terminée, on peut remarquer dans le fichier hosts de notre OS Windows que 3CX a rajouté cette ligne :

  ``127.0.0.1 arthur.3cx.ch``

Cette dernière permet, lorsque nous tapons l'URL en question dans notre navigateur, que notre ordinateur pointe vers notre adresse loopback.

Attention, cela se produit seulement si ... config préalable dns non

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/3cx-hosts.png

----

Interface
^^^^^^^^^^^^^^^^^^^^^^

Web interface (admin)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Après avoir terminé la configuration du 3CX, vous pourrez accéder à l'URL correspondante à l'installation de votre 3CX (\ *ici arthur.3cx.ch:5001*\ ), et ainsi vous logger avec les identifiants administrateur précédemment choisis.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/3cx-login.png

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/dashboard.png

Après s'être identifiés, nous débarquons sur l'interface admin.

Pour avoir une ligne entrante et sortante opérationnelle, il est nécessaire de configurer un trunk SIP.
3CX prend en charge plusieurs opérateurs en Suisse, notamment sipcall...

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/sip-trunk.png


Ci-dessus, nos 2 trunks sont déjà configurés. Nous pouvons cependant plonger dans leur configuration afin de comprendre les paramètres incontournables.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/telco1a.png


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/telco1b.png


Web Interface (client)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Il est possible d'accéder à l'interface webclient et ainsi d'avoir des fonctionnalités UCC proposées par 3CX :

Cela inclut :

- Chats
- Chats de groupe
- Meetings (avec caméra, micro, partage d'écran/app...)
- Historique des appels
- Cahier de contacts
- Boîte de messagerie vocale

Tout est accessible depuis le menu latérale de gauche :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/webclient.png



Chats :


L'interface des chats est assez rudimentaire mais efficace. 
Elle permet de partager des fichiers, faire des listes à puces...

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/webclient-chat.png

Chats de groupe :


:raw-m2r:`<u>Meetings : </u>`

3CX permet notamment de faire des conférences en ligne, grâce à une interface intuitive et pratique.
Pour pouvoir profiter pleinement de toutes ces fonctionnalités, il est nécessaire d'accorder l'accès au micro et webcam à votre navigateur web.

Durant ces conférences, il est possible de partager son écran et de donner la main à un des collaborateurs présents dans la réunion.
Partager des fichiers et écrire dans un chat dédié est aussi possible !

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/webclient-meeting.png


Historique des appels :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/callhistory.png


Cahier de contacts :

Un cahier des contacts existe, donnant la possibilité d'enregistrer des fiches contacts.
Pour aller plus loin, une intégration LDAP est même possible pour télécharger l'annuaire depuis un serveur LDAP. (disponible pour la licence 3CX Pro)

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/phonebook.png


Boîte de messagerie vocale :


Réseau
--------

Généralités Réseau
^^^^^^^^^^^^^^^^^^^^^^^^

DECT : Digital Enhanced Cordless Telecommunications
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


**Bande de fréquence :** de 1880 à 1920MHz

- Divisé en 2 plages distinctes :
   - 1880-1900 : émission
   - 1900-1920 : réception

- Chaque plage contient 12 canaux
- 8 canaux pour la communication
- 4 canaux pour la signalisation

- TDM dans chaque canal permettant 10 personnes par canal, ce qui revient à 80 communications en simultanées maximum.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/bande-dect.png

**Différence DECT VS SIP-DECT**


Gestion des canaux : 

DECT : OMM (Office manager mobile) qui gère la partie sans fil dans le central téléphonique (protocole propriétaire)

SIP DECT : Antennes liées au switch, avec une antenne master (OMM), autres antennes slave, protocole LLDP (broadcast)

.. warning::
   Le broadcast est désactivé par défaut sur les switchs CISCO et sur d' autres marques, bloquant donc le broadcast du LLDP. 
   Ceci crée des problèmes de connexions des terminaux aux antennes SIP DECT.
   Il est alors vivement recommandé d'autoriser les trames broadcast sur le swich.

Connection DECT :

2 fils, DSI (mitel), propriétaire...

Connexion SIP DECT :

Connexion au PBX via SIP puis configuration XML envoyée par le serveur


ATA (Analogique terminal adapter)

   Convertir analogique IP et IP Analogique via PCM30 / MIC
   Méthode de conversion différente pour FAX (protocole T.38)

Attention aux recommandations des fournisseurs

----

Codecs
~~~~~~


G711
~~~~~~~~~~~~~~

Les caractéristiques du codec G.711 sont les suivantes :

- Bande de fréquences : 300-3400Hz
- Fréquence d’achantillonnage de 8 khz
- Débit fixe de 64 kbits/s (échantillons de 8 bits x 8 kHz)
- Délai de compression de 0,125 ms (sans aucun délai d’anticipation)

MOS :

- Mesure de qualité en conditions idéales : 4,45 en G.711 Loi-A
- Mesure de qualité en condition dégradées :  4,11 en G.711 Loi-A

.. note::
   Les MOS ci-dessus sont basés sur le site https://w3tel.com/documentation-voip/codecs/g-711/ 

Pour tout appel passant par IP, une initiation de communications est procédé par le protocole SIP.
Ce dernier pourrait être comparable au fonctionnement du TCP, mais à la couche 7 du modèle OSI.




Capture wireshark d'une conversation en G711 (flux RTP):

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/rtp-conf-payload-G711.png


Comme escompté, nous remarquons que la discussion transite du téléphone 192.168.1.122 en passant par le serveur 3CX 192.168.1.120 .

La première chose qui est importante à souligner, est que les paquets utilisent le protocole de transport UDP (couche OSI 4) pour naviguer à travers le réseau, réduisant donc la latence potentielle de la conversation.

Étant donné que le trafic est d'interne à interne, il n'est par défaut pas chiffré, laissant le payload contenu dans le RTP visible en clair.
Il est donc tout à fait possible à partir d'un fichier d'un logiciel tel que Wireshark, d'écouter une conversation à partir de la conversation RTP !

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/i2i-call-RTP-voice-recording.png 




G722
~~~~~~~~~~~~~~


Les caractéristiques du codec G.722 sont les suivantes :

- Bande de fréquences : 50-7000Hz
- Fréquence d'échantillonnage : 16 kHz
- Débit fixe : 64 kbps

- Délai de compression : Non spécifié

MOS :

- Mesure de qualité en conditions idéales : MOS (Mean Opinion Score) similaire pour G.722 et G.711
- Mesure de qualité en conditions dégradées : MOS (Mean Opinion Score) similaire pour G.722 et G.711

Voici un graphique comparatif pour les bandes de fréquence du G711 et du G722 :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/g711-g722-frequency-response.jpg
    :alt: graph-g711-g722

:raw-m2r:`<br>`

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/rtp-conf-payload-G722.png

:raw-m2r:`<br>`

G729
~~~~~~~~~~~~~~


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/rtp-conf-payload-G729.png

Les caractéristiques du codec G.729 sont les suivantes :

- Bande de fréquences : 300-3400Hz
- Fréquence d'échantillonnage : 8 kHz
- Débit fixe : 8Kbps
- Délai de compression : 15ms

MOS :

- Mesure de qualité en conditions idéales : MOS (Mean Opinion Score) 4,04 en G.729a
- Mesure de qualité en conditions dégradées : MOS (Mean Opinion Score) 3,51 en G.729a

Parler de la MOS pour la qualité audio


----

Exigences réseau
^^^^^^^^^^^^^^^^^

Ce chapitre se base sur le cours 07-Exigences Réseau du cockpitprofessionnel.ch

**Latence**

La durée d’exécution des paquets vocaux est un critère essentiel pour la qualité vocale. On s’intéresse ici au délai total entre la parole de l’émetteur et l’écoute du récepteur (délai de bout en bout).

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/latence.png

:raw-m2r:`<br>`

**Gigue (Jitter)**

Il désigne la différence de délai de transmission de bout en bout entre différents paquets d'un même flux de paquets lors d'une transmission d'un système à l'autre.
Il s'agit en réalité d'une variation de lantence.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/jitter.png

:raw-m2r:`<br>`

**Perte de paquets**

Un paquet vocal contient seulement 20 à 30 ms de paroles, ce qui correspond environ à une syllabe. Un codec doit pouvoir compenser jusqu’à 5% de perte de données, ce qui n’est pas entendu lors d’une conversation téléphonique.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/pertedepaquets.png


Fonctions de réseau
^^^^^^^^^^^^^^^^^^^^^

PoE (Power over Ethernet)
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

La norme IEEE 802.3af, aussi appelée PoE, permet, initialement, de faire passer une alimentation en courant continu d'une puissance de max. 15,4W avec une tension d'environ 48V, en plus des données avec un débit de 100Mbit/s à 1Gbit/s.
Aujourd'hui la norme initiale a évolué (avec le PoE+, et PoE++), permettant de faire passer plus de courant, et donc d'alimenter des appareils de plus en plus gourmands en énergie !

Tableau des normes PoE à voir ci-dessous :   


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/normes-poe.png
    :alt: normes-poe


----









Exercices
-----------


Exercice 1
^^^^^^^^^^^^^^^^^

Demande
~~~~~~~~~~~~~~~~~~~

**Exercice 1: Création d’un numéro d’assistance**

L’accessibilité téléphonique du service clientèle de Cardinal Bier Import AG doit être améliorée. À l’heure actuelle, le numéro principal n’est desservi que par une seule personne. Récemment, une application de Customer Releationship Management a été installée. Désormais, les commandes, réclamations ou autres demandes des clients sont enregistrées électroniquement. Une équipe de 4 collaboratrices a été formée. La répartition des appels au sein de cette équipe doit être définie. Créez une solution de téléphonie pour le service clientèle de Cardinal Bier Import AG. Vous disposez d’une instance vPBX de Peoplefone ou d’autres installations. Lisez les exigences de l’entreprise et établissez une configuration.

**Besoins en téléphonie du service clientèle**

:raw-m2r:`<u>Exigences auxquelles doit satisfaire le numéro principal:</u>`


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

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/schema-ex1.png

La demande est désormais plus compréhensible, nous allons donc maintenant procéder à la configuration de notre PBX virtuel !

Commencons par les utilisateurs :

:raw-m2r:`<u> Disclaimer : Pour l'exercice, seuls 2 téléphones IP Yealink étaient à disposition ; ils seront configurés pour les utilisateurs 100 et 101. </u>`

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/users1.png

Configuration Janine :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/janine.png




Les champs obligatoires à remplir lors de la création de l'utilisateur sont les suivants :


* Extension
* Prénom
* Nom
* Adresse Mail


----


Exercice 2
^^^^^^^^^^^^^^^^^

1 - NAT / PAT avec installation app natel externe
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Workflow de l'exercice :

Dépannage 3CX

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/depannage-3cx.png




Vous avez la possibilité à travers ce menu de définir si oui ou non le serveur 3CX agit en tant qu'intermédiaire pour les appels.
Ici, cela nous sera utile afin de nous simplifier la tâche, au lieu de configurer un port de mirroring sur le switch par exmple.

La prochaine étape sera de créer la règle NAT/PAT dans le routeur / firewall du réseau (ici Centro Business 2.0 Swisscom)
Nous accédons donc à la web interface administrateur de ce dernier (Réseau>Port Forwarding> Create new rule)

- Port TCP 5001 (HTTPS)
- Port TCP/UDP 5090 (Tunnel 3CX)

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/natpat-swisscom-ex2.png




A la suite de cette configuration, nous pouvons télécharger l'application 3CX sur notre téléphone.

.. warning::


   Sur Android, l'application **nécessite** le GSF afin d'afficher les notifications d'appels entrants.
   Dans le cas contraire, vous ne pourrez pas répondre aux appels, mais serez en mesure d'en passer (appels sortants).

Précision faite, il est temps d'installer l'application sur notre appareil !

- Rendez-vous dans votre gestionnaire de paquets / applications préféré > Tapez 3CX dans la barre de recherche > Installez l'application 
- Ensuite, lisez et acceptez les conditions d'utilisation de l'app.
- Pour finir, scannez le QR code que vous trouvez dans la configuration de votre utilisateur 3CX.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/install-android.png
      



Vous êtes désormais connecté à votre compte, vous permettant donc de passer des appels et d'envoyer des messages dans le service de chat 3CX.

Schéma réseau de la connexion :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/schema-app-qr.png


2 - 1 App + 1 Webclient en interne avec Wireshark
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~


Après avoir vu comment fonctionnaientt les communications SIP / RTP, il est nécessaire de comprendre comment se passent les communications passant à travers des applications ou par WebRTC.

Pour illustrer cela, rien de mieux qu'une capture wireshark accompagnée d'un petit schéma réseau.d


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/udp-stream.png



Avant que la communication commence entre les appareils, un handshake TLS1.2 est initié afin d'échanger les clés nécessaires au chiffrement de la communication.
Il est important de noter qu'un chiffrement TLS 1.2 min. est recommandé pour garantir l'intégrité et la confidentialité de la communication.

Voici comment se passe un handshake TLS :


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/tls-ssl-handshake.png


.. admonition:: Lien utile

   TLS / SSL protocols  : https://www.cloudflare.com/fr-fr/learning/ssl/what-happens-in-a-tls-handshake/



3 - 2 Téléphones SIP avec Wireshark (comparaison G711/G722/G729 )
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

