.. role:: raw-html-m2r(raw)
   :format: html


Module 362 : Mettre en service les systèmes vocaux et vidéo complexes
=====================================================================



:raw-html-m2r:`<img src="https://upload.wikimedia.org/wikipedia/commons/a/a2/3CX_Logo_-_Wiki.png" align="right" height="32px" />`

3CX
----------

Qu'est-ce que 3CX ?
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

3CX est une **solution de communications virtuelle** qui permet aux entreprises de gérer leurs appels téléphoniques, leur messagerie instantanée, leur vidéoconférence ainsi que tous les services que pourrait proposer un PBX classique, grâce à différentes installations et forfaits.

12 millions d'utilisateurs l'utilisent chaque jour, le placant donc sans souci sur le podium des leaders mondiaux de la téléphonie !

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-paccueil.png" align="center"/>`

----

Licences
^^^^^^^^^^^^^^^^^^^^

Pour avoir une vue d'ensemble plus concrète de ce que propose 3CX en tant que service ou système, il est important de connaître les différentes licences proposées par l'entreprise du même nom.

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-licences.png" align="center"/>`

----

Différents types d'installation
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

:raw-html-m2r:`<br>`

:raw-html-m2r:`<img src="https://imgs.search.brave.com/t5Gh4h12EKJUKsBYlQEidsH_O2SyxBPQABqSv3rnPxU/rs:fit:860:0:0/g:ce/aHR0cHM6Ly9icmFu/ZHNsb2dvcy5jb20v/d3AtY29udGVudC91/cGxvYWRzL2ltYWdl/cy9kZWJpYW4tbG9n/by5wbmc" align="right" height="32px" />`

Linux
~~~~~~~~~~~~~~

:raw-html-m2r:`<br>`

Chez 3CX, le principal avantage de leur système est leur **OS basé sur Debian** qui est **optimisé pour leur PBX virtuel.**

L'installation s'avère simple si l'on est familiarisé avec le milieu de la virtualisation sous linux.

:raw-html-m2r:`<u>Voici les prérequis matériels pour l'installation de 3CX sur Debian : </u>`

**Votre machine a besoin d'au moins 1 cœur de processeur dédié et de 2Go de RAM. Si vous hébergez vous-même votre machine et que votre hébergeur utilise une unité centrale partagée, vous avez besoin de 2 cœurs !**

Passez en revue les spécifications matérielles suggérées afin d'allouer du temps d'unité centrale et des ressources de mémoire vive supplémentaires en fonction des critères suivants :


* Nombre d'appels simultanés gérés par le système.
* Nombre d'utilisateurs actifs - 100 sessions actives du client Web sont plus exigeantes que 100 appels occasionnels via des téléphones IP.
* L'utilisation de l'enregistrement des appels - le système est sollicité pour le mixage audio et le stockage des fichiers.

..

   3CX peut être installé sur n'importe quel système fonctionnant sous Debian 12. Si vous souhaitez faire une installation barebone, assurez-vous que le matériel fonctionne avec Debian 12 et que le fournisseur du matériel vous aidera en cas de problème. Nous ne pouvons pas vous aider à résoudre les problèmes liés à l'installation de Debian 10 sur du matériel " barebone ".

   Ne configurez pas de réseau virtuel, d'interface VPN ou d'option TeamViewer VPN sur l'hôte 3CX.


Pour les autres prérequis liés à la virtualisation, au réseau etc... Je vous invite à vous référer à leur documentation complète disponible avec le lien ci-dessous :

**https://www.3cx.fr/docs/manuel/installation-debian-linux-ipbx/**

Voici aussi le lien pour le téléchargement de l'iso linux de 3CX :

**https://downloads-global.3cx.com/downloads/debian10iso/debian-amd64-netinst-3cx.iso**

