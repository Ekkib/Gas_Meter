# Gas Meter

Dieses Programm läuft parallel zu einem Gaszähler auf einem Raspi. Der Zählerstand wird per Reed-Kontakt erfasst. Das Programm ist mit node-RED erstellt und benutzt die Erweiterung "Dashboard".

Keeps track of the gas meter reading by using a reed-contact.

Kurze Beschreibung der einfachen externen Beschaltung :

Die Nummer der Pins des Raspi I/O Pfostensteckers in Klammern :

+3,3 Volt (1, rot)---xReedx---I>LED>I---+---I 1KOhm I---Ground (9, schwarz)   
GPIO04 Pin (7, gelb)------I 1KOhm I-----+  
(als Eingang geschaltet )

Die LED geht an, sobald der Reed-Kontakt schaltet. Über einen 1 KOhm Widerstand geht das Signal an den Pin GPIO04 (Pin 7) des Raspi.

Ein anderer freier I/O Pin (Pin 13) treibt als Ausgang über einen 1 KOhm Widerstand eine LED. Diese LED blinkt im 10 Sekunden-Takt ("Heart-Beat") und bei jedem Signalwechsel des Reedkontaktes.

Mehr Infos und Fotos :

https://sites.google.com/site/heizungregelung/allgemeines/gaszaehler

Heir sind moegliche Erweiterungen gelistet :

https://sites.google.com/site/heizungregelung/allgemeines/gaszaehler/gas_pl%C3%A4ne

Wer immer diese Erweiterungen schon vorgenommen, bevor ich sie einbauen konnte : Ich übernehme sie gerne.

Zukunft :

* Diagramme weiter optimieren.
* Dividend und andere Konstante optional per Einlesen aus Datei, äquivalent zur Ini Datei, und änderbar über die /ui. So, wie das jetzt schon mit dem Zählerstand passiert.
* Programm fit machen, um die Werte per WEB abzuholen. Per Homeassistant und dergleichen.
* Beim Start den letzten Zählerstand aus Protokolldatei lesen.
* Diagramm-Breiten besser an iPhone und iPad anpassen.
* Datei mit äquidistanten Messwerten wahlweise, Aufzeichnungsstop nach 20 Minuten Leerlauf.
* Schönen Schaltplan auf die Webseite bringen.
* Git auch lokal benutzen : https://nodered.org/docs/user-guide/projects/
* Mqqt ?
* Lorawan ?
* Welche Auswerte Software ?
* Ausprobieren : Uni- and Bipolar Hall IC Switches for Magnetic Field Applications, als Alternative zu einem Reedkontakt :TLE4905L, TLE4935L, TLE4945L, TLE4945-2L.
* Magnetsensor mit I2C Interface ?



Ekkehard@Pofahl.de
