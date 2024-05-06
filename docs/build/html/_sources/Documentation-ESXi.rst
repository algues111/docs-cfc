==============
Documentation ESXi
==============


Upgrade 6.7 -> 8.0.2B (sur DL380 Gen9)
=======================================

Phase 1 : Préparation
------------------------

https://www.stephenwagner.com/2023/07/24/esxi-8-0-hpe-proliant-dl360p-gen8/

Préparer des backups des différentes VMs tournant sur l'esxi au préalable.
(Stockage > Datastore > Télécharger les dossiers de chaque VM ou via VEEAM)

Accéder à l'ESXi, activer le mode maintenance et SSH

.. image:: https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/images/ESXi/1-entrer-en-mode-maintenance.webp

Télécharger dans le datastore votre nouveau bundle de VIBs pour ESXi 8.0.2B (ici HPE)
Telecharger l'iso complet de esxi 8.0.2 via le lien donné (soit le ALL soit custom, ici HPE)


Créer une clé bootable de l'iso
Insérer la clé dans l'esxi
F11 au boot
Selectionner Generic USB
Attendre le boot
Accepter l'installation d'ESXi 8
Choisir le bon support de stockage
Selectionner Upgrade OU installer ESXI8 si vous voulez réinstaller le tout

Erreur : conflits de VIBs ou checksum invalide etc...
Désinstaller les VIBs conflicutels et invalides de la manière suivante :

- rebooter l'esxi normalement
- y accéder via ssh
liste des commandes :


esxcli software vib list  
esxcli software remove -n <vib-name>

then install the new bundle

esxcli software vib install -d /vmfs/volumes/datastore-name/folder-name/HPE-801.0.0.11.3.1.1-Jun2023-Addon-depot.zip -f

The parameter -f is not always necessary, but it does when you dont have the AcceptanceLevel "Community"

https://github.com/lamw/ghettoVCB/issues/64

esxcli software acceptance set –level=CommunitySupported

https://www.vladan.fr/how-to-understand-vmware-acceptance-levels-for-hosts-and-vibs/

Reessayer commande install

Desormais, un retour de commande expliquant que les paquets VIBs ont été installé avec succès apparaitra.

Reboot la machine

certificat openssl defaillant ;

recréer un :

https://blogs.vmware.com/cloud-foundation/2020/04/14/replacing-vmware-esxi-ssl-certificate-in-vmware-cloud-foundation/

Licences :

https://gist.github.com/ayebrian/646775424393c9a35fb8257f44df1c8b

Installation VCenter Server

Télécharger iso correspondant à la version de l'ESXi (ici 8)

.. warning::

Vérifier le checksum.
Si ce dernier n'est pas bon, votre installation plantera à 19% en indiquant une erreur de connection réseau.