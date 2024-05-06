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

      Alternative for Odoo.sh users.

   .. tab:: iBarry

      Third version for On-premise users.



Certifications 
------------------

Cybersafe, ISO27001...


Pare-feu
===========

Pare-feu à état (Stateful Firewall)

Pare-feu sans état (Stateless Firewall)


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

      Content dedicated to Odoo Online users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/system-hostname.png


   .. tab:: USB Storage

      Alternative for Odoo.sh users.

   .. tab:: Date/Time

      Third version for On-premise users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/date-time.png

      
   .. tab:: Console Speed

      Content dedicated to Odoo Online users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/console-speed.png


   .. tab:: DNS

      Alternative for Odoo.sh users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/dns-settings.png

   .. tab:: WWW

      Content dedicated to Odoo Online users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/www.png


   .. tab:: SSH

      Alternative for Odoo.sh users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/ssh.png


   .. tab:: Telnet

      Third version for On-premise users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/telnet.png


   .. tab:: FTP

      Content dedicated to Odoo Online users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/ftp.png


   .. tab:: SNMP

      Alternative for Odoo.sh users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/snmp.png


   .. tab:: Auth. Server

      Content dedicated to Odoo Online users.
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/auth-server.png

   .. tab:: Notification
      .. tabs::
         .. tab::
            Alternative for Odoo.sh users.
            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/notifs-mail.png
         .. tab::           
            Alternative blablabla 
            .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M233/notifs-sms.png

   .. tab:: Language

      Third version for On-premise users.

   .. tab:: IPv6 

      Content dedicated to Odoo Online users.

   .. tab:: ZON

      Alternative for Odoo.sh users.
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

      Content dedicated to Odoo Online users.

   .. tab:: Site-to-Site VPN (Intranet)

      Alternative for Odoo.sh users.

   .. tab:: Site-to-Site VPN (Extranet)

      Third version for On-premise users.


Phases
---------



Objets
--------------

Les objets permettent de classer la majorité des éléments utilisés par le pare-feu.
Les objets possèdent des attributs, des valeurs, et sont rangés dans différentes catégories, sous catégories ou des groupes.

La rigueur dans le maintien de l'arborscence des objets est absolument nécessaire.
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

APP PATROL
^^^^^^^^^^^^^^




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