:raw-html-m2r:`<img src="https://lh7-us.googleusercontent.com/dnv4yC4v_g33UFLJcYGuXi3QmSsWkMeu_Iir9wF8EmmyCZTKqkXkgFiIYQfmL_WMYjxXJoSGsAFnsz2kkg3GRqR_GmU9pxCSW8YbKFS63S5mnrrJkDrqopNUzxvNp9oaYDly7gzf0vpt7Ug" style="display: block; margin: 0 auto;" />`

*Premier lancement de l'iso de 3CX*

Choisissez ce que vous préférez en fonction de vos habitudes d'installation de distributions Linux.

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-linux.png" style="display: block; margin: 0 auto;" height="470px"/>`

*Attendre que l'installation s'effectue et choisir les options correspondantes à vos besoins (FQDN...)*

----

:raw-html-m2r:`<br>`

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-CLI.png" style="display: block; margin: 0 auto;" />`

Lorsque votre VM aura redémarré et que vous aurez cette interface de disponible, je vous conseille d'installer 3CX avec votre navigateur web comme support visuel.

:raw-html-m2r:`<br>`

..

   L'installation en CLI étant réservée aux utilisateurs aguerris de 3CX, je ne le vous recommanderais seulement si vous nécessitez de paramètres spéciaux/avancés.


:raw-html-m2r:`<br>`

:raw-html-m2r:`<img src=".\images\conf-3cx1.png" />`

:raw-html-m2r:`<u>Ici, 3 options sont disponibles : </u>`


* *Upload a new configuration file create on 3CX*
* *Restore a backup*
* *Install without config file (legacy, not recommended)*

Nous utiliserons la 3ème option pour cette installation.

:raw-html-m2r:`<br>`

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/conf-3cx2.png"/>`

:raw-html-m2r:`<br>`

Cette étape nous permet de configurer les différents ports utilisés par les services de 3CX.

..

   Si seulement votre instance 3CX tourne sur votre VM, je vous conseille de laiser les ports par défaut proposer par le wizard d'installation.

   Dans le cas contraire, utilisez des ports qui ne sont pas utilisés par d'autres services!


----

:raw-html-m2r:`<img src="https://upload.wikimedia.org/wikipedia/commons/2/2a/Windows_Logo_2012-2015.png" align="right" height="32px" />`

Windows
~~~~~~~

Il est aussi possible d'héberger votre PBX 3CX sous l'OS Windows.

:warning: **DISCLAIMER** :warning:

Cependant, cela nécessitera des connaissances avancées, car vous vous retrouverez face à des contraintes plus récurrentes que sur Linux.

Par exemple, lors des MàJ Windows, il est possible que l'état du Firewall Windows Defender se réinitialise et donc efface les règles de traffics entrants/sortants permettant au 3CX et aux téléphones liés de fonctionner correctement.

De plus, Windows est par défaut plus vulnérable que Linux, de par son architecture et car il est l'OS le plus répandu !

Lorsque l'installation est terminée, on peut remarquer dans le fichier hosts de notre OS Windows que 3CX a rajouté cette ligne :

  ``127.0.0.1 arthur.3cx.ch``

Cette dernière permet, lorsque nous tapons l'URL en question dans notre navigateur, que notre ordinateur pointe vers notre adresse loopback.

Attention, cela se produit seulement si ... config préalable dns non

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-hosts.png" />`

----

Interface
^^^^^^^^^^^^^^^^^^^^^^

Après avoir terminé la configuration du 3CX, vous pourrez accéder à l'URL correspondante à l'installation de votre 3CX (\ *ici arthur.3cx.ch:5001*\ ), et ainsi vous logger avec les identifiants administrateur précédemment choisis.

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/3cx-login.png" />`

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/dashboard.png" />`

Après s'être identifiés, nous débarquons sur l'interface admin.

----

Exercice 1
^^^^^^^^^^^^^^^^^

Demande
~~~~~~~~~~~~~~~~~~~

**Exercice 1: Création d’un numéro d’assistance**

