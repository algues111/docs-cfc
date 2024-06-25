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

*Prends un opérateur au choix et liste les différentes possibilités d’abonnements pour l’accès à Internet. *

*Est-ce que des abonnements spécifiques sont nécessaires pour l’installation de ton système de téléphonie ? *

*Analyse les besoins en fonction du projet (Débit de données, coûts mensuels, IP fixe, support, SLA, etc.). *

*Quelles propositions peux-tu faire au client s’il s’agit d’une nouvelle installation ou s’il s’agit d’une installation existante ?*



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

*Reprends l’opérateur choisi précédemment et liste les différentes possibilités d’abonnements pour les services* :abbr:`VoIP (Voice over Internet Protocol)`


Comme présenté dans le mandat n°2, voici les 3 solutions de téléphonies phares de VTX :

- Trunk (analogique, IP, vPBX)
- Solution de téléphonie SIP
- Solution Microsoft Teams


Trunk
~~~~~~~~~~~~~~


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/vtx-trunk-list.png


.. important::

    Pour tout trunk, les `tarifs à la minute s'appliquent <https://www.vtx.ch/zone1/>`_.


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

*Lors d’un exercice avec appel VoIP, essaie d’identifier les différents protocoles et codecs énoncés ci-dessous au moyen de l’analyseur Wireshark. *

.. note::

    Pour cette partie du mandat, je vous invite à vous dirigier vers la section `des codecs audio de la Documentation-M362 <https://docs-cfc.readthedocs.io/fr/latest/Documentation-M362.html#codecs-audio>`_.


*Quelles constatations peux-tu faire en changeant de codec par exemple ?*

Comme expliqué dans le M362, selon le codec utilisé, la taille du payload et donc du paquet sera différente dans le paquet RTP.
La fréquence d'échantillonnage sera aussi différente, et les informations SDP de même.



*Enregistre une trace d’un appel SIP et recherche les différents protocoles utilisés (SIP, SDP, RTP, RSTP, type de codecs, etc.). *


En écoutant la communication SIP via Wireshark, il est possible de générer un graphique montrant les différentes étapes de la communication, de son établissement jusqu'à sa terminaison :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/sip-g711-completed.png

Ce graphique comporte les informations suivantes :

.. tabs::

    .. tab:: Invitation SDP

        Négocie la teneur des données transférées (audio, vidéo, texte, message, application, etc.), ainsi que le format et le protocole de transport utilisés, et le port RTP.

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/sdp-g711.png

      .. note::
          Le Type-101 spécifié dans les codecs audio correspond aux touches DTMF.


    .. tab::  Flux RTP 


        Envoie de paquets audio à travers ce protocole, ports aléatoires décidés dans 

    .. tab:: Contrôle du flux RTP via RTCP

        .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/rtcp-g711.png


Documente l’ensemble de tes tests.

Si nous décidons cependant de choisir 2 codecs différents sur 2 terminaux distincts, et que ces derniers communiquent via un flux RTP direct, l'initiation de l'appel échouera.

Nous pouvons le voir ci-dessous dans le graphique :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/sip-g722-g711-rejected.png




Configure des téléphones de manière simple en utilisant les informations fournies par l’enseignant.


Mandat 5 
^^^^^^^^^^^^


*Reprends l’opérateur choisi précédemment et liste les différentes variantes possibles pour les interconnexions VoIP. *

*Pour quelles variantes aura-t-on besoin d’une appliance de type SBC ? *

*A quoi sert cette appliance ?*

.. note::
    Voir la section `SBC de la Documentation-M362 <https://docs-cfc.readthedocs.io/fr/latest/Documentation-M362.html#sbc-session-board-controller>`_.


Mandat 6 
^^^^^^^^^^^^


Fais un tableau en listant les principales caractéristiques de ces différentes plateformes Cloud. 

*Laquelle te semble la plus adaptée pour l’installation de ton système de téléphonie ?*

*Quelles sont les avantages et inconvénients d’une installation sur une plateforme Cloud par rapport à une installation On Premise (Sécurité, équipements, itinérance, interfaces, etc.) ?*

