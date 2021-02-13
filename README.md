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

Ekkehard@Pofahl.de
