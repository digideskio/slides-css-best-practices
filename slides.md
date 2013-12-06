<h1>
<small class="fragment" data-fragment-index="1">Learning from</small><br/>
CSS Best Practices<br/>
<small class="fragment" data-fragment-index="2">failing</small>
</h1>


# Damals <!-- .slide: data-state="blackout" -->


## '95: Warum CSS?
```
<font face="Comic Sans MS" color="pink">
	I can haz spaghetti on my <table>?

```
<!-- .element: style="font-size:1em" -->

Note:

- Table layout, unsemantischer Spaghetti Code


## '99: Weil's besser geht
```
<p class="spaghetti">U can</p>

```
<!-- .element: style="font-size:1em" -->

- Table-Layout blieb
- Schriften/Farben wanderten ins CSS
- CSS = Skin/Theme


## '01: CSS kann mehr
- Auch für Layout
- Semantisches Markup
- Separation of concerns
- Layout und Skin getrennt vom Markup
- Tags, Klassen und IDs als Hooks


## Best practice 2001
- CSS Zen Garden, anyone?
- Tables raus, wir floaten
- Semantisches, schlankes Markup
- IDs kapseln Bereiche im Layout
- Tags/Klassen für wiederkehrende Inhalte


# Funktioniert doch heute noch! <!-- .slide: data-state="invert" -->
## ... bis es größer wird <!-- .element: class="fragment" -->



# 2005 <!-- .slide: data-state="blackout" -->
## Big sites


## Herausforderungen
- Viele Seitentypen
- ... mit unterschiedlichem Inhalt
- Pixelgenau soll es sein
- Wartbar soll es bleiben

Note:

- Photoshop, immer mehr Design


## Lösung ca. 2004
### Deep Nesting
- So spezifisch wie möglich, so allgemein wie nötig
- Klare Struktur im CSS
- Neue Bereiche rühren alte nicht an
- Alte Bereiche können leicht entfernt werden
- Markup bleibt sauber


## Deep Nesting
- Implizite enge Kopplung von Markup und Styling
- Neue Module/Seiten brauchen neues Styling
- Stetig wachsender CSS-Code
- Inkonsistentes Styling
- Specifity Wars

Note:

- Probleme: Separation of Concerns falsch verstanden.
- Soll: an verschiedenen Stellen unabhängig arbeiten können
- Ist: Änderung von A benötigt Wissen über/Anpassung von B



# 2010 <!-- .slide: data-state="blackout" -->
## Alles dynamisch


## Alles dynamisch
### Webapps kommen
- CSS kommt an seine Grenzen
- Wasserfall auch

Note:

- CSS wie bisher: Seitenmetapher passt immer weniger
- Interdisziplinarität, Rapid Dev., Scrum
- &rarr; verschiedene Lösungsansätze


## Preprocessors
### Sass, Less, Stylus, ...
- Variablen und Mixins lösen Konsistenzprobleme
- Deep-Nesting einfacher durch DRY-Schreibweise

Note:

- Vars/Mix für Farben/Schriften/Abstände
- Selektorketten


## Preprocessors
### Probleme
- Fördert stumpfes Nachbauen von Designs
- CSS-Code wächst weiter
- Abstraktionsschicht
- &rarr; Komplexität, Unachtsamkeit

Note:

- Mehr Möglichkeiten, mehr Verantwortung


## OOCSS
### Kombinieren von Klassen
- Wiederverwendbare, variable Module & Aspekte
- Kontext-unabhängig
- No Specifity War
- Neue Seiten ohne neues CSS
- CSS bleibt klein
- Design bleibt konsistent
- Fördert Rapid Development

Note:

- CSS-Layout verstehen!
- auch Bootstrap, Foundation


## OOCSS
### Probleme
- Specifity War &rarr; Class Hell
- Semantik leidet (Namensfindung!)
- CSS-Änderungen &rarr; Auswirkungen?
- CSS löschen wird haarig
- Macht Feintuning hart
- Responsive Design evtl. schwierig

Note:

- Welche Klasse macht was? Copy/Paste => unnötige Klassen bleiben hängen
- Namensschema fehlte ursprünglich => Clashes (small, back, box, col)
- Modifier/Skin vs. Teilbereich immer noch nicht getrennt (box boxBody boxTabs)
- Namensfindung nach visueller Semantik
- Tuning: Neue Klasse für Sonderfälle? OO-Klasse zweckentfremden?
- col-xl-6 col-md-4


## BEM
### OOCSS+ mit Namensschema
- ```.block``` (Layout/Komponente)
- ```.block__elemente``` (Content/Einzelteile)
- ```.block--modifier``` (Variationen/Skin)

Note:

- Namensschema geht reduzierter
- aber gute Inspiration


## BEM
### Probleme
- kann zu unnötigem Markup führen
- Feintuning bleibt schwierig
<br/><br/>
```.form--compact__row__button--primary--wtf``` <!-- .element: class="fragment" -->

Note:

- *FRAG* Maßlos übertrieben ;)