L’accessibilité téléphonique du service clientèle de Cardinal Bier Import AG doit être améliorée. À l’heure actuelle, le numéro principal n’est desservi que par une seule personne. Récemment, une application de Customer Releationship Management a été installée. Désormais, les commandes, réclamations ou autres demandes des clients sont enregistrées électroniquement. Une équipe de 4 collaboratrices a été formée. La répartition des appels au sein de cette équipe doit être définie. Créez une solution de téléphonie pour le service clientèle de Cardinal Bier Import AG. Vous disposez d’une instance vPBX de Peoplefone ou d’autres installations. Lisez les exigences de l’entreprise et établissez une configuration.

**Besoins en téléphonie du service clientèle**

:raw-html-m2r:`<u>Exigences auxquelles doit satisfaire le numéro principal:</u>`


* Horaires d’ouverture du lundi au vendredi de 8h00 à 18h00 et le samedi de 8h00 à 17h00
* Saisie de tous les jours fériés catholiques légaux pour le site de Fribourg, pour les 12 prochains mois.
* IVR pour allemand, français et anglais en amont

Formez des groupes pertinents. Les appels doivent être répartis de manière séquentielle au sein du groupe. Il doit y avoir passage d’un groupe à un autre, si personne ne répond ou si la ligne est occupée. L’appel passera sur messagerie et signalera qu’aucun collaborateur n’est libre, seulement aucune personne ne répond. Les équipes parlant les langues officielles du canton reçoivent un numéro d’appel externe et les collaboratrices peuvent passer des appels externes sur lle téléphone IP avec ce numéro ou avec le numéro principal.

Les textes de message suivants peuvent être repris dans le fichier ZIP ou vous pouvez en enregistrer vous-même:


* HPN_AB_FeiertagFerien.wav
* HPN_AB_keinMitarbeiterFrei.wav
* HPN_AB_Oefffnungszeiten.wav
* IVR_Ansage.wav

Fichiers WAV
Le texte parlé des fichiers WAV ne doit pas correspondre à 100% à la problématique de cet exercice.
Les utilisateurs suivants doivent être enregistrés:


* Meier Anna, parle allemand, français
* Müller Janine, parle allemand, anglais
* Angeloz Marie, parle français
* Ducrest Sophie, parle français, anglais

Mission par groupe de 2 ou 4:


* Tracez le Call Flow pour le numéro principal (modèles disponibles dans le chapitre 10 du module 361)
* Configurez l’installation en fonction des exigences

Testez l’installation et consignez les tests dans un protocole

Workflow :
~~~~~~~~~~~~~~~~~~~~~~

La chose la plus importante à faire dans un exercice tel quel, est de dessiner un schéma de principe très simple, à la main de préférence.

Cela permet de visualiser au mieux la demande et de pouvoir poser des questions au client si les indications ne sont pas claires !

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/sch%C3%A9ma-ex1.png" />`

La demande est désormais plus compréhensible, nous allons donc maintenant procéder à la configuration de notre PBX virtuel !

Commencons par les utilisateurs :

:raw-html-m2r:`<u> Disclaimer : Pour l'exercice, seuls 2 téléphones IP Yealink étaient à disposition ; ils seront configurés pour les utilisateurs 100 et 101. </u>`

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/users1.png" />`

Configuration Janine :

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/janine.png" />`

Les champs obligatoires à remplir lors de la création de l'utilisateur sont les suivants :


* Extension
* Prénom
* Nom
* Adresse Mail

----

Exigences réseau
^^^^^^^^^^^^^^^^^
**Latence**

La durée d’exécution des paquets vocaux est un critère essentiel pour la qualité vocale. On s’intéresse ici au délai total entre la parole de l’émetteur et l’écoute du récepteur (délai de bout en bout).




----


Exercice 2
^^^^^^^^^^^^^^^^^

:raw-html-m2r:`<u> 1. NAT / PAT avec installation app natel externe </u>`
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

Workflow de l'exercice :

Dépannage 3CX

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/depannage-3cx.png" />`

Vous avez la possibilité à travers ce menu de définir si oui ou non le serveur 3CX agit en tant qu'intermédiaire pour les appels.
Ici, cela nous sera utile afin de nous simplifier la tâche, au lieu de configurer un port de mirroring sur le switch.

