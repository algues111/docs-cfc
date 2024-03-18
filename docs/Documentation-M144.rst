==============
Module 144 : Réseaux sans-fil (en travaux)
==============

Introduction
------------

La première leçon du module était une introduction à ce dernier. Elle nous a permis de tester nos connaissances sur diverses technologies sans-fil afin de nous mettre en bouche les prochaines leçons qui suivront.

Durant la première année, lors du module M145, nous avions déjà eu la chance d’étudier les différentes caractéristiques du Wi-Fi, notamment :

- Ses topologies
- Ses normes
- Son évolution dans le temps
- Les mécanismes d’association et de transfert des données
- Sa sécurité
- Ses avantages
- Ses inconvénients

Le Wi-Fi est donc une technologie qui ne nous est pas inconnue, bien que nous l’ayons plus ou moins survolée.

C’est ici que le module M144 intervient ; pour rentrer en profondeur dans cette technologie qui nous entoure quotidiennement.

Ici, quelques QCM disponibles sur eitswiss.cockpitprofessionnel.ch concernant les technologies sans-fil

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M144/qcm-1.png
   :align: center


Semaine 2
-----------

Introduction
^^^^^^^^^^^^

Voici la liste des sujets abordés durant la semaine 2 :

- La fréquence 
- La bande passante 
- Le débit binaire 
- Les différents types de modulations ( 5 )
- Étalement de spectre ( 6 ) 
- Multiplexage ( 7 )

	OFDM
	FHSS
	DSSS
	Les normes 802.11

Fréquence
^^^^^^^^^^^^

Qu’est-ce que la fréquence (Hz) ?

- La fréquence (Hz) est le nombre de périodes (oscillations) qui se répète en une période de temps t.

Comment la calcule-t-on ?

f=  1/(t (en s))

Un exemple concret et graphique :

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M144/sinus-1.png
   :align: center

Bande passante
^^^^^^^^^^^^

La bande passante représente la bande de fréquence dans laquelle peuvent passer les données.

Nous pouvons faire une analogie avec une autoroute qui a tant de voies pour faire passer tant de voitures.

Attention : La bande passante est à ne pas confondre avec le débit, bien que les deux aient un lien :

- Une bande passante élevée ne garantit pas nécessairement un débit élevé, tandis qu'un débit élevé est toujours le résultat d'une bande passante élevée.

Débit binaire
^^^^^^^^^^^^

Le débit binaire, souvent simplement appelé "débit," est la mesure de la quantité d'informations numériques (bits) transmises ou traitées par unité de temps, généralement en bits par seconde (bps).

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M144/speedtest.jpg
   :align: center

Modulation
^^^^^^^^^^^^

Qu’est-ce que la modulation ?

La modulation est le processus de modification d’une onde porteuse afin qu’elle puisse porter des informations (data, voix…), sur un canal de communication.

Y a-t-il plusieurs types de modulation existants dans le monde des télécommunications ? 

Oui, les voici :

- Modulation d’amplitude (AM)

    La modulation d’amplitude consiste à moduler l’amplitude d’un signal porteur.
    Exemple concret ci-dessous :

    .. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/M144/am.png
        :align: center

- Modulation de fréquence (FM)
- Modulation de phase (PM)

Normes 802.11
^^^^^^^^^^^^

La norme 802.11 est une série de normes qui spécifient les protocoles de communication sans fil pour les réseaux locaux (Wi-Fi). Ces normes ont été développées par l’IEEE, un organisme de normalisation international. La famille de normes 802.11 définit les spécifications techniques pour les réseaux sans fil, notamment les fréquences, les débits de données, les protocoles de sécurité, etc.

Les normes 802.11 ont évolué au fil du temps pour s’améliorer et permettre :
- Des débits plus élevés
- Plus de fiabilité
- Plus de sécurité
- Plus de bande de fréquences

