# Gas Meter

Dieses Programm läuft parallel zu einem Gaszähler auf einem Raspi. Der Zählerstand wird per Reed-Kontakt erfasst. Das Programm ist mit node-RED erstellt und benutzt die Erweiterung "Dashboard".

Keeps track of the gas meter reading by using a reed-contact.

Kurze Beschreibung der einfachen externen Beschaltung :

Die Nummer der Pins des Raspi I/O Pfostensteckers in Klammern :

+3,3 Volt (1, rot)---xReedx---I>LED>I---+---I 1KOhm I---Ground (9, schwarz)
GPIO04 Pin (7, gelb)------I 1KOhm I-----+
(als Eingang geschaltet )

Die LED geht an, sobald der Reed-Kontakt schaltet. Über einen 1 KOhm Widerstand geht das Signal an den Pin GPIO04 (Pin 7) des Raspi.

Ein anderer freier I/O Pin (Pin 13) treibt als Ausgang eine LED, siehe unten. Diese LED blinkt im 10 Sekunden-Takt ("Heart-Beat") und bei jedem Signalwechsel des Reedkontaktes.

https://sites.google.com/site/heizungregelung/allgemeines/gaszaehler

Ekkehard@Pofahl.de