Sécurité
~~~~~~~~~~~~~~


Cloud :
*************

Sécurité physique gérée par le fournisseur cloud, avec des équipes dédiées. 
Maintenance et mises à jour des serveurs par le fournisseur.

Risque potentiel d'accès non autorisé aux données par des tiers (selon le niveau de sécurité du fournisseur).

On Premise :
****************

Contrôle total sur la sécurité et les données.

Nécessite cependant une expertise / maintenance interne rigoureuse et régulière, et des investissements pour maintenir un niveau de sécurité optimal dans le temps.



Équipements
~~~~~~~~~~~~~~

Cloud :
**************

Aucun investissement de départ, l'infrastructure est gérée par le fournisseur.
Évolutivité facile des ressources selon les besoins, approche granulaire.

On Premise :
****************

Nécessite des investissements de départ importants en matériel et maintenance. Des coûts sont aussi à prévoir tous les ≈ 5 ans pour mettre à niveau le matériel ou le changer complètement selon les besoins.

Évolutivité plus complexe et coûteuse.


Itinérance / Mobilité
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Cloud :
**********

Accès aux données et applications de n'importe où avec une connexion internet, aucune nécessité de VPN pour un drive par exemple.
Facilite le travail à distance et la collaboration.

On Premise :
**************

Accès généralement limité au réseau local de l'entreprise.
Nécessite des configurations supplémentaires pour l'accès à distance (ex. VPN).


Interfaces / Intégrations
~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Cloud :
**********

Selon le fournisseur, les intégrations sont facilitées avec d'autres services cloud, augmentant donc l'interopérabilité.
Mises à jour automatiques des interfaces et fonctionnalités (dépendant du service et du fournisseur)

On Premise :
************

Intégrations potentiellement plus complexes avec des systèmes externes
Contrôle total sur les interfaces et personnalisations

Coûts
~~~~~~~

Cloud :
***********

Modèle de coûts prévisible basé sur l'abonnement
Pas d'investissement initial important en infrastructure

On Premise :
**************

Coûts initiaux élevés pour l'achat de licences et d'équipements.
Coûts de maintenance et de mise à jour à long terme.


Conclusion
~~~~~~~~~~~~~~

De nos jours, la majorité des entreprises disposent de services hébergés dans le cloud, ou du moins, sur un site distant.
Selon les critères du client et certains cas, les services cloud peuvent s'avérer parfait pour limiter les coûts grâce à une approche qui se veut granulaire.

Toutefois, il ne faut pas oublier en tant que technicien les inconvénients de ces systèmes :

- Déploiement plus ou moins technique
- Migration de services complexe voire impossible entre fournisseurs
- Risques de pannes sans possibilité d'intervention
- Risques de sécurité et de confidentialité (attention aux lois, réglementations locales, et criticité des données).
- Dépendance au fournisseur

Il faut garder à l'esprit que chaque service doit être configuré minutieusement et hébergé chez un fournisseur de confiance.
Tous les aspects listés plus haut doivent être pris en compte pour le choix de solutions optimales pour les clients.





Mandat 7
^^^^^^^^^^^^^^

*Choisis un des fournisseurs proposés, crée un compte sur la plateforme Cloud et procède à l’installation de ta première machine virtuelle. *

*Il est aussi possible de procéder à l’installation d’un hyperviseur. Suis les procédures fournies par le fournisseur. Etablis un rapport de cette première installation.*


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

:download:`source/other/SetupConfig-combined`



Call4Tell
------------------

Call4Tell est une entreprise fabricant des ordinateurs au format NUC, dans lesquels 3CX est préinstallé.
Ils proposent plusieurs gammes de produits en fonction de vos besoins.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/call4tell-products.png


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

*Recherche quelles sont les différentes possibilités d’installation de ton système de téléphonie (On Premise, Cloud, machine physique, machine virtuelle…). *

*Liste les avantages et les contraintes en fonction des différentes possibilités.*

.. note::
    Pour ce mandat, nous utiliserons 3CX, car c'est un produit que nous connaissons et utilisons.



