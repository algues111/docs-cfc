===============================
Module 391 : PBX Virtualisé
===============================



Jour 1
========

Ce jour est destiné à introduire la matière que nous verrons lors des prochains cours du module M291.

Voici le fichier d'introduction téléchargeable ci-dessous :

:download:`source/other/Module_391_Intro_FR.pdf`


Mandats
-----------

Mandat 1 
^^^^^^^^^^^^^^

Recherche combien d’opérateurs sont présent uniquement dans ton canton.

La fédération met à disposition une liste complète des FST (a mettre la definition) enregistrés en Suisse.

Il y en a approximativement 500 !

.. note::
    Lien vers la liste :
    :download:`Fichier excel à télécharger <source/other/liste-excel-opérateurs.xlsx>`

Voici quelques exemples qui ressortent le plus souvent :

- Swisscom 
- Sunrise 
- Salt 
- Mucho 
- Coop Mobile 
- M-Budget Mobile 
- Yallo 
- Das Abo 
- Lidl Connect 
- Wingo
- Telcopack
- Peoplefone 
- VTX Telecoms
- etc etc....

Noyé sous la multitude de services disponibles, il est donc très important en tant que technicien conseiller de proposer une solution que nous connaissons, dont la qualité/fiabilité est certaine, et surtout qui est adaptée aux besoins du client !


Mandat 2 (a completer)
^^^^^^^^^^^^^^^^^^^^^^^^^^

Prends un opérateur au choix et liste les différentes possibilités d’abonnements pour l’accès à Internet. 

Est-ce que des abonnements spécifiques sont nécessaires pour l’installation de ton
système de téléphonie. 

Analyse les besoins en fonction du projet (Débit de données, coûts mensuels,
IP fixe, support, SLA, etc.). 

Quelles propositions peux-tu faire au client s’il s’agit d’une nouvelle
installation ou s’il s’agit d’une installation existante ?


Pour ce mandat, nous explorerons les différentes solutions que nous propose `VTX Telecom <https://www.vtx.ch/>`_.

Concernant les abonnements Internet, VTX propose 2 types de connectivité comprenant chacune 2 options (cela fait donc 4 solutions au total).

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/vtx-internet.png



En complément des solutions de raccordement Internet, VTX propose des solutions de téléphonie variées !

3 types de forfaits phares sont disponibles :

- Trunk (analogique, IP, vPBX)
- Solution de téléphonie SIP
- Solution Microsoft Teams

Prenons l'exemple d'une petite entreprise de 10 personnes dans un bureau d'avocats comprenant 1 secrétaire à temps plein.
Ce bureau d'avocats vient d'ouvrir et nécessite une ouverture de ligne et une solution de téléphonie adéquate (comprenant un FAX)


Le forfait Internet Corporate Access sera raccordé, avec une connexion fibre dédiée et 200Mbit/s en symmétrique permettant une connectivié haut-débit et de qualité !

De plus, VTX double les forfaits téléphoniques si vous n'avez pas de raccordement Internet chez eux. On a donc tout intérêt à prendre un forfait Int


Étant donné que l'infrastructure est nouvelle, nous pouvons proposer une solution 3CX hébergée sur site sur un NUC, avec un trunk SIP IP VTX comprenant 4 canaux.

15.- / mois :  le trunk de 4 canaux

Tarifs à la minute ci-dessous :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/forfait-min.png




Mandat 3 
^^^^^^^^^^^^

Reprends l’opérateur choisi précédemment et liste les différentes possibilités d’abonnements pour les services :abbr:`VoIP (Voice over Internet Protocol)`

Comme présenté dans le mandat n°2, voici les 3 solutions de téléphonies phares de VTX :

- Trunk (analogique, IP, vPBX)
- Solution de téléphonie SIP
- Solution Microsoft Teams


Trunk
~~~~~~~~~~~~~~


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/vtx-trunk-list.png


.. important::

    Pour tout trunk, les `tarifs à la minute s'appliquent <https://www.vtx.ch/zone1/>`_.

    Si toutefois vous pensez que les collaborateurs appelleront.....

    .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/illimite-vtx.png

    

