=====================
Reclaim the Internet!
=====================

Vortrag und Diskussion über Möglichkeiten des Webpublishing.

Download der Materialien: https://github.com/thet/talk-reclaim-the-internet

Inhalt:

.. toctree::
   :maxdepth: 2


================
Technology Track
================

Das Internet
============

Geschichte
----------

* Vorläufer vernetzter Kommunikation

  * Telegraphen System, Telefon
  * `Fernschreiber`_, Fax
  * `BTX`_, `Teletext`_

* 60er Jahre: ARPA Forschungsprojekt zur effizienten verteilten Nutzung von
  Rechenleistung.

* Start des Internet: 29.10.1969 - Vernetzung von vier Großrechnern
  amerikanischer Universitäten und Übertragung der Botschaft "LO".

    * 1971: 14 Knoten
    * 1975: 61 Knoten
    * 1988: 60.000 Knoten
    * 2000: 100.000.000 Knoten
    * 2007: 500.000.000 Knoten
    * ...

* Mehr Informationen auf Wikipedia: `Geschichte des Internets`_ und `History of the Internet`_

.. _Geschichte des Internets: http://de.wikipedia.org/wiki/Geschichte_des_Internets
.. _History of the Internet: http://en.wikipedia.org/wiki/History_of_the_Internet
.. _Fernschreiber: http://de.wikipedia.org/wiki/Fernschreiber
.. _BTX: http://de.wikipedia.org/wiki/Bildschirmtext
.. _Teletext: http://de.wikipedia.org/wiki/Teletext


Aufbau
------

Internet Protocol
.................

* Jeder Knoten hat eine eindeutige Netzwerkadresse, die 
  
  `IP-Adresse`_.
  Wobei ... : Subnetzte (NAT - Network Adress Translation) sind sehr häufig.
  Bei den meisten privaten Internetanschlüssen und in Firmennetzen kommen
  reservierte Adresspools zur internen Verwendung (10.x.x.x, 192.168.x.x) zum Einsatz. Nach aussen
  hin - für das Internet - wird nur die IP Adresse des letzten Knotens
  verwendet, der die Vermittlung zwischen Internet und Intranet herstellt
  (Router).

* `IPv4`_

    * bsp 195.58.172.219
    * 32bit, 4 Byte, max 255.255.255.255 = 2^32 = 4.294.967.296 Möglichkeiten
    * Adresspool ist endlich. Voraussichtlicher Termin, an dem die letzte IPv4
      Adresse vergeben wird: `28.April 2011`_

* Lösung: `IPv6`_

    * bsp: 2001:0db8:85a3:08d3:1319:8a2e:0370:7344
    * 128bit, 2^128, max: 3.4×10^38, 340.282.366.920.938.463.463.374.607.431.768.211.456
    * "jeden Quadratmillimeter der Erdoberfläche mindestens 665.570.793.348.866.944 (= 6,65 · 10^17) IP-Adressen"
    * Notwendige Lösung, noch nicht weit verbreitet. Verbreitung scheitert in
      erster Linie an Server, die IPv6 nicht unterstützen.

DNS - Domain Name System
........................

* `DNS - Domain Name System`_

    * Ordnet registrierten Computern einen Namen zu.
    * Namen sind einfacher zu Merken als IP Adressen.
    * Erlaubt durch "Virtual Hosting" auf einem Computer mit der selben IP
      Adresse mehrere Dienste laufen zu lassen, die der Server durch den
      unterschiedlichen Namen unter auseinander halten kann.

* Registrierung eines Domain Namens
    
    * Registrierungsbehören verwalten Länderspezifische Domains. Für
      Österreich: `nic.at`_
    * Domain Regsitrars übernehmen den Registrierungsprozess bei
      Registrierungsbehörden und das Eintragen in einen DNS Server. Bsp:
      `easyname.at`_.

.. _IP-Adresse: http://de.wikipedia.org/wiki/IP-Adresse
.. _IPv4: http://en.wikipedia.org/wiki/IPv4
.. _28.April 2011: http://inetcore.com/project/ipv4ec/index_en.html
.. _IPv6: http://en.wikipedia.org/wiki/IPv6
.. _DNS - Domain Name System: http://de.wikipedia.org/wiki/Domain_Name_System
.. _nic.at: http://www.nic.at/
.. _easyname.at: http://www.easyname.at/

