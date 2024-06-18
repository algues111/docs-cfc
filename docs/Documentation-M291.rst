===============================
Module 291 : PBX Virtualisé
===============================



Jour 1
========

Ce jour est destiné à introduire la matière que nous verrons lors des prochains cours du module M291.

Voici le fichier d'introduction téléchargeable ci-dessous :

:download: `source/other/Module_391_Intro_FR.pdf`


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

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/vtx-internet.png



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

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/forfait-min.png




Mandat 3 
^^^^^^^^^^^^

Reprends l’opérateur choisi précédemment et liste les différentes possibilités d’abonnements pour les services VoIP.

Comme présenté dans le mandat n°2, voici les 3 solutions de téléphonies phares de VTX :

- Trunk (analogique, IP, vPBX)
- Solution de téléphonie SIP
- Solution Microsoft Teams


Trunk
~~~~~~~~~~~~~~


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/vtx-trunk-list.png


.. important::

    Pour tout trunk, les `tarifs à la minute s'appliquent <https://www.vtx.ch/zone1/>`_.

    Si toutefois vous pensez que les collaborateurs appelleront.....

    .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/illimite-vtx.png

    

.. tabs::
   .. tab:: Analogique
      
        VTX propose des trunks analogiques, de 4 à 30 canaux en simultanés (jusqu'à 120 canaux sous devis) avec la location du matériel incluse.
        
        .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/vtx-trunk-analogique.png


   .. tab:: SIP-IP

        En plus des trunks analogiques, VTX vend des trunks SIP, de 4 à 60 canaux en simultanés (jusqu'à 200 canaux sous devis) que vous pouvez gérer via une interface web.

        .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/vtx-trunk-analogique.png

        
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

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/sip-g711-completed.png

Ce graphique comporte les informations suivantes :

.. tabs::

    .. tab::

      - Invitation SDP : négocie la teneur des données transférées (audio, vidéo, texte, message, application, etc.), ainsi que le format et le protocole de transport utilisés, et le port RTP.

      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/sdp-g711.png

      .. note::
          Le Type-101 spécifié dans les codecs audio correspond aux touches DTMF.


    .. tab::


      - Flux RTP : envoie de paquets audio à travers ce protocole, ports aléatoires décidés dans 

    .. tab::

      - Contrôle du flux RTP via RTCP
        
      .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/rtcp-g711.png


Documente l’ensemble de tes tests.

Si nous décidons cependant de choisir 2 codecs différents sur 2 terminaux distincts, et que ces derniers communiquent via un flux RTP direct, l'initiation de l'appel échouera.

Nous pouvons le voir ci-dessous dans le graphique :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/sip-g722-g711-rejected.png




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

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/ovh-vps-tarifs.png




Ici, nous prendrons le VPS "VLE-2" possédant 2 coeurs virtuels, 2Go de RAM, 40GB de stockage en NVME ainsi qu'une bande passante de 500Mbit/s.

Nous choisissons aussi l'OS, qui sera ici Ubuntu 24LTS !!

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/ovh-paiement.png




OVH propose d'ajouter des options à votre serveur VPS, telles que des backups automatisées, des snapshots, ou bien du stockage supplémentaire.


.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/ovh-options.png




Après avoir choisi les options souhaitées, il suffit de passer au paiement et vous obtiendrez un recu de votre commande ainsi qu'un accès à votre nouveau VPS !

Voici le dashboard de gestion du VPS :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M291/ovh-options.png

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





Question Bonus du jour :
^^^^^^^^^^^^^^^^^^^^^^^^^^^^



Est-il possible d'avoir un trunk SIP Swisscom sur un 3CX installé dans le cloud ?

réponse :

Non, pas avec le SBC

Oui avec Enterprise SIP Cloud

https://documents.swisscom.com/product/filestore/lib/047dea54-3e19-43b0-a36e-9eed5af4f3b8/enterprise_sip_cloud_factsheet-fr.pdf?idxme=pex-search