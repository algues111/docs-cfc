======================================================================
Module 233 : Protéger et assurer la maintenance d'un réseau
======================================================================


Formation des collaborateurs
================================

De nos jours, la formation des collaborateurs d'une entreprise à la sécurité informatique est primordiale.
Au premier trimestre 2023, le nombre de cyberattaques a augmenté de 20% par rapport à la même période de l'année précédentes.

Cela va sans dire, la cybersécurité doit faire partie de notre quotidien, qu'il soit professionnel ou personnel.

Outils
-----------

Formation
^^^^^^^^^^^

Pour cela, des outils plus performants les uns que les autres nous permettent d'établir des campagnes de formation ainsi que des campagnes de phishing !
Certaines entreprises sont même spécialisées dans le domaine, allant jusqu'à infiltrer les entreprises physiquement comme s'ils étaient du personnel légitime.

Kaspersky ASAP est une solution d'apprentissage et de formation à la vigilence informatique.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/kasap.png
   :align: center

Cet aspect de la cybersécurité est absolument primordial, car un seul lien malveillant pourrait mettre à mal toute une infrastructure.
Le danger se trouve d'ailleurs souvent **entre la chaise et le clavier !**

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/user-meme.jpg
   :width: 300

End-user
^^^^^^^^^

Pour se protéger d'avantage, des extensions, sites web, logiciels gratuits sont à disposition en ligne.


.. tabs::

   .. tab:: SquareX

      SquareX est une extension s'ajoutant à votre navigateur vous permettant de sandboxer un site que vous visitez, un fichier ou même un mail que vous pouvez recevoir sur une adresse temporaire.
      Rendez-vous sur https://sqrx.com/ pour la télécharger !

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/sqrx.png


   .. tab:: VirusTotal

      `VirusTotal <https://www.virustotal.com/gui/home/upload>`_ est un outil 100% gratuit permettant de scanner des URL, des fichiers, des hashs/checksums, des domaines et adresses IP.
      Ses analyses sont basés sur plus de 70 anti-virus connus du marché de la cybersécurité et vous offre en plus de cela un score de communauté.

      Accueil du site :

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/virustotal.png

      Regroupant toutes ces informations, il est bien plus facile de savoir si tel site ou tel fichier est malveillant.

      L'entreprise offre aussi des applications de bureau pour Mac, Linux et Windows ainsi que des services payant pour du threat hunting et des graphs !

      Ci-dessous une démonstration d'un scan de site malveillant (ici phishing).

       .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/virustotal-malurl.png
     


   .. tab:: iBarry

     `iBarry <https://www.ibarry.ch/fr/controles-de-securite/>`_ centralise des fonctionnalités similaires et complémentaires à VirusTotal, il permet de :

         - Vérifier un site web
         - Vérifier si une adresse mail a été compromis via des fuites de données (vérification faite par Have I Been Powned)
         - Vérifier si son IP publique est potentiellement sujette à des attaques (iBarry effectue des tests de ports)

     Le site propose aussi dvers logiciels de sécurité dont l'antivirus de Sophos ainsi que Qualys pour la veille des logiciels.

     .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/ibarry.png

MFA
^^^^^^^^

La MFA (multi-factor authentication) permet une authentification plus complète et sécurisée des utilisateurs.

Elle se base sur au moins 2 méthodes comprenant :

   - Quelque chose que je suis (ex : biométrie)
   - Quelque chose que j'ai (clé FIDO2, token physique, badge d'authentification...)
   - Quelque chose que je connais (mot de passe, phrase de passe, PIN...)

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/MFA.png

La MFA fait aujourd'hui partie intégrante de l'authentification moderne des utilisateurs.
Elle est un frein aux attaques les plus communes et au social engineering de base.

Il est donc de plus en plus recommandé de mettre en place de la MFA, qu'elle soit au niveau personnel ou professionnel pour protéger nos comptes en ligne de tentatives de connexion non autorisées.

Cependant, la sécurité est souvent bien loin d'être agréable ou confortable pour les collaborateurs qui font face à des contraintes de plus en plus rudes.
Il est alors préférable, voire indispensable de planifier les méthodes MFA que nous voulons appliquer, afin que la productivité et le confort des employés soient le moins touchés possible.



Bases légales et juridiques
===============================

Au delà de la sécurité informatique en elle même, de plus en plus de lois et d'ordonnances sont publiées chaque année afin d'encadrer la protection des systèmes et des données.

En Suisse, voici les documents valables :

   - La constitution fédérale (Cst ; RS 101)
   - Le code civil (CC ; RS 210)
   - Le code des obligations (CO ; RS 220)
   - L’ordonnance concernant la tenue et la conservation des livres de comptes (Olico ; RS 221.431)
   - La loi sur le droit d’auteur et les droits voisins (loi sur le droit d’auteur, LDA, RS 231.1)
   - La loi sur les brevets d’invention (LBI ; RS 232.14)
   - La loi fédérale sur la protection des données (LPD ; RS 235.1), en particulier l’article 7 et l’ordonnance relative à la loi fédérale sur la protection des données (OLPD ; RS 235.11), en particulier les articles 8 à 11 et 20 à 21
   - La loi fédérale contre la concurrence déloyale (LCD ; RS 241)
   - Le code de procédure civile (CPC ; RS 272)
   - Le code pénal (CP ; RS 311.0)
   - La loi sur le travail dans l’industrie, l’artisanat et le commerce (LTr ; RS 822.11)
   - L’ordonnance relative à la loi sur le travail (Hygiène) (OLT 3 ; RS 822.113)
   - La loi fédérale sur les services de certification dans le domaine de la signature électronique (Loi sur la signature électronique ; SCSE : RS 943.03)
   - L’ordonnance sur les services de certification dans le domaine de la signature électronique (Ordonnance sur la signature électronique ; OSCSE)
   - Le manuel de droit européen en matière de protection des données (la Suisse est également concernée du fait de son adhésion au conseil de l’Europe en 1963, ainsi que par d’autres aspects)
   - L’ordonnance du 15 novembre 2017 sur la surveillance de la correspondance par poste et télécommunication (OSPT : RS 780.11), y compris notice explicative du 4 juillet 2018
   - Guide relatif au traitement des données personnelles dans le domaine médical, traitement des données personnelles par des personnes privées et organes fédéraux de juillet 2002
   - Etc.

