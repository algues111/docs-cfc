======================================================================
Module 233 : Protéger et assurer la maintenance d'un réseau
======================================================================


Formation des collaborateurs
=============================

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



End-user
^^^^^^^^^

Pour se protéger d'avantage, des extensions, sites web, logiciels gratuits sont à disposition en ligne.


.. tabs::

   .. tab:: SquareX

      SquareX est une extension s'ajoutant à votre navigateur vous permettant de sandboxer un site que vous visitez, un fichier ou même un mail que vous pouvez recevoir sur une adresse temporaire.
      Rendez-vous sur https://sqrx.com/ pour la télécharger !

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/sqrx.png


   .. tab:: VirusTotal



   .. tab:: iBarry

     


Certifications 
------------------

Cybersafe, ISO27001...


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
- RELATED : Peut éventuellement être une nouvelle connexion, mais elle présente un rapport
direct avec une connexion déjà connue.
- INVALID : Correspond à un paquet qui n'est pas valide.

Pare-feu applicatif
----------------------



Configuration
----------------

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



   .. tab:: Date/Time

     
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/date-time.png

      
   .. tab:: Console Speed

      

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/console-speed.png


   .. tab:: DNS



      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/dns-settings.png

   .. tab:: WWW

      

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/www.png


   .. tab:: SSH



      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/ssh.png


   .. tab:: Telnet

     
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/telnet.png


   .. tab:: FTP

      

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/ftp.png


   .. tab:: SNMP



      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/snmp.png


   .. tab:: Auth. Server

      

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/auth-server.png

   .. tab:: Notification
      .. tabs::
         .. tab::
      

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/notifs-mail.png
         .. tab::           
            

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/notifs-sms.png

   .. tab:: Language

     
   .. tab:: IPv6 

      

   .. tab:: ZON




      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/zon.png


PPP (Point-to-Point Protocol)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

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

VPN (Virtual Private Network)
================================

Qu'est-ce qu'un VPN  ?
---------------------------

La notion de VPN avait déjà été abordée lors du module M145 de 1ère année.
Sa définition est simple :"Relier entre eux des systèmes informatiques de manière **sûre** en s’appuyant sur un réseau existant."

On distingue 3 types de VPN :


.. tabs::

   .. tab:: Client-to-Site VPN

      

   .. tab:: Site-to-Site VPN (Intranet)



   .. tab:: Site-to-Site VPN (Extranet)

     

Phases
---------

Phase 1

L'objectif principal de la phase 1 est la mise en place d'un canal chiffré sécurisé par l'intermédiaire duquel deux pairs peuvent négocier la phase 2. Lorsque la phase 1 se termine avec succès, les pairs passent rapidement aux négociations de phase 2. Si la phase 1 échoue, les périphériques ne peuvent entamer la phase 2.

Phase 2

L'objectif des négociations de phase 2 est que les deux pairs s'accordent sur un ensemble de paramètres qui définissent le type de trafic pouvant passer par le VPN et sur la manière de chiffrer et d'authentifier le trafic. Cet accord s'appelle une association de sécurité.

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



Fonctionnalités UTM
----------------------

.. tabs::

   .. tab:: APP PATROL

      L'App Patrol est un **pare-feu applicatif.**
      Il permet de **filtrer et bloquer des applications définies** par l'administrateur.
      Ces dernières vont des réseaux sociaux jusqu'à l'accès au réseau Tor (onion routing) par exemple...

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
            
            

            Cette catégorie est spécifique aux adresses IP.

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/ip-reputation.png


         .. tab:: DNS Threat Filter
            
            

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/dns-filter.png

         .. tab:: URL Threat Filter           
            
            

            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/url-filter.png

         
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/utm/url-filter.png



   .. tab:: IPS

      

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/


   .. tab:: Sandboxing



      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/


   .. tab:: Email Security

     
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/


   .. tab:: CDR

      

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/


   .. tab:: SSL Inspection



      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/


   .. tab:: IP Exception

      

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/

   .. tab:: Astra Cloud Security
     


Client-to-Site VPN
----------------------

Site-to-Site VPN (Intranet)
--------------------------------

.. warning:: 
   Pour cet exemple, nous utiliserons un **VPN de type IPSec**.

Pour configurer un VPN site-à-site sur l'ATP200 de Zyxell, il faut configurer dans l'ordre la phase 1 et la phase 2 d'une connexion VPN.

Dirigeons nous donc vers l'onglet VPN Gateway.
En premier temps, cliquer sur "ADD"
Donner un nom reconnaissable et pertinent à notre connection site à site.
Choisir la version 2 d'IKE (IKEv2) car IKEv1 est désormais obsolète.
Définir l'interface sur laquelle le site distant doit se connecter.





Site-to-Site VPN (Extranet)
-------------------------------