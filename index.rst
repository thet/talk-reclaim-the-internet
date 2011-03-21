Reclaim the Internet!
=====================

Vortrag und Diskussion über Möglichkeiten des Webpublishing.

Download der Materialien: 
Mehr info über das Projekt Backpackjournalism: http://wikis.spektral.at/bpj/

Inhalt:

.. toctree::
   :maxdepth: 2


HTML Einführung
===============

Geschichte
----------

* HyperText Markup Language
* Von Tim Berners-Lee, CERN 1990
* SGML -> HTML -> XML -> XHTML
* Ursprüngliches Ziel: Einfaches publizieren von verlinkten wissenschaftlichen
  Dokumenten.

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


info
----

* http://en.wikipedia.org/wiki/HTML
* http://en.wikipedia.org/wiki/HTML_element
* http://de.selfhtml.org/
* http://diveintohtml5.org/


Entwicklungshilfen
------------------
* Firebug für Firefox http://getfirebug.com/

* Editoren
  * Gedit (Linux, http://projects.gnome.org/gedit/)
  * Notepad++ (Windows, http://notepad-plus-plus.org/)
  * TextMate (OSX, http://macromates.com/)
  * Vim oder Emacs (Alle Plattformen. Editor für Programmierer)

* HTML WYSIWYG (What You See is What You Get) Editoren

  * KompoZer (Ehemals Nvu, vormals Netscape)
    http://www.kompozer.net/

  * Abiword
  * OpenOffice
  * Microsoft Office


through the web publishing
==========================

# --> cms vendor map

vorteil gegenüber direktem html publishing:

* HTML Kenntnisse sind keine Voraussetzung
* Einheitliches Design über alle Inhalte hinweg
* Strukturierung der Inhalte ist einfacher
* Bestimmte Funktionalitäten werden erst durch CMS Systeme möglich
  
    * Kommentare
    * Dynamische Suche
    * Behandlung unterschiedlicher Inhaltstypen
    * Datenbanksysteme
    * ...


wiki systeme
------------
pros:
    * einfache, unbürokratische kolloboration
    * schnelles erstellen von verlinkten dokumenten
    * ideal zur projektorganisation, ideenfindung, wissensmanagement

cons:
    * wenig ausgeprägt bei rechtemanagement und eingabehilfen
    * inhalte können nicht hierarchisch organisiert werden
    * datenbankapplikationen können nicht umgesetzt werden

examples:
    * moinmoin - http://moinmo.in/
        + keine datenbank notwendig
        + viele eingabeformate (bsp reStructuredText)
        + bewährt sich seit jahren als mur.at wiki system
    * dokuwiki - http://www.dokuwiki.org/
        + bewährt sich seit jahren im spektral als wiki system
    * mediawiki - http://www.mediawiki.org/
        + wiki system des weltweit größten wikis: wikipedia.org
    * ... diverse weitere + als plugins für cms systeme

    * first ever created wiki: http://c2.com/cgi/wiki?FrontPage


blog systeme
------------
pros:
    * optimiert für das publizieren von nachrichten
    * viele community features
        * kommentare
        * backlinks

cons:
    die optimierung als blog system schränkt andere einsatzzwecke etwas ein

examples:
    * wordpress - http://wordpress.org/
        + bekanntestes blog system mit vielen features
        + einfache bedienung
        + auch als cms system einsetzbar
        - als cms system weniger gut brauchbar

        * mehr info: http://en.wikipedia.org/wiki/WordPress
        * gratis blogs: http://wordpress.com/

    * moveable type - http://www.movabletype.org/
        + bekanntes blog system
        
        * hr info: http://en.wikipedia.org/wiki/Movable_Type

    * zine - http://zine.pocoo.org/
        + blog system in python
        + geschrieben vom grazer armin ronnacher

cms systeme
-----------
what's that?
    * Content Management System
    * Wichtige Bestandteile:
        * Theming Engine (Design der Website)
        * Verschiedene Inhaltstypen

examples:
    * joomla
        + sehr weit verbreitet
        + relativ einfache bedienung
        - schlecht wartbar und erweiterbar

    * drupal
        + weit verbreitet mit vielen community features
        + gut wartbar und erweiterbar

    * wordpress
        + weit verbreitet
        + wird immer öfter als cms system genutzt
        - als cms system eingeschränkt geeignet

    * plone
        + sehr einfache bedienung
        + robustes technisches backend
        + wenige bekanne sicherheitslücken (u.a. python, zope)
        + sehr gut erweiterbar
        - geringe verbreitung
        - relativ komplizierte technik
        - relativ hohe kosten für hosting