A moins d'être un expert en conformité des systèmes de sécurité informatique, il n'est pas très pertinent de lire ces ressources dans leur intégralité.
Il est néanmoins important de savoir qu'elles existent et qu'elles ne sont pas à prendre à la légère.



Certifications 
------------------

Plusieurs entreprises et institutions proposent des services d'audits de sécurité informatique.

Ces audits se basent sur des normes et vérifient la conformité de l'infrastructure et des sytèmes informatiques d'autrui.
Si les entreprises réussissent l'audit, elles se voient alors attribuées un label indiquant leur conformité à la certification en question !

Très souvent, ces audits sont à effectuer environ tous les 2 ans afin de garantir la mise à niveau des normes de sécurité.

En Suisse, les labels CyberSafe et CyberSeal sont mis en avant par la confédération et les hautes autorités publiques.
Cependant, d'autres certifications plus globales existent, telles que l'ISO27001.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/certifs.png




Confidentialité
-----------------

La confidentialité est de nos jours aseez complexe.
Entre les Big Tech mettant à jour tous les mois leurs politiques et les gouvernements pondant de nouvelles lois pour règlementer le tout, les utilisateurs sont très souvent perdus.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/privacy-meme.jpg
   :width: 300



Il est donc essentiel de d'alerter les collaborateurs et clients concernant le traitement de leurs données, et qui y a **réellement accès.**


Pare-feu
===========

Tout d'abord, qu'est-ce qu'un pare-feu ?

Un pare-feu est un appareil ou un logiciel permettant de filtrer et bloquer de connections réseaux en fonction de règles définies.
Aujourd'hui, les pare-feux vont beaucoup plus loin car ils intègrent des fonctionnalités avancées d'analyse de traffics.


Pare-feu sans état (Stateless Firewall)
----------------------------------------

Ce sont les firewalls les plus anciens mais surtout les plus basiques qui existent. Ils font un contrôle
de chaque paquet indépendamment des autres en se basant sur les règles prédéfinies par
l'administrateur (généralement appelées ACL, Access Control Lists)

Pare-feu à état (Stateful Firewall)
-------------------------------------

Ils sont une évolution des pares-feu sans état.
Ils intègrent la fonctionnalité de stateful inspection permettant d'inspecter l'état des paquets qui transitent en son sein.

En complément de l'ACL rédigé par l'administrateur (IP, port, protocole...), il sera donc en mesure de détecter les anomalies des connexions TCP 

- NEW : Un client envoie sa première requête.
- ESTABLISHED : Connexion déjà initiée. Elle suit une connexion NEW.
- RELATED : Peut éventuellement être une nouvelle connexion, mais elle présente un rapport direct avec une connexion déjà connue.
- INVALID : Correspond à un paquet qui n'est pas valide.

Pare-feu applicatif
----------------------

Le pare-feu applicatif agit sur la couche 7 du modèle OSI.
Ce dernier nous permet donc d'être beaucoup plus granuleux sur la manière dont nous allons filtrer le traffic.

.. tip::
   Nous pouvons donc créer une règle interdisant le protocole ssh pour le traffic sortant, que ce dernier fonctionne sur le port 22 ou autre !


Pare-feu personnel
----------------------

Les pares-feu personnels sont ceux que nous retrouvons installés directement sur notre ordinateur.
Ces derniers sont surtout utilisés pour bloquer l'ouverture de ports critiquent.

Mais ce terme est presque devenu un abus de langage car nous parlons désormais d'EDR (Endpoint Detection & Response) ou XDR (Extended Detection & Response) selon les protections configurées.
Ces derniers préviennent aussi l'éxecution de malwares, spywares, trojans, worms etc... sur les postes de travail.

Cet **élément** est **essentiel** à toute **infrastructure informatique sécurisée**.


Configuration de pare-feu physique
------------------------------------

L'établissement d'une procédure peut aider grandement à la configuration d'un équipement réseau.
Que ce soit un switch, un pare-feu, une antenne wi-fi, un NAS etc..., vous gagnerez du temps et vous éviterez de vous perdre.




Paramètres Système
^^^^^^^^^^^^^^^^^^^^^

La première chose à faire lors de la configuration d'un nouvel équipement réseau, est de régler ses paramètres système.

Pourquoi cela ? 
Car ces paramètres vont définir comment nous allons nous connecter à cet apareil et avec quels protocoles, la date et le temps, la langue, son nom etc...

Voici les paramètres disponibles dans un ATP200 chez Zyxell


.. tabs::

   .. tab:: Host Name

      Comme son nom l'indique, l'onglet Host Name permet de définir le nom que nous voulons donner à notre appareil.
      Si vous voulez lier ce dernier à votre domaine, vous pouvez aussi indiquer son nom auprès du domaine.

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/system-hostname.png


   .. tab:: USB Storage

      Si un périphérique de stockage USB est connecté au pare-feu, il est possible de le configurer via cette interface.

   .. tab:: Date/Time

      Réglages de la date et de l'heure.

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/date-time.png

      
   .. tab:: Console Speed

      Permet de définir le Baud Rate utilisé par l'interface console de l'ATP.

      Par défaut fixé à 115200 bauds.

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/console-speed.png


   .. tab:: DNS

      Puisque le Zywall peut être utilisé en tant que serveur DNS, il est possible de définir plusieurs enregistrements DNS, tels que PTR, CNAME, zone forward, MX etc...


      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/dns-settings.png

   .. tab:: WWW

      Configuration de l'accès à la web GUI administrative du pare-feu.
      Il est **préférable de désactiver complètement le protocole HTTP**, ce dernier n'étant **pas chiffré**.

      Il est aussi tout à fait possible de changer le port HTTPS et HTTP par défaut, ce qui peut s'avérer utile si d'autres services utilisent ces protocoles. 

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/www.png


   .. tab:: SSH

      Configuration du protocole SSH pour accéder au pare-feu via le réseau.

      Si vous n'avez pas besoin de paramétrer des fichiers spéciaux dans l'arborescence même du pare-feu, il est déconseillé d'utiliser ce protocole car il peut être vulnérable si mal configuré !

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/ssh.png


   .. tab:: Telnet

      **Protocole déconseillé**

      Le telnet est disponible sur l'ATP200.
      Attention, ce protocole est vulnérable et obsolète, utilisez plutôt SSH si besoin.
     
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/telnet.png


   .. tab:: FTP

      Paramétrage du protocole FTP possible, désactivé par défaut.

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/ftp.png


   .. tab:: SNMP

      Cette section permet de configurer la gestion du pare-feu via SNMP.
      Ce dernier est désactivé par défaut.


      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/snmp.png


   .. tab:: Notification

      .. tabs::
         .. tab:: Mail Notification
            
            Si vous êtes désireux de configurer des alertes ou bien d'activer la MFA par envoi de mails, il est possible de le faire via cette section.

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/notifs-mail.png

         .. tab:: SMS Notification          
            
            Il est aussi possible de faire la même chose via SMS.

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/notifs-sms.png

   .. tab:: Language

      Possibilité de changer de langue pour l'interface système de Zyxell.

   .. tab:: IPv6 

      Possibilité dâctiver le protocole IPv6 sur l'ATP200.     

   .. tab:: ZON

     `ZON  <https://www.zyxel.com/fr/fr/products/management-and-reporting/zyxel-devices-installation-tool-zon-utility/>`_ est un protocole propriétaire à Zyxell facilitant la découverte et la configuration dans le réseau des équipements de cette marque.


      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/zon.png