3CX est une **solution de communications virtuelle** qui permet aux entreprises de gérer leurs appels téléphoniques, leur messagerie instantanée, leur vidéoconférence ainsi que tous les services que pourrait proposer un PBX classique, grâce à différentes installations et forfaits.

Ce système est hébergeable sur différents systèmes d'exploitation, notamment linux et windows, et dans différentes infrastructures (on-premise, cloud, hosted 3cx...), le rendant très flexible selon les demandes.

De plus, un forum utilisateur est accessible, facilitant les petits dépannages et le contact avec le fournisseur ainsi que les autres utilisateurs.

12 millions d'utilisateurs l'utilisent chaque jour, le placant donc sans souci sur le podium des leaders mondiaux de la téléphonie !


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


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/hyperv.jpeg



Conclusion
^^^^^^^^^^^^^^

Toutes ces solutions permettent aux techniciens d'avoir une approche granulaire de ce dont le client nécessite.

Le plus important reste donc d'être à l'écoute de ce dernier et de lui proposer certains services en fonction.



----------------------


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

Étant un composant non négligeable d'une infrastructure d'entreprise, la VoIP est aussi soumise à des menaces, failles de sécurité et autres...

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

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/sips-srtp.jpeg



Schéma réseau
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Que ce soit un schéma de principe ou un schéma réseau détaillé, cela est très utile pour comprendre le concept de l'infrastructure et intervenir rapidement et efficacement.

Le schéma devrait donc comprendre :

- Les noms des appareils (nom dns local, la marque, le modèle...)
- Les adresses IP / MAC des appareils ou des interfaces
- Le VLAN utilisé
- Les liens physiques et la technologie (CUC ou Fibre Optique)
- 


Cela peut se présenter comme suit, plus ou moins complété. Aucun schéma n'est parfait, il faut seulement qu'il soit parlant, visuel et assez tecnhique pour comprendre l'infrastructure globale.



.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/schema-reseau.png




Inventaire du parc informatique
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

- Liste des équipements installés chez le client (marque, modèle...)
- Versions de firmware / OS
- N° de série
- Adresse MAC



Gestion des mots de passe
~~~~~~~~~~~~~~~~~~~~~~~~~~

Différents moyens sont possibles pour stocker des mots de passe, que ces derniers soient personnels ou professionnels.



Bitwarden, proton, keepass, lastpass.....


Par exemple, Proton AG met à disposition une `page web destinée à générer des mots de passe aléatoires <https://proton.me/fr/pass/password-generator>`_.

Sur cette même page des conseils et explications sur comment créer de bons mots de passe et ce qui les rend plus ou moins forts.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/protonpass.png


Cependant, il y a des pratiques à ABSOLUMENT éviter, telles que :

- Stocker ses mots de passe dans un fichier .txt ou excel, qu'il soit protégé ou non
- Reprendre le même mot de passe pour chaque client
- Utiliser des mots de passe de moins de 14 caractères, ne contenant pas de caractères de type : a-A,0-9,$*#




Décommissionnement
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Avoir un protocole de décommissionnement rigoureux et clair est important pour ne pas se perdre dans notre inventaire.





Exigences de matériel
^^^^^^^^^^^^^^^^^^^^^^^^


En plus des exigences de sécurité, il peut également avoir des exigences liées au matériel et à sa 
conception, notamment pour des terminaux spéciaux comme :

- **Les terminaux ATEX** : prévenir des explosions en garantissant que les équipements utilisés dans les environnements dangereux sont conçus et construits de manière à minimiser les risques


- **Les terminaux antibactériens** : le but du matériau utilisé est d’empêcher le développement et la prolifération des bactéries. Ce genre de terminaux peut être utilisé dans les hôtels ou les hôpitaux



--------------------------


Mandat 3
--------------------
*Recherche les différentes fonctionnalités disponibles sur ton système et fait un 
comparatif avec un autre système de ton choix, comme, par exemple un système hébergé chez un 
opérateur ou un fournisseur. Quels sont les avantages et les inconvénients des systèmes proposés ? *


