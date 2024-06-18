<<<<<<< HEAD
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

Mandat 4 
^^^^^^^^^^^^

Lors d’un exercice avec appel VoIP, essaie d’identifier les différents protocoles et codecs énoncés ci-dessous au moyen de l’analyseur Wireshark. 

.. note::

    Pour cette partie du mandat, je vous invite à vous dirigier vers la section `des codecs audio de la Documentation-M362 <https://docs-cfc.readthedocs.io/fr/latest/Documentation-M362.html#codecs-audio>`_.

Quelles constatations peux-tu faire en changeant de codec par exemple. 

Enregistre une trace d’un appel SIP et recherche les différents protocoles utilisés (SIP, SDP, RTP, RSTP, type de codecs, etc.). 

Documente l’ensemble de tes tests.


Configure des téléphones de manière simple en utilisant les informations fournies par l’enseignant.


Mandat 5 
^^^^^^^^^^^^


reprend l’opérateur choisi précédemment et liste les différentes variantes possibles pour
les interconnexions VoIP. Pour quelles variantes aura-t-on besoin d’une appliance de type SBC ? A
quoi sert cette appliance ?


Mandat 6 
^^^^^^^^^^^^


Fais un tableau en listant les principales caractéristiques de ces différentes plateformes
Cloud. Laquelle te semble la plus adaptée pour l’installation de ton système de téléphonie ? Quelles
sont les avantages et inconvénients d’une installation sur une plateforme Cloud par rapport à une
installation On Premise (Sécurité, équipements, itinérance, interfaces, etc.) ?


Mandat 7
^^^^^^^^^^^^^^

Choisis un des fournisseurs proposés, crée un compte sur la plateforme Cloud et procède
à l’installation de ta première machine virtuelle. Il est aussi possible de procéder à l’installation d’un
hyperviseur. Suis les procédures fournies par le fournisseur. Etablis un rapport de cette première
installation.


Mandat 8 
^^^^^^^^^^^^^^

Choisis une solution de central téléphonique virtuel et procède à son installation sur une
plateforme d’hébergement Cloud ou sur un hyperviseur. Etablis un rapport de cette première
=======
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

Mandat 4 
^^^^^^^^^^^^

Lors d’un exercice avec appel VoIP, essaie d’identifier les différents protocoles et codecs énoncés ci-dessous au moyen de l’analyseur Wireshark. 

.. note::

    Pour cette partie du mandat, je vous invite à vous dirigier vers la section `des codecs audio de la Documentation-M362 <https://docs-cfc.readthedocs.io/fr/latest/Documentation-M362.html#codecs-audio>`_.

Quelles constatations peux-tu faire en changeant de codec par exemple. 

Enregistre une trace d’un appel SIP et recherche les différents protocoles utilisés (SIP, SDP, RTP, RSTP, type de codecs, etc.). 

Documente l’ensemble de tes tests.


Configure des téléphones de manière simple en utilisant les informations fournies par l’enseignant.


Mandat 5 
^^^^^^^^^^^^


reprend l’opérateur choisi précédemment et liste les différentes variantes possibles pour
les interconnexions VoIP. Pour quelles variantes aura-t-on besoin d’une appliance de type SBC ? A
quoi sert cette appliance ?


Mandat 6 
^^^^^^^^^^^^


Fais un tableau en listant les principales caractéristiques de ces différentes plateformes
Cloud. Laquelle te semble la plus adaptée pour l’installation de ton système de téléphonie ? Quelles
sont les avantages et inconvénients d’une installation sur une plateforme Cloud par rapport à une
installation On Premise (Sécurité, équipements, itinérance, interfaces, etc.) ?


Mandat 7
^^^^^^^^^^^^^^

Choisis un des fournisseurs proposés, crée un compte sur la plateforme Cloud et procède
à l’installation de ta première machine virtuelle. Il est aussi possible de procéder à l’installation d’un
hyperviseur. Suis les procédures fournies par le fournisseur. Etablis un rapport de cette première
installation.


Mandat 8 
^^^^^^^^^^^^^^

Choisis une solution de central téléphonique virtuel et procède à son installation sur une
plateforme d’hébergement Cloud ou sur un hyperviseur. Etablis un rapport de cette première
>>>>>>> 7696c50 (test)
installation.