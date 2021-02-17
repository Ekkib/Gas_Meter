# Gas Meter

Dieses Programm laeuft parallel zu einem Gaszaehler auf einem Raspi. Der Zaehlerstand wird per Reed-Kontakt erfasst. Die momentane Leistung wird aus dem zeitlichen Abstand der Zaehlimpulse berechnet. Das Programm ist mit node-RED erstellt und benutzt die Erweiterung "Dashboard".

Keeps track of the gas meter reading and performance by using a reed-contact.

Kurze Beschreibung der einfachen externen Beschaltung :

Die Nummer der Pins des Raspi I/O Pfostensteckers in Klammern :

+3,3 Volt (1, rot)---xReedx---I>LED>I---+---I 1KOhm I---Ground (9, schwarz)   
GPIO04 Pin (7, gelb)------I 1KOhm I-----+  
(als Eingang geschaltet )

Die LED geht an, sobald der Reed-Kontakt schaltet. Über einen 1 KOhm Widerstand geht das Signal an den Pin GPIO04 (Pin 7) des Raspi.

Ein anderer freier I/O Pin (Pin 13) treibt als Ausgang über einen 1 KOhm Widerstand eine LED. Diese LED blinkt im 10 Sekunden-Takt ("Heart-Beat") und bei jedem Signalwechsel des Reedkontaktes.

Mehr Infos und Fotos :

https://sites.google.com/site/heizungregelung/allgemeines/gaszaehler

Hier sind moegliche Erweiterungen gelistet :

https://sites.google.com/site/heizungregelung/allgemeines/gaszaehler/gas_pl%C3%A4ne

Wer immer diese Erweiterungen schon vorgenommen, bevor ich sie einbauen konnte : Ich übernehme sie gerne.

Zukunft :

1. Diagramme weiter optimieren.
1. Dividend und andere Konstante optional per Einlesen aus Datei, äquivalent zur Ini Datei, und aenderbar über die /ui. So, wie das jetzt schon mit dem Zaehlerstand passiert.
1. Programm fit machen, um die Werte per WEB abzuholen. Per Homeassistant und dergleichen.
1. Beim Start den letzten Zählerstand aus Protokolldatei lesen.
1. Die 3 Protokolldateien nur wahlweise schreiben.
1. Diagramm-Breiten besser an iPhone und iPad anpassen.
1. Datei mit äquidistanten Messwerten wahlweise, Aufzeichnungsstop nach 20 Minuten Leerlauf.
1. Schönen Schaltplan auf die Webseite bringen.
1. Git auch lokal benutzen : https://nodered.org/docs/user-guide/projects/
1. Mqtt ?
1. Lorawan ?
1. Welche Auswerte Software ?
1. Ausprobieren : Uni- and Bipolar Hall IC Switches for Magnetic Field Applications, als Alternative zu einem Reedkontakt :TLE4905L, TLE4935L, TLE4945L, TLE4945-2L.
1. Magnetsensor mit I2C Interface (QMC5883 Magnetometer oder so) ?



Ekkehard@Pofahl.de