*Quels sont les coûts liés au système choisi ? Quel système te semble être le plus approprié ?*





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

Ce sont par exemple les fonctionnalités **en gras** dans la liste ci-dessus.


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

Dans ce cas précis, 3CX pro revient moins cher que Swisscom Hosted Telephony.

Au final, pour comparer réellement deux solutions, il est nécessaire de faire des calculs en fonction du nombre d'utilisateurs, du nombre d'appels simultanés et du temps passé au téléphone au total par mois. (cela reste non exhaustif puisque selon les besoins, beaucoup plus de paramètres sont à prendre en compte)

Ce calcul **dégrossira une** bonne partie des coûts réels par solution proposée.  


Avantages et inconvénients
~~~~~~~~~~~~~~~~~~~~~~~~~~~

Mais les coûts ne sont pas toujours l'élément décisif d'une solution, qu'elle soit téléphonique, informatique ou autre.

Pour compléter le comparatif 





-------------------------------



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
C'est un gain de temps considérable.0

Voici une liste non-exhaustives de fournisseurs proposant un serveur RPS.


- `Grandstream : <https://www.gdms.cloud/login>`_
- `Yealink : <https://dm.yealink.com>`_
- `Snom : <https://sraps.snom.com/>`_
- `Fanvil : <https://fanvil.com/products/fdms/20220322/7307.html>`_


Schéma RPS :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/rps-schema-yealink.png



172.16.101.2

attention Call4tell interfaces Ethernet inversées !!

De gauche à droite : interface 2 puis interface 1 (contre-intuitif) pour le nx32 seulement

Setup classique de montage de volume linux à faire lors de l'installation

capture d'écran pour LVM

Choisir SBC ou System en focntion


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M362/3cx-CLI.png


.. important::

    Lors du choix du fuseau horaire, il est important de sélectionner celui de Paris, car choisir celui de Berne est moins fiable et peut causer des problèmes de synchronisation temporelle.




------------------------



Jour 3
===============


Il est possible d'accéder à la console du linux 3cx via une web console :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/console-3cx-web.png




Commencer extensions a partir de 200 car numero durgences dans la 1ère centaine

Accès shell linux 3cx :

:command:`apt-get update` (mettre a jour la liste des paquets)
:command:`apt-get upgrade` (mettre a jour les paquets comportant des upgrades)
:command:`apt-get install <package>` (ici ntp et net-tools (déjà installé))

Bonne pratique :

:command:`sudo adduser arthur`

:command:`sudo usermod arthur -aG  sudo` 
:command:`sudo usermod arthur -aG phonesystem`

Vérifier l'apartenance aux groupes : 

:command:`groups arthur` 


Commandes pour définir une adresse IP statique ainsi que la gateway et serveurs DNS :


Sous debian 10 : :command:`cd /etc/network/ && sudo nano interfaces`

Modifier les lignes :