Webserver
---------

* Sind Computer, die öffentlich im Internet erreichbar sind und bestimmte Dienste
  für Besucher (Clients) bereitstellen, die von denen abgerufen werden können.
* Werden meist von Firmen als Kostenpflichtiges Service angeboten. Bsp:
  hetzner.de, inode.at, ... Aber auch `mur.at`_, dazu später mehr.
* Bieten Speicherplatz für Webseiten in Form von HTML Dateien, aber oft auch 
  Datenbanksysteme, Programmierumgebungen für Webseiten mit dynamischen
  Inhalten, Zugriffsstatistik Analysesoftware, etc.
* Zugriffsmöglichkeit über (S)FTP und/oder SSH.

.. _mur.at: https://wiki.mur.at/

HTML Einführung
===============

Geschichte
----------

* HyperText Markup Language
* Von Tim Berners-Lee, CERN 1990
* SGML -> HTML -> XML -> XHTML
* Ursprüngliches Ziel: Einfaches publizieren von verlinkten wissenschaftlichen
  Dokumenten.

Allgemein
---------

* Strukturierung von Inhalten.
* Struktur- und Formatelemente teilweise gemischt.
* Weniger geeignet, um Texte zu entwickeln.

Syntax Allgemein
----------------

* <tag attribute="value">content</tag>
* Elemente (Tags) können hierarchisch strukturiert werden.
* Elemente (Tags) haben ein öffnendes (<tag>) und ein schließendes (</tag>)Element
* Manche Elemente haben kein explizit schließendes Element und werden gleich
  beim öffnen geschlossen (<tag />).

Syntax Überblick
----------------

* Dokumentenstrukturelemente

    * <html>..</html>
    * <head>..</head>
    * <body>..</body>

* Kopfelemente

    * <title>..<title>
    * <meta />
    * <link />
    * <script />

* Inhalts-Blockelemente

  Erzeugen einen neuen Absatz / Umbruch.

    * <p>
    * <h1>..</h1>, <h2>..</h2>, ... <h6>..</h6>
    * <ol>, <ul>, ..
    * <table> ...
    * <div> ...

* Inhalts-Inlineelemente

  Werden im Textfluss dargestellt.

    * <img>, <a>, ..
    * <b>, <i>, ..


Syntax Beispiel
---------------

Siehe `html-example/index.html <../html-example/index.html>`_

Andere Markupsprachen
---------------------

* Wiki Syntax
* ReStructuredText

  * http://en.wikipedia.org/wiki/ReStructuredText
  * http://docutils.sourceforge.net/rst.html
  * http://sphinx.pocoo.org/rest.html

* Markdown

  * http://en.wikipedia.org/wiki/Markdown

Entwicklungshilfen
------------------
* Firebug für Firefox: http://getfirebug.com/
* HTML validation check: http://validator.w3.org/
* HTML im allgemeinen, englisch: http://en.wikipedia.org/wiki/HTML
* HTML im allgemeinen, deutsch: http://en.wikipedia.org/wiki/HTML_element
* HTML4 im selbststudium: http://de.selfhtml.org/
* Überblick über HTML5: http://diveintohtml5.org/


CSS - Cascading Style Sheets
============================

CSS validation check: http://jigsaw.w3.org/css-validator/


=================
Create a Website!
=================

Static HTML
===========

* Tools

    * KompoZer: http://www.kompozer.net/
    * BlueFish: http://bluefish.openoffice.nl/
    * Abiword: http://en.wikipedia.org/wiki/AbiWord
    * https://sites.google.com/site/thetetet/



Through The Web Publishing
==========================

Vorteile gegenüber direktem HTML Publishing:

* HTML Kenntnisse sind keine Voraussetzung
* Einheitliches Design über alle Inhalte hinweg
* Strukturierung der Inhalte ist einfacher
* Bestimmte Funktionalitäten werden erst durch CMS Systeme möglich
  
    * Kommentare
    * Dynamische Suche
    * Behandlung unterschiedlicher Inhaltstypen
    * Datenbanksysteme
    * ...