:raw-html-m2r:`<u> 2. 1 App + 1 Webclient en interne avec Wireshark </u>`
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

:raw-html-m2r:`<u> 3. 2 Téléphones SIP avec Wireshark (comparaison G711/G722/G729 ) </u>`
~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

G711
********

Les caractéristiques du codec G.711 sont les suivantes :

- Bande de fréquences : 300-3400Hz
- Fréquence d’achantillonnage de 8 khz
- Débit fixe de 64 kbits/s (échantillons de 8 bits x 8 kHz)
- Délai de compression de 0,125 ms (sans aucun délai d’anticipation)

MOS :

- Mesure de qualité en conditions idéales : MOS 4,45 en G.711 Loi-µ et 4,45 en G.711 Loi-A
- Mesure de qualité en condition dégradées : MOS 4,13 en G.711 Loi-µ et 4,11 en G.711 Loi-A


Capture wireshark d'une conversation en G711 :

:raw-html-m2r:`<img src="https://raw.githubusercontent.com/algues111/docs-cfc/main/docs/source/html/images/rtp-conf-payload-G711.png" />`

Comme escompté, nous remarquons que la discussion transite du téléphone _\_(192.168.1.122)\__ en passant par le serveur 3CX _\_(192.168.1.120)\__ .

La première chose qui est importante à souligner, est que les paquets utilisent le protocole de transport UDP (couche OSI 4) pour naviguer à travers le réseau, réduisant donc la latence potentielle de la conversation.






G722
********

Les caractéristiques du codec G.722 sont les suivantes :

- Bande de fréquences : 50-7000Hz
- Fréquence d'échantillonnage : 16 kHz
- Débit fixe : 64 kbps
- Délai de compression : Non spécifié

MOS :

- Mesure de qualité en conditions idéales : MOS (Mean Opinion Score) similaire pour G.722 et G.711
- Mesure de qualité en conditions dégradées : MOS (Mean Opinion Score) similaire pour G.722 et G.711


G729
********


Parler de la MOS pour la qualité audio

*
  To toggle the **HTML Preview** press **F12** or click @icon-globe in the Window bar

*
  To toggle the **Folder Browser Sidebar** press **Ctrl-Shift-B** or click **@icon-bars**

*
  The **@icon-bars SideBar** also holds **Favorites** and **Markdown Document Outline**

*
  To change **UI Themes**\ , click on the dropdown lists on the bottom right status bar:


.. image:: https://markdownmonster.west-wind.com/docs/images/EditorPreviewThemeUi.png
   :target: https://markdownmonster.west-wind.com/docs/images/EditorPreviewThemeUi.png
   :alt: Image and Preview Themes on the toolbar



*
  For **light editor themes** look at ``visualstudio``\ , ``github`` or ``xcode``

*
  For **dark editor themes** look at ``vscodedark``\ , ``twilight``\ , ``monokai``\ , ``terminal``

Problems? Please let us know
^^^^^^^^^^^^^^^^^^^^^^^^^^^^

If you run into any problems or issues, **please** let us know so we can address and fix them right away. You can report issues on GitHub:


* `Markdown Monster Bug Reports and Feature Requests <https://github.com/RickStrahl/MarkdownMonster/issues>`_

Markdown Features
=================

This topic is meant to give you a very basic overview of how Markdown works, showing some of the most frequently used operations.

Bold and Italic
^^^^^^^^^^^^^^^

This text **is bold**.\ :raw-html-m2r:`<br>`
This text *is italic*.\ :raw-html-m2r:`<br>`
This text :raw-html-m2r:`<del>is struck out</del>`.

Header Text
^^^^^^^^^^^

Header 1
========

Header 2
--------

Header 3
^^^^^^^^

Header 4
~~~~~~~~

Header 5
""""""""

Header 6
########

Line Continuation
^^^^^^^^^^^^^^^^^