`enp2so static
address 172.16.201.32
netmask 255.255.255.0 
gateway 172.16.201.1
dns-nameservers 172.16.201.1 1.1.1.1 1.0.0.1 9.9.9.9``


Sécuriser les connexions SSH :

:file:`sshd_config` :

Ne pas autoriser l'accès en ssh pour l'user root
Limiter les attempts failures

.. admonition:: Liens utiles
    Pour connaître plus de bonnes pratiques quant au service SSH, je vous invite à regarder la page d'`IT Connect <it-connect.fr/chapitres/bonnes-pratiques-de-configuration-ssh/>`_.

puisque problemes avec le dns, changer le record A / PTR pour pointer vers l'ip local (soit sur le routeur soit sur le serveur dns (ici windows serveur servoce dns))

Après avoir fait cela, nous pouvons sur Windows effacer le cache DNS et ainsi récupérer les nouveaux enregistrements A du serveur DNS local !



.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/options-3cx.png
    
     : changer le nom des status (traduire en francais)

.. note:: 
    Sous la V20, les utilisateurs peuvent changer eux-mêmes ces status



Forcer le 3CX Phone System EN ou HORS heures bureau : plus disponible sur la V20, car plus d'horaires systèmes mais par départements


Faire attention aux adresses mails pour le reporting (par défaut, l'addresse de la première extension créée est enregistrée)
Le mieux est de désactiver la notification de création d'une nouvelle extension.

Activer seulement ce qui est adéquat.


Permettre de changer les modèles d'envoi de mails mais attention aux appels de variables systèmes



Paramètres généraux 
------------------------

Opérateur 6000 (en général la secrétaire mais par défaut le propriétaire système)
suppression utiliasteur refusée si défini en tant qu'opérateur

Rajouter les numéros d'urgence : c'est une whitelist.


Sécurité 
---------------

Comme tout appareil en réseau, le 3CX (hébergé par le NX96) a besoin de sécurité, que nous parametrons via la section "Scéurité" dans l'interface web admin de la V18.


Antipiratage 
^^^^^^^^^^^^^^

Permet de définir des règles sur le comportement du 3CX en cas d'attaques.

Best practices :

Temps blacklist x100 (8640000) et failed attempts maximum 5 to 3

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/anti-piratage.png




Codes pays autorisés
^^^^^^^^^^^^^^^^^^^^^^

Afin de limiter les spams, les appels surtaxés etc... Nous pouvons définir une liste précise des pays ou régions autorisées.

Dans notre cas, il est utile de ne seulement autoriser les appels provenants de Suisse


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/codes-pays-autorises.png

.. tip::
    International Freephone number pour les n° de support 0 0800 internationaux.



Restrictions de la console 
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Comme une console est dispomible à travers la web interface, il est nécessaire d'y restreindre l'accès au maximum pour prévenir les ataques et les intrusions malveillantes.

Best practices :

Autoriser seulement ladresse ip publique du bureau (pour le management offsite)

Mails
-----------

Options
----------


Sauvegardes 
----------------

Afin de garantir un RTO optimal, il est nécessaire de sauvegarder notre système de manière fiable et sécurisée.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/backup-folder.png


Planifier les sauvegardes avec une rétention d'environ 7 jours
Choisir ce que nous voulons sauvegarder

.. warning:: 
    Eviter de backup les enregistrements chez soi car prend de la place. Plutot a faire chez le client.   


Mandat 1
-------------

En présence d’une appliance physique, rechercher les limitations et les possibilités 
d’extensions du système de téléphonie.


Cartes FXO : cartes de ligne analogique (branché sur le port ATA du routeur par exemple)
Cartes PRI : primaires : 30 canaux ISDN (possibilité de mettre des modules médias EIP)
Cartes BRI-T : raccordement de base ISDN

Cartes FXS : cartes terminales analogique (a partir de 16, rappatrié sur un panel en plus)
Cartes DSI : numérique propriétaire Mitel par exemple
Cartes BR-S 
Cartes BRI-S

Cartes DSP
Cartes EIP : Si besoin de plus de ressources
Cartes TAX : taxation, peu répamndu

Cartes d'extensions pour ventilations, PSU 48V, alimentation redondante.


Gestion FAX, seulement sur CPU 2


Aujourd'hui, de moins en moins de PBX physiques tels que Mitel, Siemens ou autres sont installés chez le client.
Ces systèmes restent cependant maintenus bien que nous passons à des solutions virtualisées plus légères, rapides et simples à mettre en place.


Chez 3CX, il est toujours possible d'intégrer des postes analogiques, il faudra seulement acheter un ATA à part (ici `Grandstream HT802 <https://www.grandstream.com/products/gateways-and-atas/analog-telephone-adaptors/product/ht802>`_)

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/HT802.jpg


- Enregistrer MAC address dans la section FXS/DECT de 3CX
- Attribuer une extension à 1 des ports FXS

    .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/ht802-extension.png


- Enregistrer le fichier de config XML et l'injecter dans l'HT802 via la web interface.

    .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/ht802-web-provision.png






Il existe aussi des appliances intégrant directement des ports FXS, permettant donc une simplicité de déploiement pour les terminaux analogiques. (`NX64 AiO <https://www.call4tel.com/voip-gateways/aio-nx64/>`_)

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/AiO.png