Sauvegardes
^^^^^^^^^^^^^^^^^^

Les sauvegardes sont un élément essetiel de la configuration de n'importe quel équipement réseau.
Il est donc indispensable d'en effectuer périodiquement, avec une nomanclature pertinente !

Voici un exemple :

EVO-FW001_20220525_0832 : Trigramme client – nom du pare-feu – date – heure

Aujourd'hui, beaucoup de méthodes sont possibles pour effectuer des backups de manière sécurisée (rclone, rsync, SFTP, FTPS etc...)



Documentation
^^^^^^^^^^^^^^^^

Cet aspect du métier a déjà été abordé lors du module M145, mais un rappel ne fait jamais de mal !

Une bonne documentation devrait contenir au moins les éléments suivants :

  • Photos de l’installation, des connexions et des équipements
  • Fichier sécurisé avec les mots de passes et comptes utilisateurs
  • Matrice des droits d’accès (infrastructure et/ou données)
  • Journaux des modifications et configurations listant toutes les interventions effectuées
  • Schémas de l’installation, plans d’étages
  • Listing des licences actuelles et dates de renouvellement
  • Backup du système avant et après l’intervention, éventuellement la gestion de backups automatisés
  • Etiquetage des équipements avec une nomenclature propre à chaque client
  • Procédures particulières en lien avec l’infrastructure du client final
  • Plan d’adressage complet avec tous les réseaux (LAN, VLAN, …)


Il est évident que d’autres documents devraient encore faire partie d’une documentation complète
d’un client. Voici un listing non-exhaustif qui peut être complété selon les besoins :


  - Clauses de confidentialité en lien avec le client final
  - Offres, devis, bulletins de livraison, offres complémentaires / plus-value, factures du matériel, demandes d’acomptes, facture finale
  - Listing des intervenants dans le projet (chef de projet, technicien, référant du client, autres personnes impactées, …)
  - PV de mise en service et de rendu de l’installation au client final
  - Décharge de responsabilité
  - Correspondances, mails importants
  - Automatismes (GPO, …)
  - Procédures de traitement des données (suppression, élimination, …)

PPP (Point-to-Point Protocol)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Pour configurer un accès à des services d'ISP, 2 choix s'offrent à nous :

- Se connecter en PPP directement depuis le routeur Zyxell DSL 
- Se connecter en PPP sur notre pare-feu Zywall placé derrière le routeur DSL

Nous allons choisir la 2ème option.

Étant donné que notre pare-feu est placé derrière le routeur DSL, il est nécessaire que ce dernier soit configurer en mode bridge (il convertira les trames Ethernet locales en trames ATM ou PTM pour le réseau public)

En premier lieu, connectons-nous sur l'interface de gestion web du routeur.
Après avoir saisi les informations d'identification valides, nous débarquons sur cette première page :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/status.png

Nous voyons que 2 appareils sont connectés sur le routeur :

- Mon laptop
- Le pare-feu (ici un ATP200 de chez Zyxell)

Ici notre but est précis, nous allons donc seulement les paramètres nécessaires à notre tâche.

Rendons-nous dans Network Setting > Broadband :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/broadband.png


Par défaut, 2 interfaces sont disponibles :

- WAN ADSL type ATM
- WAN VDSL type PTM

Nous supprimons l'interface ADSL puisque notre raccordement est de type 17a (VDSL2)

Cliquons maintenant sur l'icône de modification de l'interface VDSL afin de la définir en mode bridge.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/broadband-wan.png

Activons la si ce n'est pas déjà fait et définissons la en tant que bridge !

.. note::
    Il se peut que votre opérateur définisse des VLANs pour chaque service qu'il propose (data, voip, tv...)
    Si c'est le cas, il faut configurer le bon ID !


La dernière étape sur le modem est de désactiver son firewall intégré :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/parefeu.png



Pour utiliser le compte PPP sur le firewall Zyxell ATP200, il est tout d'abord nécessaire de créer un objet !

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/ppp-conf.png


Rentrez les informations d'identification.

.. warning:: 
   Ne pas remplir le champ "service" si vitre opérateur ne le spécifie pas explicitement !
   Cela empêchera l'authentification aurpès du RADIUS du DSLAM.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/pppconf1.png


Objets
--------------

Les objets permettent de classer la majorité des éléments utilisés par le pare-feu.
Les objets possèdent des attributs, des valeurs, et sont rangés dans différentes catégories, sous catégories ou des groupes.

La **rigueur dans le maintien de l'arborscence** des objets est **absolument nécessaire.**
Il est imporant d'être précis dans le nom qu'on leur donne.

.. admonition:: Exemple
   Nous avons un subnet avec cette adresse réseau : 172.18.12.0/24
   Son nom est VLAN_300

   Son objet pourrait être : 
      - Nom : SUBNET_VLAN_300
      - Adresse : 172.18.12.0
      - Masque : 255.255.255.0