# Lessons learned <!-- .slide: data-state="blackout" -->
## Pick the cherries!

Note:

- Alle Ansätze: Vor- & Nachteile
- Kombination führt zum guten Weg


## Vermeiden!
- Specifity Wars
- Class Hell
- Kontextabhängigkeit
- Markup Bloat
- Implizite starke Kopplung


## Was Wir Wollen
- Schlankes, semantisches Markup
- Kompaktes CSS
- Konsistentes Design ohne Langeweile
- Wiederverwendbare Module
- Klarheit im Code<br/>&nbsp;
- *Wie wollen wir arbeiten?* <!-- .element: class="fragment" -->


## Wasserfall
- Design final, dann Code
- Klare Deadlines, Feature-Commitments
- Keine verschwendete Arbeitszeit
- Wenig Abstimmungsaufwand<br/>&nbsp;
- *Ich hab meine Ruhe* <!-- .element: class="fragment" -->

Note:

- Ich muss mich nicht mit Kreativen hauen


# Yeah!! <!-- .slide: data-state="invert" -->
## Weihnachtsmann? <!-- .element: class="fragment" -->


 <!-- .slide: data-background="images/cheese-santa.jpg" data-background-size="cover" -->

Note:

- Käse!


## Rapid
- Häufige, enge Abstimmung zw. Design & Code
- Code so früh wie möglich
- Photoshop so viel wie nötig
- Bessere Ideen, *in echt* verprobt
- Schnelle Entscheidungen & Ergebnisse
- Minimierte Missverständnisse


# Intergalacto<br/>disciplinary!!! <!-- .slide: data-state="invert" -->
## unde Sch... Code <!-- .element: class="fragment" -->



 <!-- .slide: data-background="images/santashit.png" data-background-size="cover" -->

Note:

- Hinsetzen, nachdenken
- Coder wollen klare Ansagen... denken viele Designer
- Designer wollen immer rumspielen... denken viele Coder
- Quatsch - aber was dran


## Designer will spielen?
- Problem von überall beleuchten <!-- .element: class="fragment" -->
- Ansätze wie Legosteine zusammensetzen <!-- .element: class="fragment" -->
- ... nach und nach ergibt sich ein Bild <!-- .element: class="fragment" -->
- Verfeinern, ausarbeiten <!-- .element: class="fragment" -->


## Design
- ... funktioniert iterativ
- vom Groben zum Feinen
- ... dann vom Kleinen zum Großen


## Coder wollen Klarheit?
- Problem von überall beleuchten <!-- .element: class="fragment" -->
- Ansätze wie Legosteine zusammensetzen <!-- .element: class="fragment" -->
- ... nach und nach ergibt sich ein Bild <!-- .element: class="fragment" -->
- Verfeinern, ausarbeiten <!-- .element: class="fragment" -->


## Coden
- ... funktioniert iterativ
- vom Groben zum Feinen
- ... dann vom Kleinen zum Großen

Note:

- Klarheit? Briefing - gilt für beide
- Design/Konzept: Bisher Coder's Briefing
- Warum nicht zusammen erarbeiten?


# iterativ <!-- .element: style="text-transform:none;font:italic normal normal 6em/1 Georgia,serif" -->
<!-- .slide: data-state="blackout" -->


# grob <!-- .element: style="font:normal normal bold 6em/1 Impact" --> 
<!-- .slide: data-state="blackout" -->


# fein <!-- .element: style="text-transform:none;font:normal normal normal 6em/1 'HelveticaNeue-Thin','Helvetica Neue Thin',sans-serif" -->
<!-- .slide: data-state="blackout" -->


# klein <!-- .element: style="text-transform:none;font:normal normal normal 1em/1 'Courier New',monospace;margin-top:7em" -->
<!-- .slide: data-state="blackout" -->


# gross <!-- .element: style="font:normal normal normal 9em/1 'Big Caslon',serif;margin:.3em -9em" -->
<!-- .slide: data-state="blackout" -->


# iterativ <!-- .element: style="text-transform:none;font:italic normal normal 6em/1 Georgia,serif" -->
<!-- .slide: data-state="blackout" -->


# grob <!-- .element: style="font:normal normal bold 6em/1 Impact" --> 
<!-- .slide: data-state="blackout" -->


# fein <!-- .element: style="text-transform:none;font:normal normal normal 6em/1 'HelveticaNeue-Thin','Helvetica Neue Thin',sans-serif" -->
<!-- .slide: data-state="blackout" -->


# klein <!-- .element: style="text-transform:none;font:normal normal normal 1em/1 'Courier New',monospace;margin-top:7em" -->
<!-- .slide: data-state="blackout" -->


# gross <!-- .element: style="font:normal normal normal 9em/1 'Big Caslon',serif;margin:.3em -9em" -->
<!-- .slide: data-state="blackout" -->



# Atomic Design <!-- .element: class="fragment" style="margin-top:1.5em;text-shadow:0 0 .2em #000" -->
<!-- .slide: data-background="images/radioactive-sign.jpg" data-background-size="cover" -->