Mandat 2
-------------

Rechercher si cette fonctionnalité est disponible sur votre système de téléphonie et si 
elle nécessite une licence particulière. Procéder à l’installation et la configuration de cette 
fonctionnalité.



Flexibilité des postes de travail (terminaux en mode enregistrement)


Chez 3CX : Hotdesking

Les terminaux sont gérés sur cette interface car non attriubé à une extension spécifique

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/hotdesking.png





Il faut cependant attribuer les droits de hotdesking aux utilisateurs


Dans :menuselection:`Utilisateurs  --> <user> --> Options --> onglet "options"`.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/hotdesking-user.png






"*77*200* puis -> XXXX#" (pin de la messagerie vocale) pour activer le hotdesking de l'utilisateur.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/secure-pin-user.png





.. admonition:: Cas concret

    En voulant paramétrer un Yealink T46G, nous nou ssommes rendus compte qu'il était déjà enregistré auprès du RSP de Swisscom.
    Nous avons donc du le supprimer du RPS en question.

    Pour cela nous sommes passés par l'interface Yealink et non Swisscom, pour plus de simplicité et de réactivité.
    Il faut cependant un compte partenaire Yealink, la MAC address ainsi que le S/N, et un RPS déjà configuré chez Yealink.

    Après cette étape, nous avons voulu metre à jour le firmware, ce qui ne s'est pas passé comme prévu.
    Étant donné que le firmware était très ancien, il a fallu passer par plusieurs mises à jours intermédiaires pour y arriver.

    Suite à une mise à jour vers une version un peu plus récente, nous pouvons faire la dernière firmware update depuis le 3CX

    .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/update-firmware-3cx.png
 




Mandat 3
------------

Afin de reprendre les bases de comment fonctionne un sytème DECT, je vous invite à vous rediriger vers la `section DECT de la documentation M362 <https://docs-cfc.readthedocs.io/fr/latest/Documentation-M362.html#dect-digital-enhanced-cordless-telecommunications>`_.



3 types de DECT :

- Système sans fil propriétaire ou non-propriétaire avec connexion de type analogique ou numérique : 

Connexion au moyen de **câbles téléphoniques avec 2, 4 ou 6 brins.** 

Cette possibilité permet de gérer **4, 8 voire 12 communications simultanées** par base DECT (grâce au codec G726). 

Cette solution nécessite parfois des licences et du matériel complémentaires (carte d’extensions 
numériques, carte processeurs DSP, …). 
Une planification et une installation rigoureuse doit être faite. 

Les fournisseurs mettent parfois à disposition un kit de mesures qui permet de définir précisément l’emplacement des bases DECT. 
Des recommandations en ce sens sont généralement fournies par le constructeur. Standalone ou ....

- Système sans fil SIP : connexion au moyen de l’infrastructure informatique du client final. 
Cette variante nécessite généralement des switches avec alimentation PoE. Il faut donc 
vérifier que le budget PoE à disposition par switch est suffisant. De plus, certaines solutions 
doivent se synchroniser au moyen du réseau Ethernet, ce qui **nécessite l’utilisation du 
protocole PTP (Precision Time Protocol)** mais qui nécessitent des **switchs compatibles et très coûteux**. 
Certains systèmes requièrent l’installation d’un contrôleur (ou manager DECT) qui sera en 
lien avec le système de téléphonie d’un côté et, de l’autre, en lien avec toutes les bases 
DECT. Une planification et une installation rigoureuse doit être faite. 
Les fournisseurs mettent parfois à disposition un kit de mesures qui permet de définir précisément 
l’emplacement des bases DECT (pour un site survey).
Des recommandations en ce sens sont généralement fournies par le constructeur

SIP DECT - Il faut que les antennes se voient pour le roaming et échanges d'informations

2 brins : 2 communications en G711 (64kbit/s)
          4 communications en G726 (32Kbit/s) 


  Les bases DECT sont réparties en deux familles : 

