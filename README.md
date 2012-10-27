Modern Web Development with Rails and Backbone
==============================================

Presentation about modern web applications using Rails and Backbone.js in German.

Moderne Webanwendungen mit Rails und Backbone.js
================================================

Wir halten auf der MetaNook 2012 den Vortrag "Moderne Webanwendungen mit Rails und Backbone.js".
Dieses Repository enthält den LaTeX-Quellcode des Vortrags und die gerenderten Folien im Downloadbereich.
Weitere Informationen zur MetaNook unte http://metameute.de/nook2012/.

Zusammenfassung
---------------

Für die Realisierung von Mehrbenutzersystem mit Datenbankanbindung existieren verschiedene Ansätze. Bei einer
Desktopanwendung wird eine spezielle Software mit der Geschäftslogik und der GUI auf dem Client installiert. Die
Kommunikation mit dem Server ist dabei auf den Austausch von Daten beschränkt. Bei klassischen Webanwendungen
befindet sich die Geschäftslogik komplett auf dem Server, der auch die GUI in Form von HTML-Seiten generiert und
an den Client überträgt. Der Nachteil dieser Lösung liegt darin, dass für jede Aktion des Anwenders die GUI
vollständig neu übertragen werden muss. 

Dank JavaScript können moderne Webanwendungen die Vorteile beider Welten kombinieren. Die Geschäftslogik wird in
einem RESTful Webservice gekapselt und auf dem Server durchgeführt. Auf dem Client wird nur ein Browser benötigt,
der eine Single-Page-Application ausführt. Die GUI wird vollständig auf dem Client im Browser erzeugt, sodass die
Kommunikation über das Netzwerk wieder auf die reinen Daten beschränkt bleibt.

Im Rahmen unserer Fallstudie entwickeln wir eine Hotelverwaltungssoftware als moderne Webanwendung. In diesem
Vortrag wollen wir die dafür durchgeführte Entwicklungsarbeit vorstellen und praktische Hinweise zur Realisierung
von modernen Webanwendungen geben. Wir beginnen mit einer Einführung in Webanwendungen und Webservices und erläutern
anschließend unsere Realisierung von Server und Client.

Ruby on Rails erlaubt es sehr leicht, RESTful Webservices zu implementieren. Wir beschreiben die Grundideen von
Rails und die Trennung von Model, View und Controller. Wir gehen insbesondere auf die spezielle Anforderungen im
Bereich der Views zur Generierung von JSON und XML ein und erläutern die Realiserung und Validierung von
one-to-many und many-to-many Relationen. Mit Backbone.js steht ein JavaScript-Framework zur Verfügung, dass es
erlaubt, Collections und Models der REST-Schnittstelle einfach auf dem Client zu implementieren. Für die Erzeugung
der GUI verwenden wir jQuery und ein eigenes Templates-System, dass die template-Funktion aus Underscore.js
verwendet. Weiter erläutern wir den Erhalt der Browser-Historie und Lesezeichen Dank Routing und die Verwaltung von
JavaScript-Abhängigkeiten mit Require.js.

Gliederung
----------

  * Webanwendungen
    * Webanwendungen vs. Desktopanwendung
    * moderne Webanwendungen: Teile der Geschäftslogik und GUI im Client
      * Daten statt HTML übertragen
    * Server als RESTful Webservice mit Ruby on Rails
    * Client als Single-Page-Application mit JavaScript
  * Webservice mit Rails 3.2
    * Model-View-Controller-Realisierung in Rails
    * Rails kann REST
    * Verwendung der Responder aus Rails 3
    * Zurück zu MVC mit representative_view oder RABL
      * Entkopplung der Repräsentation von den internen Datenstrukturen
      * Trennung von View und Controller
    * Assoziationen zwischen Ressourcen
      * one-to-one und one-to-many mit Rails-Bordmitteln
      * Warum many-to-many nicht funktioniert
    * Validierung der referenziellen Integrität
  * Client mit Backbone.js
    * JavaScript aufbohren mit Underscore.js
    * DOM-Manipulation mit jQuery
    * REST-Client mit Backbone.js
      * Collections realisieren Resourcen
      * Models realisieren Datenmodelle
    * Browser-Historie und Lesezeichen Dank Routing
    * Navigation mit dem StateModel
    * HTML-Erzeugung Dank _.template und eigenem FormBuilder
      * innerHTML / $.html() ist der schnellste Weg
      * Browser sind gut im HTML parsen
    * Abhängigkeiten auflösen mit Require.js