.. tabs::
   .. tab:: Analogique
      
        VTX propose des trunks analogiques, de 4 à 30 canaux en simultanés (jusqu'à 120 canaux sous devis) avec la location du matériel incluse.
        
        .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/vtx-trunk-analogique.png


   .. tab:: SIP-IP

        En plus des trunks analogiques, VTX vend des trunks SIP, de 4 à 60 canaux en simultanés (jusqu'à 200 canaux sous devis) que vous pouvez gérer via une interface web.

        .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/vtx-trunk-analogique.png

        
   .. tab:: vPBX

      En naviguant dans ce profil, nous voyons que nous l'avons configuré pour que :

Mandat 4 (a completer)
^^^^^^^^^^^^^^^^^^^^^^^^

Lors d’un exercice avec appel VoIP, essaie d’identifier les différents protocoles et codecs énoncés ci-dessous au moyen de l’analyseur Wireshark. 

.. note::

    Pour cette partie du mandat, je vous invite à vous dirigier vers la section `des codecs audio de la Documentation-M362 <https://docs-cfc.readthedocs.io/fr/latest/Documentation-M362.html#codecs-audio>`_.

Quelles constatations peux-tu faire en changeant de codec par exemple ? 

Comme expliqué dans le M362, selon le codec utilisé, la taille du payload sera différente dans le paquet RTP.



Enregistre une trace d’un appel SIP et recherche les différents protocoles utilisés (SIP, SDP, RTP, RSTP, type de codecs, etc.). 

En écoutant la communication SIP via Wireshark, il est possible de générer un graphique montrant les différentes étapes de la communication, de son établissement jusqu'à sa terminaison :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/sip-g711-completed.png

Ce graphique comporte les informations suivantes :

.. tabs::

    .. tab::

      - Invitation SDP : négocie la teneur des données transférées (audio, vidéo, texte, message, application, etc.), ainsi que le format et le protocole de transport utilisés, et le port RTP.

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/sdp-g711.png

      .. note::
          Le Type-101 spécifié dans les codecs audio correspond aux touches DTMF.


    .. tab::


      - Flux RTP : envoie de paquets audio à travers ce protocole, ports aléatoires décidés dans 

    .. tab::

      - Contrôle du flux RTP via RTCP
        
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/rtcp-g711.png


Documente l’ensemble de tes tests.

Si nous décidons cependant de choisir 2 codecs différents sur 2 terminaux distincts, et que ces derniers communiquent via un flux RTP direct, l'initiation de l'appel échouera.

Nous pouvons le voir ci-dessous dans le graphique :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/sip-g722-g711-rejected.png




Configure des téléphones de manière simple en utilisant les informations fournies par l’enseignant.


Mandat 5 
^^^^^^^^^^^^


Reprends l’opérateur choisi précédemment et liste les différentes variantes possibles pour les interconnexions VoIP. 

Pour quelles variantes aura-t-on besoin d’une appliance de type SBC ? 

A quoi sert cette appliance ?

.. note::
    Voir la section `SBC de la Documentation-M362 <https://docs-cfc.readthedocs.io/fr/latest/Documentation-M362.html#sbc-session-board-controller>`_.


Mandat 6 
^^^^^^^^^^^^


Fais un tableau en listant les principales caractéristiques de ces différentes plateformes Cloud. 

Laquelle te semble la plus adaptée pour l’installation de ton système de téléphonie ? 

Quelles sont les avantages et inconvénients d’une installation sur une plateforme Cloud par rapport à une installation On Premise (Sécurité, équipements, itinérance, interfaces, etc.) ?


Mandat 7
^^^^^^^^^^^^^^

Choisis un des fournisseurs proposés, crée un compte sur la plateforme Cloud et procède à l’installation de ta première machine virtuelle. 

Il est aussi possible de procéder à l’installation d’un hyperviseur. Suis les procédures fournies par le fournisseur. Etablis un rapport de cette première installation.


Pour compléter ce mandat, nous louerons un serveur VPS chez `OVH <https://www.ovhcloud.com/fr/vps/>`_, qui propose plusieurs tarifs intéressants pour des petits labs comme celui-ci.

Commencons donc par choisir le forfait qui nous convient !

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/ovh-vps-tarifs.png




Ici, nous prendrons le VPS "VLE-2" possédant 2 coeurs virtuels, 2Go de RAM, 40GB de stockage en NVME ainsi qu'une bande passante de 500Mbit/s.

Nous choisissons aussi l'OS, qui sera ici Ubuntu 24LTS !!

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/ovh-paiement.png




OVH propose d'ajouter des options à votre serveur VPS, telles que des backups automatisées, des snapshots, ou bien du stockage supplémentaire.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/ovh-options.png




Après avoir choisi les options souhaitées, il suffit de passer au paiement et vous obtiendrez un recu de votre commande ainsi qu'un accès à votre nouveau VPS !

Voici le dashboard de gestion du VPS :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/ovh-options.png

En fonction de l'OS et des paramètres de connexion choisis, il suffit de se connecter via ssh avec user@ip avec le mot de passe pour prendre contrôle du serveur Linux.

Beaucoup d'autres providers proposent des services de hosting cloud, avec plus ou moins d'options.

C'est à vous de convenir de ce dont le client à besoin et d'adapter en fonction !





Mandat 8 
^^^^^^^^^^^^^^

Choisis une solution de central téléphonique virtuel et procède à son installation sur une
plateforme d’hébergement Cloud ou sur un hyperviseur. Etablis un rapport de cette première
installation.


Pour la solution de PBX virtuel, nous installerons une instance 3CX avec une licence de test Enterprise sur le Public Cloud d'OVH

.. note::
    Depuis que 3CX ne prend plus en charge les installations post-boot sur Linux, il est soit nécessaire de télécharger et de monter l'iso sur la VM, ou alors de trouver un provider cloud permettant l'installation de 3CX via un script d'installation. 

    C'est la 2ème option qui sera présentée ici.





Clé SSH RSA tuto public cloud OVH 

https://help.ovhcloud.com/csm/fr-public-cloud-compute-getting-started?id=kb_article_view&sysparm_article=KB0051011#etape-1-creer-des-cles-ssh%2F

Installation 3CX OVH Public cloud :abbr:
https://help.ovhcloud.com/csm/en-gb-voip-3cx-public-cloud-automatic-deployment?id=kb_article_view&sysparm_article=KB0059072

Attention, il faut prendre les scripts bash d'OVH, mais prendre la config XML de 3CX via ce lien : https://install.3cx.com/?license=AAAA-BBBB-CCCC-DDDD

Script bash+xml installation 3cx cloud OVH :abbr:

:download: `source/other/SetupConfig-combined`



Call4Tell
------------------

Call4Tell est une entreprise fabricant des ordinateurs au format NUC, dans lesquels 3CX est préinstallé.
Ils proposent plusieurs gammes de produits en fonction de vos besoins.

NX32
^^^^^^^^^^^^^^^^^

Au labo, nous disposons d'un de leurs boîtiers NX32, étant l'entrée de gamme de l'entreprise.

Voici ses caractéristiques :

    - Software: 3CX pre installed (Debian)
    - CPU: Intel Atom
    - RAM: 4GB DDR3
    - Storage: 32GB EMMC
    - Ethernet ports: 2 (100Mbps speed)
    - HDMI port: 1
    - USB: 2* USB 2.0 for external storage or disaster recovery system
    - Form Factor: 165*165*40mm
    - Color: Blue
    - Warranty: 1 year


Web Interface
^^^^^^^^^^^^^^^^^^^^


En plus de 3CX, Call4Tell fournit une interface web administrative permettant de configurer plusieurs paramètres de l'appareil.


Question Bonus du jour :
----------------------------



Est-il possible d'avoir un trunk SIP Swisscom sur un 3CX installé dans le cloud ?

réponse :

Non, pas avec le SBC

Oui avec Enterprise SIP Cloud

https://documents.swisscom.com/product/filestore/lib/047dea54-3e19-43b0-a36e-9eed5af4f3b8/enterprise_sip_cloud_factsheet-fr.pdf?idxme=pex-search




Jour 2
===================


Mandat 1
------------------

Recherche quelles sont les différentes possibilités d’installation de ton système de 
téléphonie (On Premise, Cloud, machine physique, machine virtuelle…). 

Liste les avantages et les contraintes en fonction des différentes possibilités.

.. note::
    Pour ce mandat, nous utiliserons 3CX.

Il est possible de faire beaucoup de choses avec ce produit.

On premise
^^^^^^^^^^^^^^^^

Comme nous l'avons vu durant le jour 1, des sociétés telles que Call4Tell proposent des ordinateurs au format NUC avec 3CX préinstallé.


Cette solution peut être avantageuse pour les clients n'ayant pas d'hyperviseur ou de serveurs mais souhaitant garder un appareil sur site.
Cela demande cependant un cout unique de départ important (à partir de 300.-).

Selon les marques, modèles, gammes, il est important d'établir précisément les besoins du client pour lui proposer la solution la plus adéquate.

Cloud / Cloud d'entreprise
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

De nouveau, nous avons exploré cette possibilité lors du jour 1 et de l'installation de 3CX sur le Public Cloud d'OVH.

Cette solution est envisageable pour les entreprises ayant déjà des services hébergés dans le cloud (Azure VMs, Infomaniak, Amazon etc..) ou pour les clients n'ayant ni le souhait ni la place d'avoir d'équipements informatiques sur site.
Selon les hébergeurs, il est possible de choisir une facturation mensuelle ou par heure, ce choix dépendant exclusivement des besoins du client.

L'entreprise mandatée pourrait aussi très bien proposer d'héberger ces solutions dans son propre cloud et proposer des forfaits avantageux ainsi qu'une gestion centralisée des services proposés au client.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/cloud1.png



Virtualisation
^^^^^^^^^^^^^^^^

Puisque 3CX propose une image linux personnalisée, il est tout à fait envisageable de la virtualiser dans un hyperviseur. Cela est même officiellement supporté dans la documentation de 3CX.

Pour les clients disposant d'ores et déjà d'un serveur ayant les fonctionnalités et ressources nécessaires pour une VM de plus.
Cette solution n'est pas recommandé si le client ne possède pas cette infrastructure, car le coût de départ unique serait bien trop élevé !





Conclusion
^^^^^^^^^^^^^^

Toutes ces solutions permettent aux techniciens d'avoir une approche granulaire de ce dont le client nécessite.

Le plus important reste donc d'être à l'écoute de ce dernier et de lui proposer certains services en fonction.


Mandat 2 
------------

Établir une checklist reprenant les différents thèmes du point précédent afin de pouvoir 
fixer précisément les besoins du client final (choix des terminaux, gestion de la sécurité, …). 

Etablir également un schéma de l’installation et un inventaire du matériel installé (SN, MAC address, version 
de firmware, …). Utiliser un système de gestion de mots de passes spécifiques afin de les répertorier


De nos jours, la sécurité est un aspect fondamental de toute infrastructure informatique, évoluant tous les jours.

Toutefois, certains principes fondamentaux régissent les règles de la séurité informatique.


Menaces pour la VoIP
^^^^^^^^^^^^^^^^^^^^^^^^

Étant un composant non négligeable d'une infrastructure d'entreprise, la VoIp est aussi soumise à des menaces, failles de sécurité et autres...

Voici les 10 menaces principales auxquelles elle doit faire face :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/voip-threats.jpeg




CIA Triad et autres principes
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

La triad CIA a déjà été évoqué dans des modules précédents.

Elle est composé de 3 principes :

#. La confidentialité : L'information n'est disponible seulement pour les personnes autorisées.
#. L'intégrité : L'information n'a pas été modifiée / altérée sans autorisation.
#. La disponibilité : L'information est stockée, accessible et disponible en tout temps.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/cia-triad.png



A ce triangle se rajoute 4 autres concepts importants qu'on applique aussi à la téléphonie IP :

.. tabs::

    .. tab:: L'authentification
        
        Garantir l’identité de l’usager qui envoie le message dans le cadre de la ToIP, cette propriété permet par exemple à un serveur de vérifier qu’il fournit le service à l’usager légitime


    .. tab:: La non-répudiation

        La non répudiation des données nécessite l’archivage des données échangées.


        Dans le cadre de la ToIP, cette propriété permet d’associer une communication à une personne de manière certaine


    .. tab:: Le non rejeu

      Éviter de mémoriser puis de réinjecter les données dans le réseau.
      

      Dans le cadre de la ToIP, cette propriété permet de ne pas pouvoir rejouer des échanges protocolaires par une personne tierce souhaitant accéder au service

    .. tab:: L'anonymat

      Capacité du système à masquer l’identité de l’usager.
      

      Dans le cadre de la ToIP, cette propriété peut se traduire par le masquage de l’identité de l’appelant



Bonnes pratiques (a completer)
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Activation de protocoles sécurisés : 
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



- SIPS (SIP Secure) : utilise TLS

If a SIP User Agent, UA1, wants to establish a secure SIP session with UA2:

UA1 contacts proxy server1 requesting a TLS session along with a session invitation for UA2. The proxy server provides a public certificate and UA1 validates it. UA1 and proxy server1 exchange session keys to encrypt/decrypt data for that particular session.
Proxy server1 forwards the session invitation to the next proxy server using a TLS session or IPSec mechanism.
UA1 and proxy server2 authenticate over TLS. The same procedure is repeated till the last hop ensuring SIP over TLS is used end-to-end.
The secured session between UA1 and UA2 is now established.


- SRTP (Secure RTP)


Schéma de principe communication VoIP sécurisée :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/sips-srtp.png



Schéma réseau
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Que ce soit un schéma de principe ou un schéma réseau détaillé, cela est très utile pour comprendre le concept de l'infrastructure et intervenir rapidement et efficacement.

Le schéma devrait donc comprendre :

- Les noms des appareils (nom dns local, la marque, le modèle...)
- Les adresses IP / MAC des appareils ou des interfaces
- Le VLAN utilisé
- Les liens physiques et la technologie (CUC ou Fibre Optique)
- 



Inventaire du parc informatique
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Liste des équipements installés chez le client (marque, modèle...)
- Versions de firmware / OS
- N° de série
- Adresse MAC



Gestion des mots de passe
~~~~~~~~~~~~~~~~~~~~~~~~~~


Bitwarden, proton, keepass, lastpass.....



Décommissionnement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~



Exigences de matériel
^^^^^^^^^^^^^^^^^^^^^^^^


En plus des exigences de sécurité, il peut également avoir des exigences liées au matériel et à sa 
conception, notamment pour des terminaux spéciaux comme :

- **Les terminaux ATEX** : prévenir des explosions en garantissant que les équipements utilisés dans les environnements dangereux sont conçus et construits de manière à minimiser les risques


- **Les terminaux antibactériens** : le but du matériau utilisé est d’empêcher le développement et la prolifération des bactéries. Ce genre de terminaux peut être utilisé dans les hôtels ou les hôpitaux



Mandat 3
--------------------
Recherche les différentes fonctionnalités disponibles sur ton système et fait un 
comparatif avec un autre système de ton choix, comme, par exemple un système hébergé chez un 
opérateur ou un fournisseur. Quels sont les avantages et les inconvénients des systèmes proposés ? 
Quels sont les coûts liés au système choisi ? Quel système te semble être le plus approprié ?





Fonctionnalités d'un système de téléphonie 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

gestion ds droits utilisateurs (opérateurs de groupe, administrateurs etc..)

Api... système d'hotellerie, CRM, interphonie, alarmes....


- **Gestion des appels, renvois, déviations, …**
- **Gestion de présence (disponible, absent, ne pas déranger, …)**
- Gestion de parking d’appels
- **Groupes d’appels**
- Système d’auto-attendant avec gestion d’agents et de files d’attentes
- Gestion de la musique d’attente
- Gestion d’annonces et de messages vocaux
- Gestion des utilisateurs, permissions, droits, … (opérateurs de groupes côté client)
- **Gestion de systèmes IVR**
- Intégration de système tiers
- Gestion des fax
- **Gestion de la connectivité SIP avec l’opérateur, gestion des codecs**
- Gestion de système de visio-conférence
- Gestion d’une messagerie ou d’un chat interne
- Gestion et attribution des numéros externes aux utilisateurs
- Gestion de calendrier et de fonctions automatisées
- Gestion de l’enregistrement des appels
- …

Certaines fonctionnalités sont considérées comme "basiques", ce qui veut dire qu'elles sont généralement intégrées par défaut dans les systèmes de téléphonie.

Ce sont par exemple les fonctionnalités en gras dans a liste ci-dessus.


3CX vs Swisscom
^^^^^^^^^^^^^^^^


3CX propose énormément de fonctionnalités au sein de son système, permettant donc une grande flexibilité par rapport aux demandes parfois exotiques des clients.

Cependant, combien coûte réellement une infrastructure 3CX par rapport à une solution hosted chez Swisscom par exemple ?
Quels sont les avantages et les inconvénients ?



Tarifs Swisscom
~~~~~~~~~~~~~~~~


.. admonition:: Information
    Pour essayer de faire un comparatif concret des 2 systèmes, nous allons imaginer un bureau d'études avec 10 utilisateurs finaux.
    Au total, le bureau passe 10 heures au téléphone par moi.

    1 appel sur 2 est émetteur donc cela revient à 5 heures facturées.

SBC hosted telephony :

Appels standards Suisse mobiles et fixes illimité : 22.-/mois par utilisateur
Apels standards Suisse mobiles et fixes à la minute : 12.-/ mois par utilisateur + 0,08ct la minute pour mobiles / 0,30 ct la minute pour fixes

220.- par mois pour le forfait illimité.

144.- par mois au moins cher. 


3CX Pro :

Pour 10 utilisateurs, 205.- sont facturés par an. ce qui revient à 1,708.- par utilisateur par mois.

Cependant, il faut un trunk pour que les utilisateurs puissent appeler des numéros externes.
Pour cela, nous allons choisir un trunk avec 2 canaux, ce qui est suffisant pour une entreprise de 10 personnes.

15chf par mois pour 10 numeros

0.- pour les canaux.

0,03chf par minute réseau mobile
0,25chf par minute réseau fixe

Au plus cher, le coût serait de 90.- par mois pour les communications émises !

Si nous regroupons cela avec la licence 3CX, cela revient à 107,08.- par mois maximum.



Conclusion
******************

Dans ce cas, 3CX pro revient moins cher que Swisscom Hosted Telephony.

Au final, pour comparer réellement deux solutions, il est nécessaire de faire des calculs en fonction du nombre d'utilisateurs, du nombre d'appels simultanés et du temps passé au téléphone au total par mois.

Ce calcul dégrossira une bonne partie des coûts réels par solution proposée.  


Avantages et inconvénients
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Mais les coûts ne sont pas toujours l'élément décisif d'une solution, qu'elle soit téléphonique, informatique ou autre.

Pour compléter le comparatif 









Mandat 4 A TESTER DERNIER JOUR
----------------------------------

Recherche les différentes possibilités d’interaction de ton système avec des systèmes tiers 
et recherche également les caractéristiques des paramètres de ton système, s’ils sont disponibles.
Réalise également une intégration d’un système tiers (Annuaire, CRM, …) avec ton serveur de 
communication et test le bon fonctionnement de cette intégration


Aujourd'hui, de plus en plus de logiciels proposent des APIs ou des middlewares permettant une intégration facilitée avec d'autres softwares.

Cela donnant donc beaucoup de possibilités pour centraliser et regrouper des services entre eux.


Ci-desous quelques exemples de services ou softwares s'intégrant avec 3CX.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/3cx-integrations.jpeg


- Gestion des utilisateurs internes (extensions) et intégration de calendriers et de contacts 
avec Microsoft, Google, …
- Interaction avec des outils de CRM, par exemple, Salesforce, Zendesk, Freshdesk, Bitrix, 
Odoo, …
- Interaction avec des outils hôteliers comme Fidelio, Mitel, …
- Interaction avec Teams
- Interaction avec des systèmes de messagerie instantanée comme WhatsApp, services SMS, …

greffer chat 3cx dans un site web et meem faire des appels audio/video

- Interaction avec les réseaux sociaux comme Facebook, …
- Interaction avec des systèmes de taxation comme Easytax, …

existe quasi plus, pour dispatcher les couts des forfaits telephonques par secteur departement

- Interaction avec des systèmes d’alarmes ou d’appel malade, comme Siemens, Tyco, GETS, …



Mandat 5
-----------

Les constructeurs de terminaux mettent souvent à disposition des :abbr:`RPS (Redirection and Provisioning Service)` pour centraliser et simplifier la gestion des terminaux.

Selon les licences et les providers, un RPS permet notamment :

- Gestion basique des terminaux
- Gestion avancée des terminaux
- Possibilités de mise à jour à distance des terminaux
- Possibilités de redémarrage à distance des terminaux
- Indication du système de téléphonie sur lequel un terminal doit être affecté
- Gestion de comptes VoIP
- Journaux d’événements
- Diagnostics
- Connectivité avec des systèmes tiers au moyen d’API’s (Application Program Interface) 


L'utilisation d'un RPS est donc un avantage à la fois pour le technicien et pour le client, car il limite les déplacements et donc les frais qui les entourent !
C'est un gain de temps considérable.

Voici une liste non-exhaustives de fournisseurs proposant un serveur RPS.


- `Grandstream : <https://www.gdms.cloud/login>`_
- `Yealink : <https://dm.yealink.com>`_
- `Snom : <https://sraps.snom.com/>`_
- `Fanvil : <https://fanvil.com/products/fdms/20220322/7307.html>`_


Schéma RPS :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/schema-rps.jpeg



172.16.101.2

attention Call4tell interfaces Ethernet inversées !!

De gauche à droite : interface 2 puis interface 1 (contre-intuitif) pour le nx32 seulement

Setup classique de montage de volume linux à faire lors de l'installation

capture d'écran pour LVM

Choisir SBC ou System en focntion


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/3cx-CLI.png


ATTENTION, CHOISIR TIMEZONE PARIS CAR SUISSE PROBLEMES

Adlocal1$$


commencer extensions a partir de 200 car numero durgences dans la 1ère centaine