Wiki Systeme
------------

**Vorteile**

* Einfache, unbürokratische Kolloboration
* Schnelles Erstellen von verlinkten Dokumenten
* Ideal zur Projektorganisation, Ideenfindung, Wissensmanagement

**Nachteile**

* Wenig ausgeprägt bei Rechtemanagement und Eingabehilfen
* Inhalte können nicht hierarchisch organisiert werden
* Datenbankapplikationen können nicht umgesetzt werden

**Beispiele**

* Moin Moin - http://moinmo.in/
| + keine datenbank notwendig
| + viele eingabeformate (bsp reStructuredText)
| + bewährt sich seit jahren als mur.at wiki system

* Dokuwiki - http://www.dokuwiki.org/
| + bewährt sich seit jahren im spektral als wiki system

* mediawiki - http://www.mediawiki.org/
| + wiki system des weltweit größten wikis: wikipedia.org

* ... diverse weitere + als plugins für cms systeme
* first ever created wiki: http://c2.com/cgi/wiki?FrontPage


Blog systeme
------------
**Vorteile**

* Optimiert für das Publizieren von Nachrichten
* Viele Community features (Kommentare, Backlinks, ...)

**Nachteile**

* Die Optimierung als Blog System schränkt andere Einsatzzwecke etwas ein

**Beispiele**

* WordPress - http://wordpress.org/
| + Open Source
| + Bekanntestes Blog System mit vielen Features
| + Einfache Bedienung
| + Auch als CMS System einsetzbar
| + Viele Plugins
| - als cms system weniger gut brauchbar
|  mehr info: http://en.wikipedia.org/wiki/WordPress
|  gratis blogs: http://wordpress.com/

* Moveable Type - http://www.movabletype.org/
| + Open Source
| + Bekanntes Blog System
| + TypePad basiert darauf: http://en.wikipedia.org/wiki/TypePad
| mehr info: http://en.wikipedia.org/wiki/Movable_Type

* zine - http://zine.pocoo.org/
| + blog system in python
| + geschrieben vom grazer armin ronnacher


CMS Systeme
-----------
**what's That?**

* Content Management System
* Wichtige Bestandteile:

    * Theming Engine (Design der Website)
    * Verschiedene Inhaltstypen
    * Rechteverwaltung

**Beispiele**

* plone - http://plone.org/
| Ein in der Programmiersprache Python geschriebenes professionelles CMS.
| + sehr einfache bedienung
| + robustes technisches backend
| + wenige bekanne sicherheitslücken (u.a. python, zope)
| + sehr gut erweiterbar
| - geringe verbreitung
| - relativ komplizierte technik
| - relativ hohe kosten für hosting

* joomla
| PHP
| + sehr weit verbreitet
| + relativ einfache bedienung
| - schlecht wartbar und erweiterbar

* drupal
| PHP
| + weit verbreitet mit vielen community features
| + gut wartbar und erweiterbar

* wordpress
| PHP
| + weit verbreitet
| + wird immer öfter als cms system genutzt
| - als cms system eingeschränkt geeignet


Software Verzeichnis
====================

FTP Clients
-----------

Filezilla
.........
| Open Source
| Linux, Windows und Mac OS X
| http://filezilla-project.org/
| http://en.wikipedia.org/wiki/FileZilla


Text-Editoren
-------------

Gedit
.....
| Open Source
| Linux
| http://projects.gnome.org/gedit/

Notepad++
.........
| Open Source
| Windows
| http://notepad-plus-plus.org/
| http://en.wikipedia.org/wiki/Notepad%2B%2B

TextMate
........
| Kommerziell
| OSX
| http://macromates.com/

Vim oder Emacs
..............
| Alle Plattformen. Editor für Programmierer.


Online WYSIWYG (What You See is What You Get) Editoren
------------------------------------------------------

"What You See Is What You Mean" Editor
......................................
| Open Source
| Fokus auf Struktur, nicht Design. Eignet sich besser für Semantik.
| http://en.wikipedia.org/wiki/WYMeditor
| http://www.wymeditor.org/demo/