Certaines des versions les plus couramment connues de la norme 802.11 incluent :
- 802.11a
- 802.11b 
- 802.11g 
- 802.11n
- 802.11ac 
- 802.11ax 
- 802.11ay


Semaine 3
------------

Introduction
^^^^^^^^^^^^

Voici les différents sujets abordés lors de la 3ème semaine de cours sur le module M144 :

- Tableau comparatif des technologies sans fil (suite)
- Le roaming
- Organismes de normalisation
- La trame 802.11
- Les topologies
- Étalement de spectre ( 6 ) 
- Multiplexage ( 7 )

Le roaming
^^^^^^^^^^^^

Il est possible d’exploiter deux points d’accès (AP1 et AP2) avec des zones de couverture différentes mais le même SSID et le même réseau W-LAN. Ces deux AP sont câblés avec le même switch. Si un terminal actuellement connecté au point d’accès AP1 via le SSID « Edu_WLAN1 » est déplacé en direction du point d’accès AP2, le signal du point d’accès AP1 s’affaiblit soudainement et celui du point d’accès AP2 s’intensifie. Le terminal se connecte désormais presque de manière ininterrompue à AP2. Ce procédé est appelé roaming. L’utilisateur n’est au courant de rien. Idéalement, AP1 et AP2 (et éventuellement d’autres AP) ont une plage qui se chevauche. La répartition roaming convient aux zones de couverture plus grandes, telles que dans des moyennes et grandes entreprises ou dans des écoles.

Trame 802.11
^^^^^^^^^^^^
Afin de pouvoir comprendre de quoi est composé une trame 802.11, il est intéressant de se pencher sur la trame Ethernet II (802.3), ces dernières ayant, non seulement, beaucoup de similitudes, mais aussi, plusieurs différences conséquentes telles que :

- La différence de taille :
  - 802.3 : 1542 octets
  - 802.11 : 2312 octets

- La méthode d’accès au média :
  - 802.3 : CSMA-CD
  - 802.11 : CSMA-CA   

Topologies & Environnement
^^^^^^^^^^^^

Différentes topologies existent pour les réseaux sans-fil, ces dernières permettant une flexibilité dans l’adaptation des besoins des clients.

IBSS :
  
BSS :

ESS :

SOHO :

Il s’agit ici d’un routeur W-LAN usuel. C’est un appareil très performant, qui intègre certains niveaux de fonction et qui se trouve dans pratiquement tous les foyers et/ou petits bureau (small office). Ce routeur W-LAN intègre un switch, un modem Internet (DSL, câble, 4G, 5G), un serveur DHCP, un pare-feu et un point d’accès pour la connexion sans fil. L’un des représentants les plus populaires de cette catégorie est la « Fritzbox ». Le routeur W-LAN est un ESS en lui-même.

Cependant, il est important de notifier que l’usage de répéteur afin d’augmenter la couverture de votre W-LAN est possible.

Mais attention car l’usage d’un seul répéteur permet de garder un débit élevé car il dirige le signal vers un autre canal, mais tout autre répéteur ajouté divisera le débit par 2.

C’est donc une solution de dernier recours si rien d’autre est possible.

Nous allons maintenant nous intéressons à l’environnement entourant notre AP et pouvant éventuellement causer des perturbations ou des atténuations sur nos signaux.

Avant toute chose, il est important de comparer les fréquences utilisées pour la technologie 802.11.

Mandat pratique 30.3.5
^^^^^^^^^^^^

Quelques questions du cockpit :

Mandat pratique IBSS
^^^^^^^^^^^^

Afin de comprendre dans quels domaines d’applications nous pouvons utiliser la topologie IBSS, il nous a été demandé de réaliser un partage de fichier soit :

- Par AirDrop (technologie Apple)
- Par Wifi Direct (disponible sur les smartphones sous Android)

Ayant un iPhone, j’ai décidé de compléter le mandat en utilisant AirDrop :