## Atomic Design
### Design-Methode
- Starte beim *Allgemeinen*, werde dann *spezieller*
- Starte beim *Kleinen*, gehe dann zum *Großen*
- *Alles* ist aus kleineren Teilen aufgebaut

Note:

- kein Framework o.ä.
- geht für visuelles Design, aber gerade auch für Code-Architektur


## Cherry Picking!
1. Style von allgemein nach speziell (AD)
1. Module flexibel und wiederverwendbar (OOCSS, BEM)
1. Nutze Präprozessoren intelligent
1. Arbeite in interdisziplinären Teams



# #1 Basics <!-- .slide: data-state="blackout" -->
## Allgemein &rarr; speziell


## Helfer vorbereiten
- vars.less: Standardfarben, Größen, Schriften, Timings etc.
- Agnostische mixins.less, verwendet vars<br/>
<small>Venor Prefixes, Hacks, Grids, Meta-Module wie OOCSS Media-Block, Clearfix, Image Replacement</small>


## Normalisiere mit Stil
- Resets sind out
- normalize.css tut mehr als nötig
- Content = Basis<br/>
<small>Headlines, Standard-Links, Listen, Tabellen etc. für Standard-Fließtext</small>
- &rarr; *Atome* in der basic.less

Note:

- AGB-Seite als Start


## Universelle Mini-Objekte
- Klassen, wenn es keine Tags gibt (```.weak```)
- ... oder visuelle Semantik und Element-Natur auseinander laufen können
- Buttons: universell für ```a```, ```button```, ```input```<br/>
<small>.btn, .btn-forth, .btn-primary</small>
- Headline-Klassen ```.h1```–```.h6``` 
- In Ruhe lassen: ```form```, ```fieldset```, ```label```

Note:

- ... oder was auch immer das Projekt verlangt
- js_foo als JS-Hooks, kein JS an universelle Klassen binden


# &frac12; Styleguide <!-- .slide: data-state="invert" -->
## Grid, Farben, Typografie tunen



# #2 Module <!-- .slide: data-state="blackout" -->
## flexibel & wiederverwendbar


## Modul
- Container zum Strukturieren von Content
- Teaser, Sidebar-Box, Slider, Tabs, Kommentare, Produkte
- Können ineinander geschachtelt sein


## Flexibel
- Breite von außen vorgegeben
- Content bestimmt die Höhe
- Meide feste Höhen & Breiten
- Meide absolute Positionierung


## Wiederverwendbar
- Minimaler Kontext für Module
- Gerade so viel, dass es ganz bleibt
- Header/Footer, Seitentypen, Media Queries dazu
- &rarr; Rahmen für Module

Note:

- Bsp. Produkte: Prod.-Kategorien, Cross-Selling, Landing Page
- Modul: max. 2 Nesting-Levels tief


# Projekt-Bootstrap <!-- .slide: data-state="invert" -->
## 80% am Ziel, 20% Code!



# #3 Tuning <!-- .slide: data-state="blackout" -->
## mit Präprozessor-Power


## Tuning
- *Nie* generische Klassen für Kontext verwenden
- Klassenanzahl pro Element gering halten
- Blöcke für Sonderfälle identifizieren

Note:

- Generische Klassen sind unabhängig, sonst Hölle
- Mehr als 4 Klassen unübersichtlich
- Blöcke: Teaser-Duo, Cross-Selling-Produktblock


## Präprozessoren
### Tuning über Mixins & Extends
- Neues Modul: Partial + Less-Datei
- Scope über neuen Modul-Klassennamen
- Mixin/Extend der alten Klassennamen
- Tuning-Regeln dazu

Note:

- Mixin/Extend bei Spezialisierung
- Sonst: Alte Klassen weiter verwenden


## Warum?
- Universelle Regeln bleiben übersichtlich
- Markup wird sauberer
- Sonderlocken leicht zu löschen
- Nicht zu viel Kontext und Spezifität


# Best of both worlds <!-- .slide: data-state="invert" -->
## Modular und Feingetuned



# #4 Teamwork <!-- .slide: data-state="blackout" -->
## interdisziplinäre Arbeitsweise


## Vom Groben ...
- Design: Moods, Farbwelt, Typo, Grid
- Code: vars.less = wachsender Styleguide


## ... und Kleinen
- Design/Code: Grundelemente tunen
- Code/Design: Module identifizieren/bauen


## Zum Großen ...
- Code: Prototyp aus Modulen bootstrappen
- Design/Code: Zusammen feintunen


## ... und Feinen
- Design/Code: Sonderfälle identifizieren
- Code: Bauen
- Design/Code: Zusammen feintunen


# Intergalacto<br/>disciplinary!!! <!-- .slide: data-state="invert" -->
## und schöner Code! <!-- .element: class="fragment" -->
## und geile UX!! <!-- .element: class="fragment" -->


# the end <!-- .element: style="text-transform:none;font:normal normal normal 1em/1 'Courier New';margin-top:7em" -->
<!-- .slide: data-state="blackout" -->