Adresses
^^^^^^^^^^^^^^^^^^

Les adresses sont des objets à part entière.
Celles-ci peuvent être des subnets, une adresse hôte ou un subnet d'interface...

Typiquement, dans l'image ci-dessous, nous constatons que les subnets de la RFC 1918 sont créés par défaut.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/adresses.png


Il sera donc tout à fait possible de créer des règles par la suite spécifiant que seule le subnet RFC1918_1 n'est autorisé à sortir sur le WAN...


Mais cela ne s'arrête pas là, car Zyxell donne la possibilité de créer des filtres via GeoIP.

Nous pourrons donc très bien exclure toutes les connexions entrantes ne provenant pas de la Suisse par exemple.


.. note::
   Il est cependant important de prendre en considération les potentiels collaborateurs travaillant à l'étranger afin de ne pas les bloquer.


Zones de sécurité
^^^^^^^^^^^^^^^^^^^^

Les zones de sécurité sont importantes car elles permettent de regrouper logiquement plusieurs interfaces dans un seul et même groupe.
Il est donc plus facile de créer une règle spécifiant que le VLAN avec l'ID 200 peut communiquer avec le VLAN 300 par exemple, ou bien qu'elles sont asujetties à une même policy control.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/zones.png


Services
^^^^^^^^^^

Les communications réseaux reposent sur des protocoles qui eux-mêmes reposent sur des ports.

La notion de services est donc très importante car elle permet d'identifier les protocoles.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/services.png

Créer des groupes de services peut s'avérer très utile lorsque que nous voulons par exemple créer des règles interdisant ou autorisant un groupe de protocoles / ports spécifique.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/services-group.png


AP Profiles
^^^^^^^^^^^^

Cette section concerne la configuration des WLAN et des APs correspondant.
Il est donc possible de créer des SSID, des groupes d'APs, des modes de sécurité et plus encore...


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/aps.png


Lors des exercices de ce module, nous reviendrons en profondeur sur les objets WLAN...

AAA
^^^^

**(Authentication, Authorization, Accounting)**

C'est ici que nous retrouvons les différents serveurs permettant l'authentification, l'autorisation et la compatbilité.

Nous pouvons donc y définir des serveurs LDAP, Microsoft AD et RADIUS.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/aaa.png


Fonctionnalités UTM
----------------------

Les services UTM (Unified Threat Management) est une solution de sécurité tout-en-un, généralement une appliance de sécurité unique, qui fournit plusieurs fonctions de sécurité en un seul point du réseau.

Voici quelques-uns des services couramment proposés par les solutions UTM :

- Logiciel antivirus : pour détecter et éliminer les logiciels malveillants et les virus.
- Logiciel anti-espion : pour détecter et empêcher l’installation de logiciels espions sur les ordinateurs.
- Protection antispam : pour filtrer les e-mails et les messages instantanés pour éviter les spam et les e-mails malveillants.
- Pare-feu réseau : pour contrôler et filtrer le trafic réseau pour éviter les attaques et les intrusions.
- Prévention et détection des intrusions : pour détecter et empêcher les tentatives d’intrusion dans le réseau.
- Filtrage des contenus : pour filtrer les contenus en ligne pour éviter les sites web malveillants et les contenus dangereux (via DNS ou URL).


Voici un petit schéma de principe d'un filtrage via UTM :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/schema-utm.png