By default Markdown **adds paragraphs at double line breaks**. Single line breaks by themselves are simply wrapped together into a single line. If you want to have **soft returns** that break a single line, add **two spaces at the end of the line** :raw-html-m2r:`<small>(shift-enter)</small>` or use a backslash ``\``.

----

This line has a paragraph break at the end (empty line after).

Theses two lines should display as a single
line because there's no double space at the end.

The following line has a soft break at the end (two spaces or a ``\`` at end)\ :raw-html-m2r:`<br>`
This line should be following on the very next line.

You can also use ``shift-enter`` to inject the two spaces plus linefeed at the end of a line.\ :raw-html-m2r:`<br>`
To show all white space and returns in a document you can use **View -> Toggle Invisible Characters**.

----

Links
^^^^^

You can easily link using ``[text](link)`` syntax:

`Markdown Monster Web Site <http://MarkdownMonster.west-wind.com/>`_

If you need additional image tags like targets or title attributes you can also embed HTML directly using raw HTML markup:

.. code-block:: html

   Go to the
   <a href="https://markdownmonster.west-wind.com" style="font-style: italic">
       Markdown Monster Web Site
   </a>

renders:

Go to the
:raw-html-m2r:`<a href="https://markdownmonster.west-wind.com" style="font-style: italic">
    Markdown Monster Web Site
</a>`

----

Images
^^^^^^

Images are similar to links:

.. code-block:: markdown

   ![Markdown Monster](https://markdownmonster.west-wind.com/Images/MarkdownMonster_Icon_128.png)

which renders:


.. image:: https://markdownmonster.west-wind.com/Images/MarkdownMonster_Icon_128.png
   :target: https://markdownmonster.west-wind.com/Images/MarkdownMonster_Icon_128.png
   :alt: Markdown Monster


You can embed images from the Clipboard by pasting (\ **ctrl-v**\ ), by using the @icon-image Image Dialog, or by dragging and dropping images into the document from the Folder Browser, Windows Explorer or a

Block Quotes
^^^^^^^^^^^^

Block quotes are callouts that are great for adding notes or warnings into documentation.

Simple block quotes simply use a ``>`` to start a quote block:

.. code-block:: markdown

   > **Note:** Block quotes can be used to highlight important ideas.

This renders to:

..

   **Note:** Block quotes can be used to highlight important ideas.


You can make quote blocks look nicer with headers and icons (using FontAwesome here):

.. code-block:: markdown

   > ### @ icon-info-circle Headers break on their own
   > Note that headers don't need line continuation characters
   > as they are block elements and automatically break. Only text lines
   > require the double spaces for single line breaks.

Note that lines automatically wrap in the quote block, if no newline with `>' is provided. Shown with the breaks here to make it easier to read. The following uses a single line for the second block which renders identically:

..

   @icon-info-circle Headers break on their own
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   Note that headers don't need line continuation characters as they are block elements and automatically break. Only text lines require the double spaces for single line breaks.


Fontawesome Icons
^^^^^^^^^^^^^^^^^

Markdown Monster includes custom syntax for FontAwesome icons in its templates. You can embed a ``@ icon-`` followed by a font-awesome icon name to automatically embed that icon without full HTML syntax.

.. code-block:: markdown

   @ icon-gear Configuration

which renders:

----

@icon-gear Configuration

----

Note that this renders the following html:

.. code-block:: html

   <i class="fa fa-gear"></i>

Emojis
^^^^^^

You can also embed Emojis into your markdown using the Emoji dialog or common

.. code-block:: markdown

   :smile: :rage: :sweat: :point_down:

   :-) :-( :-/
   `

This renders:

----

:smile: :rage: :sweat: :point_down:

:-) :-( :-/

----

HTML Markup
^^^^^^^^^^^

You can also embed plain HTML markup into the page if you like. For example, if you want full control over fontawesome icons you can use this:

This text can be **embedded** into Markdown:

.. code-block:: markdown

   <i class="fa fa-refresh fa-spin fa-2x"></i> &nbsp;**Refresh Page**

:raw-html-m2r:`<i class="fa fa-refresh fa-spin fa-2x"></i>` &nbsp;\ **Refresh Page**

Note that blocks of raw HTML markup should be separated from text by empty lines above and below the HTML blocks.

Comment Blocks - Keep Markdown from Rendering
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

Markdown has support for HTML comments and you can use ``<!--`` for the beginning and ``-->`` for the end of a block of markdown that you don't want to render.

.. code-block:: markdown

   ### Commenting
   This text and header renders fine.

   <!--
   This paragraph is commented out and **does not render**.
   -->

   This footer is comming across just fine.

This renders:

----

Commenting
^^^^^^^^^^

This text and header renders fine.


.. raw:: html

   <!--
   This paragraph is commented out and **does not render**.
   -->



This footer is coming across just fine.

----

Unordered Lists
^^^^^^^^^^^^^^^

.. code-block:: markdown

   * Item 1
   * Item 2
   * Item 3

This renders:

----


* Item 1
* Item 2
* Item 3

----

This text is part of the third item. Use a soft return (\ ``shift-enter`` or two spaces or ``\``\ ) at the end of the the list item to break the line and continue at the bullet indentation.

A double line break, breaks out of the list.

Ordered Lists
^^^^^^^^^^^^^

Ordered lists use number like ``1.`` or ``2.`` for the bullet items.

.. code-block:: markdown

   1. **Item 1**
   Item 1 is really something
   2. **Item 2**
   Item two is really something else

renders to:


#. **Item 1**\ :raw-html-m2r:`<br>`
   Item 1 is really something
#. **Item 2**\ :raw-html-m2r:`<br>`
   Item two is really something else

If you want lines to break (like after the bold headers) you cna use **soft returns**.

..

   **Note**\ : Numbered lists **order themselves based on order** rather than the number you explicitly use. If you frequently reorder lists it's useful to number all items ``1.``.


You can also nest lists and mix ordered and unordered lists:

.. code-block:: markdown

   1. First, get these ingredients:

         * carrots
         * celery
         * lentils

   2. Boil some water.

   3. Dump everything in the pot and follow
   this algorithm:

This renders:

----


#.
   First, get these ingredients:


   * carrots
   * celery
   * lentils


   #.
      Boil some water.

   #.
      Dump everything in the pot and follow\ :raw-html-m2r:`<br>`
      this algorithm:

----

Inline Code
^^^^^^^^^^^

If you want to embed code in the middle of a paragraph of text to highlight a coding syntax or class/member name you can use inline code syntax:

.. code-block:: markdown

   Inline code or member references  like `SomeMethod()` can be codified...

----

Inline code or member references  like ``SomeMethod()`` can be codified... You can use the ``'{}'`` menu or **Ctrl-`** to embed inline code.

----

Indented Code Blocks
^^^^^^^^^^^^^^^^^^^^

Markdown supports code blocks syntax in a couple of ways:

Using an indented text block for code:

.. code-block:: markdown

   Some rendered text...

       // This is code by way of four leading spaces
       // or a leading tab
       int x = 0;
       string text = null;
       for(int i; i < 10; i++;) {
           text += text + "Line " + i;
       }

   More text here

renders:

----

Some rendered text...

.. code-block::

   // This is code by way of four leading spaces
   // or a leading tab
   int x = 0;
   string text = null;
   for(int i; i < 10; i++;) {
       text += text + "Line " + i;
   }


More text here

----

Fenced Code Blocks with Syntax Highlighting
^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

You can also use triple back ticks plus an optional coding language to support for syntax highlighting.

The following is C# code.

.. code-block:: markdown

   ```csharp
   // this code will be syntax highlighted
   for(var i=0; i++; i < 10)
   {
       Console.WriteLine(i);
   }
   ```

which renders syntax colored code:

.. code-block:: csharp

   // this code will be syntax highlighted
   for(var i=0; i++; i < 10)
   {
       Console.WriteLine(i);
   }

Many languages are supported: html, xml, javascript, typescript, css, csharp, fsharp foxpro, vbnet, sql, python, ruby, php, powershell, dos, markdown, yaml and many more. Use the Code drop down list to get a list of available languages.

You can also leave out the language to attempt auto-detection or use ``text`` for plain text:

.. code-block:: markdown

   ```text
   robocopy c:\temp\test d:\temp\test
   ```

renders plain, but formatted text:

.. code-block:: text

   robocopy c:\temp\test d:\temp\test

..

   **Note**\ : Prefer using ``text`` for non-highlighted syntax over no syntax as no syntax tries to auto-discover the syntax which often is not correct. Always be specific with syntax specified.


Footnotes
^^^^^^^^^

Footnotes can be embedded like this:

Here is some text that includes a Footnote [#fn-1]_ in the middle of its text. And here's another footnote [#fn-2]_. The actual footnotes render on the very bottom of the page.

Pipe Tables
^^^^^^^^^^^

`Pipe Tables <https://github.com/lunet-io/markdig/blob/master/src/Markdig.Tests/Specs/PipeTableSpecs.md>`_ can be used to create simple single line tables:

.. code-block:: markdown

   |size | material     | color       |
   |---- | ------------ | ------------|
   |9    | leather      | brown **fox**  |
   |10   | hemp canvas  | natural |
   |11   | glass        | transparent |

----

.. list-table::
   :header-rows: 1

   * - size
     - material
     - color
   * - 9
     - leather
     - brown **fox**
   * - 10
     - hemp canvas
     - natural
   * - 11
     - glass
     - transparent


..

   **Note:** Cell lines don't have to line up to render properly. Max columns in any row determines table columns for the entire table. Pipe tables also don't need leading and trailing pipes to render as tables, but make sure you check compatibility with your final rendering site.


Grid Tables
^^^^^^^^^^^

`Grid Tables <https://github.com/lunet-io/markdig/blob/master/src/Markdig.Tests/Specs/GridTableSpecs.md>`_ are a bit more flexible than Pipe Tables in that they can have multiple lines of text per cell and handle multi-line embedded Markdown text.

.. code-block:: markdown

   +---------+---------+
   | Header  | Header  |
   | Column1 | Column2 |
   +=========+=========+
   | 1. ab   | > This is a quote
   | 2. cde  | > For the second column
   | 3. f    |
   +---------+---------+
   | Second row spanning
   | on two columns
   +---------+---------+
   | Back    |         |
   | to      |         |
   | one     |         |
   | column  |         |

----

+---------+---------+
| Header  | Header  |
| Column1 | Column2 |
+=========+=========+
| 1. ab   | > This is a quote
| 2. cde  | > For the second column
| 3. f    |
+---------+---------+
| Second row spanning
| on two columns
+---------+---------+
| Back    |         |
| to      |         |
| one     |         |
| column  |         |

..

   @icon-info-circle Use the @icon-table Table Editor
   ^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^^

   For easier table data entry and pretty rendered tables you can use the table editor which provides grid based table data entry. You can use the table editor with **Pipe**\ , **Grid** and **HTML** tables.


DocFx Extensions
^^^^^^^^^^^^^^^^

Markdown Monster supports some DocFx extensions if you enable the ``ParseDocFx`` option in the settings.

Blockquote Formatters
~~~~~~~~~~~~~~~~~~~~~

There's support for the following block quote formatters:

..

   [!NOTE]
   This is a note

   [!IMPORTANT]
   This is important

   [!CAUTION]
   This is important

   [!WARNING]
   This is important


File Includes
~~~~~~~~~~~~~

You can embed another Markdown file into the current document via an ``!Include``\ :

.. code-block:: md

   [!include[Included Test File](test1.md)]

----

[!include\ `Included Test File <./test.md>`_\ ]

----

[!code-csharp\ ` <~/program.cs>`_\ ]


.. [#fn-1] Source: `Markdown Monster Web Site <http://markdownmonster.west-wind.com>`_\
.. [#fn-2] Source: `Markdown Monster Web Site <http://markdownmonster.west-wind.com>`_\