- Monocell (monocellulaire) : Il s’agit d’un système avec une base unique pouvant gérer entre 
6 à 10 terminaux sans fil. Elle peut être de type propriétaire, non-propriétaire ou SIP. Il est 
également possible d’augmenter la couverture du signal DECT en utilisant des répéteurs 
(Repeater). Ces derniers occupent alors chacun une place d’un terminal DECT. Plus nous 
ajoutons de répéteur, moins il est possible de configurer de terminaux DECT.
Ex : Base Yealink W70B, Repeater Yealink RT30

- Multicell (multicellulaire) : Il s’agit d’un système avec un contrôleur DECT et plusieurs bases 
DECT permettant de couvrir une zone beaucoup plus grande. L’utilisateur peut, au moyen de 
la fonctionnalité Handover, se déplacer de base en base sans interruption du signal DECT et 
donc, de la communication. Ce système est beaucoup plus complexe à mettre en service et 
doit respecter toutes les indications fournies par le constructeur. La limite du nombre de 
terminaux se situe entre 200 et 250. En fonction de l’installation, plusieurs contrôleurs de 
site peuvent être utilisés en lien avec un ‘’super contrôleur’’. Chaque système ayant ses 
particularités, il est nécessaire de lire attentivement les recommandations avant de procéder    


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/w90-system.png



Selon le lien de `compatibilité 3CX <https://www.3cx.fr/sip-phones/>`_, les systèmes DECT compatibles sont les suivants :

- Yealink
- Snom
- Gigaset (avec limitations)



Pour configurer une antenne DECT, cela se passe de la même manière que pour enregistrer un ATA, c'est à dire dans la section "Avancés" -> "FXS/DECT"

Il faut par la suite choisir le modèle et enregistrer l'adresse MAC.
Dans l'onglet "Extensions" il faut choisir l'utilisateur que l'on veut attribuer au DECT.


Analysons désormais le flux SIP et RTP entre les deux terminaux.

Sur la première capture prise depuis le PBX, nous pouvons voir que seul le flux SIP apparaît.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/pcap-pbx-dect-to-t46.png




Cela veut donc dire que le flux RTP passe lui en direct du DECT vers le T46G.


Nous le voyons très bien ci-desous avec la capture du T46 lui-même :


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/pcap-t46-dect-to-t46.png


Si cependant nous souhaitons que le flux RTP passe par le PBX, il faut activer ce paramètre dans : "Utilisateurs" -> <user> -> Options -> Dépannage -> "Le PBX délivre l'audio"

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/pbx-audio.png



Template personalisé :

.. warning::
    Ne jamais modifier un template par défaut !
    Il faut le dupliquer et en créer un nouveau à partir du duplicata.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/custom-template-hotdesking.png


Si nous voulons changer l'ordre des codecs chargés par défaut, cela est possible.
Souvent, il suffit de glisser nos options préférées en premières afin que le système les charge par défaut.

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/custom-template-codecs.png






.. tip::
    Tip Yealink ; pour afficher l'écran d'un poste yealink sur votre pc, il est possible de le faire via le web avec cette url : `https://<ip>/screencapture`



    .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/yealink-screencapture.png



Mandat 4
----------

Les intégrations de systèmes de contacts peuvent être intéressantes pour faciliter la recherche de numéros aux collaborateurs.
Cela permet aussi de centraliser la gestion du carnet d'adresses.

Chez 3CX, plusieurs intégrations sont possibles :

liste...


Ici nous nous intéresserons à telsearch, qui est gratuit jusqu'à 1'000 recherches par mois.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M391/integration-crm.png

Ici, nous utiliserons une template pré-faite disponible avec ce lien de téléchargement :download:`source/other/TelsearchCRM-template.xml`

Il faut remplacer 


Mandat 6
----------------

Mandat 7
-----------


Sauvegarde et restauration d'une configuration 3CX


Backup SFTP sur Nas Synology DS220+.

Utilisateur spécifique : 3cx

Autorisation seulement sur le dossier partagé en question
Autorisation seulement pour le protocole SFTP
Mot de passe fort
Pas de chiffrement de la config, infra non critique


sftp://<ip>/<folder> sur 3cx avec user-mdp
port par défaut : 22
backup manuel, successful