.. tabs::

   .. tab:: APP PATROL

      L'App Patrol est un **pare-feu applicatif.**
      Il permet de **filtrer et bloquer des applications définies** par l'administrateur.
      Ces dernières vont des réseaux sociaux jusqu'à l'accès au réseau Tor (onion routing) par exemple...

      Bloquer les services Facebook (aujourd'hui Meta), pourrait se schématiser ainsi :

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/schema-apppatrol.png


      Ici, nous établissons une règle nommée "NO_TO_WHATSAPP".

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/no-to-whatsapp.png

      Dans celle-ci, nous retrouvons les éléments suivants :

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/no-to-whatsapp-conf.png

      Ces "Application Rules" sont des services spécifiques de Whatsapp (Chat, Audio, Video...)
      Elles nous permettent d'avoir de la granularité dans la configuration de nos règles.

      Nous pouvons par exemple bloquer seulement les appels (vocaux et vidéos), mais laisser la possibilité d'envoyer des messages.

      Afin que cette règle soit fonctionnelle, il faut l'appliquer à une "Policy Control".

      Ici, nous avons donc créé la policy "VLAN100_Outgoing_WAN", afin que seuls les appareils du réseau VLAN100 soient affectés par cette règle. 

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/no-to-whatsapp-vlan100.png

      
      Il est important de désormais la tester ! 
      Si nous essayons d'accèder au site web de whatsapp, le navigateur n'y arrivera pas, et un log apparaîtra sur le firewall !

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/log-access-block-AP.png




   .. tab:: Content Filter

      DNS :

      .. warning:: 
         Si votre pare-feu est configuré en tant que DNS, il est nécessaire d'ajouter le content filter sur la règle "LANx_TO_DEVICE" car les requêtes DNS passent par le pare-feu.
         
      

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/


      .. tabs::
         .. tab:: BPP
            
            

            La Business Productivity Protection est un profil créé par défaut dans le Content Filtering de Zyxell.
            Lorsque nous cliquons dessus, nous voyons apparaître plusieurs paramètres intéressants, tels que :

            - Enable SafeSearch : permet l'activation forcée du SafeSearch dans les navigateurs.
            - Managed Categories : permet de choisir les catégories bloquées par le profil en question
         

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/bpp-web-content-filter.png

            Lorsque nous essayons d'accéder à un site-web catégorisé dans le profil, nous avons une jolie page d'accès bloqué qui apparaît !

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/access-blocked.png
            

      
   .. tab:: Anti-Malware

      L'anti-malware vérifie les hashs / checksums des fichiers transitant en son sein, et les met en quarataine / les supprimes si ces derniers correspondent à un hash / checksum malveillant connu.
      Vous pouvez choisir les types de fichiers à analyser.

      .. note::
         Ici, les .exe, .swf, .doc, .pdf, .rtf, .zip sont analysés (car majoritairement enclin à contenir des malwares).

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/malware.png

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/


   .. tab:: Reputation Filter

      A partir d'une base de données, le Reputation Filter peut bloquer des requêtes DNS, des connexions à des IP et URL spécifiques.
      Les possibilités sont très larges. 
      Des white lists et block lists peuvent être ajoutées en fonction des besoins.

      .. tabs::
         .. tab:: IP Reputation
            
            

            Cette catégorie est spécifique aux adresses IP, et regroupe une grande base de données d'adresses IP reconnus comme malveillantes.
            Vous pouvez cependant créer des whitelists et blocklists pour personnaliser cette fonctionnalité.
         
            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/ip-reputation-schema.png


            Sur l'ATP200, le menu se présente comme suit :

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/ip-reputation.png
            
            
            Il est même possible d'intégrer des blocklists externes, que le pare-feu ira chercher via un lien.

            .. admonition:: Lien utile
               Plusieurs IP blacklists sont disponibles sur GitHub notamment, en voici une relativement bien maintenue :

               https://github.com/trskrbz/BlackIPforFirewall


         .. tab:: DNS Threat Filter
            
            Filtre de menaces basés sur des noms de domaines.
            L'ATP inclut des catégories prédéfinies telles que : phishing, spam, spyware...

            Il est possible d'établir des blacklists et whitelists de domaines précis.

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/dns-filter.png

         .. tab:: URL Threat Filter           
            
            Filtre de menaces basés sur des URLs.
            Aussi bien que pour le DNS Threat Filter, l'ATP inclut des catégories prédéfinies telles que : phishing, spam, spyware...

            Il est possible d'établir des blacklists et whitelists de domaines précis.

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/url-filter.png

         
      



   .. tab:: IPS / IDS
      
      
      L’IPS (Intrusion Prevention System) est un outil de cybersécurité qui examine le trafic réseau pour détecter les menaces potentielles et prendre des mesures pour les contrer. 
      Il peut reconnaître et bloquer les logiciels malveillants (malware) ou les exploits avant qu’ils ne puissent pénétrer dans le réseau et causer des dommages.

      L'IDS quant à lui se contente seulement de détecter les intrusions et les menaces sur le réseau

      Sur l'ATP200, la fonctionnalité IPS est disponible et se présente sous la forme suivante :

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/


   .. tab:: Sandboxing

      Le sandboxing permet de tester de potentiels logiciels ou pièces jointes malveillants dans un environnement clos situé dans le cloud de Zyxell.

      Après les tests, le cloud fait un retour à l'ATP, qui autorisera la pièce jointe / le logiciel ou le mettra en quarantaine.


      Évidemment, comme la plupart des fonctionnalités UTM, ce service est payant. 

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/sandboxing.png


   .. tab:: Email Security

     Grâce à l'option email security disponible dans l'ATP200, il est possible de mettre en place un scan des emails entrants.
     Si cette fonctionnalité est activée, les emails répondant aux critères de suspition du système se verront soit mis en quarantaine, soit ajouté un tag au début de leur objet.

     Cela permettant la plus grande attention des collaborateurs sur la possible origine malveillante de l'email en question.


      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/


   .. tab:: SSL Inspection

      Aujourd'hui, la plupart des trafics sur Internet (notamment sur le web) sont chiffrés par SSL pour les plus anciens et TLS pour les plus récents.
      Cela permet de garder une confidentialité et une intégrité des données qui transitent, néanmoins, ce chiffrement peut être un obstacle pour la protection des collaborateurs.

      En effet, des fichiers malveillants pourraient atteindre le LAN sans qu'on puisse les détecter grâce (ou à cause) du chiffrement SSL/TLS.


      Pour l'SSL Inspection, le pare-feu agira donc comme un MITM (Man In The Middle), c'est à dire qu'il déchiffrera le certificat SSL/TLS pour inspecter le contenu du paquet, avant de le chiffrer de nouveau et l'envoyer au destinataire.

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/ssl-inspection.png

      .. warning:: 
         Il est important de vérifier les protocoles de chiffrement ainsi que les versions SSL/TLS supportés par le pare-feu.
         Les plus anciens pourraient ne pas supporter certains, amenant donc à des erreurs et disfonctionnements potentiels. 




Configuration réseau
------------------------------

Avant de s'attaquer à la configuration complète de réseaux, il est plus judicieux de commencer par les notions de ports, d'interfaces, de zones de sécurité etc...

Nous avons dans la section "Objets", que ces derniers sont très utilisés pour configurer n'importe quel aspect du pare-feu.
Cela comprend donc les zones de sécurité.

Interfaces
^^^^^^^^^^^^^^^^^^

Une interface est le point d’interaction logique entre le périphérique (port) et le logiciel du firewall.
Dans la plupart des firewalls, il est possible d’attribuer une interface à un port disponible. Il peut y
avoir plusieurs types d’interfaces :


- Interface interne (lan, dmz, opt, …), connectée à un réseau local. Le firewall ajoute les paramètres de routage et de NAT source correspondant par défaut.

- Interface externe (wan, ppp, …), connectée à un réseau externe (ISP). Le firewall ajoute les paramètres de routage et de NAT source correspondant par défaut

- Interface générale, connectée à un réseau local ou externe. Les règles de routages ne sont pas créées automatiquement et doivent être configurées manuellement. 


Les caractéristiques des interfaces sont les suivantes :


- Entité logique qui effectue le routage L3 et se rapporte à toutes les interfaces
  
- Chaque interface a une et une seule adresse IP associée
  
- Les informations de routage sont automatiquement dérivées des paramètres IP de l’interface du firewall
  
Les fonctionnalités suivantes sont en général supportées :


- Les paramètres généraux comprennent une adresse IP statique, un client/serveur DHCP, etc.
- Un ou deux serveurs relais DHCP peuvent être pris en charge
- La bande passante ascendante et descendante est généralement configurable ainsi que la valeur MTU (Unité de Transmission Maximale)
- Une option de passerelle peut être disponible
- Un proxy IGMP peut être disponible
- Les options DHCP peuvent en général être configurées, incluant donc le DNS, bail, la passerelle, le serveur WINS et d'autres options spéicifiques (ex. code 150 TFTP)



Règles NAT-PAT
------------------

Qu'est-ce que le NAT ? Qu'est-ce que le PAT ?

Le NAT permet la traduction d'une adresse IP de classe publique, à une adresse de classe privée.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/nat.png


Le PAT, quant à lui, permet la transition d'un port externe *x* vers un port interne *y*.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/dnat-pat.png

La combinaison des deux devient...... du NAT-PAT !




Wi-Fi Management (a mettre dans section parefeu)
--------------------------------------------------

Avec l'ATP200, il est tout à fait possible de gérer des réseaux wi-fi ainsi que les points d'accès.
La première chose à faire est de définir les différents objets et profils qu'on utilisera pour notre AP / groupe d'APs.

Rendons nous donc dans les profils radio !

Radio
^^^^^^^^

Nous avons ici configuré le "default" et le "default2".
Ces derniers utilisent respectivement la bande des 2,4GHz et des 5GHz.

.. tabs::
   .. tab:: default (2,4GHz) 
      
      En naviguant dans ce profil, nous voyons que nous l'avons configuré pour que :


      - il utilise la norme 802.11ax (Wifi6)
      - il utilise les canaux en 80MHz (4 canaux aggrégés)
      - il utilise les canaux 36, 52, 100 et 116
      - le DCS vérifie tous les jours à 3h du matin si le canal en question est libre
      - la dissociation du client s'effectue à partir de -88dBm
      - la norme 802.11b soit inutilisable (car débit min. de 12Mbps)

   .. tab:: default2 (5GHz)

      En naviguant dans ce profil, nous voyons que nous l'avons configuré pour que :


      - il utilise la norme 802.11ax (Wifi6)
      - il utilise les canaux en 20MHz
      - il utilise les canaux 1,6 et 11
      - le DCS vérifie tous les jours à 3h du matin si le canal en question est libre
      - la dissociation du client s'effectue à partir de -88dBm
      - la norme 802.11b soit inutilisable (car débit min. de 12Mbps)
    

.. note::
   De nouveau, nous ferons ces tests sur notre environnement de lab.



SSID
^^^^^^^^

Par la suite, nous devons définir les SSID que nous voulons diffuser !
Pour ce faire, il suffit de les créer dans le menu "SSID LIST".

Cela se présente comme suit :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/wifi/ap-profile-ssid-list-wlancorp.png

Dans cet exemple nous possédons 3 SSID diffusant 3 réseaux distincts :

- WLAN_P12_CORP   : VLAN100 -> 172.18.12.0/24
- WLAN_P12_PUBLIC : VLAN300 -> 172.18.212.0/24
- WLAN_P12_VoIP   : VLAN200 -> 172.18.112.0/24

Pour appliquer des profils de sécurité spécifiques, il est possible d'en créer dans l'onglet Security List.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/wifi/ap-profile-ssid-sec-list.png

Dans celui-ci, nous choisissons :

- Le nom du profil
- Le mode de sécurité (WEP, WPA2, WPA2-ENT, WPA3... ) Voir tableau ci-dessous pour le détail des protocoles
   .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/wifi/wpa.png

- La méthode d'authentiication (Enterprise/RADIUS ou Personnel/PSK)
- L'activation ou pas du fast-roaming (802.11r)

Un objet supplémentaire sera nécessaire si nous utilisons un serveur RADIUS pour l'authentification et l'autorisation :

.. note::
   Voir https://datatracker.ietf.org/doc/html/rfc2865


.. note::
   
   Dans ma documentation d'administration système, une section sera dédié au serveur RADIUS. De sa théorie jusqu'à son application.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/wifi/radius-conf-atp.png

Voici les paramètres essentiels à rentrer pour que la configuration fonctionne :

- L'adresse du/des serveur/s
- Les ports utilisés par ce dernier
- La clé partagée


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/wifi/ap-profile-ssid-sec-list-vlan100.png


Ici, nous créons un profil RADIUS, que nous configurons dans le RADIUS Server intégré au NAS Synology.

N'étant pas installé nativement, il est nécessaire de le faire via le gestionnaire de paquets Synology.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/wifi/radius-syno.png

Après cela, nous pouvons le démarrer et le configurer.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/wifi/radius-home.png

La configuration ne sera pas très complexe étant donné que nous n'avons pas de serveur LDAP à proprement parler sur notre réseau, donc nous utiliserons les utilisateurs locaux du NAS.

Il est désormais temps d'ajouter le client RADIUS sur le serveur :

.. warning:: 
   Puisque c'est notre pare-feu qui fait office de contrôleur d'APs, il est nécessaire de mettre son IP à lui, et non celle des APs ! 

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/wifi/ap-profile-ssid-list-wlancorp.png

.. note::
   Les ports par défaut utilisés par le RADIUS sont :
   - 1812 : authentication et authorization
   - 1813 : accounting

Lorsque cela est fait, il faut retourner dans la configuration du SSID afin d'ajouter l'IP du serveur RADIUS ainsi que les ports utilisés pour l'authentification et l'autorisation.


----------


VPN
======

Qu'est-ce qu'un VPN  ?
---------------------------

La notion de VPN avait déjà été abordée lors du module M145 de 1ère année.
Sa définition est simple :"Relier entre eux des systèmes informatiques de manière **sûre** en s’appuyant sur un réseau existant."

Qu'est-ce que le mot *sûre* veut dire concrètement ?

The CIA triad est en général ce que nous utilisons pour déterminer si un système est considéré comme *sûr* ou non.

   - "C" : Confidentiality -> Seules les personnes autorisées ont accès à la ressource en question. (chiffrement des données)
   - "I" : Integrity       -> La ressource n'a pas été modifié ou altéré sans autorisation. (CRC)
   - "A" : Availibitlity   -> La ressource est stockée et accessible en tout temps de manière sécurisé. 

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/CIA-triad.png
   :width: 250




Client-to-Site VPN
----------------------

Avec l'essort du télé-travail ces 5 dernières années, de plus en plus de personnes travaillent depuis leur domicile voire depuis l'étranger.
Les entreprises autorisant cela ont donc besoin d'un système permettant la connexion d'utilisateurs depuis Internet.

Le VPN client-to-site répond à cela. 


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/client-to-site-schema.png


Exercice pratique
^^^^^^^^^^^^^^^^^^^^^^

VPN client-to-site SSL
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Sur l'ATP200, nous pouvons configurer un serveur VPN SSL.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ssl-vpn-serv-menu.png

Voici les paramètres d'une connexion basique :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ssl-vpn-serv-policy.png

- Nom de la connexion
- Zone de sécurité (ici SSL_VPN)
- Description (optionnel)
- Utilisateurs ou groupes autorisés (ici localadmin)
- Le pool d'adresses IP octroyé aux clients (10.1.1.0/24)
- Le serveur DNS utilisé par les clients (ici 10.1.1.1)
- Les réseaux auxquels ils ont accès (ici VLAN_DATAS)

L'onglet "Global settings" permet de définir le port utilisé par le service ainsi que l'interface VPN SSL.

.. warning::
   Ne pas choisir une IP présente dans le pool d'adresses octroyé aux clients.
   Cela pourrait créer des problèmes de routage.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ssl-vpn-serv-policy.png


Côté client, il est possible de télécharger le client SecuExtender pour se connecter au serveur VPN.

Ici, nous voyons très clairement que ce sont l'IP publique du pare-feu ainsi que le port 10443 qui sont utilisés.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ssl-vpn-client.png


Après avoir cliqué sur le bouton "Connect", la connexion s'établit rapidement et nous demande si nous voulons faire confiance au certiifcat auto-signé de l'ATP200 : 

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ssl-vpn-client-connection.png

A la suite de cela, on nous amène sur un nouvel onglet "Status" nous donnant les détails de la connexion, dont l'IP du client et du serveur, l'IP du DNS et les routes autorisées vers d'autres réseaux.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ssl-vpn-client-connected.png


Site-to-Site VPN (Intranet)
--------------------------------

Un VPN site à site basé sur l'Intranet permet une interconnection sécurisé de 2 réseaux d'une même entreprise. 

.. warning:: 
   Pour cet exemple, nous utiliserons un **VPN de type IPSec**.

Exercice pratique
^^^^^^^^^^^^^^^^^^

Phase 1
~~~~~~~~~~

Pour configurer un VPN site-à-site sur l'ATP200 de Zyxell, il faut configurer dans l'ordre la phase 1 et la phase 2 d'une connexion VPN.

Dirigeons nous donc vers l'onglet **VPN Gateway.**

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/vpn-conf.png

En premier temps, cliquer sur **"ADD"**

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/vpn-conf-phase1-s2s.png

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/vpn-conf-phase1-s2s-2.png


Donner un nom reconnaissable et pertinent à notre connection site à site.


Choisir la version 2 d'IKE (IKEv2) car IKEv1 est désormais obsolète.
Définir l'interface sur laquelle le site distant doit se connecter (ici, ce sera wan1_ppp).

Définir l'adresse IP de l'autre pare-feu / serveur VPN, avec lequel nous allons nous interconnecter.

Entrer une clé pré-partagée forte (recommandation de 32 caractères aléatoires A-a-0-$).

Choisir les types d'ID que vous vous partagerez communément des 2 côtés du tunnel. 

Définir la durée de la Security Association en secondes.

Configurer les types de chiffrement pour l'authentification ainsi que le groupe de clés Diffie-Hellman.


.. admonition:: Conseil
   Avant de passer au paramétrage de la phase 2, je vous conseille de vérifier avec votre collaborateur la bonne configuration des 2 gateways (chaque côté du tunnel).


Phase 2
^^^^^^^^^^

Nous pouvons désormais passer à l'onglet VPN Connection, correspondant à la phase 2.

Le menu principal se présente comme suit : 

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/vpn-conf-phase2-menu.png



Lorsque nous cliquons sur "ADD", voici le menu de configuration : 

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/vpn-conf-phase2-s2s.png

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/vpn-conf-phase2-s2s-2.png



Dans celui-ci, nous devons rentrer : 

- Nom de la connexion
- Si notre connexion est celle "nailed-up" (si un problème de connectivité survient entre les 2 réseaux, ce sera cette connexion qui initiera de nouveau la connectivité)
- Le type de passerelle (Site-to-Site, Site-to-Site with dynamic peer, remote access, tunnel interface...)
- La police locale (ce que nous octroyons à l'autre site)
- La police distante (ce que l'autre site nous octroie)
- Le temps de vie de la SA (par défaut 28800sec)
- Le procotole actif (ici ESP)
- La méthode d'encapsulation (ici mode tunnel)
- La paire de clés DH (ici DH14)
- La zone de sécurité
- D'autres options avancées si nécessaires.


.. danger::
   Il est absolument primordial que les paramètres concordent avec le site distant.
   Sans cela, vous risquez de rencontrer des erreurs lors de l'initiation de la connexion !


Après avoir configuré et vérifié les paramètres, nous pouvons initier la connexion.

Il est intéressant d'aller jeter un oeil aux logs afin de déterminer de vérifier les phases IKE et si des warn apparaissent.


Ici RAS, tout fonctionne comme prévu !!

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/vpn-log-success-s2s.png



Site-to-Site VPN (Extranet)
-------------------------------

Le VPN site-à-site extranet fonctionne globalement de la même facon que le site-à-site intranet.
La différence réside dans le fait qu'il sera établi pour permettre l'accès au réseau d'entreprise à une société externe.

La configuration des utilisateurs sera donc plus restrictive selon les exigences et les besoins de collaboration !

Protocoles VPN
----------------

Différentes technologies et protocoles proposent des VPNs :

- IPSec
- L2TP (basé sur IPSec)
- SSL
- OpenVPN
- Wireguard



IPSec
^^^^^^^^

C'est l'un des protocoles les plus utilisés pour les VPN actuels, il permet l'intégrité et la confidentialité des données.
Comme son nom l'indique, il fonctionne sur la couche réseau du modèle OSI (couche 3)

Schéma de principe :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ipsec-tunnel.png

.. _IPSEC: https://www.frameip.com/ipsec/

.. seealso::
   IPSEC_

Modes de fonctionnement
~~~~~~~~~~~~~~~~~~~~~~~~~

Le protocole IPSec peut fonctionner de 2 manières différentes ; en mode tunnel ou en mode transport.
Quelle est la différence entre les deux ?

Mode Tunnel :

Ce mode est le plus sécurisé car il encapsule l'entièreté du paquet IP, c'est à dire son header, payload etc...
Il est largement utilisé pour les VPN "anonymes" car les IP source / destination des en-têtes sont chiffrées !

Mode Transport :

Le mode transport quant à lui va seulement encapsuler le payload du paquet IP ce qui rend ce mode plus léger que le mode tunnel.

Le fonctionnement du protocole IPSec peut être décomposé en 5 étapes principales :


• Etape 1 : Initiation du processus IPSec
• Etape 2 : Phase 1 avec le protocole IKE (Internet Key Exchange)
• Etape 3 : Phase 2 avec le protocole IKE
• Etape 4 : Transfert de données
• Etape 5 : Terminaison du tunnel IPSec


 
IKE
^^^^

Après avori compris le fonctionnement d'IPSec, il est légitime de se demander comment est initié le VPN !
IKE (Internet Key Exchange) est la réponse.

Ce protocole permet l'initiation de la connexion et l'association des systèmes ; les fameuses SA (security association).

IKE utilise l'échange de clés Diffie-Hellman pour mettre en place un secret partagé d'où les clefs de chiffrement sont dérivées.


IKEv1
~~~~~~~~~~~~~~

IKEv1 est la première version du protocole IKE.


IKEv2
~~~~~~~~~~~~~~

IKEv2 est la version succédant à IKEv2 avec plus d'interopérabilité ainsi qu'une résistance plus forte aux attaques de type DOS.

.. _RFC-5996: https://datatracker.ietf.org/doc/html/rfc5996

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ikev1-protocol-12.png

.. seealso::
   RFC-5996_


Phases
^^^^^^^^^^^^

Phase 1
~~~~~~~~~~~~

L'objectif principal de la phase 1 est la mise en place d'un canal chiffré sécurisé par l'intermédiaire duquel deux pairs peuvent négocier la phase 2. Lorsque la phase 1 se termine avec succès, les pairs passent rapidement aux négociations de phase 2. Si la phase 1 échoue, les périphériques ne peuvent entamer la phase 2.

Deux modes existent pour cette première phase :

• Mode principal
• Mode Agressif

Le mode principal comporte 6 étapes d’échange entre l’initiateur et le récepteur :

• Echange de propositions (algorithme d’authentification, algorithme de chiffrement, groupe de clés Diffie-Hellmann)
• Echange de clés Diffie-Hellmann
• Echange d’identité (crypté avec la clé Diffie-Hellmann)

Voici son schéma :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ike-pr.png
   
Le mode agressif comporte 3 étapes d’échange entre l’initiateur et le récepteur. 
Il y aura donc **moins d’échanges** et **moins de paquets.**


• Envoi d’une proposition IKE locale, d’informations relatives à la clé et d’informations d’identité
• Recherche d’une proposition IKE correspondante. Envoi de la proposition IKE correspondante avec les informations relatives à la clé, les informations d’identification et les informations d’authentification locale
• Réponse avec les informations d’authentification locale pour implémenter l’authentification.


Voici son schéma :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/ike-ag.png



Phase 2
~~~~~~~~~~

La construction de la phase 2 s’établi selon le processus suivant :

• Négociation des paramètres SA IPSec par un SA IKE existant, comme, par exemple :
   o AH ou ESP
   o Mode d’encapsulation (Tunnel ou Transport)
• Renégociation des SA IPSec pour assurer la sécurité
• Etablissement des SA IPSec définitif
• Périodicité du renouvellement des SA


Authentification et chiffrement (cryptage)

Ce processus utilise soit le protocole ESP soit le protocole AH.

• ESP ou Encapsulation de la Charge Utile assure l’authentification et le chiffrement
• AH ou Entête d’Authentification assure uniquement l’authentification

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/esp-ah.png

Mode d’encapsulation :

Il existe le mode tunnel ou le mode transport.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/tunnel-transport.png


Finalisation
~~~~~~~~~~~~~~~~

La finalisation du tunnel IPSec intervient :


• Lorsque les SA IPSec prennent fin par suppression ou par temporisation
• Lors les SA IPSec sont terminées, les clés sont également supprimées
• Lorsque des SA IPSec ultérieurs sont requis pour un flux, IKE effectue un nouveau processus de négociation
• Une nouvelle négociation réussie aboutit à de nouvelles SA IPSec et à de nouvelles clés.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/finalisation.png


Et voilà, la connexion est désormais établie et nous connaissons les grandes lignes, voire un peu plus, du fonctionnement d'un VPN IPSec !

Sources et liens
==================

https://www.cisco.com/c/fr_ca/support/docs/security-vpn/ipsec-negotiation-ike-protocols/217432-understand-ipsec-ikev1-protocol.html

https://www.juniper.net/documentation/fr/fr/software/junos/vpn-ipsec/topics/topic-map/security-ike-basics.html

https://www.frameip.com/ipsec/

https://datatracker.ietf.org/doc/html/rfc5996

https://www.iso.org/fr/standard/27001

https://www.cloudflare.com/fr-fr/learning/network-layer/what-is-ipsec/

https://itbusinessconnect.fr/domaines/securite/ficheExpert/l-UTM-Unified-Threat-management

https://support.zyxel.eu/hc/fr/articles/4410547427218-Configuration-de-base-de-Zyxel-Firewall-Objets-zones-NAT-VPN-et-plus-encore-USG-FLEX-ATP

https://eitswiss-supports-didactiques.cockpitprofessionnel.ch/gebaeudeinformatik/gun4

https://github.com/algues111/docs-cfc/blob/main/docs/source/other/Module_233_FR.pdf

https://www.lemagit.fr/conseil/MFA-quels-sont-les-principaux-produits-du-marche

https://kb.synology.com/fr-fr/DSM/help/RadiusServer/rad_desc?version=7

Et plus encore....

Remerciements
====================================

Merci à N. Borowy d'avoir dispensé ce cours passionant à la classe des 2IBM !