TinyMCE
.......
| Open Source
| Beliebter Online Editor zum Formatieren von Texten in CMS Systemen. Unter
  anderem in Plone und WordPress zu finden.
| http://tinymce.moxiecode.com/
| http://en.wikipedia.org/wiki/TinyMCE

Aloha Editor
............
| Next Generation HTML 5 basierter Online Editor.
| http://www.aloha-editor.org/
| http://en.wikipedia.org/wiki/Aloha_Editor

CKEditor
........
| Open Source.
| Ehemals FCKEditor.
| http://en.wikipedia.org/wiki/CKEditor
| http://ckeditor.com/

Kupu
....
| Open Source.
| Ehemaliger Standardeditor unter Plone.
| http://en.wikipedia.org/wiki/Kupu


HTML Editoren
-------------

BlueFish
........
| Open Source
| HTML Text Editor, ohne Graphische Editierung. Unterstützt aber gut beim
| Erstellen von HTML Layouts.
| http://bluefish.openoffice.nl/
| http://en.wikipedia.org/wiki/Bluefish_%28text_editor%29

Amaya
.....
| Open Source, W3C
| Visueller HTML Editor. Wird vom W3C zum Testen neuer Webstandards verwendet.
| http://en.wikipedia.org/wiki/Amaya_%28web_browser%29

KompoZer
........
| Open Source
| Ehemals Nvu, vormals Netscape
| http://www.kompozer.net/
| http://en.wikipedia.org/wiki/KompoZer

BlueGriffon
...........
| Open Source, in Beta Phase
| Nvu Nachfolger
| Unterstützt HTML5, CSS3, SVG und andere aktuelle Standards.
| http://bluegriffon.org/
| http://en.wikipedia.org/wiki/BlueGriffon

Adobe Dreamweaver
.................
| Kommerziell
| Vormals Macromedia Dreamweaver, Ersetzt Adobe GoLive.
| http://en.wikipedia.org/wiki/Adobe_Dreamweaver

Microsoft Expression Web
........................
| Kommerziell
| Ersetzt Microsoft FrontPage
| http://en.wikipedia.org/wiki/Microsoft_Expression_Web

Microsoft Visual Web Developer
..............................
| Kommerziell, aber kostenlos
| http://en.wikipedia.org/wiki/Microsoft_Visual_Web_Developer#Visual_Web_Developer_Express

NetObjects Fusion
.................
| Früher und einfach zu bedienender HTML Editor
| http://en.wikipedia.org/wiki/NetObjects_Fusion

Office Suites
-------------
Die meisten Office Programme können Dokumente als HTML Seiten speichern. Da
Microsoft Office viele eigene HTML Erweiterungen verwendet, empfiehlt es sich,
auf eine Freie Office Variante wie Abiword oder OpenOffice / Libre Office
zurückzugreifen.

Abiword
.......
| Open Source
| Einfaches aber trotzdem genügend umfangreiches Office Packet.
| http://en.wikipedia.org/wiki/AbiWord

OpenOffice / LibreOffice
........................
| Open Source
| Microsoft Office Alternative. LibreOffice ist eine Abspaltung von
 OpenOffice, welches von Oracle gekauft wurde und ein Entwicklungsstreit
 ausgebrochen ist. LibreOffice wird vermutlich bald relevanter als
 OpenOffice werden.
| http://en.wikipedia.org/wiki/OpenOffice.org
| http://en.wikipedia.org/wiki/LibreOffice

Microsoft Office
................
| Kommerziell
| Bekannteste Office Suite. Es existieren Varianten für Microsoft Windows und
| Apple Mac OS X.
| http://en.wikipedia.org/wiki/Microsoft_Office

KOffice
........
| Open Source
| KDE Office Suite
| http://en.wikipedia.org/wiki/KOffice

Online Website Builder
----------------------

Blogger
.......
| http://www.blogger.com/
| http://en.wikipedia.org/wiki/Blogger_%28service%29

Google Sites
............
| https://sites.google.com/site/thetetet/


Squarespace
...........
http://www.squarespace.com/
