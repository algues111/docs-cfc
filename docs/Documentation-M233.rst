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

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/user-meme.png

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


Confidentialité
-----------------

La confidentialité est de nos jours aseez complexe.
Entre les Big Tech mettant à jour tous les mois leurs politiques et les gouvernements pondant de nouvelles lois pour règlementer le tout, les utilisateurs sont très souvent perdus.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/privacy-meme.png

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



   .. tab:: IPS / IDS
      
      

      

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

- WLAN_P12_CORP : VLAN100 -> 172.18.12.0/24
- WLAN_P12_PUBLIC : VLAN300 -> 172.18.212.0/24
- WLAN_P12_VoIP : VLAN200 -> 172.18.112.0/24

Pour appliquer des profils de sécurité spécifiques, il est possible d'en créer dans l'onglet Security List.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/wifi/ap-profile-ssid-sec-list.png

Dans celui-ci, nous choisissons :

- Le nom du profil
- Le mode de sécurité (WEP, WPA2, WPA2-ENT, WPA3 etc...)
- La méthode d'authentiication (Enterprise/RADIUS ou Personnel/PSK)
- L'activation ou pas du fast-roaming (802.11r)

Un objet supplémentaire sera nécessaire si nous utilisons un serveur RADIUS pour l'authentification et l'autorisation :

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





VPN
======

Qu'est-ce qu'un VPN  ?
---------------------------

La notion de VPN avait déjà été abordée lors du module M145 de 1ère année.
Sa définition est simple :"Relier entre eux des systèmes informatiques de manière **sûre** en s’appuyant sur un réseau existant."

Intro VPN blablabla

Client-to-Site VPN
----------------------

Avec l'essort du télé-travail ces 5 dernières années, de plus en plus de personnes travaillent depuis leur domicile voire depuis l'étranger.
Les entreprises autorisant cela ont donc besoin d'un système permettant la connexion d'utilisateurs depuis Internet.

Le VPN client-to-site répond à cela. 


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/vpn/client-to-site-schema.png

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

Le VPN site-à-site extranet fonctionne globalement de la même facon que le site-à-site intranet.
La différence réside dans le fait qu'il sera établi pour permettre l'accès au réseau d'entreprise à une société externe.

La configuration des utilisateurs sera donc plus restrictive selon les exigences et les besoins de collaboration !

Protocoles VPN
----------------


IPSec
^^^^^^^^

C'est l'un des protocoles les plus utilisés pour les VPN actuels, il permet l'intégrité et la confidentialité des données.
Comme son nom l'indique, il fonctionne sur la couche réseau du modèle OSI (couche 3)



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
IKE est la réponse.

Ce protocole permet l'initiation de la connexion et l'association des systèmes ; les fameuses SA (security association).
Comment fon


IKEv1
~~~~~~~~~~~~~~

IKEv1 est la première version du protocole IKE.


IKEv2
~~~~~~~~~~~~~~

IKEv2 est la version succédant à IKEv2 avec plus d'interopérabilité ainsi qu'une résistance plus forte aux attaques de type DOS.

.. _RFC-5996: https://datatracker.ietf.org/doc/html/rfc5996



.. seealso::
   RFC-5996_


Phases
^^^^^^^^^^^^

Phase 1

L'objectif principal de la phase 1 est la mise en place d'un canal chiffré sécurisé par l'intermédiaire duquel deux pairs peuvent négocier la phase 2. Lorsque la phase 1 se termine avec succès, les pairs passent rapidement aux négociations de phase 2. Si la phase 1 échoue, les périphériques ne peuvent entamer la phase 2.

La construction de la phase 1 s’établi selon le processus suivant :


• Négociation d’une politique IKE SA correspondante entre pairs pour protéger l’échange IKE
• Echange authentifié de clé Diffie-Hellman afin d’obtenir une correspondance des clés
secrètes partagées
• Authentification et protection de l’identité des pairs avec IPSec
• Construction du tunnel sécurisé pour négocier ensuite les paramètres de la phase 2 de IKE


Deux modes existent pour cette première phase :

Phase 2

L'objectif des négociations de phase 2 est que les deux pairs s'accordent sur un ensemble de paramètres qui définissent le type de trafic pouvant passer par le VPN et sur la manière de chiffrer et d'authentifier le trafic. Cet accord s'appelle une association de sécurité.







